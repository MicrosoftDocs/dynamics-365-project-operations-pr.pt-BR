---
title: Por que o preço padrão está sendo definido como zero em dados reais de custo de tempo?
description: Solução de problemas do preço padrão definido como zero em dados reais de custo de tempo.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749179"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Por que o preço padrão está sendo definido como zero em dados reais de custo de tempo?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas Perguntas frequentes se aplicam a dados reais em que a classe da transação está definida como Tempo e o tipo de transação é Custo. Estas três verificações ajudarão você a solucionar problemas do preço padrão estar sendo definido como zero em dados reais de custo de tempo.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Verificação 1: identifique a lista de preços de custo para o projeto

Localize o projeto no campo de projeto dos dados reais e acesse a página do projeto. Clique no link da unidade de contratação no campo. Na página Unidade de contratação, verifique se a unidade de contratação tem uma lista de preços na grade Listas de preços de custo.

Se houver mais de uma lista de preços, você isolou o problema. O Project Service oferece suporte a apenas uma lista de preços por unidade organizacional. Remova todas as listas de preços dessa entidade até haver apenas uma lista de preços anexada à grade Listas de preços de custo da unidade organizacional.

Se não houver uma lista de preços anexada à unidade organizacional, crie uma anotação da moeda da unidade organizacional. Acesse o Project Service, Parâmetros e depois abra a guia Listas de preços. Verifique se há alguma lista de preços com o contexto definido como Custo e uma moeda que corresponda à moeda da unidade organizacional.
 
Se não houver uma lista de preços que corresponda a esses critérios, você isolou o problema. Certifique-se ter pelo menos uma lista de preços cujo contexto esteja definido como Custo e cuja moeda corresponda à moeda da unidade organizacional.

Se houver mais de uma lista de preços que corresponda a esses critérios, continue lendo este documento para fazer mais verificações.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Verificação 2: alguma das listas de preços identificadas acima é válida para a data específica dos dados reais de custo de tempo?

Para que o Project Service considere uma lista de preços para definir o preço padrão, essa lista de preços deve ser aplicável para a data nos dados reais de custo de tempo. Verifique os seguintes aspectos para conferir se a lista de preços identificada acima é aplicável:

- Verifique se as datas de início e de término na guia geral para as listas de preços anexadas não estão vazias. Se as datas de início e de término nas listas de preços identificadas acima estão vazias, você isolou o problema. 
- Crie uma anotação do campo de data de início nos dados reais de custo de tempo e verifique se as listas de preços identificadas são aplicáveis para essa data. Por exemplo, a data dos dados reais de custo de tempo dever ficar entre a data de início e a data de término na lista de preços. 
    - Se não houver nenhuma lista de preços que cubra essa data nos dados reais de custo de tempo, você isolou o problema. Modifique as datas de início e término da lista de preços para garantir que a lista de preços cubra a data dos dados reais de custo de tempo. 
    - Se houver mais de uma uma lista de preços que cubra a data nos dados reais de custo de tempo, você isolou o problema. É possível corrigir isso editando as datas de início e de término das listas de preços para que haja apenas uma lista de preços cubra a data dos dados reais de custo de tempo. 
    - Se houver apenas uma lista de preços que cubra essa data dos dados reais de custo de tempo, prossiga para a próxima verificação no documento.
Depois que você fizer as correções necessárias, recrie uma entrada de tempo, aprove-a e verifique se os dados reais de custo de tempo mostram um preço válido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Verificação 3: há um preço na lista de preços para as dimensões de precificação nos dados reais de custo de tempo?

Se você tiver concluído a verificação 1 e 2, será necessário ter apenas uma lista de preços que seja aplicável para a data dos dados reais de custo de tempo. Abra essa Lista de preços e vá para a guia Preços de funções. Verifique se há uma linha na grade para as dimensões de precificação nos dados reais de custo de tempo.

Se não houver nenhuma linha na grade de preços de funções para as dimensões de precificação nos dados reais de custo de tempo, você isolou o problema. Criar uma linha na grade Preços de funções para as dimensões de precificação nos dados reais de custo de tempo. Depois que você fizer isso, recrie uma entrada de tempo, aprove-a e verifique se os dados reais de custo de tempo mostram um preço válido.
 
Se você ainda não vir um preço válido nos dados reais de custo de tempo depois de fazer as três verificações acima, abra um tíquete de suporte.



