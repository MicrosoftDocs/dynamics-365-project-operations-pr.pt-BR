---
title: Visão geral do assistente de agendamento
description: Este tópico fornece informações sobre como trabalhar com o assistente de Agenda para reservar recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279214"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="77997-103">Visão geral do assistente de agendamento</span><span class="sxs-lookup"><span data-stu-id="77997-103">Schedule assistant overview</span></span>

<span data-ttu-id="77997-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="77997-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="77997-105">O assistente de Agenda é usado para reservar recursos com base nos requisitos definidos pelo gerente de projeto.</span><span class="sxs-lookup"><span data-stu-id="77997-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="77997-106">O assistente de Agenda depende dos parâmetros fornecidos no requisito de recursos para localizar o recurso.</span><span class="sxs-lookup"><span data-stu-id="77997-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="77997-107">O assistente de Agenda recomenda recursos que atendam aos requisitos relevantes, como janelas de tempo ou habilidades necessárias.</span><span class="sxs-lookup"><span data-stu-id="77997-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="77997-108">Depois que os recursos adequados são identificados, o gerente de recursos ou de projeto pode reservar o recurso para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="77997-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="77997-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="77997-109">Prerequisites</span></span>

<span data-ttu-id="77997-110">O assistente de Agenda faz parte da solução Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="77997-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="77997-111">Esta solução está incluída e instalada com o Dynamics 365 Project Operations, o Dynamics 365 Field Service e o Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="77997-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="77997-112">Correspondência entre requisitos e recursos</span><span class="sxs-lookup"><span data-stu-id="77997-112">Matching requirements and resources</span></span>

<span data-ttu-id="77997-113">Um requisito de recurso gerado é baseado em detalhes como:</span><span class="sxs-lookup"><span data-stu-id="77997-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="77997-114">Características</span><span class="sxs-lookup"><span data-stu-id="77997-114">Characteristics</span></span>
-   <span data-ttu-id="77997-115">Direitos</span><span class="sxs-lookup"><span data-stu-id="77997-115">Roles</span></span>
-   <span data-ttu-id="77997-116">Unidades de negócios</span><span class="sxs-lookup"><span data-stu-id="77997-116">Business units</span></span>
-   <span data-ttu-id="77997-117">Preferências de recurso</span><span class="sxs-lookup"><span data-stu-id="77997-117">Resource preferences</span></span>
-   <span data-ttu-id="77997-118">Contornos de esforço</span><span class="sxs-lookup"><span data-stu-id="77997-118">Effort contours</span></span>
-   <span data-ttu-id="77997-119">Fuso horário</span><span class="sxs-lookup"><span data-stu-id="77997-119">Time zone</span></span>

<span data-ttu-id="77997-120">O assistente de Agenda usa esses detalhes para filtrar recursos.</span><span class="sxs-lookup"><span data-stu-id="77997-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="77997-121">Iniciar o assistente de Agenda</span><span class="sxs-lookup"><span data-stu-id="77997-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="77997-122">Existem duas maneiras de iniciar o assistente de Agenda.</span><span class="sxs-lookup"><span data-stu-id="77997-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="77997-123">Se você estiver usando o modo híbrido, na grade de membros da equipe, selecione qualquer membro da equipe com um requisito de recurso não atendido e, em seguida, **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="77997-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="77997-124">Se você estiver usando o modo central, o gerente de recursos encontra e seleciona o recurso.</span><span class="sxs-lookup"><span data-stu-id="77997-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="77997-125">Filtros do assistente de agendamento</span><span class="sxs-lookup"><span data-stu-id="77997-125">Schedule assistant filters</span></span>

<span data-ttu-id="77997-126">Depois que o assistente de Agenda é executado, os detalhes do requisito de recurso são exibidos como valores filtrados no painel à esquerda.</span><span class="sxs-lookup"><span data-stu-id="77997-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="77997-127">O gerente de recursos ou o gerente de projeto podem ajustar os resultados alterando os filtros para atender às necessidades de agendamento.</span><span class="sxs-lookup"><span data-stu-id="77997-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="77997-128">O painel de filtro mostra opções relacionadas ao trabalho, incluindo:</span><span class="sxs-lookup"><span data-stu-id="77997-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="77997-129">Início e término do trabalho</span><span class="sxs-lookup"><span data-stu-id="77997-129">Work start and end</span></span>
-   <span data-ttu-id="77997-130">Características</span><span class="sxs-lookup"><span data-stu-id="77997-130">Characteristics</span></span>
-   <span data-ttu-id="77997-131">Direitos</span><span class="sxs-lookup"><span data-stu-id="77997-131">Roles</span></span>
-   <span data-ttu-id="77997-132">Unidades organizacionais</span><span class="sxs-lookup"><span data-stu-id="77997-132">Organizational units</span></span>
-   <span data-ttu-id="77997-133">Empresa de recursos</span><span class="sxs-lookup"><span data-stu-id="77997-133">Resourcing company</span></span>
-   <span data-ttu-id="77997-134">Tipos de recurso</span><span class="sxs-lookup"><span data-stu-id="77997-134">Resource types</span></span>
-   <span data-ttu-id="77997-135">Recursos preferenciais</span><span class="sxs-lookup"><span data-stu-id="77997-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]