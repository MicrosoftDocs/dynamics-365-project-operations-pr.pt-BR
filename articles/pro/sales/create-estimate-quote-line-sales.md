---
title: Estimando uma linha de cotação baseada no projeto
description: Este tópico fornece informações sobre como criar uma estimativa em uma linha de cotação baseada no projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966731"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimando uma linha de cotação baseada no projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Uma linha de cotação baseada no projeto contém detalhes que ajudam a estimar o custo e a receita potencial do trabalho envolvido para entregar a linha de cotação.

Para estimar uma linha de cotação baseada no projeto, na linha de cotação baseada no projeto, selecione a guia **Detalhe da Linha de Cotação**. Há duas formas de criar uma estimativa em uma linha de cotação baseada no projeto:

- Criar manualmente a estimativa diretamente na linha de cotação usando os detalhes da linha de cotação 
- Criar um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas no projeto à linha de cotação. O processo de importação das estimativas no plano do projeto para a linha de cotação com base nas informações fornecidas será habilitado.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Criar estimativas diretamente em uma linha de cotação baseada no projeto

Para criar uma estimativa em uma linha de cotação baseada no projeto, selecione a guia **Detalhe da Linha de Cotação**. O item de linha que você criar nesta guia resumirá o valor cotado para esta linha de cotação. 

Para criar detalhes da linha de cotação, selecione **+Novo detalhe da linha de cotação** na subgrade **Detalhes da Linha de Cotação**. Um controle deslizante de criação rápida será exibido. Os seguintes campos no formulário **Linha de Cotação**:

| **Campo** | **Local** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Descrição | Criação rápida | Uma descrição da estimativa específica. | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Classe da Transação | Criação rápida | Esta lista suspensa fornece as classes de transação que estão incluídas na guia **Geral** da linha de cotação baseada no projeto.  | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Função | Criação rápida | A pessoa que executará este trabalho ou incorrerá nesta despesa. | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Categoria | Criação rápida | Categoria do trabalho ou da despesa. | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Data de Início | Criação rápida | Data de início do trabalho. | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Data de Término | Criação rápida | Data de término do trabalho. | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Unidade de Recursos | Criação rápida | Unidade de recursos que incorrerá neste custo e fornecerá o recurso para trabalhar nisso. | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. Este campo também é usado na recuperação do preço de custo. |
| Agenda da unidade | Criação rápida | Grupo de unidades do trabalho ou da despesa. As unidades pertencem a uma agenda da unidade ou a um grupo de unidades. Por exemplo, Milhas e KMs são unidades que pertencem a um grupo de unidades que descreve a distância. | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Unidade | Criação rápida | Unidade do trabalho ou da despesa. | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Quantidade | Criação rápida | Quantidade do trabalho ou da despesa | O padrão deste campo é o detalhe da linha de cotação relacionada que é criada automaticamente. |
| Preço unitário | Criação rápida | Taxa de cobrança da função que está executando o trabalho ou o Preço de venda da categoria de despesas. Este campo é padronizado para Hora com base na combinação de função e unidade de recursos na lista de preços do projeto efetiva para a data de início. Para despesas, este campo é padronizado com base na configuração de preço para a categoria de transação na lista de preços do projeto que está em vigor para a data de início. Se o método de precificação da categoria de transação não for preço por unidade, não haverá padrão e este campo ficará em branco. | Taxa de custo da função que está executando o trabalho ou o preço por unidade da categoria de despesas. Este campo é padronizado para Hora com base na combinação de função e unidade de recursos no preço da Unidade de contratação da Lista de preços da cotação que está em vigor para a data de início. Para despesas, este campo é padronizado com base na configuração de preço para a categoria de transação na lista de preços de custo da Unidade de contratação que está em vigor para a data de início. Se o método de precificação da categoria de transação não for preço por unidade não haverá padrão e este campo ficará em branco. |
| Imposto Estimado | Criação rápida | Você pode inserir o imposto estimado manualmente para este trabalho ou despesa. | Não há impacto a jusante deste campo. |
| Valor | Criação rápida | Você pode inserir informações manualmente neste campo se os campos **Quantidade** e **Preço** estiverem em branco. Se esses campos não estiverem em branco, ele se tornará somente leitura e calculado como (Quantidade \* Preço unitário) + Imposto. | Não há impacto a jusante deste campo. |

## <a name="update-prices-on-quote-line-details"></a>Atualizar preços nos detalhes da linha de cotação

Se você alterou preços na lista de preços do projeto que está anexado à cotação, ou na lista de preços de custo da unidade de contratação, será possível selecionar **Recalcular** na página **Cotação**, para atualizar os preços nos detalhes da linha de cotação individual para refletir essa alteração. Ao selecionar **Recalcular**, um aviso é gerado informando que os preços nos detalhes da linha de cotação de todas as linhas de cotação nessa cotação serão redefinidos. Selecione **Sim** para atualizar os preços dos detalhes da linha de cotação de vendas e de custo.

## <a name="access-quote-line-details-for-cost"></a>Acessar os detalhes da linha de cotação para custo

Na guia **Detalhes da Linha de Cotação**, selecione uma linha na grade para habilitar algumas ações na barra de ferramentas da subgrade. A primeira ação na barra de ferramentas da subgrade quando um detalhe da linha de cotação selecionado for **Abrir Detalhes de Custo**. Selecione **Abrir Detalhes de Custo** para ver a taxa de custo relacionada e o valor dessa linha de cotação.

> [!NOTE]
> Alterar os valores da unidade de recursos, da quantidade, das datas, da função ou da categoria no detalhe da linha de cotação para custos mudará os valores correspondentes nos detalhes da linha de cotação de vendas.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moeda nos detalhes da linha de cotação para custo e vendas

A moeda no detalhe da linha de cotação para os padrões de venda da lista de preços do projeto que está em vigor para a data de início do detalhe da linha de cotação.

A moeda no detalhe da linha de cotação para os padrões de custo da lista de preços da unidade de contratação da cotação que está em vigor para a data de início do detalhe da linha de cotação de custos.

Os cálculos de lucratividade convertem o valor dos detalhes da linha de cotação para custos e vendas na moeda base do ambiente para relatar a margem estimada geral da cotação.

Isso pode resultar em erros de arredondamento de moeda e alteração das margens devido à falta de taxas de câmbio de data efetiva. Use esses cálculos nas cotações do Projeto somente como aproximações e não em relatórios estatutários reais ou outros que exijam maior precisão de arredondamento e conhecimento da efetividade da data para as taxas de câmbio.
