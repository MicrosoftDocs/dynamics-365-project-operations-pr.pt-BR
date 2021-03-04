---
title: Usar um campo existente no Project Service como uma dimensão de precificação
description: Este tópico inclui informações sobre o uso de campos existentes do Project Service como dimensões de precificação.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bc3a1df7669dac43b45d781448ed5c795a65be4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144130"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="d081d-103">Usar um campo existente no Project Service como uma dimensão de precificação</span><span class="sxs-lookup"><span data-stu-id="d081d-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d081d-104">O PSA (Project Service Automation) tem vários campos na entidade **Dados Reais** que podem ser usados como dimensões de precificação para a precificação com base em recurso em organizações de projetos.</span><span class="sxs-lookup"><span data-stu-id="d081d-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="d081d-105">Por exemplo, um campo comum é o **Recurso Reservável**.</span><span class="sxs-lookup"><span data-stu-id="d081d-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="d081d-106">Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de cobrança e de custo específicas para cada recurso é uma abordagem mais simples.</span><span class="sxs-lookup"><span data-stu-id="d081d-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="d081d-107">Entretanto, conforme a equipe de trabalho faturável cresce, taxas específicas podem se tornar irreais de manter, pois as taxas de cobrança e de custo dos recursos começam a variar à medida que os recursos são promovidos, ganham mais experiência ou adquirem conjuntos de habilidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="d081d-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="d081d-108">Como essa abordagem ainda funciona para empresas de um determinado porte, consulte [Usar recurso reservável como dimensão de precificação](bookable-resource-pricing-dimension.md) para compreender como um campo existente do Project Service pode ser usado como dimensão de precificação.</span><span class="sxs-lookup"><span data-stu-id="d081d-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="d081d-109">Outro exemplo é a categoria de transação.</span><span class="sxs-lookup"><span data-stu-id="d081d-109">Another example is that of transaction category.</span></span> <span data-ttu-id="d081d-110">Os clientes e os implementadores usavam a categoria de transação do PSA para classificar o trabalho e usavam o campo para definir o preço e o custo com base na categoria do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d081d-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="d081d-111">Para obter mais informações, consulte [Usar categoria de transação como dimensão de precificação](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="d081d-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
