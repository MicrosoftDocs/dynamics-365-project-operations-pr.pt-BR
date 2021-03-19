---
title: Por que o preço padrão está sendo definido como zero nos dados reais de vendas de despesas?
description: Estas três verificações ajudarão você a solucionar problemas do preço padrão definido como zero nos dados reais de vendas de despesas.
author: rumant
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bd474d7c0cd64262fdb21d6269efa781b6dc31f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285855"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Por que o preço padrão está sendo definido como zero nos dados reais de vendas de despesas?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas Perguntas frequentes se aplicam a dados reais de despesas em que a classe da transação está definida como Despesa e o tipo de transação é Vendas não cobradas. Estas três verificações ajudarão você a solucionar problemas do preço padrão (taxa de cobrança) definido como zero em dados reais de vendas de despesas.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Verificação 1: identifique a lista de preços de vendas para o projeto

Localize o projeto no campo de projeto dos dados reais e vá para a página do projeto. Vá para a guia Vendas. Na grade Linhas de contrato do projeto, clique no link do campo Contrato do projeto. A página Contrato do projeto abrirá. Na página Contrato do projeto, vá para a guia Listas de preços do projeto. Verifique se há pelo menos uma lista de preços anexada.

Se não houver nenhuma lista de preços anexada à grade Listas de preços do projeto do Contrato do projeto:

- Anexe uma lista de preços à grade Listas de preços do projeto. As listas de preços que podem ser anexadas deverão ter campo de contexto definido como Vendas, e o campo de moeda na lista de preços deve corresponder ao campo de moeda no Contrato do projeto. Depois que você fizer as correções necessárias, recrie uma entrada de despesa, aprove-a e verifique se os dados reais de vendas não cobradas mostram um preço válido.
- Caso tenha uma ou mais listas de preços anexadas à grade Listas de preços do projeto do Contrato do projeto, vá para a verificação 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Verificação 2: alguma das listas de preços identificadas acima é válida para a data específica dos dados reais de despesas?

Para que o Project Service considere uma lista de preços para definir o preço padrão, essa lista de preços deve se aplicável para a data nos dados reais de vendas de despesas. Verifique os seguintes aspectos para conferir se a lista de preços identificada acima é aplicável:

- Comece verificando se as datas de início e de término na guia geral para as listas de preços anexadas não estão vazias. Se as datas de início e de término nas listas de preços identificadas acima estão vazias, você isolou o problema. 
- Crie uma anotação do campo de data de início nos dados reais de vendas de despesas e verifique se as listas de preços identificadas são aplicáveis para essa data. Por exemplo, a data dos dados reais de despesas deve estar entre a data de início e a data de término na lista de preços. 
    - Se não houver nenhuma lista de preços que cubra essa data nos dados reais de vendas de despesas, você isolou o problema. Modifique as datas de início e de término da lista de preços para garantir que a lista de preços cubra a data dos dados reais de despesas. 
    - Se houver mais de uma uma lista de preços que cubra a data nos dados reais de vendas de despesas, você isolou o problema. Edite as datas de início e de término das listas de preços para que haja apenas uma lista de preços que cubra a data dos dados reais de despesas. 
    - Se houver apenas uma lista de preços que cubra a data dos dados reais de despesas, prossiga para a verificação 3.
Depois que você fizer as correções necessárias, recrie uma entrada de despesa, aprove-a e verifique se os dados reais de vendas não cobradas mostram um preço válido.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Verificação 3: há um preço válido para categoria de despesas na lista de preços do projeto aplicável? 

Se você tiver concluído a verificação 1 e 2, é necessário ter apenas uma lista de preços do projeto que seja aplicável para a data dos dados reais de vendas de despesas. Abra essa Lista de preços do projeto e vá para a guia Preços de categorias. Verifique se há uma linha na grade para a categoria de despesa específica dos dados reais de despesa.
 
- Se não houver nenhuma linha, você isolou o problema. Crie uma linha na grade de preços Categoria para a categoria nos dados reais de despesas. Em seguida, recrie uma entrada de despesa, aprove-a e verifique se os dados reais de vendas não cobradas mostram um preço válido. 
- Se houver uma linha para a categoria de despesa na grade de preços da categoria, verifique se há um preço válido.

Para entender o que é um preço válido, use estes métodos:

- Se o campo Método de precificação na linha de preço Categoria está definido como A preço de custo, a taxa unitária nos dados reais de vendas de despesas terá como padrão o valor na entrada Despesa.
- Se o campo Método de precificação na linha de preço Categoria está definido como Porcentagem de markup, verifique se o campo Porcentagem está definido como um valor válido. A taxa unitária nos dados reais de vendas de despesas é definida como padrão aplicando essa porcentagem de markup ao preço na entrada Despesa.
- Se o campo Método de precificação na linha de preço Categoria está definido como Preço por unidade, verifique se o campo Preço está definido como um valor válido. A taxa unitária padrão nos dados reais de vendas de despesas será definida como o valor de moeda especificado no campo Preço.

Se a configuração de preço para a categoria de despesa não é válida, você isolou o problema. A solução é editar a linha de preço da categoria com um preço válido para a categoria de despesa de acordo com as regras acima. Depois que você fizer isso, recrie uma entrada de despesa, aprove-a e verifique se os dados reais de vendas não cobradas obtêm um preço válido.

Se você ainda não vir um preço válido nos dados reais de vendas de despesas depois de fazer as três verificações acima, abra um tíquete de suporte.




[!INCLUDE[footer-include](../includes/footer-banner.md)]