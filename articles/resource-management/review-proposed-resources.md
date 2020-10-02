---
title: Revisar recursos propostos
description: Este tópico fornece informações sobre como propor recursos de projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897347"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="6b409-103">Revisar recursos propostos</span><span class="sxs-lookup"><span data-stu-id="6b409-103">Review proposed resources</span></span>

<span data-ttu-id="6b409-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="6b409-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6b409-105">Os gerentes de recursos podem propor um recurso ao gerente de projetos usando uma solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="6b409-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="6b409-106">Na grade de solicitações ou na própria solicitação, selecione **Localizar Recursos**.</span><span class="sxs-lookup"><span data-stu-id="6b409-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="6b409-107">Na página **Assistente de Agendamento**, selecione o recurso e, em seguida, no painel **Criar Reserva de Recursos**, no campo **Status da Reserva**, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="6b409-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="6b409-108">As seguintes atualizações de status ocorrem:</span><span class="sxs-lookup"><span data-stu-id="6b409-108">The following status updates occur:</span></span>

- <span data-ttu-id="6b409-109">Na página **Assistente de Agendamento**, os indicadores de status são atualizados para indicar que a reserva é proposta, não fixa.</span><span class="sxs-lookup"><span data-stu-id="6b409-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="6b409-110">Na solicitação de recurso, o status é alterado para **Precisa de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="6b409-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="6b409-111">Na guia **Equipe** do projeto, o valor **Status de Solicitação** do membro genérico da equipe é alterado para **Precisa de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="6b409-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="6b409-112">O gerente de projetos pode aceitar ou rejeitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="6b409-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="6b409-113">Quando os gerentes de recursos processam solicitações de recursos, eles podem usar qualquer uma das seguintes abordagens:</span><span class="sxs-lookup"><span data-stu-id="6b409-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="6b409-114">Propor vários recursos para satisfazer a demanda caso não haja um recurso único disponível para atender às horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="6b409-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="6b409-115">As horas propostas então serão divididas entre vários recursos que possam satisfazer as horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="6b409-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="6b409-116">Nesse cenário, não pode haver sobreposição de horas.</span><span class="sxs-lookup"><span data-stu-id="6b409-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="6b409-117">Propor menos recursos do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="6b409-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="6b409-118">Nesse cenário, a capacidade do recurso proposta é menor do que as horas necessárias especificadas pelo solicitante.</span><span class="sxs-lookup"><span data-stu-id="6b409-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="6b409-119">Portanto, quando o solicitante aceita os recursos propostos, um requisito de recurso não atendido é criado para capturar a demanda restante.</span><span class="sxs-lookup"><span data-stu-id="6b409-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="6b409-120">Reservar vários recursos para satisfazer a demanda caso não haja um recurso único disponível para concluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="6b409-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="6b409-121">Reservar menos recursos do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="6b409-121">Book fewer resources than are required.</span></span> <span data-ttu-id="6b409-122">Nesse cenário, o número de horas reservadas é inferior ao de horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="6b409-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="6b409-123">O sistema orienta você a propor recursos em vez de reservas, para que o solicitante possa verificar e acompanhar a demanda restante.</span><span class="sxs-lookup"><span data-stu-id="6b409-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="6b409-124">Horas trabalhadas faturáveis</span><span class="sxs-lookup"><span data-stu-id="6b409-124">Billable utilization</span></span>

<span data-ttu-id="6b409-125">Os recursos podem ter horas trabalhadas faturáveis de destino.</span><span class="sxs-lookup"><span data-stu-id="6b409-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="6b409-126">Essas horas trabalhadas de destino são definidas como um atributo na função padrão de um recurso ou definidas no registro do recurso reservável individual.</span><span class="sxs-lookup"><span data-stu-id="6b409-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="6b409-127">Os cálculos de horas trabalhadas se baseiam nas horas reais que os recursos relataram usando entradas de hora aprovadas.</span><span class="sxs-lookup"><span data-stu-id="6b409-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="6b409-128">As fórmulas a seguir são usadas para calcular as horas trabalhadas:</span><span class="sxs-lookup"><span data-stu-id="6b409-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="6b409-129">Horas trabalhadas faturáveis = Horas reais passíveis de cobrança ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6b409-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="6b409-130">Horas trabalhadas não faturáveis = Tempo real com ID do tipo de cobrança = Não passível de cobrança, Complementar ou Não disponível ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6b409-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="6b409-131">Interno = Tempo real sem contrato de vendas ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6b409-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="6b409-132">Capacidade do recurso = Horas de trabalho do recurso – Ausência temporária – Dias de folga</span><span class="sxs-lookup"><span data-stu-id="6b409-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="6b409-133">Você pode encontrar a exibição **Horas Trabalhadas do Recurso** no painel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="6b409-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="6b409-134">Cada célula na grade representa o percentual de horas trabalhadas faturáveis do recurso em um período, como dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="6b409-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="6b409-135">As fórmulas a seguir são usadas para colorir as células:</span><span class="sxs-lookup"><span data-stu-id="6b409-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="6b409-136">**Verde:** Horas trabalhadas faturáveis \>= Horas trabalhadas de destino do recurso</span><span class="sxs-lookup"><span data-stu-id="6b409-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="6b409-137">**Amarelo:** Horas trabalhadas de destino – 20 \<= Horas trabalhadas faturáveis \< Horas trabalhadas de destino</span><span class="sxs-lookup"><span data-stu-id="6b409-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="6b409-138">**Vermelho:** Horas trabalhadas faturáveis \< Horas trabalhadas de destino – 20</span><span class="sxs-lookup"><span data-stu-id="6b409-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="6b409-139">Como a exibição **Horas Trabalhadas do Recurso** é baseada no Painel de Agendamento, você pode usar as funcionalidades de filtragem dele para filtrar seus resultados.</span><span class="sxs-lookup"><span data-stu-id="6b409-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="6b409-140">A grade exige que você defina as horas trabalhadas de destino na função ou no recurso individual.</span><span class="sxs-lookup"><span data-stu-id="6b409-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="6b409-141">Para definir essa configuração, vá para **Recursos** \> **Funções de recursos**.</span><span class="sxs-lookup"><span data-stu-id="6b409-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="6b409-142">Além disso, uma função padrão deve ser atribuída a cada recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="6b409-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="6b409-143">Vá para **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="6b409-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="6b409-144">Na guia **Project Service**, verifique se a função de um recurso está definida e se o campo **É Padrão** dela está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="6b409-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="6b409-145">É possível adicionar outras funções onde **É Padrão = Não**.</span><span class="sxs-lookup"><span data-stu-id="6b409-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="6b409-146">A função em que **É Padrão = Sim** é usada para avaliar as horas trabalhadas do recurso em relação ao destino dessa função.</span><span class="sxs-lookup"><span data-stu-id="6b409-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="6b409-147">Na guia **Project Service**, você também pode definir horas trabalhadas de destino individuais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="6b409-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="6b409-148">O cálculo de horas trabalhadas então usa essas horas trabalhadas de destino para avaliar o destino do recurso em vez do destino da função padrão do recurso.</span><span class="sxs-lookup"><span data-stu-id="6b409-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="6b409-149">As horas trabalhadas são mostradas para um recurso somente se ele tiver tempo passível de cobrança e aprovado durante o período exibido na grade.</span><span class="sxs-lookup"><span data-stu-id="6b409-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="6b409-150">Disponibilidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6b409-150">Resource availability</span></span>

<span data-ttu-id="6b409-151">É essencial que os gerentes de recursos possam visualizar a disponibilidade de recursos e atualizar as reservas.</span><span class="sxs-lookup"><span data-stu-id="6b409-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="6b409-152">Em alguns casos, não há demanda formal (solicitação de recurso), mas um gerente de recursos deve responder a uma demanda não planejada recebida por meio de canais como email, telefonema ou mensagem instantânea.</span><span class="sxs-lookup"><span data-stu-id="6b409-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="6b409-153">Os gerentes de recursos usam o Painel de Agendamento para atualizar recursos e reservas.</span><span class="sxs-lookup"><span data-stu-id="6b409-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="6b409-154">As horas de trabalho do recurso são usadas como base para calcular a disponibilidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="6b409-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="6b409-155">As reservas de recursos consomem a capacidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="6b409-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="6b409-156">O Painel de Agendamento usa cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, além do status das reservas.</span><span class="sxs-lookup"><span data-stu-id="6b409-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="6b409-157">Uma das configurações do Painel de Agendamento permite mostrar uma legenda.</span><span class="sxs-lookup"><span data-stu-id="6b409-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="6b409-158">Se uma seta que aponta para a direita aparecer ao lado de um recurso reservável individual no Painel de Agendamento, o recurso poderá ser expandido para mostrar detalhes do trabalho no qual o recurso está reservado.</span><span class="sxs-lookup"><span data-stu-id="6b409-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="6b409-159">Como o Dynamics 365 Project Operations usa o mecanismo Universal Resource Scheduling, se você também tiver o Dynamics 365 Field Service instalado, poderá ver os detalhes das reservas de recursos para projetos, ordens de serviço e qualquer outra entidade à qual tenha estendido o agendamento.</span><span class="sxs-lookup"><span data-stu-id="6b409-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="6b409-160">Para exibir mais detalhes sobre um recurso individual, clique com o botão direito do mouse nele para abrir o cartão de recurso.</span><span class="sxs-lookup"><span data-stu-id="6b409-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

