---
title: Por que o preço padrão está sendo definido como zero em dados reais de vendas de tempo?
description: Solução de problemas do preço padrão definido como zero em dados reais de vendas de tempo.
author: rumant
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
ms.openlocfilehash: 2df4ce2d6391e70fea8e8f15c1b5774c9a9bfbe5f5ef2e6d8da8668afd34d4c9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992552"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Por que o preço padrão está sendo definido como zero em dados reais de vendas de tempo?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas Perguntas frequentes se aplicam a dados reais em que a classe da transação está definida como Tempo e o tipo de transação é Vendas não cobradas. Estas três verificações ajudarão você a solucionar problemas do preço padrão (taxa de cobrança) definido como zero em dados reais de vendas de tempo.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Verificação 1: identifique a lista de preços de vendas para o projeto

Localize o projeto no campo de projeto dos dados reais e vá para a página do projeto. Vá para a guia Vendas e, na grade Linhas de contrato do projeto, clique no link do campo Contrato do projeto. A página Contrato do projeto abrirá. Na página Contrato do projeto, vá para a guia Listas de preços do projeto. Verifique se há pelo menos uma lista de preços anexada. Se não houver uma lista de preços anexada à grade Listas de preços do projeto do Contrato do projeto, você isolou o problema. Anexe uma lista de preços à grade Listas de preços do projeto. As listas de preços que podem ser anexadas deverão ter campo de contexto definido como Vendas, e o campo de moeda na lista de preços deve corresponder ao campo de moeda no Contrato do projeto. Depois que você fizer as correções necessárias, recrie uma entrada de tempo, aprove-a e verifique se os dados reais de vendas não cobradas mostram um preço válido. 

Caso tenha uma ou mais listas de preços anexadas à grade Listas de preços do projeto do Contrato do projeto, prossiga para a próxima verificação no documento.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Verificação 2: alguma das listas de preços identificadas acima é válida para a data específica dos dados reais de vendas de tempo?

Para que o Project Service considere uma lista de preços para definir o preço padrão, ela deve ser aplicável para a data nos dados reais de vendas de tempo. Verifique os seguintes aspectos para conferir se a lista de preços identificada acima é aplicável:
- Verifique se as datas de início e de término na guia geral para as listas de preços anexadas não estão vazias. Se as datas de início e de término nas listas de preços identificadas acima estão vazias, você isolou o problema. 
- Crie uma anotação do campo de data de início nos dados reais de vendas de tempo e verifique se as listas de preços identificadas são aplicáveis para essa data. Por exemplo, a data dos dados reais de vendas de tempo deve estar entre a data de início e a data de término na lista de preços. 
    - Se não houver uma lista de preços que cubra essa data nos dados reais de vendas de tempo, você isolou o problema. Modifique as datas de início e de término da lista de preços para garantir que a lista de preços cubra a data dos dados reais de vendas de tempo. 
    - Se houver mais de uma uma lista de preços que cubra a data nos dados reais de vendas de tempo, você isolou o problema. É possível corrigir isso editando as datas de início e de término da lista de preços para que haja apenas uma lista de preços cubra a data dos dados reais de vendas de tempo. 
    - Se houver apenas uma lista de preços que cubra a data dos dados reais de vendas de tempo, prossiga para a verificação 3.
Depois que você fizer as correções necessárias, recrie uma entrada de tempo, aprove-a e verifique se os dados reais de vendas de tempo mostram um preço válido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Verificação 3: há um preço na lista de preços para as dimensões de precificação nos dados reais de vendas de tempo?

Se você concluiu com êxito a verificação 1 e 2, é necessário ter apenas uma lista de preços que seja aplicável para a data dos dados reais de vendas de tempo. Abra essa Lista de preços e vá para a guia Preços de funções. Verifique se há uma linha na grade para as dimensões de precificação nos dados reais de vendas de tempo.

Se não houver nenhuma linha na grade de preços de funções para as dimensões de precificação nos dados reais de vendas de tempo, você isolou o problema. Crie uma linha na grade Preços de funções para as dimensões de precificação nos dados reais de vendas de tempo. Depois que você fizer isso, recrie uma entrada de tempo, aprove-a e verifique se os dados reais de vendas de tempo mostram um preço válido.

Se você ainda não vir um preço válido nos dados reais de vendas de tempo depois de seguir as três verificações acima, abra um tíquete de suporte. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]