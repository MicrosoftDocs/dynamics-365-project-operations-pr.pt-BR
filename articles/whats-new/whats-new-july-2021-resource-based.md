---
title: Novidades em julho de 2021 – Project Operations para cenários baseados em recursos/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de julho de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5dbf9c7158ce7d9e568e270791e7e7aaf8ce731d
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433504"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em julho de 2021 – Project Operations para cenários baseados em recursos/sem estoque

*Aplicável A: Project Operations para cenários baseados em recursos/sem estoque*

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

   - Project Operations na versão 4.12.0.148 do ambiente do Microsoft Dataverse.
   - Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance versão 10.0.20.

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- Capacidade dos administradores de visualizar os logs do PSS e os logs do Conjunto de Operações no menu de configurações. Os logs são armazenados durante 90 dias.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão.

Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, conforme você atualiza sua solução do Project Operations Dataverse e a versão da solução do Finance. Certos recursos e funcionalidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Você pode ver a versão ativa do mapa na página **Gravação dupla** na coluna **Versão**. Ative uma nova versão do mapa selecionando **Versões do mapa da tabela**, selecionando a versão mais recente e salvando a versão selecionada. Se você personalizou um mapa de tabela pronto para usar, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) no guia de solução de problemas de Gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área do recurso**              | **Número de referência** | **Atualização de qualidade**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cobrança e preço           | 2224046              | O campo **Classe de Transação** é editável na guia **Detalhes da Linha de Cotação**, mas fica bloqueado se você estiver trabalhando usando a página **Detalhes da Linha de Cotação**.                                                                     |
| Cobrança e preço           | 2224400              | A ação **Fechar Cotação como Ganha** falha quando uma cotação não tem marcos de data.                                                                                                                                    |
| Cobrança e preço           | 2234089              | Quando você insere manualmente uma descrição de produto, ela é removida depois que você insere uma quantidade para uma estimativa de material.                                                                                                                         |
| Cobrança e preço           | 2234100              | A grade **Configuração de Cobrança da Tarefa** não inclui a coluna **Material** e seu valor na guia **Cobrança da Tarefa** do projeto.                                                                                                       |
| Cobrança e preço           | 2277409              | O ID do produto não está disponível no detalhe da linha do contrato para uma linha de tipo de material.                                                                                                                                        |
| Cobrança e preço           | 2281728              | A criação de uma linha de contrato reavalia desnecessariamente os valores reais, que causam aumentos significativos no volume de dados, o que afeta o desempenho.                                                                                |
| Cobrança e preço           | 2298668              | As linhas do diário associadas a uma despesa recuperada e excluída não serão removidas.                                                                                                                                     |
| Cobrança e preço           | 2300192              | Quando vários usuários estão editando uma fatura, é possível que um novo detalhe da linha da fatura seja criado em uma fatura confirmada.                                                                                   |
| Cobrança e preço           | 2301569              | As faturas não podem ser corrigidas se um \$retentor com valor 0 foi aplicado.                                                                                                                                        |
| Cobrança e preço           | 2307965              | Ocorre um erro, se um preço de categoria for criado com valores ausentes.                                                                                                                           |
| Cobrança e preço           | 2326870              | Ocorre um erro no **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** se **producttypecode** for nulo.                                                                            |
| Cobrança e preço           | 2332732              | Ocorre um erro se um marco de linha de contrato for criado sem uma linha de ordem.                                                                                                                |
| Planejamento e acompanhamento de projeto | 2181094              | A API de Agendamento do Project agora oferece suporte a Logs de PSS e Logs do Conjunto de Operações, que são armazenados durante 90 dias.                                                                                                                  |
| Planejamento e acompanhamento de projeto | 2254201              | O rótulo **Modo de Agendamento** é atualizado com detalhes que descrevem a lógica padrão.                                                                                                                                      |
| Planejamento e acompanhamento de projeto | 2300252              | O cache de resposta do **openProject** é atualizado e inclui o proprietário do token na chave do cache, **Url base** e a **URL do Segmento**, de forma que a **Url de Solicitação** sempre possa ser recriada, se a **Url base** for alterada. |
| Planejamento e acompanhamento de projeto | 2301312              | **msdyn_membershipstatus** foi removido da exibição **Membro da Equipe do Projeto**.                                                                                                                                        |
| Planejamento e acompanhamento de projeto | 2302759              | Os produtos são obtidos desnecessariamente nas guias **Atribuições de Recurso**, **Estimativas** e **Estimativas de Despesas**.                                                                                                        |
| Planejamento e acompanhamento de projeto | 2308050              | **CopyProject** falha com o erro "Falha ao obter o token para falar com o serviço remoto".                                                                                                                           |
| Planejamento e acompanhamento de projeto | 2322650              | A exibição **Lista de Tarefas do Projeto** foi atualizada para exibir a data da tarefa, por padrão.                                                                                                            |
| Planejamento e acompanhamento de projeto | 2327266              | **CopyProject** gera o erro "Chave não encontrada no dicionário" ao copiar as estimativas.                                                                                                      |
| Planejamento e acompanhamento de projeto | 2328123              | **CopyProject** gera o erro "Falha ao obter o token para falar com o serviço remoto".                                                                                                                          |
| Planejamento e acompanhamento de projeto | 2336258              | **CopyProject** copia incorretamente os nomes das posições dos recursos.                                                                                                                                                 |
| Cobrança e preço           | 2224476              | O campo **Recurso Reservável** não é padronizado corretamente para o usuário conectado na página **Uso de Material**.                                                                                                            |
| Gerenciamento de Recursos           | 2277249              | Ocorre um erro quando um requisito de recurso não baseado em projeto é atualizado.                                                                                                            |
| Gerenciamento de Recursos           | 2323869              | A utilização de recursos não reconhece corretamente os recursos filtrados.                                                                                                                                             |
| Tempo e Despesa              | 2176538              | Operadores de filtro incorretos são aplicados ao controle **Entrada de Hora**.                                                                                                                                                   |
| Tempo e Despesa              | 2177462              | A exclusão de uma entrada de hora na grade não atualiza os status dos botões **Enviar**, **Recuperar**, **Excluir** e **Editar Entrada**, conforme o esperado.                                                                                        |
| Tempo e Despesa              | 2299985              | **TimeEntriesImportFromResourceAssignment** não mantém a hora de início/término dos contornos da atribuição.                                                                                                  |
| Tempo e Despesa              | 2318426              | Depois que uma entrada de hora é enviada, os campos bloqueados ainda podem ser editados.                                                                                                                                   |
| Tempo e Despesa              | 2323749              | Ocorre um erro quando uma despesa é criada usando a guia **Relacionado** de um recurso reservável.                                                                                                      |
| Tempo e Despesa              | 2327678              | Quando você cria uma entrada de hora a partir da guia **Relacionado** de um recurso reservável, o recurso pai não é passado para o controle de entrada de hora.                                                                            |
| Geral                       | 2296857              | Rastreamento de progresso para trabalhos de execução prolongada.                                                                                                                                                                        |
| Geral                       | 2253682              | A solução de gravação dupla do Project Operations não deve ser instalada quando a solução principal de gravação dupla é instalado em um ambiente sem a solução de orquestração de gravação dupla.                                                |
| Geral                       | 2316420              | O provisionamento principal do Project service falhará se a unidade de negócios do usuário do aplicativo for alterada.                                                                                                                     |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Visão geral de gerenciamento e contabilidade de projeto no Dynamics 365 Finance

| Área do recurso                      | Número de referência | Atualização de qualidade                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gerenciamento e contabilidade de projeto | 4620267          | Não é possível personalizar formulários para adicionar um campo **Objetivo** às páginas **Transação postada do projeto**, **Criação de proposta de fatura** e **Proposta de fatura**.                                                                                                                                                                                         |
| Gerenciamento e contabilidade de projeto | 4613449          | Quando você seleciona um ID de contrato de Projeto no Finance, o ambiente integrado do Project Operations abre a página para criar um novo registro, em vez da página para contratos de projeto já criados.                                                                                                                                           |
| Gerenciamento e contabilidade de projeto | 4614445          | Na implantação do cenário integrado do Project Operations, você não pode editar o campo **grupo de impostos de itens** na proposta de fatura importada da preparação. O grupo de impostos do item deve ser editável para uma proposta de fatura em aberto de todos os tipos de transação, incluindo conta, horas, despesas, taxas e itens. |
| Gerenciamento e contabilidade de projeto |                  | Não é possível lançar uma proposta de fatura resultante de uma correção de transação de tempo negativo.                                                                                                                                                                                                                                              |
| Gerenciamento e contabilidade de projeto |                  | As linhas da proposta de fatura são duplicadas devido a vários processos periódicos **Importar da preparação** em execução ao mesmo tempo.                                                                                                                                                                                                                |

