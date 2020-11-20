---
title: Estimativas de recurso
description: Este tópico fornece informações sobre como são calculadas as estimativas de recursos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127332"
---
# <a name="resource-estimates"></a><span data-ttu-id="8ffec-103">Estimativas de recurso</span><span class="sxs-lookup"><span data-stu-id="8ffec-103">Resource estimates</span></span>

<span data-ttu-id="8ffec-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="8ffec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8ffec-105">As estimativas de recursos vêm de esforço dividido em fases que é definido na estrutura de detalhamento de trabalho junto com as dimensões de preços aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="8ffec-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="8ffec-106">Normalmente, o cálculo é **taxa/hora para cada função x horas**.</span><span class="sxs-lookup"><span data-stu-id="8ffec-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="8ffec-107">O esforço dividido em fases para cada recurso é armazenado no registro de atribuição do recurso.</span><span class="sxs-lookup"><span data-stu-id="8ffec-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="8ffec-108">O preço é armazenado em uma lista de preços predefinida.</span><span class="sxs-lookup"><span data-stu-id="8ffec-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="8ffec-109">A conversão de unidades é aplicada com base na lista de preços aplicável.</span><span class="sxs-lookup"><span data-stu-id="8ffec-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimativas de Recurso](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="8ffec-111">Preço de custo e moeda de custo padrão</span><span class="sxs-lookup"><span data-stu-id="8ffec-111">Default cost price and cost currency</span></span>

<span data-ttu-id="8ffec-112">Os preços de custo são padronizados na Unidade Organizacional.</span><span class="sxs-lookup"><span data-stu-id="8ffec-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="8ffec-113">Taxa de cobrança e moeda de vendas padrão</span><span class="sxs-lookup"><span data-stu-id="8ffec-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="8ffec-114">Os preços de venda são aplicados uma vez por negócio.</span><span class="sxs-lookup"><span data-stu-id="8ffec-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="8ffec-115">A hierarquia para a lista de preços de venda é padronizada desta forma:</span><span class="sxs-lookup"><span data-stu-id="8ffec-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="8ffec-116">Organização</span><span class="sxs-lookup"><span data-stu-id="8ffec-116">Organization</span></span>
2. <span data-ttu-id="8ffec-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="8ffec-117">Customer</span></span>
3. <span data-ttu-id="8ffec-118">Cotação/contrato</span><span class="sxs-lookup"><span data-stu-id="8ffec-118">Quote/contract</span></span>
