---
title: Por que o preço padrão está sendo definido como zero nos dados reais de custo de despesas?
description: Solução de problemas do preço padrão definido como zero nos dados reais de custo de despesas.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146334"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="913af-103">Por que o preço padrão está sendo definido como zero nos dados reais de custo de despesas</span><span class="sxs-lookup"><span data-stu-id="913af-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="913af-104">Estas Perguntas frequentes se aplicam a dados reais de despesas em que a classe da transação está definida como Despesa e o tipo de transação é Custo.</span><span class="sxs-lookup"><span data-stu-id="913af-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="913af-105">Solucionar problemas de taxas de custo em dados reais de custo de despesas</span><span class="sxs-lookup"><span data-stu-id="913af-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="913af-106">Vá para a entrada da despesa relacionada e verifique se há um valor no campo da entrada de despesa.</span><span class="sxs-lookup"><span data-stu-id="913af-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="913af-107">Caso a entrada de despesa de origem não tiver o campo com um valor preenchido, você isolou o problema.</span><span class="sxs-lookup"><span data-stu-id="913af-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="913af-108">Para resolvê-lo, recrie a entrada de despesa com um valor válido e aprove-a.</span><span class="sxs-lookup"><span data-stu-id="913af-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
