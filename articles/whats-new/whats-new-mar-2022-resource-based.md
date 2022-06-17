---
title: Novidades em março de 2022 – Project Operations para cenários baseados em recursos/sem estoque
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de março de 2022 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910892"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em março de 2022 – Project Operations para cenários baseados em recursos/sem estoque

*Aplicável A: Project Operations para cenários baseados em recursos/sem estoque*

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.30.0.99
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.25

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

As diárias agora têm suporte no novo e reformulado espaço de trabalho de despesas moderno. As empresas que usam diárias podem habilitar este recurso para oferecer aos usuários uma maneira fácil de enviar e receber reembolsos por suas despesas com diárias. Para obter mais informações, consulte [Despesas com diárias](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

A lista a seguir mostra os mapas de gravação dupla que foram modificados ou adicionados na versão de março de 2022 do Project Operations.

| **Mapa de entidade** | **Versão atualizada** | **Comentários** |
| --- | --- | --- |
| Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mapeamentos atualizados para se alinharem à entidade de linha de fatura de fornecedor no Dataverse. <br>Não ative o mapeamento versão 1.0.0.4. Ele estará pronto para uso em combinação com o ambiente do Finance versão 10.0.26 na próxima atualização mensal. |

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Horas e despesas | 2388011 | Mostre os comentários de rejeição aos remetentes de entrada de hora durante a aprovação em massa. |
| Planejamento e acompanhamento de projeto | 2495294 | Os detalhes do projeto não devem ser editáveis na página **Detalhes da tarefa**. |
| Cobrança e preço | 2499605 | As etapas do contrato criadas com base em etapas de cotação são marcadas incorretamente como somente leitura. |
| Planejamento e acompanhamento de projeto | 2506050 | O conjunto de operações fica pendente por uma hora se não houver nenhuma alteração a ser salva. O conjunto é então falsamente marcado como **Com falha**, mas deve ser concluído de forma imediata. |
| Cobrança e preço | 2507401 | As unidades de contratação padrão são inseridas incorretamente nos projetos devido ao armazenamento em cache incorreto. |
| Cobrança e preço | 2541660 | A **Validação da Criação da Ordem de Venda** na gravação dupla deve ser apenas para ordens baseadas em projetos. |
| Cobrança e preço | 2552745 | O imposto não é dividido entre os clientes que configuraram regras de cobrança dividida. |
| Cobrança e preço | 2558859 | Aprimoradas as mensagens de erro quando as dimensões de preços são configuradas. |
| Cobrança e preço | 2558933 | **Importar de Estimativas do Projeto** falha quando **msdyn\_project** é adicionado como uma dimensão de preço. |
| Cobrança e preço | 2559101 | A exclusão de parâmetros do projeto não está bloqueada e causa problemas. |
| Gerenciamento de oportunidades | 2570390 | O plug-in de gravação dupla força o tipo de conta em cotações, ordens e oportunidades a ser **Cliente**, mesmo quando esse tipo de conta não está correto. |
| Cobrança e preço | 2586097 | Os dados reais do custo cobrado dividido não são revertidos quando um projeto é removido de uma linha de contrato de projeto. |
| Cobrança e preço | 2589619 | O imposto sobre o material fora do catálogo é propagado para os dados reais de vendas não cobradas e a fatura. |
| Gerenciamento de oportunidades | 2594015 | Uma cotação não pode ser fechada como ganha para clientes com condições de pagamento **Net60**. |
| Planejamento e acompanhamento de projeto | 2595841 | No Project for the Web, os usuários recebem uma mensagem de erro sobre um **msdyn\_actualstart** ausente quando eles criam uma nova solicitação de recurso. |
| Tempo e Despesa | 2602511 | O campo **Rejeitado por** para entradas de horas mostra **Sistema** em vez de um usuário nomeado como o rejeitador. |
| Tempo e Despesa | 2602528 | Um aprovador de projeto pode aprovar tempo em projetos nos quais ele não está listado como aprovador. |
| Cobrança e preço | 2608550 | Uma fatura de correção pode ser confirmada mesmo que não haja alterações na original. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gerenciamento e contabilidade de projetos no Dynamics 365 Finance

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gerenciamento e contabilidade de projeto | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Há uma incompatibilidade entre o Finance e o Project Operations no tamanho permitido do campo **ID da Categoria**. |
| Gerenciamento e contabilidade de projeto | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Os projetos de preço fixo não poderão ser eliminados quando o campo **Faturamento por conta** estiver definido como **Lucros e perdas** e o princípio **Percentual concluído** for usado. |
| Gerenciamento e contabilidade de projeto | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Um grupo incorreto de impostos sobre vendas padrão é inserido na configuração do projeto em linhas de despesas do diário de integração do Project Operations. |
| Gerenciamento e contabilidade de projeto | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Você não pode editar as dimensões do cabeçalho da proposta de fatura do projeto em uma implantação integrada com o Project Operations. |
| Gerenciamento e contabilidade de projeto | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | As faturas de fornecedor intercompanhia não devem ser integradas ao Dataverse. |
| Gerenciamento e contabilidade de projeto | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Há uma incompatibilidade entre a moeda dos saldos do cliente e a moeda do relatório. |
| Gerenciamento e contabilidade de projeto | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Você pode lançar uma fatura de projeto mesmo se o cliente estiver em espera para todas as faturas. |
| Gerenciamento e contabilidade de projeto | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | O botão **Excluir todas as linhas** está ausente nas propostas de fatura do projeto que têm as exibições **Cabeçalho** e **Linhas**. |
| Gerenciamento e contabilidade de projeto | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Quando você lança uma fatura de fornecedor, ocorre o seguinte erro: "A data contábil da fatura deve estar no mesmo ano contábil da ordem de compra relacionada. Execute o processo de fechamento do exercício da ordem de compra ou altere a data para o ano contábil atual". |
| Viagens e Despesas | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | O custo comprometido de um projeto não é liberado depois que o custo comprometido da requisição de viagem é liberado. |
| Viagens e Despesas | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | O seguinte erro ocorre quando você envia um relatório de despesas: "Rastreamento de Pilha: a empresa não existe". |
| Viagens e Despesas | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | A **ID do Projeto** padrão não é inserida nos relatórios de despesas quando o parâmetro **Exigir atividades no diário** é selecionado no projeto. |
| Viagens e Despesas | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | O botão **Lançar Despesas** não funciona corretamente no Project Operations para cenários baseados em recursos/sem estoque. |
| Viagens e Despesas | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Há um problema com a **Taxa por milha** de um relatório de despesas de milhagem que inclui passageiros. |
| Viagens e Despesas | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | As taxas de milhagem de despesas para funcionários não são totalizadas corretamente quando dois tipos de veículos diferentes são usados na categoria de despesa **Níveis de taxa de milhagem**. |
| Viagens e Despesas | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | A pesquisa do campo **Projeto** em uma linha de requisição de viagem não retorna a lista correta de projetos. |
| Viagens e Despesas | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Milhagem em revisão** mostra um aviso nos relatórios de despesas. |
| Viagens e Despesas | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | O serviço de reconhecimento óptico de caracteres (OCR) de recibo não funciona devido a um problema com a URL do serviço de OCR de despesas. |
| Viagens e Despesas | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Quando o recurso **Capacidade de discriminar despesas recorrentes rapidamente** estiver habilitado, os valores nas linhas de discriminação dos relatórios de despesas mudarão toda vez que a página **Discriminar** for aberta. |
| Viagens e Despesas | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Você não pode excluir um relatório de despesas quando a lista provisória tem mais de um aprovador. |

## <a name="removed-and-deprecated-features"></a>Recursos removidos e preteridos

O artigo [Recursos removidos ou preteridos no Project Operations](removed-depreciated-features-project.md) descreve recursos que foram removidos ou preteridos no Dynamics 365 Project Operations.

- Um recurso removido não está mais disponível no produto.
- Um recurso preterido não está em desenvolvimento ativo e poderá ser removido em uma atualização futura.

Um anúncio de preterimento será exibido no artigo [Recursos removidos ou preteridos no Project Operations](removed-depreciated-features-project.md) 12 meses antes da remoção de qualquer recurso do produto.

Para as alterações interruptivas que afetam somente o tempo de compilação, mas são compatíveis binárias com ambientes de área restrita e de produção, o tempo de preterimento será inferior a 12 meses. Normalmente, essas alterações são atualizações funcionais que precisam ser feitas no compilador.
