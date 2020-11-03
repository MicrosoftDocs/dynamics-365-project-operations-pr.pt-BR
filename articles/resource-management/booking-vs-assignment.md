---
title: Reservas x atribuições
description: Este tópico fornece informações sobre as diferenças entre reservas de recursos e atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071277"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="79e37-103">Reservas x atribuições</span><span class="sxs-lookup"><span data-stu-id="79e37-103">Bookings vs assignments</span></span>

<span data-ttu-id="79e37-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="79e37-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="79e37-105">As reservas são a alocação fixa ou flexível de recursos para um projeto.</span><span class="sxs-lookup"><span data-stu-id="79e37-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="79e37-106">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="79e37-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="79e37-107">As atribuições são a atribuição de recursos a tarefas do projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="79e37-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="79e37-108">Os recursos podem ser reais ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="79e37-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="79e37-109">O ideal é que, para recursos reais, as reservas e atribuições sejam correspondentes, pois elas não diferem.</span><span class="sxs-lookup"><span data-stu-id="79e37-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="79e37-110">No entanto, o Microsoft Dynamics Project Operations não impõe essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="79e37-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="79e37-111">A exibição **Reconciliação** mostra a um gerente de projetos os locais em que as reservas e atribuições de um recurso não correspondem.</span><span class="sxs-lookup"><span data-stu-id="79e37-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
