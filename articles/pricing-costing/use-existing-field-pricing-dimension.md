---
title: Campos do Project Operations como dimensões de precificação
description: Este tópico fornece informações sobre o uso de campos como dimensões de precificação no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119224"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="ac548-103">Campos do Project Operations como dimensões de precificação</span><span class="sxs-lookup"><span data-stu-id="ac548-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="ac548-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="ac548-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ac548-105">A entidade **Dados Reais** tem muitos campos que podem ser usados como dimensões de precificação para precificação baseada em recursos.</span><span class="sxs-lookup"><span data-stu-id="ac548-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="ac548-106">Por exemplo, um campo comum é o **Recurso Reservável**.</span><span class="sxs-lookup"><span data-stu-id="ac548-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="ac548-107">Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de cobrança e de custo específicas para cada recurso é uma abordagem mais simples.</span><span class="sxs-lookup"><span data-stu-id="ac548-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="ac548-108">No entanto, à medida que a força de trabalho faturável cresce, a manutenção de taxas específicas para os recursos pode se tornar irreal.</span><span class="sxs-lookup"><span data-stu-id="ac548-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="ac548-109">As taxas de cobrança e de custo dos recursos começam a variar conforme eles são promovidos, ganham mais experiência ou adquirem um conjunto diferente de habilidades.</span><span class="sxs-lookup"><span data-stu-id="ac548-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="ac548-110">Outro exemplo é a categoria de transação.</span><span class="sxs-lookup"><span data-stu-id="ac548-110">Another example is that of transaction category.</span></span> <span data-ttu-id="ac548-111">Os clientes e os implementadores usavam a categoria de transação para classificar o trabalho e usam o campo para definir o preço e o custo com base na categoria de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ac548-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
