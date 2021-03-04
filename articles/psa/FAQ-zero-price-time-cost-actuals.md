---
title: Por que o preço padrão está sendo definido como zero em dados reais de custo de tempo?
description: Solução de problemas do preço padrão definido como zero em dados reais de custo de tempo.
author: rumant
manager: kfend
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
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146244"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="379c1-103">Por que o preço padrão está sendo definido como zero em dados reais de custo de tempo?</span><span class="sxs-lookup"><span data-stu-id="379c1-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="379c1-104">Estas Perguntas frequentes se aplicam a dados reais em que a classe da transação está definida como Tempo e o tipo de transação é Custo.</span><span class="sxs-lookup"><span data-stu-id="379c1-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="379c1-105">Estas três verificações ajudarão você a solucionar problemas do preço padrão estar sendo definido como zero em dados reais de custo de tempo.</span><span class="sxs-lookup"><span data-stu-id="379c1-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="379c1-106">Verificação 1: identifique a lista de preços de custo para o projeto</span><span class="sxs-lookup"><span data-stu-id="379c1-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="379c1-107">Localize o projeto no campo de projeto dos dados reais e acesse a página do projeto.</span><span class="sxs-lookup"><span data-stu-id="379c1-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="379c1-108">Clique no link da unidade de contratação no campo.</span><span class="sxs-lookup"><span data-stu-id="379c1-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="379c1-109">Na página Unidade de contratação, verifique se a unidade de contratação tem uma lista de preços na grade Listas de preços de custo.</span><span class="sxs-lookup"><span data-stu-id="379c1-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="379c1-110">Se houver mais de uma lista de preços, você isolou o problema.</span><span class="sxs-lookup"><span data-stu-id="379c1-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="379c1-111">O Project Service oferece suporte a apenas uma lista de preços por unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="379c1-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="379c1-112">Remova todas as listas de preços dessa entidade até haver apenas uma lista de preços anexada à grade Listas de preços de custo da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="379c1-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="379c1-113">Se não houver uma lista de preços anexada à unidade organizacional, crie uma anotação da moeda da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="379c1-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="379c1-114">Acesse o Project Service, Parâmetros e depois abra a guia Listas de preços. Verifique se há alguma lista de preços com o contexto definido como Custo e uma moeda que corresponda à moeda da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="379c1-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="379c1-115">Se não houver uma lista de preços que corresponda a esses critérios, você isolou o problema.</span><span class="sxs-lookup"><span data-stu-id="379c1-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="379c1-116">Certifique-se ter pelo menos uma lista de preços cujo contexto esteja definido como Custo e cuja moeda corresponda à moeda da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="379c1-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="379c1-117">Se houver mais de uma lista de preços que corresponda a esses critérios, continue lendo este documento para fazer mais verificações.</span><span class="sxs-lookup"><span data-stu-id="379c1-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="379c1-118">Verificação 2: alguma das listas de preços identificadas acima é válida para a data específica dos dados reais de custo de tempo?</span><span class="sxs-lookup"><span data-stu-id="379c1-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="379c1-119">Para que o Project Service considere uma lista de preços para definir o preço padrão, essa lista de preços deve ser aplicável para a data nos dados reais de custo de tempo.</span><span class="sxs-lookup"><span data-stu-id="379c1-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="379c1-120">Verifique os seguintes aspectos para conferir se a lista de preços identificada acima é aplicável:</span><span class="sxs-lookup"><span data-stu-id="379c1-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="379c1-121">Verifique se as datas de início e de término na guia geral para as listas de preços anexadas não estão vazias.</span><span class="sxs-lookup"><span data-stu-id="379c1-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="379c1-122">Se as datas de início e de término nas listas de preços identificadas acima estão vazias, você isolou o problema.</span><span class="sxs-lookup"><span data-stu-id="379c1-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="379c1-123">Crie uma anotação do campo de data de início nos dados reais de custo de tempo e verifique se as listas de preços identificadas são aplicáveis para essa data.</span><span class="sxs-lookup"><span data-stu-id="379c1-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="379c1-124">Por exemplo, a data dos dados reais de custo de tempo dever ficar entre a data de início e a data de término na lista de preços.</span><span class="sxs-lookup"><span data-stu-id="379c1-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="379c1-125">Se não houver nenhuma lista de preços que cubra essa data nos dados reais de custo de tempo, você isolou o problema.</span><span class="sxs-lookup"><span data-stu-id="379c1-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="379c1-126">Modifique as datas de início e término da lista de preços para garantir que a lista de preços cubra a data dos dados reais de custo de tempo.</span><span class="sxs-lookup"><span data-stu-id="379c1-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="379c1-127">Se houver mais de uma uma lista de preços que cubra a data nos dados reais de custo de tempo, você isolou o problema.</span><span class="sxs-lookup"><span data-stu-id="379c1-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="379c1-128">É possível corrigir isso editando as datas de início e de término das listas de preços para que haja apenas uma lista de preços cubra a data dos dados reais de custo de tempo.</span><span class="sxs-lookup"><span data-stu-id="379c1-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="379c1-129">Se houver apenas uma lista de preços que cubra essa data dos dados reais de custo de tempo, prossiga para a próxima verificação no documento.</span><span class="sxs-lookup"><span data-stu-id="379c1-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="379c1-130">Depois que você fizer as correções necessárias, recrie uma entrada de tempo, aprove-a e verifique se os dados reais de custo de tempo mostram um preço válido.</span><span class="sxs-lookup"><span data-stu-id="379c1-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="379c1-131">Verificação 3: há um preço na lista de preços para as dimensões de precificação nos dados reais de custo de tempo?</span><span class="sxs-lookup"><span data-stu-id="379c1-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="379c1-132">Se você tiver concluído a verificação 1 e 2, será necessário ter apenas uma lista de preços que seja aplicável para a data dos dados reais de custo de tempo.</span><span class="sxs-lookup"><span data-stu-id="379c1-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="379c1-133">Abra essa Lista de preços e vá para a guia Preços de funções. Verifique se há uma linha na grade para as dimensões de precificação nos dados reais de custo de tempo.</span><span class="sxs-lookup"><span data-stu-id="379c1-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="379c1-134">Se não houver nenhuma linha na grade de preços de funções para as dimensões de precificação nos dados reais de custo de tempo, você isolou o problema.</span><span class="sxs-lookup"><span data-stu-id="379c1-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="379c1-135">Criar uma linha na grade Preços de funções para as dimensões de precificação nos dados reais de custo de tempo.</span><span class="sxs-lookup"><span data-stu-id="379c1-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="379c1-136">Depois que você fizer isso, recrie uma entrada de tempo, aprove-a e verifique se os dados reais de custo de tempo mostram um preço válido.</span><span class="sxs-lookup"><span data-stu-id="379c1-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="379c1-137">Se você ainda não vir um preço válido nos dados reais de custo de tempo depois de fazer as três verificações acima, abra um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="379c1-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



