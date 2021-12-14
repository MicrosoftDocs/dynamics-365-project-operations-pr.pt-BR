---
title: Novidades ou alterações no Project Operations, outubro de 2021 para cenários baseados em estoque/produção
description: Este tópico fornece informações sobre as atualizações de qualidade, que estão disponíveis na versão de outubro de 2021 do Project Operations para cenários baseados em estoque/produção.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818462"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novidades ou alterações no Project Operations, outubro de 2021 para cenários baseados em estoque/produção

_**Aplicável a:** Project Operations para cenários baseados em estoque/produção_

Este tópico se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.22
 
## <a name="quality-updates"></a>Atualizações de qualidade

| Área do recurso | Número de referência | Atualização de qualidade |
|--------------|------------------|----------------|
| Gerenciamento e contabilidade de projeto | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | O trabalho em andamento do projeto (WIP) e os valores de receita acumulada não são revertidos corretamente quando uma fatura de cliente intercompanhia é postada. |
| Gerenciamento e contabilidade de projeto | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | A funcionalidade **Impedir o fechamento do projeto se houver transações abertas** não funciona. |
| Gerenciamento e contabilidade de projeto | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | A classificação do faturamento em uma fatura de texto livre não preenche automaticamente as dimensões de projetos quando essa funcionalidade está habilitada. |
| Gerenciamento e contabilidade de projeto | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Em cenários não intercompanhia, o WIP e os valores de receita acumulada não são revertidos corretamente quando a fatura de projeto é postada. |
| Gerenciamento e contabilidade de projeto | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Os valores de débito e crédito são alternados quando o suplemento do Microsoft Excel é usado com o diário de despesas do projeto e o campo **Tipo de conta de compensação** é definido como **Projeto**. |
| Gerenciamento e contabilidade de projeto | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | O valor postado em transações do projeto é exagerado em um pedido de compra do projeto que inclui itens em estoque e que tem valores de impostos não dedutíveis quando **UseTax** é marcado. |
| Gerenciamento e contabilidade de projeto | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | O sistema divide o valor entre os relatórios de lucros e perdas do projeto e os relatórios WIP do projeto. |
| Gerenciamento e contabilidade de projeto | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | O estoque disponível fica incorreto depois que um requisito de item parcialmente devolvido é ajustado. |
| Gerenciamento e contabilidade de projeto | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Os nomes dos recursos são duplicados no Project Operations quando são editados no Microsoft Project. |
| Gerenciamento e contabilidade de projeto | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Os relatórios de despesas intercompanhia que têm custos de fatura de fornecedor pendentes de Contas a pagar são postados primeiro no tipo de postagem **Custo WIP do projeto**. No entanto, durante o processamento, os custos relacionados à estimativa são postados no tipo de postagem **Custo do projeto** em vez do tipo de postagem **Custo intercompanhia** esperado. |
| Gerenciamento e contabilidade de projeto | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Os resultados da retenção do fornecedor nas transações de despesas do projeto não são mostrados. |
| Gerenciamento e contabilidade de projeto | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | A folha de ponto deve arredondar o valor da transação na moeda da transação para um número especificado de casas decimais em todas as distribuições contábeis e entradas de alocação de diário geral. |
| Gerenciamento e contabilidade de projeto | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | As quantidades de requisitos de itens de projeto são atualizadas automaticamente quando as ordens planejadas são firmadas. |
| Gerenciamento e contabilidade de projeto | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | O número do comprovante, o saldo do fornecedor do tipo de transação e o número da conta não podem ser revertidos na fatura de pré-pagamento de um pedido de compra. |
| Gerenciamento e contabilidade de projeto | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A fatura do fornecedor intercompanhia é dividida quando a integração da fatura do fornecedor é ativada. |
| Gerenciamento e contabilidade de projeto | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Quando você cria um diário de despesas do projeto, o valor do custo é mostrado no campo **Crédito**. |
| Gerenciamento e contabilidade de projeto | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | O termos de pagamento das faturas do projeto não funcionam conforme o esperado. |
| Gerenciamento e contabilidade de projeto | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Os comprovantes de folha de ponto podem ser reutilizados quando a sequência numérica é configurada como contínua. |
| Gerenciamento e contabilidade de projeto | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANÇA: a lógica **Quantidade de retenção manual** não corresponde à lógica **Quantidade de retenção automática** na proposta de fatura do contrato do projeto. |
| Gerenciamento e contabilidade de projeto | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quando a retenção do fornecedor é liberada, a postagem do comprovante tem linhas adicionais incorretas. |
| Gerenciamento e contabilidade de projeto | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Quando o campo **Data da fatura** na página **Criar proposta de fatura** for alterado, o seguinte erro poderá ocorrer: "Referência de objeto não definida para uma instância de um objeto." |
| Gerenciamento e contabilidade de projeto | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Ocorre um erro quando você tenta aprovar uma folha de ponto do fluxo de trabalho **TSLine** e há uma política de folha de ponto para sábado e domingo. |
| Gerenciamento e contabilidade de projeto | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | O tipo de item de projeto de saldo inicial é excluído de **Resumos de transações de propostas de faturas** quando o total da fatura da proposta de fatura é calculado. |
| Gerenciamento e contabilidade de projeto | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Se o custo de consumo em uma ordem de produção do projeto for 0 (zero), ocorrerá o seguinte erro quando você tentar fazer a estimativa: "Tentativa de divisão por zero." |
| Gerenciamento e contabilidade de projeto | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | O aplicativo Project Timesheet Mobile para Android para de responder. O problema está relacionado a **TimeEntryDataManager ArgumentNullException**. |
| Gerenciamento e contabilidade de projeto | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Falha no diário de integração do Project Operations quando você o posta porque faltam dimensões em uma conta. No entanto, a conta que não tem as dimensões não é a conta em que você faz a postagem. |
| Gerenciamento e contabilidade de projeto | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | O filtro **ToDate** em pesquisas não é limpo quando é removido da caixa de diálogo **Selecionar** na página **Postar custos**. |
| Gerenciamento e contabilidade de projeto | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Redefinir toda a distribuição** falha e mostra um erro para as folhas de ponto que são criadas para um projeto do tipo **Somente hora**. |
| Gerenciamento e contabilidade de projeto | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A guia **Projeto** não é editável em uma fatura de fornecedor pendente quando a categoria de compras é atribuída ao item. |
| Gerenciamento e contabilidade de projeto | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | O painel de navegação estará ausente se você não estiver conectado ao Project Operations Dataverse. |
| Gerenciamento e contabilidade de projeto | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Para transações de ajuste de projeto intercompanhia, há problemas na empresa de destino. |
| Gerenciamento e contabilidade de projeto | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Os custos comprometidos para um projeto calcularão a quantidade errada e o preço de custo se o pedido de compra foi processado por **Processamento de final de ano para ordem de compra** no razão geral. |
| Gerenciamento e contabilidade de projeto | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Quando uma ordem de produção de projeto com ordens de qualidade é relatada como concluída, ocorre o seguinte erro: "Nenhuma transação virtual marcada com transação de estoque." |
| Gerenciamento e contabilidade de projeto | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Quando uma fatura de Contas a pagar relacionada ao projeto é postada, ocorre o seguinte erro: "Projeto de texto enumerado - custo - item não existe." |
| Gerenciamento e contabilidade de projeto | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Os custos indiretos dobram quando você acumula receita manualmente. |
| Gerenciamento e contabilidade de projeto | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | A receita acumulada e a postagem de WIP não geram transações. |
| Gerenciamento e contabilidade de projeto | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | A ativação do preço pendente falha para um item de custo padrão quando existe uma ordem de compra de projeto recebida. |
| Gerenciamento e contabilidade de projeto | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | O valor do WIP estornado de uma postagem da fatura difere do valor original do WIP postado em uma entrada de hora. |
| Gerenciamento e contabilidade de projeto | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Há um problema de postagem da receita faturada do projeto em casos de honorários aplicados em que as transações no comprovante não são equilibradas. |
| Gerenciamento e contabilidade de projeto | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A criação de uma estimativa após a postagem de uma proposta de fatura bloqueia a importação de linhas de correção no Project Operations. |
| Gerenciamento e contabilidade de projeto | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A modificação de um registro de etapa totalmente faturado não deve ser possível. |
| Gerenciamento e contabilidade de projeto | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Quando os encargos automáticos são usados, a fatura do cliente intercompanhia para uma folha de ponto não pode ser postada e uma mensagem de erro é exibida. |
| Gerenciamento e contabilidade de projeto | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | O endereço em um subprojeto não foi atualizado corretamente. |
| Gerenciamento e contabilidade de projeto | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | O preço de custo em requisitos do item é atualizado com o preço de compra para pedidos de compra consolidados. |
| Gerenciamento e contabilidade de projeto | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | O custo postado não está correto depois que o preço de compra é atualizado e o parâmetro **Ativar gerenciamento de alterações** é habilitado. |
| Viagens e Despesas | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Todas as despesas de usuário podem ser vistas quando você pesquisa uma categoria no aplicativo móvel de despesas. |
| Viagens e Despesas | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Valores incorretos em transações de fornecedores e transações de impostos postados de uma despesa que foi criada a partir de uma transação de cartão de crédito. |
| Viagens e Despesas | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Uma mensagem de aviso irrelevante é mostrada quando você atualiza as páginas de relatório de despesas. |
| Viagens e Despesas | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | O aprovador provisório errado é usado quando você exclui um aprovador provisório e, depois, reenvia por meio do fluxo de trabalho. |
| Viagens e Despesas | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ocorre um erro de postagem relacionado à configuração de milhagem. |
| Viagens e Despesas | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | A distribuição não atualiza a entidade legal quando uma transação não anexada é adicionada novamente ao relatório de despesas em uma despesa intercompanhia. |

### <a name="regulatory-updates"></a>Atualizações regulatórias

Para obter informações sobre atualizações regulatórias do Finance and Operations, consulte [Atualizações regulatórias](/dynamics365/finance/localizations/regulatory-updates). Você também pode entrar no Microsoft Dynamics Lifecycle Services (LCS) e usar a ferramenta de pesquisa de problemas para exibir as atualizações regulamentares planejadas. A pesquisa de problemas permite pesquisar por país ou região, tipo de recurso e versão.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
