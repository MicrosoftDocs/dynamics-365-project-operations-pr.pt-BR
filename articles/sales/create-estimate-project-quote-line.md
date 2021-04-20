---
title: Estimar uma linha de cotação do projeto
description: Este tópico fornece informações sobre como criar uma estimativa em uma linha de cotação do projeto.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b941511f842a81764ddd1c05a437578b9fd902ce
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858774"
---
# <a name="estimate-a-project-quote-line"></a>Estimar uma linha de cotação do projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Uma linha de cotação baseada no projeto contém detalhes que ajudam a estimar o custo e a receita potencial do trabalho envolvido para entregar a linha de cotação.

Para estimar uma linha de cotação baseada em projeto, na linha de cotação, selecione a guia **Detalhe da Linha de Cotação**. Existem duas maneiras de criar uma estimativa em uma linha de cotação baseada em projeto:

   - Criar manualmente a estimativa diretamente na linha de cotação usando os detalhes da linha de cotação. 
   - Criar um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas no projeto à linha de cotação. O processo de importação das estimativas no plano do projeto para a linha de cotação com base nas informações fornecidas será habilitado.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Criar estimativas diretamente em uma linha de cotação baseada no projeto

Para criar estimativas diretamente em uma linha de cotação baseada em projeto, siga estas etapas:

1. Para criar uma estimativa em uma linha de cotação baseada no projeto, selecione a guia **Detalhe da Linha de Cotação**. O item de linha que você criar nesta guia resumirá o valor cotado para esta linha de cotação. 
2. Para criar detalhes da linha de cotação, selecione **Novo detalhe da linha de cotação** na subgrade **Detalhes da Linha de Cotação**. Um controle deslizante de criação rápida será exibido. Os seguintes campos na pagina **Linha de Cotação**.

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Descrição | Criação rápida | Uma descrição da estimativa específica. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Classe da Transação | Criação rápida | Esta lista suspensa fornece as classes de transação que estão incluídas na guia **Geral** da linha de cotação baseada no projeto.  | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Selecionar Produto | Criação rápida | Aplica-se quando a classe de transação é **Material**. É possível optar por especificar se esta linha de estimativa é para um produto **Existente** (catálogo) ou um produto **Fora do Catálogo**. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Produto | Criação rápida | O ID do produto do catálogo de produtos. Esse campo só estará ativado quando você selecionar **Existente** no campo **Selecionar Produto**. A ID é usada para recuperar o preço de venda da lista de preços do projeto na cotação. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Produto Fora do Catálogo | Criação rápida | Uma caixa de texto para escrever o nome do produto. Esse campo só estará ativado quando você selecionar **Fora do Catálogo** no campo **Selecionar Produto**.| Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Função | Criação rápida | A função da pessoa que executará este trabalho ou incorrerá nesta despesa. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Categoria | Criação rápida | A categoria do trabalho ou da despesa. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Data de Início | Criação rápida | A data de início do trabalho. | Este campo é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Data de Término | Criação rápida | A data de término do trabalho. | Este campo é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Empresa de Recursos | Criação Rápida | A empresa de recursos ou entidade legal irá incorrer neste custo e fornecer o recurso para trabalhar nisso. | O valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente e usado na recuperação do preço de custo. |
| Unidade de Recursos | Criação rápida | A unidade de recursos que irá incorrer neste custo e fornecer o recurso para trabalhar nisso. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente e usado na recuperação do preço de custo. |
| Agenda da unidade | Criação rápida | O grupo de unidades de trabalho, produto ou despesa. As unidades pertencem a uma agenda da unidade ou a um grupo de unidades. Por exemplo, milhas e quilômetros são unidades que pertencem a um grupo de unidades que descreve a distância. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Unidade | Criação rápida | A unidade de trabalho, produto ou despesa. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Quantidade | Criação rápida | A quantidade de trabalho, produto ou despesa. | Este valor é padronizado para o detalhe da linha da cotação relacionado para o custo que é criado automaticamente. |
| Preço unitário | Criação Rápida |A taxa de faturamento da função que está executando o trabalho, o preço unitário do produto, ou o preço de venda do produto ou a categoria de despesa. O padrão para **Tempo** é baseado na combinação de valores de dimensão de preço na linha de preço da função da lista de preços do projeto que está em vigor para a data de início. Para **Despesas**, o padrão é da configuração de preço para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de precificação da categoria de transação não for preço por unidade, não haverá padrão e este campo ficará em branco. Para produtos, o padrão deste campo é baseado na linha **Item da lista de preços** na lista de preços do projeto que está em vigor para a data de início.| A taxa de custo da função que está executando o trabalho, o custo por unidade da categoria de despesas ou o custo unitário do produto. O padrão para **Tempo** com base na combinação de valores de dimensão de preço na linha de preço da função da lista de preços de custo anexada à unidade de contratação efetiva para a data de início. Para despesas, o padrão é baseado na linha de preço da categoria da lista de preços de custo anexada à unidade de contratação que é efetiva para a data de início. Se o método de precificação para a categoria de transação não for preço por unidade, não há padrão e este campo é deixado em branco. Para produtos, este padrão do campo é baseado na linha do **Item da lista de preços** da lista de preços de custo anexada à unidade de contratação que é efetiva para a data de início.|
| Imposto Estimado | Criação rápida | Você pode inserir o imposto estimado manualmente para este trabalho ou despesa. | Não há impacto posterior para este campo. |
| Valor | Criação rápida | Você pode inserir informações manualmente neste campo se os campos **Quantidade** e **Preço** estiverem em branco. Se esses campos não estiverem em branco, ele se tornará somente leitura e calculado como (Quantidade \* Preço unitário) + Imposto. | Não há impacto posterior para este campo. |

## <a name="update-prices-on-quote-line-details"></a>Atualizar preços nos detalhes da linha de cotação

Se você alterou preços na lista de preços do projeto que está anexado à cotação, ou na lista de preços de custo da unidade de contratação, será possível selecionar **Recalcular** na página **Cotação**, para atualizar os preços nos detalhes da linha de cotação individual para refletir essa alteração. Quando você seleciona **Recalcular**, um aviso aparecerá informando que os preços nos detalhes da linha de cotação para todas as linhas de cotação nesta cotação serão redefinidos. Selecione **Sim** para atualizar os preços dos detalhes da linha de cotação de vendas e de custo.

## <a name="access-quote-line-details-for-cost"></a>Acessar os detalhes da linha de cotação para custo

Para acessar os detalhes da linha de cotação para custo, siga estas etapas:

1. Na guia **Detalhes da Linha de Cotação**, selecione uma linha na grade para permitir ações na barra de ferramentas da subgrade. 
2. Selecione **Abrir Detalhes de Custo** para ver a taxa de custo relacionada e o valor dessa linha de cotação.

> [!NOTE]
> Alterar os valores da unidade de recursos, da quantidade, das datas, da função ou da categoria no detalhe da linha de cotação para custos mudará os valores correspondentes nos detalhes da linha de cotação de vendas.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moeda nos detalhes da linha de cotação para custo e vendas

A moeda no detalhe da linha de cotação para padrões de vendas da lista de preços do projeto que é efetiva para a data de início do detalhe da linha de cotação.

A moeda no detalhe da linha de cotação para padrões de custo da lista de preços da unidade de contratação da cotação que é efetiva para a data de início do detalhe da linha de cotação para custo.

> [!NOTE]
> Os cálculos de lucratividade convertem o valor dos detalhes da linha de cotação para custos e vendas na moeda base do ambiente para relatar a margem estimada geral da cotação. Erros de arredondamento de moeda e margens alteradas podem ocorrer devido à falta de taxas de câmbio efetivas de data. Use esses cálculos apenas nas cotações do projeto, pois são aproximações e não são estatutários reais ou outros relatórios que exigem maior precisão de arredondamento e consciência da data efetiva para as taxas de câmbio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
