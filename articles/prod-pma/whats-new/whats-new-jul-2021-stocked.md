---
title: Novidades ou alterações no Project Operations de julho de 2021 para cenários baseados em estoque/produção
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de julho de 2021 do Project Operations cenários baseados em estoque/produção.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: fb1814330b5e474ccbda0ab85dd67758a6f270a9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334501"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Novidades ou alterações no Project Operations de julho de 2021 para cenários baseados em estoque/produção

_**Aplicável a:** Project Operations para cenários baseados em estoque/produção_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance versão 10.0.20
 
### <a name="quality-updates"></a>Atualizações de qualidade
                                                                                                                                                                                  
| Área do recurso                      | Número de referência| Atualização de qualidade                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gerenciamento e contabilidade de projeto | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Os registros de compromisso de custo de uma requisição de compra são compensados assim que a ordem de compra é liberada da emissão da requisição de compra.                                                                           |
| Gerenciamento e contabilidade de projeto | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | A validação do orçamento ocorre duas vezes em uma requisição de compra. Essa duplicação significa que a requisição não pode ser fechada e a ordem de compra correspondente não é criada.                                                                                                                        |
| Gerenciamento e contabilidade de projeto | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | A regra de faturamento **Percentual para faturar em** pôde ser concluída devido a um problema de arredondamento.                                                                              |
| Gerenciamento e contabilidade de projeto | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Quando você ajusta a transação e a porcentagem tem decimais, o custo e o preço de venda não são ajustados corretamente.                                      |
| Gerenciamento e contabilidade de projeto | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | O explorador da origem de contabilidade mostra horas para uma única linha da folha de ponto para várias linhas da folha de ponto com atividades diferentes.                                      |
| Gerenciamento e contabilidade de projeto | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | As visualizações salvas e a personalização dos detalhes da linha da linha da folha de ponto fazem com que o sistema sempre abra os detalhes do primeira folha de ponto na lista ao tentar abrir uma folha de ponto.  |
| Gerenciamento e contabilidade de projeto | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | O nó raiz do projeto desaparece e os registros da estrutura de detalhamento de trabalho são excluídos após a importação.                                                                                             |
| Gerenciamento e contabilidade de projeto | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Quando os itens são recebidos e emitidos parcialmente da necessidade do item, o sistema atualiza o saldo de consumo do orçamento incorreto. |
| Gerenciamento e contabilidade de projeto | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | As ordens de compra de retenção do projeto não estão mostrando os totais corretamente no painel **Totais** ou na grade **Fatura pendente**.                                                                  |
| Gerenciamento e contabilidade de projeto | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Ao fechar o estoque, os ajustes de custo do item do projeto são lançados na conta de saldo, em vez de na conta de lucros e perdas.                                                            |
| Gerenciamento e contabilidade de projeto | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Um voucher de transação publicado pelo projeto e um voucher de estimativa usam USD como moeda contábil, mas o valor está mostrando o que seria o equivalente em CAD.              |
| Gerenciamento e contabilidade de projeto | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Os custos comprometidos com um requisito de item e ordem de compra estão errados no processo de fatura da ordem de compra com recebimento de produto de parte e faturamento de parte.       |
| Gerenciamento e contabilidade de projeto | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | O ajuste do projeto não está atualizando corretamente o valor das vendas com custos indiretos.                                                                                    |
| Gerenciamento e contabilidade de projeto | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | A tabela **Folha de ponto** não tem um relacionamento definido com a exibição **Trabalhador/Recurso**.                                                                                   |
| Gerenciamento e contabilidade de projeto | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Não é possível preencher o campo **Número de atividade** ao selecioná-lo no menu suspenso para uma folha de ponto entre empresas.                                                                 |
| Gerenciamento e contabilidade de projeto | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Não é possível adicionar um campo **Objetivo** ou **Descrição da atividade** às seguintes páginas: **Transação postada do projeto**, **Criação de proposta de fatura** ou **Proposta de fatura**.  |
| Gerenciamento e contabilidade de projeto | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | O controle de data de entrega incorreto é fornecido quando você cria requisitos de itens usando o gerenciamento de dados (**ProjSalesItemRequirementEntity**).                                              |
| Gerenciamento e contabilidade de projeto | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Quando você seleciona um ID de contrato de projeto no Finance, o ambiente integrado do Project Operations abre a página para criar um novo registro, em vez de abrir o contrato do projeto existente.                                                                                                                 |
| Gerenciamento e contabilidade de projeto | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  O rótulo, "@SYS4083080" ("Não foi possível encontrar um registro de Trabalhador exclusivo correspondente aos valores inseridos") não foi traduzido para o dinamarquês.                                |
| Gerenciamento e contabilidade de projeto | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | O campo **Grupo de impostos de itens** não é editável em uma proposta de fatura.                                                                               |
| Gerenciamento e contabilidade de projeto | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | O custo comprometido é superestimado com valores de impostos não dedutíveis.                                                                                                    |
| Gerenciamento e contabilidade de projeto | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Lançar uma folha de horas entre empresas com vários projetos e diferentes dimensões financeiras gera valores inesperados no razão geral.                             |
| Gerenciamento e contabilidade de projeto | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | As linhas da proposta de fatura são duplicadas devido à várias instâncias de processos periódicos **Importar da preparação** em execução ao mesmo tempo.                                      |
| Gerenciamento e contabilidade de projeto | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Há um erro no lançamento da proposta de nota de crédito, portanto, as transações no voucher não são balanceadas.    |
| Gerenciamento e contabilidade de projeto | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Os custos comprometidos do projeto tornam-se incorretos depois que as faturas pendentes em espera são liberadas.                                                                             |
| Gerenciamento e contabilidade de projeto | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Você não pode criar uma nota de crédito para uma ordem de venda de projeto quando o imposto está em uma moeda diferente da moeda da empresa.                                      |
| Gerenciamento e contabilidade de projeto | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | A exclusão de um contrato também exclui o endereço associado ao cliente.                                                                                     |
| Gerenciamento e contabilidade de projeto | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Não é possível lançar uma proposta de fatura resultante de uma correção de transação de tempo negativo.                                                                    |
| Viagens e Despesas                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | O imposto é calculado de maneira diferente nos relatórios de despesas.                                                                                                                  |
| Viagens e Despesas                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Atualização de lançamento **DB72_Expense.updateTrvExpTransProjTransId()** não permite **trvExpTrans.ReferenceDataAreaId** para criar a nova sequência numérica.                    |
| Viagens e Despesas                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | O valor apresentado não consta com o campo obrigatório.                                                                                                             |
| Viagens e Despesas                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Melhorias no desempenho de anexar uma despesa ao relatório de despesas usando a interface do usuário Despesa Reinventada.                                                            |
| Viagens e Despesas                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Você pode excluir relatórios de despesas lançados.                                                                                           |
| Viagens e Despesas                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | A mensagem da política de despesas é exibida várias vezes.                                                                                                       |
| Viagens e Despesas                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | O campo **Forma de pagamento** está incluído no painel **Nova despesa**.                                                                                                      |
| Viagens e Despesas                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | A ferramenta **Redefinir o status do documento de despesas** deve redefinir o status do relatório de despesas para **Rascunho** se o fluxo de trabalho não foi encontrado. 

### <a name="regulatory-updates"></a>Atualizações regulatórias
Para obter informações sobre atualizações regulatórias do Finance and Operations, consulte [Atualizações regulatórias](/dynamics365/finance/localizations/regulatory-updates). Você também pode entrar no Lifecycle Services (LCS) e visualizar as atualizações regulamentares planejadas usando a ferramenta de pesquisa de problemas. A pesquisa de problemas permite pesquisar por país, tipo de recurso e versão.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
