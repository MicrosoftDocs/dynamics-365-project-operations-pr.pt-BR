---
title: Novidades em junho de 2021 – Project Operations para cenários baseados em recursos/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de junho de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 483992768f8b8a02dd0d56b9479c7d591fa676d1eca41161e68b7cf3f97107af
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003847"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em junho de 2021 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations na versão 4.11.0.156 ou 4.11.0.164 do ambiente do Dynamics 365 Dataverse.
- Gerenciamento de projeto e contabilidade na versão 10.0.19 dos ambientes dos aplicativos Finance and Operations.

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- Capacidade de excluir [Linhas de proposta de fatura do projeto para cenários de ajuste](../invoicing/correct-project-invoice-proposals.md).
- As linhas de despesas discriminadas refletem os nomes das subcategorias no relatório de despesas [Relatórios de Despesas Reinventados - Novos Recursos](../expense/expense-reports-reimagined.md#new-features).
- A forma de pagamento está disponível no novo painel de despesas ao criar uma nova despesa.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão. 

Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre executar a versão mais recente do mapa em seu ambiente e habilitar todos os mapas de tabela relacionados, conforme você atualiza sua solução do Dataverse do Project Operations e a versão da solução do Finance and Operations. Certos recursos e funcionalidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Você pode ver a versão ativa do mapa na página **Gravação dupla** na coluna **Versão**. Ative uma nova versão do mapa selecionando **Versões do mapa da tabela**, selecionando a versão mais recente e salvando a versão selecionada. Se você personalizou um mapa de tabela pronto para usar, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) no guia de solução de problemas de Gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2281417 | Corrigido o problema relacionado à falha da ação de criação automática de fatura por meio do agendamento de fatura. |
| Cobrança e preço | 2287835 | Melhor desempenho de confirmação de fatura. |
| Gerenciamento de Oportunidades | 2222555 | A exigibilidade das estimativas de material deve ser copiada corretamente para os detalhes da linha de cotação ao usar **Importar da Estimativa do Projeto**. |
| Gerenciamento de Oportunidades | 2223427 | As personalizações agora são permitidas para a ação, **GenerateRetainersFromRetainerScheduleOptions**. |
| Gerenciamento de Oportunidades | 2277528 | Cálculo do valor do marco de faturamento fixo para linhas de contrato de projeto com vários clientes. |
| Planejamento e acompanhamento de projeto | 2226110 | Corrigido o problema intermitente com a função **Gerar Requisito** na grade **Equipe de projeto**. |
| Planejamento e acompanhamento de projeto | 2208109 | Os usuários não podem criar um projeto em uma moeda com tarefas relacionadas em outra moeda. |
| Planejamento e acompanhamento de projeto | 2258228 | A lista de campos que podem ser modificados com as entidades de **Agendamento** que usam a API de Agendamento foi atualizada. |
| Planejamento e acompanhamento de projeto | 2293989 | O idioma correto e as configurações regionais devem ser passados para a grade **Tarefas do Projeto**. |
| Gerenciamento de Recursos | 2220493 | Corrigida a experiência do usuário na grade **Tarefa** ao marcar rapidamente uma solicitação de recurso como concluída. |
| Gerenciamento de Recursos | 2330496 | Corrigido o problema de carregamento do **Quadro de Agendamento**. (A atualização de qualidade está disponível na versão 4.11.0.164) |
| Tempo e Despesa | 2194431 | A grade **Entrada de hora** deve honrar o início da semana, conforme definido na **Configurações do sistema**. |
| Tempo e Despesa | 2277311 | Depois de excluir o valor em uma célula na grade **Entrada de tempo**, o cursor permanece na grade. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Visão geral de gerenciamento e contabilidade de projeto no Dynamics 365 Finance

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gerenciamento e contabilidade de projeto | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notas do formulário** e **Configuração de formulário** não são visíveis em **Configuração de gerenciamento de projeto** em entidades legais do Finance que estão integradas ao Project Operations. |
| Gerenciamento e contabilidade de projeto | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | A descrição padrão do IVA fica em branco quando o **Tipo de postagem** = **Imposto** para vouchers de fatura de projeto. |
| Gerenciamento e contabilidade de projeto | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Transações duplas são lançadas quando o faturamento baseado em tarefas é usado no Dataverse com integração do Project Operations. |
| Gerenciamento e contabilidade de projeto | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | A porcentagem concluída no reconhecimento de receita está incorreta ao usar a integração do Project Operations. |
| Gerenciamento e contabilidade de projeto | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | O acúmulo de receita é duplicado em uma fatura de fornecedor pendente em um cenário integrado do Project Operations. |
| Gerenciamento e contabilidade de projeto | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Não é possível postar o diário de integração quando a regra do perfil de receita está definida para a configuração **Grupo**. |
| Gerenciamento e contabilidade de projeto | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Uma fatura de compra não pode ser lançada para ordens de compra do projeto que possuem linhas com várias unidades de medida. |
| Gerenciamento e contabilidade de projeto | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | A dimensão financeira padrão em um projeto não pode ser atualizada usando os projetos da entidade de dados **V2**. |
| Gerenciamento e contabilidade de projeto | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | O processo em lote para criar estimativas de projeto leva muito tempo para ser concluído. |
| Gerenciamento e contabilidade de projeto | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | A exclusão de um contrato também exclui o endereço associado ao cliente. |
| Viagens e despesas | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | A condição do fluxo de trabalho de aprovação do relatório de despesas não foi avaliada corretamente. |
| Viagens e despesas | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | A política de relatório de despesas não está avaliando corretamente o ID do projeto. |
| Viagens e despesas | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | A ação, **Dividir para pessoal para transações de despesas entre empresas** não está funcionando corretamente. |
| Viagens e despesas | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | As justificativas da linha do relatório de despesas são excluídas acidentalmente quando certas requisições de viagem são excluídas. Isso ocorre quando o recID do relatório de despesas e a requisição de viagem são iguais. |
| Viagens e despesas | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Há um problema no aplicativo móvel Expense quando o campo **ID do projeto** é obrigatório nas políticas de relatório de despesas. |
| Viagens e despesas | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Despesas intercompanhia associadas a um projeto não podem ser editadas. Em vez disso, a seguinte mensagem de erro é exibida, "Referência de objeto não definida para uma instância de um objeto." |
| Viagens e despesas | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Depois que o relatório de despesas é lançado, a moeda e o valor incorretos são listados no livro auxiliar do banco. |
| Viagens e despesas | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Melhorias foram feitas para o recurso *Excluir transações de cartão de crédito*.  |
| Viagens e despesas | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | O imposto incluído em um relatório de despesas não é calculado de forma consistente quando uma moeda de relatório diferente é especificada em uma entidade legal. |
| Viagens e despesas | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | O desempenho é afetado ao adicionar uma nova despesa de viagem em dinheiro. |
| Viagens e despesas | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | As regras de política de despesas não são acionadas em um relatório de despesas. |
| Viagens e despesas | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | O upload de uma nova categoria compartilhada usando o Data Management Framework remove todas as subcategorias de todas as categorias compartilhadas. |
| Viagens e despesas | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Quando você cria uma linha de despesas e, em seguida, seleciona uma categoria, a seguinte mensagem de erro é exibida: "A combinação do grupo de impostos sobre vendas DOM e do grupo de impostos sobre vendas STD do item não é válida." |
| Viagens e despesas | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Existem problemas de sincronização no aplicativo móvel Expense. |
