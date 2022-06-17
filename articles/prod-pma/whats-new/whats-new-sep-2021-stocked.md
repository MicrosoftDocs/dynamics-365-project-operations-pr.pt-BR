---
title: Novidades ou alterações no Project Operations, setembro de 2021 para cenários baseados em estoque/produção
description: Este artigo fornece informações sobre as atualizações de qualidade, que estão disponíveis na versão de setembro de 2021 do Project Operations para cenários baseados em estoque/produção.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916504"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novidades ou alterações no Project Operations, setembro de 2021 para cenários baseados em estoque/produção

_**Aplicável a:** Project Operations para cenários baseados em estoque/produção_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.21
 
## <a name="quality-updates"></a>Atualizações de qualidade

| Área do recurso | Número de referência | Atualização de qualidade |
|---|---|---|
| Gerenciamento e contabilidade de projeto | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Se a função Gerente de compras tiver acesso a uma entidade legal, ela também obterá acesso a todos os projetos em todas as entidades legais. |
| Gerenciamento e contabilidade de projeto | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Um problema de arredondamento do imposto sobre valor agregado (IVA) ocorre enquanto uma nota de crédito é liquidada em relação a uma fatura de projeto original. |
| Gerenciamento e contabilidade de projeto | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Use um orçamento de projeto alternativo para verificação do orçamento. |
| Gerenciamento e contabilidade de projeto | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | O grupo de preços de **Preço de venda por hora** não é calculado na estrutura de detalhamento de trabalho para as cotações do projeto. |
| Gerenciamento e contabilidade de projeto | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Há falha na eliminação da estimativa quando o recurso **Habilitar moeda do contrato de projeto para o cálculo de estimativa** está habilitado. |
| Gerenciamento e contabilidade de projeto | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | A fatoração do imposto sobre vendas por quantidade é adicionada ao valor do preço de venda quando o imposto de uso é usado no grupo de impostos sobre vendas do diário de despesas do projeto. |
| Gerenciamento e contabilidade de projeto | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | O imposto condicional não é calculado corretamente para o último pagamento quando a retenção do fornecedor e o pré-pagamento são aplicados a faturas de ordem de compra. |
| Gerenciamento e contabilidade de projeto | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | O rastreamento de ajuste não funciona para diários de saldo inicial. |
| Gerenciamento e contabilidade de projeto | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Alocação da revisão do orçamento do projeto por período** é dividida em todos os períodos do orçamento. Quando a alocação é enviada, o registro não é limpa. |
| Gerenciamento e contabilidade de projeto | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | As postagens de trabalho em andamento (WIP) no razão têm um valor incorreto. |
| Gerenciamento e contabilidade de projeto | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | A aprovação do diário de horas do projeto não funciona. |
| Gerenciamento e contabilidade de projeto | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | O preço de venda do ajuste do projeto não é atualizado com custos indiretos quando o limite de financiamento não está marcado. |
| Gerenciamento e contabilidade de projeto | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Um requisito de item não pode ser criado quando o cabeçalho da tabela de vendas é faturado e a ordem de compra de backup para as linhas existentes foi finalizada. |
| Gerenciamento e contabilidade de projeto | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | O valor de retenção para uma regra de cobrança que tem uma etapa para um projeto diferente não é postado na ID do projeto correspondente que foi selecionada para a etapa. Ele é postado com o primeiro projeto. |
| Gerenciamento e contabilidade de projeto | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Quando você seleciona **Conjunto de dimensões financeiras** em uma proposta de fatura, ocorre o seguinte erro: "Impossível lançar objeto do tipo 'Dynamics.AX.Application.FormIntControl' para o tipo 'Dynamics.AX.Application.FormStringControl'." |
| Gerenciamento e contabilidade de projeto | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | O relatório **Fatura do projeto** ignora linhas. |
| Gerenciamento e contabilidade de projeto | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Ocorre um erro ao calcular o controle de custos para um projeto de investimento. |
| Gerenciamento e contabilidade de projeto | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | O método **ProjTable::InitFromCustTable - canDeletePostalAddress** causa um problema de desempenho. |
| Gerenciamento e contabilidade de projeto | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | A mensagem de erro deve ser mais clara do que "Erro inesperado". |
| Gerenciamento e contabilidade de projeto | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | O trabalho em lote de postagem de fatura do projeto processará e postará a proposta de fatura, mesmo que as linhas da fatura não tenham sido geradas. |
| Gerenciamento e contabilidade de projeto | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Um problema de arredondamento ocorre quando a chave de configuração de licença do setor público é desativada. Um custo ou preço de venda incorreto é gerado nas horas da folha de ponto para contratos com várias fontes de fundação. |
| Gerenciamento e contabilidade de projeto | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | O preço de venda do projeto em uma ordem de compra do projeto faturada é calculado incorretamente quando o modelo de preço de venda é **Relação de contribuição**. |
| Gerenciamento e contabilidade de projeto | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | O sistema não considera os dias ativos intermediários ao calcular a taxa efetiva de trabalho de um funcionário. |
| Gerenciamento e contabilidade de projeto | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Um erro de postagem ocorre na folha de ponto intercompanhia devido ao seguinte erro de validação: "Nenhum parceiro comercial está configurado para entidade legal." |
| Gerenciamento e contabilidade de projeto | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | A descrição de uma ordem de compra que tem uma categoria de despesas não é recuperada na lista de transações do projeto postada. |
| Gerenciamento e contabilidade de projeto | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Há uma conversão incorreta em diários de item que são postados em um projeto. |
| Gerenciamento e contabilidade de projeto | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Você poderá confirmar uma ordem de compra mesmo se o limite de financiamento for excedido. |
| Gerenciamento e contabilidade de projeto | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | A seção **Correção/Cancelar fatura** em uma fatura de texto livre desaparece quando uma ID de projeto é selecionada. |
| Gerenciamento e contabilidade de projeto | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Há problemas de desempenho quando uma proposta de fatura do projeto é postada de uma ordem de venda do projeto que inclui um item em estoque. |
| Gerenciamento e contabilidade de projeto | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | As faturas de compra do projeto não podem ser postadas porque ocorre o seguinte erro: "A função AccDistProcessorProjectExtension.createForProjectRevenueLine foi chamada incorretamente." |
| Gerenciamento e contabilidade de projeto | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Atualize para a criação de trabalhos em lote de estimativa de projeto para dar suporte à execução de várias subtarefas. |
| Gerenciamento e contabilidade de projeto | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | O status de uma folha de ponto não pode ser atualizado para **Rascunho** quando o fluxo de trabalho está preso em um estado **Cancelado**. |
| Gerenciamento e contabilidade de projeto | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Os valores de retenção não serão calculados na proposta de fatura da nota de crédito se houver várias linhas. |
| Gerenciamento e contabilidade de projeto | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Ao tentar alterar o valor em uma fatura gerada a partir de uma ordem de compra, ocorre o seguinte erro: "As transações no comprovante não têm saldo de acordo com XX/XX/XXXX. (moeda contábil: 0,00 – moeda de relatório: 0,01)." |
| Gerenciamento e contabilidade de projeto | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Há um problema de desempenho quando uma proposta de fatura do projeto é postada no modo em lote, por causa da união com **GeneralJournalAccountEntry**. |
| Gerenciamento e contabilidade de projeto | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Existem problemas de desempenho quando uma folha de ponto é postada. |
| Gerenciamento e contabilidade de projeto | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | A hierarquia das estimativas de custo da estrutura de detalhamento de trabalho não está alinhada corretamente depois que todas as tarefas são expandidas ou que uma única tarefa é expandida manualmente. |
| Gerenciamento e contabilidade de projeto | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | O modelo Excel de cotação do projeto não pode ser adicionado ao menu **Abrir no Excel**. |
| Gerenciamento e contabilidade de projeto | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | O número de isenção de impostos para uma entidade legal não é incluído na fatura de projeto impressa. |
| Gerenciamento e contabilidade de projeto | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Nenhum dado financeiro é atualizado no erro da unidade de estoque quando um projeto é ajustado em relação às linhas de crédito. |
| Gerenciamento e contabilidade de projeto | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Depois de aplicar o KB 461935, você não poderá postar estimativas se alternar para sequências numéricas contínuas. |
| Gerenciamento e contabilidade de projeto | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** faz com que o aplicativo móvel de folha de ponto do projeto para Android pare de responder. |
| Gerenciamento e contabilidade de projeto | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | O valor do WIP estornado de uma postagem da fatura difere do valor do WIP postado originalmente na entrada de hora. |
| Gerenciamento e contabilidade de projeto | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Em casos de honorários aplicados, as transações em um comprovante não são equilibradas quando a receita faturada de um projeto é postada. |
| Gerenciamento e contabilidade de projeto | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Quando o recurso **Aprimoramento de desempenho de agendamento de recursos do projeto** está habilitado, os valores decimais são arredondados incorretamente para a disponibilidade e capacidade do recurso. |
| Gerenciamento e contabilidade de projeto | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Quando o recurso **Criar estimativas de projeto usando várias tarefas em lote** está habilitado, a criação de estimativas em um lote com várias subtarefas funciona apenas para o período atual. |
| Viagens e Despesas | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Uma política de requisição de viagens é ignorada e o fluxo de trabalho é aprovado sem erros. |
| Viagens e Despesas | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>O aplicativo móvel de despesas não salva as seguintes informações na linha de despesas:</p><ul><li>A ID do projeto</li><li>Se a despesa é faturável</li><li>O número da atividade</li></ul> |
| Viagens e Despesas | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | O campo **Recibos anexados** será definido como **Sim** mesmo se nenhum recibo for anexado à linha de despesas. |
| Viagens e Despesas | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Um erro ocorre quando você altera a categoria de despesas para **Pessoal**. |
| Viagens e Despesas | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Você não pode anexar um recibo e editar a despesa pai após uma transação de cartão de crédito ser dividida em despesas pessoais. |
| Viagens e Despesas | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | A política de despesas para transações intercompanhia que tem uma ID de projeto não funciona corretamente. |
| Viagens e Despesas | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | As informações da data de postagem estão ausentes nos relatórios de despesas postados. |
| Viagens e Despesas | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Existem problemas de método de pagamento no aplicativo móvel de despesas. |
| Viagens e Despesas | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Uma requisição de viagem que é criada para um trabalhador pode ser usada para o relatório de despesas de outro trabalhador antes da data delegada. |
| Viagens e Despesas | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Quando você cria uma despesa, as alterações nos valores da dimensão financeira não são atualizadas corretamente no nível da distribuição contábil no espaço de trabalho **Gerenciamento de despesas**. |
| Viagens e Despesas | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | O status de aprovação da linha de despesas principal não é sincronizado com o status de aprovação do fluxo de trabalho da linha discriminada. |
| Viagens e Despesas | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Ocorrerá um erro se você postar um relatório de despesas e a recuperação de impostos estiver habilitada. |
| Viagens e Despesas | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Um delegado não pode excluir documentos de despesas de um funcionário demitido. |
| Viagens e Despesas | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | A exclusão de uma linha de despesas leva mais tempo do que o esperado e afeta o desempenho. |
| Viagens e Despesas | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** gera um registro **TaxUncommitted** órfão porque somente **SourceDocumentLine** é excluído. |
| Viagens e Despesas | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** não honra **trvExpTrans.ReferenceDataAreaId** para criar a nova sequência numérica |

## <a name="regulatory-updates"></a>Atualizações regulatórias

Para obter informações sobre atualizações regulatórias de aplicativos de finanças e operações, consulte [Atualizações regulatórias](/dynamics365/finance/localizations/regulatory-updates). Você também pode entrar no Microsoft Dynamics Lifecycle Services (LCS) e usar a ferramenta de pesquisa de problemas para exibir as atualizações regulamentares planejadas. A pesquisa de problemas permite pesquisar por país ou região, tipo de recurso e versão.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
