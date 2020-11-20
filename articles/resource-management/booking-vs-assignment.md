---
title: Reservas x atribuições
description: Este tópico fornece informações sobre as diferenças entre reservas de recursos e atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130204"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="bf7cf-103">Reservas x atribuições</span><span class="sxs-lookup"><span data-stu-id="bf7cf-103">Bookings vs assignments</span></span>

<span data-ttu-id="bf7cf-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="bf7cf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bf7cf-105">As reservas são a alocação fixa ou flexível de recursos para um projeto.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="bf7cf-106">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="bf7cf-107">As reservas representam conceitos organizacionais para equipes, para que possam entender como os recursos serão envolvidos em vários projetos.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="bf7cf-108">O Dynamics 365 Project Operations considera as reservas um conceito de nível de projeto.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="bf7cf-109">Diferente das reservas, as atribuições representam o compromisso de recursos a tarefas do projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="bf7cf-110">Os recursos podem ser nomeados ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="bf7cf-111">Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso em uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="bf7cf-112">No entanto, o Project Operations não impõe essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="bf7cf-113">A exibição **Reconciliação** mostra ao gerente de projetos os locais em que as reservas e atribuições de um recurso não são correspondentes.</span><span class="sxs-lookup"><span data-stu-id="bf7cf-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
