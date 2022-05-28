---
title: Estimando uma linha de cotação baseada no projeto
description: Este tópico fornece informações sobre como criar uma estimativa em uma linha de cotação baseada no projeto.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a29cf20fe95ee5bfb189defded4f06aadb75a841
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598336"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimando uma linha de cotação baseada no projeto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Uma linha de cotação baseada no projeto contém detalhes que ajudam a estimar o custo e a receita potencial do trabalho envolvido para entregar a linha de cotação.

Para estimar uma linha de cotação baseada no projeto, na linha de cotação baseada no projeto, selecione a guia **Detalhe da Linha de Cotação**. Há duas formas de criar uma estimativa em uma linha de cotação baseada no projeto:

- Criar manualmente a estimativa diretamente na linha de cotação usando os detalhes da linha de cotação. 
- Criar um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas no projeto à linha de cotação. O processo de importação das estimativas no plano do projeto para a linha de cotação com base nas informações fornecidas será habilitado.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Criar estimativas diretamente em uma linha de cotação baseada no projeto

Para criar uma estimativa em uma linha de cotação baseada no projeto, selecione a guia **Detalhe da Linha de Cotação**. O item de linha que você criar nesta guia resumirá o valor cotado para esta linha de cotação. 

Para criar detalhes da linha de cotação, selecione **Novo detalhe da linha de cotação** na subgrade **Detalhes da Linha de Cotação**. Um controle deslizante de criação rápida será exibido. A tabela a seguir fornece detalhes sobre os campos na página **Detalhe da Linha de Cotação** e como os valores afetam a funcionalidade.

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Descrição | Criação rápida | Uma descrição da estimativa específica. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Classe da Transação | Criação rápida | Esta lista suspensa fornece as classes de transação que estão incluídas na guia **Geral** da linha de cotação baseada no projeto.  | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Selecionar Produto | Criação rápida | Aplica-se quando a classe de transação é **Material**. É possível optar por especificar se esta linha de estimativa é para um produto **Existente** (catálogo) ou um produto **Fora do Catálogo**. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Produto | Criação rápida | O ID do produto do catálogo de produtos. Esse campo só estará ativado se você tiver escolhido **Existente** no campo **Selecionar Produto**. A ID é usada para recuperar o preço de venda da lista de preços do projeto na cotação. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Produto Fora do Catálogo | Criação rápida | Uma caixa de texto para escrever o nome do produto. Esse campo só estará ativado se você tiver escolhido **Fora do Catálogo** no campo **Selecionar Produto**.| Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Função | Criação rápida | A função da pessoa que executará este trabalho ou incorrerá nesta despesa. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Categoria | Criação rápida | A categoria do trabalho ou da despesa. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Data de Início | Criação rápida | A data de início do trabalho. | Este campo é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Data de Término | Criação rápida | A data de término do trabalho. | Este campo é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Unidade de Recursos | Criação rápida | A unidade de recursos que irá incorrer neste custo e fornecer o recurso para trabalhar nisso. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente e usado na recuperação do preço de custo. |
| Agenda da unidade | Criação rápida | O grupo de unidades de trabalho, produto ou despesa. As unidades pertencem a uma agenda da unidade ou a um grupo de unidades. Por exemplo, milhas e quilômetros são unidades que pertencem a um grupo de unidades que descreve a distância. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Unidade | Criação rápida | A unidade de trabalho, produto ou despesa. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Quantidade | Criação rápida | A quantidade de trabalho, produto ou despesa. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Preço unitário | Criação Rápida |A taxa de faturamento da função que está executando o trabalho, o preço unitário do produto, ou o preço de venda do produto ou a categoria de despesa. O padrão para este campo é **Tempo** com base na combinação de valores de dimensão de preço na linha de preço da função da lista de preços do projeto que está em vigor para a data de início. Para **Despesas**, o padrão é da configuração de preço para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de precificação para a categoria de transação não for preço por unidade, não há padrão e este campo é deixado em branco. Para produtos, o padrão é baseado na linha **Item da lista de preços**  na lista de preços do projeto que está em vigor para a data de início.| A taxa de custo da função que está executando o trabalho, o custo por unidade da categoria de despesas ou o custo unitário do produto. O padrão para este campo é **Tempo** com base na combinação de valores de dimensão de preço na linha de preço da função da lista de preços do projeto que está em vigor para a data de início. Para **Despesas**, o padrão é da configuração de preço para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de precificação para a categoria de transação não for preço por unidade, não há padrão e este campo é deixado em branco. Para produtos, o padrão é baseado na linha **Item da lista de preços**  na lista de preços do projeto que está em vigor para a data de início.|
| Imposto Estimado | Criação rápida | Você pode inserir o imposto estimado manualmente para este trabalho ou despesa. | Não há impacto posterior para este campo. |
| Valor | Criação rápida | Você pode inserir informações manualmente neste campo se os campos **Quantidade** e **Preço** estiverem em branco. Se esses campos não estiverem em branco, ele se tornará somente leitura e calculado como (Quantidade \* Preço unitário) + Imposto. | Não há impacto posterior para este campo. |


## <a name="update-prices-on-quote-line-details"></a>Atualizar preços nos detalhes da linha de cotação

Se você alterou os preços na lista de preços do projeto que está anexada à cotação, ou na lista de preços de custo da unidade contratante, você pode selecionar **Recalcular** na página **Cotação** para atualizar os preços nos detalhes da linha de cotação individual para refletir essa mudança. Quando você seleciona **Recalcular**, um aviso aparecerá informando que os preços nos detalhes da linha de cotação para todas as linhas de cotação nesta cotação serão redefinidos. Selecione **Sim** para atualizar os preços dos detalhes da linha de cotação de vendas e de custo.

## <a name="access-quote-line-details-for-cost"></a>Acessar os detalhes da linha de cotação para custo

Na guia **Detalhes da Linha de Cotação**, selecione uma linha na grade para permitir algumas ações na barra de ferramentas da subgrade. A primeira ação na barra de ferramentas da subgrade quando um detalhe da linha de cotação é selecionado é **Abrir Detalhes do Custo**. Selecione **Abrir Detalhes de Custo** para ver a taxa de custo relacionada e o valor dessa linha de cotação.

> [!NOTE]
> Alterar os valores da unidade de recursos, da quantidade, das datas, da função ou da categoria no detalhe da linha de cotação para custos mudará os valores correspondentes nos detalhes da linha de cotação de vendas.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moeda nos detalhes da linha de cotação para custo e vendas

A moeda no detalhe da linha de cotação para os padrões de venda da lista de preços do projeto que está em vigor para a data de início do detalhe da linha de cotação.

A moeda no detalhe da linha de cotação para os padrões de custo da lista de preços da unidade de contratação da cotação que está em vigor para a data de início do detalhe da linha de cotação de custos.

Os cálculos de lucratividade convertem o valor dos detalhes da linha de cotação para custos e vendas na moeda base do ambiente para relatar a margem estimada geral da cotação.

> [!OBSERVAÇÃO
> > Erros de arredondamento de moeda e margens alteradas podem ocorrer devido à falta de taxas de câmbio efetivas de data. Use esses cálculos apenas nos contratos do projeto, pois são aproximações e não são estatutários reais ou outros relatórios que exigem maior precisão de arredondamento e consciência da data efetiva para as taxas de câmbio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
