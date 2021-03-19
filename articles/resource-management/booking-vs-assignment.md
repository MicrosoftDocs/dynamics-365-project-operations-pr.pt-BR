---
title: Reservas x atribuições
description: Este tópico fornece informações sobre as diferenças entre reservas de recursos e atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279889"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="f2ddb-103">Reservas x atribuições</span><span class="sxs-lookup"><span data-stu-id="f2ddb-103">Bookings vs assignments</span></span>

<span data-ttu-id="f2ddb-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="f2ddb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f2ddb-105">As reservas são a alocação fixa ou flexível de recursos para um projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="f2ddb-106">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="f2ddb-107">As reservas representam conceitos organizacionais para equipes, para que possam entender como os recursos serão envolvidos em vários projetos.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="f2ddb-108">O Dynamics 365 Project Operations considera as reservas como um conceito de nível de projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="f2ddb-109">Diferente das reservas, as atribuições representam o compromisso de recursos a tarefas do projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="f2ddb-110">Os recursos podem ser nomeados ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-110">The resources can be named or generic.</span></span>  <span data-ttu-id="f2ddb-111">Quando um requisito de recurso é derivado das atribuições de tarefas do projeto, o Project Operations usam os contornos de esforço da atribuição de recursos para criar os contornos dos detalhes dos requisitos de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="f2ddb-112">No entanto, uma referência às atribuições de recursos não é mantida.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="f2ddb-113">As atualizações nas reservas derivadas do requisito de recurso não atualizam nenhuma atribuição de recurso.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="f2ddb-114">Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso em uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="f2ddb-115">No entanto, o Project Operations não impõe essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="f2ddb-116">A exibição **Reconciliação** mostra ao gerente de projetos os locais em que as reservas e atribuições de um recurso não são correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f2ddb-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]