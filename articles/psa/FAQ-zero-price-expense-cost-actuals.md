---
title: Por que o preço padrão está sendo definido como zero nos dados reais de custo de despesas?
description: Solução de problemas do preço padrão definido como zero nos dados reais de custo de despesas.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071449"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Por que o preço padrão está sendo definido como zero nos dados reais de custo de despesas?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estas Perguntas frequentes se aplicam a dados reais de despesas em que a classe da transação está definida como Despesa e o tipo de transação é Custo.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Solucionar problemas de taxas de custo em dados reais de custo de despesas

Vá para a entrada da despesa relacionada e verifique se há um valor no campo da entrada de despesa. Caso a entrada de despesa de origem não tiver o campo com um valor preenchido, você isolou o problema.
 
Para resolvê-lo, recrie a entrada de despesa com um valor válido e aprove-a.
