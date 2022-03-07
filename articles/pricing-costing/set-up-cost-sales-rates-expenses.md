---
title: Configurar taxas de custo e de vendas para despesas
description: Este tópico fornece informações sobre como configurar as taxas de custo e vendas para categorias de transação e despesas.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c5e7b1ab03a170ca95a005985a13aaff7494f95ca15cf1ce726674ae9a14222
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986207"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Configurar taxas de custo e de vendas para despesas

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Você pode configurar os preços de custo e venda para categorias de transação no Dynamics 365 Project Operations. Como os preços de venda e custo são projetados para despesas, cada categoria de transação que os inclui também deve ser configurada como uma categoria de despesas. Esta configuração garante precisão na funcionalidade posterior. Os preços de venda e custo para categorias de transação só podem ser listados em uma moeda, que deve ser aquela no cabeçalho da lista de preços.

Para configurar taxas de venda e custo para categorias de transação, conclua as etapas a seguir. 

1. Acesse **Vendas** > **Clientes** > **Listas de Preços**.
2. Selecione **Novo** para criar uma nova lista de preços. 
3. Em **Preços da Categoria**, no menu de subgrade, selecione **Novo Preço da Categoria**. 
4. Na página **Criação Rápida**, insira a categoria de transação e unidade para as quais você está criando o preço.

A tabela a seguir lista os campos na guia **Geral** e na página **Criação Rápida** de uma linha de preço de categoria que você deve ter em mente ao criar preços de categoria em uma lista de preços de venda ou de custo.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Categoria da Transação | Guia **Geral** e páginas de **Criação Rápida** | Selecione a categoria de transação para a qual está criando um preço de venda ou custo. | A categoria de transação na estimativa de entrada ou linha real para despesas será comparada com essa linha para padronizar o custo ou taxa de vendas da categoria de transação. |
| Agenda da Unidade | Guia **Geral** e páginas de **Criação Rápida** | A programação da unidade é padronizada na programação da unidade da categoria de transação. | Não há impacto a jusante deste campo. |
| Unidade | Guia **Geral** e páginas de **Criação Rápida** | Selecione a unidade para a qual as taxas estão sendo configuradas. | A unidade na estimativa de entrada ou linha real é comparada com a unidade nessa linha para definir a taxa da estimativa de despesas ou real. |
| Método de Precificação | Guia **Geral** e páginas de **Criação Rápida** | Os valores possíveis dos campos **Método de Precificação** são **Preço por Unidade**, **A preço de custo** e **Markup sobre custo**. | Durante a configuração do preço, selecionar o campo **Preço por Unidade** bloqueia o campo **Porcentagem** na linha de preço da categoria. Se **A preço de custo** é selecionado, os campos **Preço** e **Porcentagem** ficam bloqueados na lista de preços de venda. Selecionar **Markup sobre custo** bloqueia o campo **Preço** na lista de preços de venda. Em uma linha real de entrada para despesas, o método de precificação **A preço de custo** ou **Markup sobre custo** resulta na linha de vendas não cobrada correspondente recebendo um preço que é igual ao preço do custo real ou sendo calculada como uma marcação sobre o preço. |
| Preço | Guia **Geral** e páginas de **Criação Rápida** | Configure uma taxa por unidade para a categoria de transação e combinação de unidades. Por exemplo, a taxa de milhagem é de 10 USD por milha e 8 USD por quilômetro. | A taxa de milhagem será a taxa padrão no preço por unidade ou custo da estimativa de entrada ou linha real para uma classe de transação de despesas.|
| Porcentagem | Guia **Geral** e páginas de **Criação Rápida** | Configure a porcentagem sobre o custo para a categoria de transação e combinação de unidades. Por exemplo, a taxa de vendas de passagens aéreas deve ser marcada com 10% sobre o custo da despesa de passagem aérea incorrida. | Essa porcentagem sobre o custo só é aplicável em uma lista de preços de venda quando o método de precificação selecionado é **Markup sobre custo**. |
| Moeda | Guia **Geral** e páginas de **Criação Rápida** | Por padrão, esse valor vem da moeda no cabeçalho da lista de preços. Para preços de categoria de transação, a moeda não pode ser substituída. | O padrão dessa moeda é o preço por unidade da linha real de entrada para a classe de transação de despesas para custos e vendas. |

## <a name="pricing-methods-for-expenses"></a>Métodos de precificação para despesas

Ao configurar preços de categoria que são relevantes apenas no contexto de preços de despesas, você pode usar um dos três métodos de preços a seguir:

- **Preço por unidade**
- **A preço de custo**
- **Markup sobre custo**

### <a name="price-per-unit"></a>Preço por unidade
Quando esse método de precificação é selecionado em uma linha de preço de categoria vinculada a uma lista de preços de venda, o preço padrão para a combinação de categoria e unidade na estimativa e na linha real. Estimativa refere-se às linhas de estimativa do projeto para despesas, o detalhe da linha de cotação e o detalhe da linha do contrato para despesas.

### <a name="at-cost"></a>A preço de custo
Quando esse método de precificação é selecionado na linha de preço da categoria vinculada a uma lista de preços de venda, o preço padrão para a combinação de categoria e unidade apenas para a despesa real. Por exemplo, vendas reais não cobradas para a classe de transação de despesas. O preço unitário é definido nas vendas não cobradas reais do preço unitário no custo real dessa despesa. A padronização de preços com base no custo não é feita nas estimativas do projeto para despesas ou na linha de cotação e nos detalhes da linha do contrato para despesas.

### <a name="markup-over-cost"></a>Markup sobre custo
Quando esse método de precificação é selecionado na linha de preço da categoria vinculada a uma lista de preços de venda, o preço padrão para a combinação de categoria e unidade apenas para uma despesa real. Por exemplo, vendas reais não cobradas para a classe de transação de despesas. Esse preço unitário é definido nas vendas não cobradas reais para um valor calculado a partir do preço unitário no custo real para a despesa após a porcentagem de marcação definida ser aplicada. A padronização de preços com base no custo não é feita nas estimativas do projeto para despesas ou na linha de cotação e nos detalhes da linha do contrato para despesas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
