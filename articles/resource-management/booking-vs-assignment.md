---
title: Reservas x atribuições
description: Este tópico fornece informações sobre as diferenças entre reservas de recursos e atribuições de recursos.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012752"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="9f634-103">Reservas x atribuições</span><span class="sxs-lookup"><span data-stu-id="9f634-103">Bookings vs assignments</span></span>

<span data-ttu-id="9f634-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="9f634-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9f634-105">As reservas são a alocação fixa ou flexível de recursos para um projeto.</span><span class="sxs-lookup"><span data-stu-id="9f634-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="9f634-106">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="9f634-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="9f634-107">As reservas representam conceitos organizacionais para equipes, para que possam entender como os recursos serão envolvidos em vários projetos.</span><span class="sxs-lookup"><span data-stu-id="9f634-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="9f634-108">O Dynamics 365 Project Operations considera as reservas como um conceito de nível de projeto.</span><span class="sxs-lookup"><span data-stu-id="9f634-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="9f634-109">Diferente das reservas, as atribuições representam o compromisso de recursos a tarefas do projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="9f634-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="9f634-110">Os recursos podem ser nomeados ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="9f634-110">The resources can be named or generic.</span></span>  <span data-ttu-id="9f634-111">Quando um requisito de recurso é derivado das atribuições de tarefas do projeto, o Project Operations usam os contornos de esforço da atribuição de recursos para criar os contornos dos detalhes dos requisitos de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f634-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="9f634-112">No entanto, uma referência às atribuições de recursos não é mantida.</span><span class="sxs-lookup"><span data-stu-id="9f634-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="9f634-113">As atualizações nas reservas derivadas do requisito de recurso não atualizam nenhuma atribuição de recurso.</span><span class="sxs-lookup"><span data-stu-id="9f634-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="9f634-114">Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso em uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="9f634-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="9f634-115">No entanto, o Project Operations não impõe essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="9f634-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="9f634-116">A exibição **Reconciliação** mostra ao gerente de projetos os locais em que as reservas e atribuições de um recurso não são correspondentes.</span><span class="sxs-lookup"><span data-stu-id="9f634-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]