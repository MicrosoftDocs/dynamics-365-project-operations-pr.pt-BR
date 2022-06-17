---
title: Novidades em fevereiro de 2022 – Project Operations para cenários baseados em recursos/sem estoque
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de fevereiro de 2022 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932972"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em fevereiro de 2022 – Project Operations para cenários baseados em recursos/sem estoque

*Aplicável A: Project Operations para cenários baseados em recursos/sem estoque*

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.28.0.120
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.24

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

- A partir desta versão, você pode adicionar até 300 membros da equipe a um único projeto. Anteriormente, o limite no número de membros da equipe era de 150. Para obter mais informações, consulte [Limites do projeto](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Atualizações no mapa de gravação dupla do Project Operations

A lista a seguir mostra os mapas de gravação dupla que foram modificados ou adicionados na versão de fevereiro de 2022 do Project Operations.

| Mapa de entidade | Versão atualizada | Comentários |
| --- | --- | --- |
| Entidade de exportação de despesas do projeto de integração do Project Operations (msdyn\_expenses) | 1.0.0.3 | Estendido para sincronização de atividades do projeto no Dataverse. |

Para obter a lista e as versões atuais dos mapas de gravação dupla do Project Operations, consulte [Versões do mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2415109 | O valor padrão no campo **Condições de pagamento de operações** deve ser o registro de cliente do contrato do projeto e o registro de fatura pro forma. |
| Cobrança e preço | 2497369 | A correção de materiais deve seguir o valor de data nos parâmetros **Correção**. |
| Cobrança e preço | 2498697 | Aprimorada a configuração de segurança para **Recuperação de entrada de hora**. |
| Cobrança e preço | 2513824 | Para cenários baseados em recursos, a ID da categoria de transação não deve exceder 28 caracteres no Project Operations. |
| Cobrança e preço | 2517455 | A ação **Atualizar transações de linha de fatura** não deve ter permissão para ser acionada várias vezes simultaneamente para a mesma fatura. |
| Cobrança e preço | 2517465 | A ação **Desativar detalhes de linha de fatura** está bloqueada porque não tem suporte. |
| Cobrança e preço | 2556660 | Corrigida a verificação de efetividade de data que é feita na lista de preços anexada ao registro de parâmetros de um projeto. |
| Gerenciamento de oportunidades | 2369202 | Corrigida a lógica de negócios que verifica se as listas de preços com datas de efetividade sobrepostas podem ser anexadas ao mesmo contrato de projeto. |
| Gerenciamento de oportunidades | 2385965 | Corrigido o comportamento na guia **Clientes** da página **Contrato do projeto** ao selecionar **Salvar e fechar**. |
| Horas e despesas | 2538503 | Uma tarefa do projeto deve estar disponível na entidade **Dados reais do projeto** após o lançamento de um relatório de despesas. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gerenciamento e contabilidade de projetos no Dynamics 365 Finance

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gerenciamento e contabilidade de projeto | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Durante a importação de notas de crédito de fornecedor, ocorre um erro. A mensagem de erro informa: "O valor de retenção não pode ser maior do que o valor líquido restante". |
| Gerenciamento e contabilidade de projeto | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Se uma proposta de fatura incluir transações de taxa de valor zero que sejam dados reais de vendas não cobradas, o faturamento não poderá ocorrer. |
| Gerenciamento e contabilidade de projeto | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | O custo lançado não fica correto depois que o preço de compra é atualizado e **Ativar gerenciamento de alterações** é habilitado.|
| Gerenciamento e contabilidade de projeto | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | A estimativa de lançamento para um projeto de preço fixo usa a moeda e o valor incorretos no comprovante de estimativa, mesmo quando o recurso **Habilitar moeda do contrato de projeto para o cálculo de estimativa** está habilitado. |
| Gerenciamento e contabilidade de projeto | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** não deve fazer uma chamada para habilitar o controle de alterações sem capturar exceções para entidades que possuem chaves de configuração que não estão habilitadas. |
| Gerenciamento e contabilidade de projeto | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | O trabalho em lotes é corrigido quando vários diários avançados são lançados e ocorre um erro. |
| Viagens e Despesas | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Devido a um problema de liquidação relacionado a adiantamentos em dinheiro nos relatórios de despesas, o valor do imposto não é coberto como parte do adiantamento em dinheiro. |
| Viagens e Despesas | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | As informações do imposto sobre vendas não estão incluídas no relatório **Despesa - Transações lançadas**. |
| Viagens e Despesas | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | A violação da política de despesas **Recibos Obrigatórios** mostra incorretamente um aviso nos relatórios de despesas. |
| Viagens e Despesas | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Uma transação de projeto não inclui um imposto sobre vendas não recuperável no valor total de vendas quando a transação é resultado de uma despesa de milhagem. |
| Viagens e Despesas | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Quando uma linha discriminada tem imposto, você não pode alterar a data da linha de discriminação e ocorre um erro de estado do documento de origem. |

## <a name="removed-and-deprecated-features"></a>Recursos removidos e preteridos

O artigo [Recursos removidos ou preteridos no Project Operations](removed-depreciated-features-project.md) descreve recursos que foram removidos ou preteridos no Dynamics 365 Project Operations.

- Um recurso removido não está mais disponível no produto.
- Um recurso preterido não está em desenvolvimento ativo e poderá ser removido em uma atualização futura.

Um anúncio de preterimento será exibido no artigo [Recursos removidos ou preteridos no Project Operations](removed-depreciated-features-project.md) 12 meses antes da remoção de qualquer recurso do produto.

Para as alterações interruptivas que afetam somente o tempo de compilação, mas são compatíveis binárias com ambientes de área restrita e de produção, o tempo de preterimento será inferior a 12 meses. Normalmente, essas alterações são atualizações funcionais que precisam ser feitas no compilador.
