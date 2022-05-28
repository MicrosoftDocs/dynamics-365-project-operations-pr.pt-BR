---
title: Desempenho da API de agenda do projeto
description: Este tópico fornece informações sobre os benchmarks de desempenho das APIs de agenda do projeto e identifica as práticas recomendadas para o uso ideal.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c14d27c561a86cd359cbdcbb448ae764dd3d90e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593828"
---
# <a name="project-schedule-api-performance"></a>Desempenho da API de agenda do projeto

_**Aplicável a:** Project Operations para cenários baseados em recursos/sem estoque, Implantação leve – para realizar o faturamento, Project for the Web_

Este tópico fornece informações sobre os benchmarks de desempenho das APIs (interfaces de programação de aplicativos) de agenda do projeto e identifica as práticas recomendadas para otimização do uso.

## <a name="project-scheduling-service"></a>Serviço de Agendamento de Projeto
O Serviço de Agendamento de Projeto é um serviço multilocatário executado no Microsoft Azure. Ele foi projetado para melhorar a interação, fornecendo uma experiência rápida e fluida quando os usuários trabalham em projetos. Essa melhoria é alcançada aceitando solicitações de mudança, processando-as e retornando imediatamente o resultado. O serviço persiste de forma assíncrona para o Dataverse e não impede que os usuários realizem outras operações.

As APIs de agendamento do projeto contam com o Serviço de Agendamento do Projeto para executar solicitações que são descritas com mais detalhes nas seções posteriores deste tópico.

As APIs de agendamento do projeto são projetadas para funcionar com as seguintes entidades de WBS (estrutura de detalhamento de trabalho):

  - Project
  - Tarefa do Projeto
  - Dependência de Tarefa do Projeto
  - Membro da Equipe do Projeto
  - Atribuição de Recurso
  
Ambos os campos prontos para uso e campos personalizados têm suporte. Salvo indicação em contrário, todas as operações comuns têm suporte, como criar, atualizar e excluir. Para mais informações, consulte [Usar APIs de agenda de projeto para realizar operações com entidades de agendamento](schedule-api-preview.md).

Como parte das APIs de agenda do projeto, um padrão de unidade de trabalho foi adicionado. Esse padrão é conhecido como OperationSet e pode ser usado quando várias solicitações tiverem de ser processadas em uma única transação.

A ilustração a seguir mostra o fluxo que um parceiro experimentará quando esse recurso for usado.

![O Dataverse e o fluxo do serviço de agendamento do projeto.](./media/dataverse-project-scheduling-service-flow.png)

**Etapa 1**: um cliente faz uma chamada à API para um ponto de extremidade OData no Dataverse para criar um OperationSet.

**Etapa 2**: depois que o OperationSet é criado, um valor **OperationSetId** é retornado.

**Etapa 3**: o cliente usa o valor **OperationSetId** para fazer outra solicitação de API de agenda do projeto. O resultado é uma solicitação para criar, atualizar ou excluir em uma entidade de agendamento. Quando essa solicitação é feita, a validação de metadados é concluída. Se a validação falhar, a solicitação será encerrada e um erro será retornado.

**Etapas 4a–4c**: essas etapas representam a fase ACEITAR. O cliente chama a API **ExecuteOperationSetV1**, que envia todas as alterações para o Serviço de Agendamento de Projeto em um lote. O Serviço de Agendamento de Projeto executa suas próprias validações nas solicitações do lote. Qualquer falha de validação desfaz o lote e retorna uma exceção ao responsável pela chamada. Se o lote for aceito com êxito pelo Serviço de Agendamento de Projeto, o status de OperationSet será atualizado para refletir o fato de que o OperationSet está sendo processado pelo Serviço de Agendamento de Projeto.

**Etapa 5**: essa etapa representa a fase PERSISTIR. O Serviço de Agendamento de Projeto grava de forma assíncrona o lote no Dataverse em uma transação. Se a operação de gravação for bem-sucedida, o OperationSet será marcado como **Concluído**. Qualquer erro reverte a transação e o lote, e o OperationSet é marcado como **Reprovado**.

## <a name="performance-methodology"></a>Metodologia de desempenho
O tempo de execução é definido como o tempo desde a chamada à API **ExecuteOperationSetV1** até que o Serviço de Agendamento de Projeto termine de gravar no Dataverse. Todas as operações são executadas combinadas 2.200 vezes e as medições de tempo de execução P99 são relatadas. As operações de registro único e em massa são medidas.

Para uma operação de registro único, o OperationSet contém uma solicitação. Para operações em massa, ele contém 20, 50 ou 100 solicitações. Cada tamanho em massa é relatado separadamente.

Essas operações são executadas em uma implantação do UR 15 Project Operations Lite na América do Norte.

## <a name="results"></a>Resultados
### <a name="create-operations"></a>Criar operações
#### <a name="single-record-create-operations"></a>Operações de criação de registro único
A tabela a seguir mostra os tempos de execução para a criação de um registro único. Os tempos estão em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;registro</th>
    <th class="tg-0lax" colspan="2">Hora</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obrigatórios</th>
    <th class="tg-0lax">Todos os campos com suporte</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuição</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro da equipe</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependência</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operações de criação em massa
A tabela a seguir mostra os tempos de execução para a criação de vários registros. Especificamente, a Microsoft mediu os tempos de execução para a criação de 20, 50 e 100 registros em um único OperationSet. Os tempos estão em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo de&nbsp;&nbsp;&nbsp;registro</th>
    <th class="tg-0lax" colspan="6">Hora</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 registros</th>
    <th class="tg-0lax" colspan="2">50 registros</th>
    <th class="tg-0lax" colspan="2">100 registros</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obrigatórios</th>
    <th class="tg-0lax">Todos os campos com suporte</th>
    <th class="tg-0lax">Campos obrigatórios</th>
    <th class="tg-0lax">Todos os campos com suporte</th>
    <th class="tg-0lax">Campos obrigatórios</th>
    <th class="tg-0lax">Todos os campos com suporte</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuição</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependência</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> As operações de criação em massa nas entidades **Projeto** e **Membro da Equipe** não são incluídas nesta tabela, porque o runtime para essas operações se assemelha ao tempo de execução quando a API para a criação de um registro único é chamada várias vezes. Essas APIs são executadas imediatamente no Dataverse.

A ilustração a seguir mostra um gráfico dos tempos de execução para as entidades **Tarefa**, **Atribuição** e **Dependência** quando 20, 50 e 100 registros são criados e todos os campos compatíveis são usados.

![Gráfico de tempo de execução de criação de registro.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operações de atualização
#### <a name="single-record-update-operations"></a>Operações de atualização de registro único
A tabela a seguir mostra os tempos de execução para atualizações de um registro único. Os tempos estão em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;registro</th>
    <th class="tg-0lax" colspan="2">Hora</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obrigatórios </th>
    <th class="tg-0lax">Todos os campos com suporte</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro da equipe</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operações de atualização não têm suporte nas entidades **Atribuições de Recursos** e **Dependência da Tarefa do Projeto**.

#### <a name="bulk-update-operations"></a>Operações de atualização em massa
A tabela a seguir mostra os tempos de execução para atualizações de vários registros. Especificamente, a Microsoft mediu os tempos de execução para atualizações de 20, 50 e 100 registros em um único OperationSet. Os tempos estão em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo de&nbsp;&nbsp;&nbsp;registro</th>
    <th class="tg-0lax" colspan="6">Hora</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 registros</th>
    <th class="tg-0lax" colspan="2">50 registros</th>
    <th class="tg-0lax" colspan="2">100 registros</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obrigatórios</th>
    <th class="tg-0lax">Todos os campos com suporte</th>
    <th class="tg-0lax">Campos obrigatórios</th>
    <th class="tg-0lax">Todos os campos com suporte</th>
    <th class="tg-0lax">Campos obrigatórios</th>
    <th class="tg-0lax">Todos os campos com suporte</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro da equipe</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operações de atualização não têm suporte nas entidades **Atribuições de Recursos** e **Dependência da Tarefa do Projeto**.

A ilustração a seguir mostra um gráfico dos tempos de execução para as entidades Tarefa e Membro da Equipe quando 20, 50 e 100 registros são atualizações e todos os campos compatíveis são usados.

![Gráfico de tempo de execução de atualização de registro.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Opções de exclusão
#### <a name="single-record-delete-operations"></a>Operações de exclusão de registro único
A tabela a seguir mostra os tempos de execução para a exclusão de um único registro. Os tempos estão em segundos.

| Tipo de registro | Hora  |
|-------------|-------|
| Tarefa        | 20.12 |
| Atribuição  | 10.86 |
| Membro da equipe | 12.52 |
| Dependência  | 20.89 |

> [!NOTE]
> As operações de exclusão não têm suporte na entidade **Projeto**.

#### <a name="bulk-delete-operations"></a>Operações de exclusão em massa
A tabela a seguir mostra os tempos de execução para a exclusão de vários registros. Especificamente, a Microsoft mediu os tempos de execução para a exclusão de 20, 50 e 100 registros em um único OperationSet. Os tempos estão em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;registro</th>
    <th class="tg-0lax" colspan="3">Hora</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 registros</th>
    <th class="tg-0lax">50 registros</th>
    <th class="tg-0lax">100 registros</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuição</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro da equipe</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependência</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operações de exclusão não têm suporte na entidade **Projeto**.

A ilustração a seguir mostra um gráfico dos tempos de execução para as entidades **Tarefa**, **Atribuição**, **Membro da Equipe** e **Dependência** quando 20, 50 e 100 registros são criados e todos os campos compatíveis são excluídos.

![Gráfico de tempo de execução de exclusão de registro.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observações
Para cada operação de registro, a API **ExecuteOperationSet** leva cerca de 800 milissegundos para enviar uma solicitação ao Serviço de Agendamento de Projeto. O Serviço de Agendamento de Projeto leva cerca de cinco segundos para processar a carga útil e chamar o Dataverse. O resto do tempo de execução é gasto com a execução da lógica de negócios e a gravação de dados no banco de dados no Dataverse.

Quando 100 registros são criados, atualizados ou excluídos, a API **ExecuteOperationSet** leva cerca de três segundos para enviar a solicitação ao Serviço de Agendamento de Projeto. O Serviço de Agendamento de Projeto leva cerca de cinco segundos para processar as solicitações e chamar o Dataverse. As operações em massa devem pagar uma **taxa de Serviço de Agendamento de Projeto** uma vez para todos os registros no OperationSet. Portanto, as operações em massa têm um tempo médio de execução significativamente menor do que as operações de registro único.

## <a name="scenarios"></a>Cenários
A tabela a seguir mostra os tempos de execução quando as APIs de agenda do projeto são usadas para atender a cenários específicos. Os tempos estão em segundos.

| Cenário                                                                   | Hora  |
|----------------------------------------------------------------------------|-------|
| Crie um projeto com 40 tarefas.                                      | 36.01 |
| Crie um projeto com 40 tarefas e 20 dependências.                  | 38.11 |
| Crie um projeto com 40 tarefas e 30 atribuições.                   | 60.17 |
| Crie um projeto com 40 tarefas e 20 dependências e 30 atribuições. | 60.27 |

## <a name="best-practices"></a>Práticas recomendadas
Com base nos resultados do cenário anterior, as APIs têm melhor desempenho nas seguintes condições:

  - Agrupe tantas operações quanto possível. O runtime médio para operações em massa é melhor do que o tempo de execução médio para operações de registro único. Quanto menor o número de OperationSets em uso, menor será o tempo médio de execução.
  - Defina apenas os atributos mínimos necessários para realizar seu cenário. Seja seletivo sobre os tipos de campos não obrigatórios incluídos em uma solicitação de OperationSet. Os campos com chaves estrangeiras ou campos cumulativos afetarão negativamente o desempenho.
