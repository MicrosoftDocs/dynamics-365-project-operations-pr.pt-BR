---
title: Determinar preços de vendas para estimativas e dados reais baseados em projetos
description: Este artigo fornece informações sobre como os preços de venda para estimativas e dados reais baseados em projetos são determinados.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475355"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Determinar preços de vendas para estimativas e dados reais baseados em projetos

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Para determinar os preços de venda em estimativas e dados reais no Microsoft Dynamics 365 Project Operations, o sistema primeiro usa a data e a moeda no contexto de estimativa de entrada ou dados reais para determinar a lista de preços de venda. No contexto real especificamente, o sistema usa o campo **Data da transação** para determinar qual lista de preços é aplicável. O valor **Data da transação** da estimativa recebida ou dado real é comparado com os valores **Início Efetivo (Independente de Fuso Horário)** e **Fim Efetivo (Independente de Fuso Horário)** na lista de preços. Depois que a lista de preços de venda é determinada, o sistema determina a taxa de vendas ou cobrança.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Determinar as taxas de venda em linhas de dados reais e estimativas para Tempo

Contexto de estimativa para **Tempo** refere-se a:

- Detalhes da linha de cotação para **Tempo**.
- Detalhes da linha de contrato para **Tempo**.
- Atribuições de recursos em um projeto.

Contexto de dados reais para **Tempo** refere-se a:

- Linhas do diário de entrada e correção para **Tempo**.
- Linhas de diário criadas quando uma entrada de tempo é enviada.
- Detalhes da linha de fatura para **Tempo**. 

Depois que uma lista de preços para vendas é determinada, o sistema conclui as etapas a seguir para inserir a taxa de faturamento padrão.

1. O sistema compara a combinação dos campos **Função**, **Empresa de Recursos** e **Unidade de Recursos** no contexto de estimativa ou dados reais para **Tempo** com as linhas de preço de função na lista de preços. Essa correspondência pressupõe que você esteja usando as dimensões de preços prontas para uso para taxas de cobrança. Se você configurou o preço para que seja baseado em campos diferentes ou além de **Função**, **Empresa de Recursos** e **Unidade de Recursos**, essa combinação de campos será usada para recuperar uma linha de preço de função correspondente.
1. Se o sistema encontrar uma linha de preço de função que tenha uma taxa de cobrança para a combinação **Função**, **Empresa de Recursos** e **Unidade de Recursos**, essa taxa de cobrança é usada como a taxa de cobrança padrão.

> [!NOTE]
> Se você configurar uma priorização diferente dos campos **Função**, **Empresa de Recursos** e **Unidade de Recursos**, ou se tiver outras dimensões com prioridade mais alta, o comportamento anterior será alterado de acordo. O sistema recupera registros de preço de função que possuem valores que correspondem a cada valor de dimensão de preço em ordem de prioridade. As linhas que têm valores nulos para essas dimensões vêm por último.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Determinar as taxas de vendas em linhas de dados reais e estimativas para Despesa

Contexto de estimativa para **Despesa** refere-se a:

- Detalhes da linha de cotação para **Despesa**.
- Detalhes da linha de contrato para **Despesa**.
- Linhas de estimativas de despesas em um projeto.

Contexto real para **Despesa** refere-se a:

- Linhas do diário de entrada e correção para **Despesa**.
- Linhas de diário criadas quando uma entrada de despesa é enviada.
- Detalhes da linha de fatura para **Despesa**. 

Depois que uma lista de preços para vendas é determinada, o sistema conclui as etapas a seguir para inserir o preço de venda unitário padrão.

1. O sistema compara a combinação dos campos **Categoria** e **Unidade** na linha de estimativa para **Despesa** com as linhas de preço da categoria na lista de preços.
1. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de venda para a combinação de **Categoria** e **Unidade**, essa taxa de vendas será usada como a taxa de vendas padrão.
1. Se o sistema encontrar uma linha de preço de categoria correspondente, o método de precificação pode ser usado para inserir o preço de venda padrão. A tabela a seguir mostra o comportamento padrão para preços de despesas no Project Operations.

    | Contexto | Método de precificação | Preço padrão |
    | --- | --- | --- |
    | Estimativa | Preço por unidade | Com base na linha de preço da categoria. |
    |        | A preço de custo | 0.00 |
    |        | Markup sobre custo | 0.00 |
    | Real | Preço por unidade | Com base na linha de preço da categoria. |
    |        | A preço de custo | Com base no custo real relacionado. |
    |        | Markup sobre custo | Um markup é aplicado, conforme definido pela linha de preço da categoria, à taxa de custo unitário do custo real relacionado. |

1. Se o sistema não corresponder aos valores **Categoria** e **Unidade**, a taxa de vendas será definida como **0** (zero) por padrão.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Determinar taxas de vendas em linhas de dados reais e estimativa para Material

Contexto de estimativa para **Material** refere-se a:

- Detalhes da linha de cotação para **Material**.
- Detalhes da linha de contrato para **Material**.
- Linhas de estimativa de materiais em um projeto.

Contexto real para **Material** refere-se a:

- Linhas do diário de entrada e correção para **Material**.
- Linhas de diário criadas quando um registro de uso de material é enviado.
- Detalhes da linha de fatura para **Material**. 

Depois que uma lista de preços para vendas é determinada, o sistema conclui as etapas a seguir para inserir o preço de venda unitário padrão.

1. O sistema compara a combinação dos campos **Produto** e **Unidade** na linha de estimativa para **Material** com as linhas de item da lista de preços na lista de preços.
1. Se o sistema encontrar uma linha de item da lista de preços com uma taxa de vendas para a combinação de **Produto** e **Unidade** e se o método de precificação for **Valor da moeda**, o preço de venda especificado na linha da lista de preços será usado. 
1. Se os valores dos campos **Produtos** e **Unidade** não corresponderem ou se o método de precificação for diferente de **Valor da moeda**, a taxa de vendas será definida como **0** (zero) por padrão. Esse comportamento ocorre porque o Project Operations oferece suporte apenas ao método de precificação **Valor da moeda** para materiais usados em um projeto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
