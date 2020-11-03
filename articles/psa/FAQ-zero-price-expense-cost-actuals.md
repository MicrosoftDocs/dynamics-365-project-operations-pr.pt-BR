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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="f92d2-103">Por que o preço padrão está sendo definido como zero nos dados reais de custo de despesas?</span><span class="sxs-lookup"><span data-stu-id="f92d2-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f92d2-104">Estas Perguntas frequentes se aplicam a dados reais de despesas em que a classe da transação está definida como Despesa e o tipo de transação é Custo.</span><span class="sxs-lookup"><span data-stu-id="f92d2-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="f92d2-105">Solucionar problemas de taxas de custo em dados reais de custo de despesas</span><span class="sxs-lookup"><span data-stu-id="f92d2-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="f92d2-106">Vá para a entrada da despesa relacionada e verifique se há um valor no campo da entrada de despesa.</span><span class="sxs-lookup"><span data-stu-id="f92d2-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="f92d2-107">Caso a entrada de despesa de origem não tiver o campo com um valor preenchido, você isolou o problema.</span><span class="sxs-lookup"><span data-stu-id="f92d2-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="f92d2-108">Para resolvê-lo, recrie a entrada de despesa com um valor válido e aprove-a.</span><span class="sxs-lookup"><span data-stu-id="f92d2-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
