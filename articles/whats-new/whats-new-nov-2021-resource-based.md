---
title: Novidades em novembro de 2021 – Project Operations para cenários baseados em recursos/sem estoque
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de novembro de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932880"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em novembro de 2021 – Project Operations para cenários baseados em recursos/sem estoque

*Aplicável A: Project Operations para cenários baseados em recursos/sem estoque*

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em uma versão 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155 do ambiente do Dataverse
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.22

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- As interfaces de programação de aplicativos (APIs) de Agendamento de Projeto agora permitem criar e excluir buckets de projetos.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão. Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-in-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2240080 | O campo **Termos de pagamento** não deve ser duplicado na fatura pro forma. |
| Cobrança e preço | 2358236 | A correção da fatura deve permitir correções com linhas de preço zero. |
| Gerenciamento de Recursos | 2410072 | Permita a configuração de um recurso atribuído à tarefa como um gerente de projeto. |
| Cobrança e preço | 2430234 | Corrija um problema de cálculo de desempenho de custo. |
| Tempo e Despesa | 2436978 | Permita que o tempo seja inserido no formato hh:mm. |
| Cobrança e preço | 2448623 | Permita que listas de preços sejam atualizadas após serem associadas a uma unidade organizacional. |
| Tempo e Despesa | 2460396 | Permita que uma entrada de tempo seja excluída limpando a célula. |
| Cobrança e preço | 2467386 | Permita que um projeto com uma tarefa seja excluído, mesmo quando a tarefa esteja associada a uma cotação ganha. |
| Tempo e Despesa | 2461744 | A exibição **Minha aprovação com falha** contém apenas aprovações de projetos no estágio **Enviado**. |
| Tempo e Despesa | 2464082 | Remova o link de aprovações de projeto para o conjunto de aprovações quando um status de destino for correspondido. |
| Tempo e Despesa | 2468108 | O trabalho de agendamento não deve definir um status **Processando** para o conjunto de aprovações. |
| Tempo e Despesa | 2471503 | Exclua conjuntos de aprovações com sete dias. |
| Cobrança e preço | 2480687 | A referência da linha de cotação não deve ser removida quando uma etapa de linha de cotação é criada. |

### <a name="project-management-and-accounting-in-finance"></a>Gerenciamento e contabilidade de projeto no Finance

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gerenciamento e contabilidade de projeto | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Os valores do fornecedor retidos em transações de despesas do projeto não são mostrados na lista de transações. |
| Gerenciamento e contabilidade de projeto | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A fatura do fornecedor intercompanhia é dividida quando a integração da fatura do fornecedor é ativada. |
| Gerenciamento e contabilidade de projeto | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | O termos de pagamento das faturas do projeto não funcionam conforme o esperado. |
| Gerenciamento e contabilidade de projeto | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quando a retenção do fornecedor é liberada, o lançamento do comprovante tem linhas adicionais incorretas. |
| Gerenciamento e contabilidade de projeto | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Quando o diário de integração do Project Operations é lançado, ele falha devido a dimensões ausentes em uma conta em que não estão sendo lançadas. |
| Gerenciamento e contabilidade de projeto | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A guia **Projeto** não é editável em uma fatura de fornecedor pendente quando a categoria de compras é atribuída ao item. |
| Gerenciamento e contabilidade de projeto | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | O painel de navegação estará ausente se você não estiver conectado ao Project Operations Dataverse. |
| Gerenciamento e contabilidade de projeto | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Quando você lança a receita de uma fatura de projeto em um caso de honorários aplicado, ocorre um problema porque as transações no comprovante não são equilibradas. |
| Gerenciamento e contabilidade de projeto | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A criação de uma estimativa após o lançamento de uma proposta de fatura bloqueia as linhas de correção da importação. |
| Gerenciamento e contabilidade de projeto | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A modificação de um registro de etapa totalmente faturado não deve ser possível. |
| Viagens e Despesas | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Todos os relatórios de despesas ficam visíveis quando você pesquisa uma categoria no aplicativo móvel de despesas. |
| Viagens e Despesas | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Valores incorretos em transações de fornecedores e transações de impostos lançados de uma despesa criada a partir de uma transação de cartão de crédito. |
| Viagens e Despesas | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Um aviso irrelevante ocorre quando você atualiza a página **Relatório de despesas**. |
| Viagens e Despesas | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | O aprovador provisório errado é usado quando você exclui um aprovador provisório e, depois, reenvia um relatório de despesas por meio do fluxo de trabalho. |
| Viagens e Despesas | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ocorre um erro de postagem relacionado à configuração de milhagem. |
