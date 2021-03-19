---
title: Como posso fazer uma reserva flexível de recursos na versão 2.x do aplicativo?
description: Este artigo descreve como fazer uma reserva flexível de membros da equipe de projeto com o Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286009"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="6c824-103">Como posso fazer uma reserva flexível de recursos no aplicativo Web (aplicativo Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="6c824-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6c824-104">Você pode tentar agendar ou fazer uma reserva flexível de um recurso em uma equipe de projeto para mostrar que planeja atribuir o recurso a um projeto.</span><span class="sxs-lookup"><span data-stu-id="6c824-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="6c824-105">As reservas flexíveis não consomem a capacidade disponível de um recurso.</span><span class="sxs-lookup"><span data-stu-id="6c824-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="6c824-106">Os membros da equipe com reserva flexível não podem ser atribuídos a tarefas do projeto.</span><span class="sxs-lookup"><span data-stu-id="6c824-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="6c824-107">Somente recursos com o status Com reserva fixa e o tipo de confirmação Confirmado podem ser atribuídos a tarefas (supondo que tenham horas com reserva fixa suficientes para cobrir o esforço da atribuição).</span><span class="sxs-lookup"><span data-stu-id="6c824-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="6c824-108">Os membros da equipe de projeto com reserva flexível na grade Membro da equipe com suas horas com reserva flexível mostradas na coluna Reserva flexível.</span><span class="sxs-lookup"><span data-stu-id="6c824-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="6c824-109">Eles também são exibidos no painel de agendamento.</span><span class="sxs-lookup"><span data-stu-id="6c824-109">They also show up on the schedule board.</span></span> <span data-ttu-id="6c824-110">Além disso, eles não indicam nenhum consumo de capacidade, pois a reserva flexível não consome a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="6c824-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="6c824-111">Há três maneiras de fazer uma reserva flexível de um membro da equipe em um projeto com a versão. 2.x do Project Service.</span><span class="sxs-lookup"><span data-stu-id="6c824-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="6c824-112">Para fazer uma reserva flexível com o painel de agendamento, use o recurso Manter Reservas ou crie um recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="6c824-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="6c824-113">Esse métodos são descritos abaixo.</span><span class="sxs-lookup"><span data-stu-id="6c824-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="6c824-114">Fazer reserva flexível com o painel de agendamento</span><span class="sxs-lookup"><span data-stu-id="6c824-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="6c824-115">Para fazer uma reserva flexível com o painel de agendamento, siga este procedimento:</span><span class="sxs-lookup"><span data-stu-id="6c824-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="6c824-116">Abra o painel de agendamento.</span><span class="sxs-lookup"><span data-stu-id="6c824-116">Open the schedule board.</span></span>
2. <span data-ttu-id="6c824-117">Selecione a guia Projeto no painel inferior Requisitos da reserva do painel de agendamento.</span><span class="sxs-lookup"><span data-stu-id="6c824-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="6c824-118">Localize o projeto no qual você deseja fazer a reserva flexível de um recurso.</span><span class="sxs-lookup"><span data-stu-id="6c824-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="6c824-119">Se você tiver muitos projetos, clique no cabeçalho da coluna Projeto e use o filtro.</span><span class="sxs-lookup"><span data-stu-id="6c824-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="6c824-120">Clique no projeto, arraste-o, solte-o na grade de tempo do recurso.</span><span class="sxs-lookup"><span data-stu-id="6c824-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="6c824-121">Isso abrirá o painel Criar reserva de recursos à direita.</span><span class="sxs-lookup"><span data-stu-id="6c824-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="6c824-122">Ajuste as datas de início e de término, selecione Status de reserva como Flexível e defina as horas.</span><span class="sxs-lookup"><span data-stu-id="6c824-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="6c824-123">Clique em Reservar.</span><span class="sxs-lookup"><span data-stu-id="6c824-123">Click Book.</span></span>
7. <span data-ttu-id="6c824-124">Novamente no projeto, o recurso agora será exibido como um membro da equipe com as horas com reserva flexível na coluna Reserva flexível.</span><span class="sxs-lookup"><span data-stu-id="6c824-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="6c824-125">Observe que não é possível atribuir tarefas a ele na estrutura de detalhamento de trabalho (WBS), pois os recursos devem ter uma reserva fixa na equipe para serem atribuídos.</span><span class="sxs-lookup"><span data-stu-id="6c824-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="6c824-126">Fazer reserva flexível com o recurso Manter Reservas</span><span class="sxs-lookup"><span data-stu-id="6c824-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="6c824-127">Para fazer uma reserva flexível com Manter Reservas, siga este procedimento:</span><span class="sxs-lookup"><span data-stu-id="6c824-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="6c824-128">Na grade de membros da equipe, clique em Novo.</span><span class="sxs-lookup"><span data-stu-id="6c824-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="6c824-129">Selecione o recurso reservável, a função e datas de início e de término.</span><span class="sxs-lookup"><span data-stu-id="6c824-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="6c824-130">Selecione um método de alocação que não seja Nenhum:</span><span class="sxs-lookup"><span data-stu-id="6c824-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="6c824-131">Capacidade total</span><span class="sxs-lookup"><span data-stu-id="6c824-131">Full Capacity</span></span>
- <span data-ttu-id="6c824-132">Capacidade percentual</span><span class="sxs-lookup"><span data-stu-id="6c824-132">Percentage Capacity</span></span>
- <span data-ttu-id="6c824-133">Por horas distribuídas igualmente</span><span class="sxs-lookup"><span data-stu-id="6c824-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="6c824-134">Por horas de distribuição inicial</span><span class="sxs-lookup"><span data-stu-id="6c824-134">By Hours Front Load</span></span>
4. <span data-ttu-id="6c824-135">Clique em Salvar.</span><span class="sxs-lookup"><span data-stu-id="6c824-135">Click Save.</span></span> <span data-ttu-id="6c824-136">O recurso será exibido na grade da equipe e suas horas indicadas como Fixas.</span><span class="sxs-lookup"><span data-stu-id="6c824-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="6c824-137">Mantenha as reservas do recurso clicando em Manter Reservas.</span><span class="sxs-lookup"><span data-stu-id="6c824-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="6c824-138">Quando o painel de agendamento abrir, expanda o recurso para mostrar suas reservas.</span><span class="sxs-lookup"><span data-stu-id="6c824-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="6c824-139">Você verá a reserva indicada como Fixa.</span><span class="sxs-lookup"><span data-stu-id="6c824-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="6c824-140">Clique com o botão direito na reserva e, em Alterar Status, selecione Reserva Flexível e Flexível.</span><span class="sxs-lookup"><span data-stu-id="6c824-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="6c824-141">O status da reserva agora é Flexível.</span><span class="sxs-lookup"><span data-stu-id="6c824-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="6c824-142">Depois de fechar o painel de agendamento, você verá que as horas para o recurso mudaram de Fixas para Flexíveis na grade de membro da equipe.</span><span class="sxs-lookup"><span data-stu-id="6c824-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="6c824-143">Observe que se você fizer uma reserva fixa de um recurso em uma equipe e atribuir tarefas a ele na WBS, ao usar Manter Reservas para alterar o status de Fixa para Flexível, as atribuições serão removidas das tarefas para esse recurso, pois apenas recursos com reservas fixas podem ser atribuídos a tarefas.</span><span class="sxs-lookup"><span data-stu-id="6c824-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="6c824-144">Fazer reserva flexível criando um recurso genérico</span><span class="sxs-lookup"><span data-stu-id="6c824-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="6c824-145">É possível criar uma reserva flexível gerando um membro da equipe de recurso genérico, atendendo ao painel de agendamento ou requisito de recursos e alterando o tipo durante a reserva.</span><span class="sxs-lookup"><span data-stu-id="6c824-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="6c824-146">Para fazer isso, siga o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="6c824-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="6c824-147">Na WBS do projeto, atribua funções às tarefas para as quais você deseja gerar membros da equipe genéricos.</span><span class="sxs-lookup"><span data-stu-id="6c824-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="6c824-148">Clique em Gerar Equipe de Projeto.</span><span class="sxs-lookup"><span data-stu-id="6c824-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="6c824-149">Na grade de membros da equipe de projeto, selecione o recurso genérico e clique em Reservar.</span><span class="sxs-lookup"><span data-stu-id="6c824-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="6c824-150">No painel de agendamento, selecione o recurso que você deseja reservar.</span><span class="sxs-lookup"><span data-stu-id="6c824-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="6c824-151">No painel Criar reserva de recursos do painel de agendamento, altere Status de reserva para Flexível.</span><span class="sxs-lookup"><span data-stu-id="6c824-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="6c824-152">Clique em Reservar ou Reservar e Sair.</span><span class="sxs-lookup"><span data-stu-id="6c824-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="6c824-153">Depois de fechar o painel de agendamento, será possível ver que o recurso selecionado foi adicionado à equipe com horas de reserva flexível e horas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="6c824-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="6c824-154">Você também verá que o recurso genérico permanece na equipe como um indicador de que as tarefas foram atribuídas a um membro da equipe com reserva flexível.</span><span class="sxs-lookup"><span data-stu-id="6c824-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="6c824-155">Quando estiver pronto para alterar um recurso de membro da equipe com reserva flexível para um membro com reserva fixa para que você possa atribuí-lo a tarefas, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6c824-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="6c824-156">Selecione esse recurso e clique em Manter Reservas.</span><span class="sxs-lookup"><span data-stu-id="6c824-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="6c824-157">Quando o painel de agendamento abrir, expanda o recurso para mostrar suas reservas.</span><span class="sxs-lookup"><span data-stu-id="6c824-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="6c824-158">Você verá a reserva marcada como Flexível.</span><span class="sxs-lookup"><span data-stu-id="6c824-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="6c824-159">Clique com o botão direito na reserva e, em Alterar Status, selecione Reserva Fixa e Fixa.</span><span class="sxs-lookup"><span data-stu-id="6c824-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="6c824-160">O status da reserva agora é Fixa.</span><span class="sxs-lookup"><span data-stu-id="6c824-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="6c824-161">Depois de fechar o painel de agendamento, você verá que as horas para o recurso mudaram de Flexíveis para Fixas na grade de membros da equipe.</span><span class="sxs-lookup"><span data-stu-id="6c824-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="6c824-162">Agora é possível atribuir recursos a tarefas (contanto que haja um alinhamento entre as horas com reserva fixa e as horas de esforço da tarefa para a atribuição).</span><span class="sxs-lookup"><span data-stu-id="6c824-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="6c824-163">Observe que se você seguiu as etapas de atendimento ao recurso genérico no item 3 acima, ao alterar o status do recurso reservável com reserva flexível para fixa, o membro da equipe genérico será removido da equipe.</span><span class="sxs-lookup"><span data-stu-id="6c824-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]