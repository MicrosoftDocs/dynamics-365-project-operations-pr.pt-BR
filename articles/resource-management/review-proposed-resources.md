---
title: Revisar recursos propostos
description: Este tópico fornece informações sobre como propor recursos de projeto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401159"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="ba058-103">Revisar recursos propostos</span><span class="sxs-lookup"><span data-stu-id="ba058-103">Review proposed resources</span></span>

<span data-ttu-id="ba058-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="ba058-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba058-105">Os gerentes de recursos podem propor um recurso ao gerente de projetos usando uma solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="ba058-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="ba058-106">Na grade de solicitações ou na própria solicitação, selecione **Localizar Recursos**.</span><span class="sxs-lookup"><span data-stu-id="ba058-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="ba058-107">Na página **Assistente de Agendamento**, selecione o recurso e, em seguida, no painel **Criar Reserva de Recursos**, no campo **Status da Reserva**, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="ba058-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="ba058-108">As seguintes atualizações de status ocorrem:</span><span class="sxs-lookup"><span data-stu-id="ba058-108">The following status updates occur:</span></span>

- <span data-ttu-id="ba058-109">Na página **Assistente de Agendamento**, os indicadores de status são atualizados para indicar que a reserva é proposta, não fixa.</span><span class="sxs-lookup"><span data-stu-id="ba058-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="ba058-110">Na solicitação de recurso, o status é alterado para **Precisa de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="ba058-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="ba058-111">Na guia **Equipe** do projeto, o valor **Status de Solicitação** do membro genérico da equipe é alterado para **Precisa de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="ba058-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="ba058-112">O gerente de projetos pode aceitar ou rejeitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="ba058-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="ba058-113">Quando os gerentes de recursos processam solicitações de recursos, eles podem usar qualquer uma das seguintes abordagens:</span><span class="sxs-lookup"><span data-stu-id="ba058-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="ba058-114">Propor vários recursos para satisfazer a demanda caso não haja um recurso único disponível para atender às horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="ba058-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="ba058-115">As horas propostas então serão divididas entre vários recursos que possam satisfazer as horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="ba058-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="ba058-116">Nesse cenário, não pode haver sobreposição de horas.</span><span class="sxs-lookup"><span data-stu-id="ba058-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="ba058-117">Propor menos recursos do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="ba058-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="ba058-118">Nesse cenário, a capacidade do recurso proposta é menor do que as horas necessárias especificadas pelo solicitante.</span><span class="sxs-lookup"><span data-stu-id="ba058-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="ba058-119">Portanto, quando o solicitante aceita os recursos propostos, um requisito de recurso não atendido é criado para capturar a demanda restante.</span><span class="sxs-lookup"><span data-stu-id="ba058-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="ba058-120">Reservar vários recursos para satisfazer a demanda caso não haja um recurso único disponível para concluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ba058-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="ba058-121">Reservar menos recursos do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="ba058-121">Book fewer resources than are required.</span></span> <span data-ttu-id="ba058-122">Nesse cenário, o número de horas reservadas é inferior ao de horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="ba058-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="ba058-123">O sistema orienta você a propor recursos em vez de reservas, para que o solicitante possa verificar e acompanhar a demanda restante.</span><span class="sxs-lookup"><span data-stu-id="ba058-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="ba058-124">Disponibilidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ba058-124">Resource availability</span></span>

<span data-ttu-id="ba058-125">É essencial que os gerentes de recursos possam visualizar a disponibilidade de recursos e atualizar as reservas.</span><span class="sxs-lookup"><span data-stu-id="ba058-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="ba058-126">Em alguns casos, não há demanda formal (solicitação de recurso), mas um gerente de recursos deve responder a uma demanda não planejada recebida por meio de canais como email, telefonema ou mensagem instantânea.</span><span class="sxs-lookup"><span data-stu-id="ba058-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="ba058-127">Os gerentes de recursos usam o Painel de Agendamento para atualizar recursos e reservas.</span><span class="sxs-lookup"><span data-stu-id="ba058-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="ba058-128">As horas de trabalho do recurso são usadas como base para calcular a disponibilidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="ba058-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="ba058-129">As reservas de recursos consomem a capacidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="ba058-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="ba058-130">O Painel de Agendamento usa cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, além do status das reservas.</span><span class="sxs-lookup"><span data-stu-id="ba058-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="ba058-131">Uma das configurações do Painel de Agendamento permite mostrar uma legenda.</span><span class="sxs-lookup"><span data-stu-id="ba058-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="ba058-132">Se uma seta que aponta para a direita aparecer ao lado de um recurso reservável individual no Painel de Agendamento, o recurso poderá ser expandido para mostrar detalhes do trabalho no qual o recurso está reservado.</span><span class="sxs-lookup"><span data-stu-id="ba058-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="ba058-133">Como o Dynamics 365 Project Operations usa o mecanismo Universal Resource Scheduling, se você também tiver o Dynamics 365 Field Service instalado, poderá ver os detalhes das reservas de recursos para projetos, ordens de serviço e qualquer outra entidade à qual tenha estendido o agendamento.</span><span class="sxs-lookup"><span data-stu-id="ba058-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="ba058-134">Para exibir mais detalhes sobre um recurso individual, clique com o botão direito do mouse nele para abrir o cartão de recurso.</span><span class="sxs-lookup"><span data-stu-id="ba058-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

