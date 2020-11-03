---
title: Como atribuir um recurso reservável a uma tarefa no aplicativo Web
description: Uma visão geral de como é possível atribuir recursos reserváveis.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 7b95eff52351904f97c62b3806f17b02db47860b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071616"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="8b673-103">Como eu atribuo um recurso agendável a uma tarefa no aplicativo Web (aplicativo Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="8b673-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8b673-104">Há duas maneiras de atribuir um recurso a uma tarefa no Project Service.</span><span class="sxs-lookup"><span data-stu-id="8b673-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="8b673-105">Você pode registrar um recurso como um membro de equipe e depois atribui-lo a tarefa.</span><span class="sxs-lookup"><span data-stu-id="8b673-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="8b673-106">Ou, você pode criar um membro de equipe genérico por meio de atribuição de função em tarefas, gerar uma equipe e depois preencher os requisitos de de backup com um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="8b673-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="8b673-107">Observe que, se você quiser atribuir um recurso agendável a uma tarefa, o membro da equipe de recurso agendável deve ter registros disponíveis o suficiente.</span><span class="sxs-lookup"><span data-stu-id="8b673-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="8b673-108">O status do registro deve ser Reserva fixa do tipo de comprometimento e Status comprometido.</span><span class="sxs-lookup"><span data-stu-id="8b673-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="8b673-109">Se não houver registros suficientes para o recurso, Project Service remove a atribuição e exibe a mensagem de erro a seguir:</span><span class="sxs-lookup"><span data-stu-id="8b673-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="8b673-110">*Impossível atribuir recursos a tarefa - Os recursos a seguir não têm horas suficientes registradas para o projeto*</span><span class="sxs-lookup"><span data-stu-id="8b673-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="8b673-111">Registre um recurso como um membro de equipe e depois atribua o recurso a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="8b673-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="8b673-112">Com esse método você adiciona um recurso a equipe de projeto e depois atribui tarefas ao recurso no agendamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="8b673-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="8b673-113">Veja como você faz isso:</span><span class="sxs-lookup"><span data-stu-id="8b673-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="8b673-114">Na grade de membro de equipe, adicione um novo membro da equipe selecionando **Novo**.</span><span class="sxs-lookup"><span data-stu-id="8b673-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="8b673-115">Na tela Criação rápida de membro de equipe, selecione o nome de recurso agendável e definir uma função.</span><span class="sxs-lookup"><span data-stu-id="8b673-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="8b673-116">Selecione as datas **De** e **Para**.</span><span class="sxs-lookup"><span data-stu-id="8b673-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="8b673-117">![Captura de tela da inclusão de membro da equipe](media/FAQ-Resources-to-Tasks2-1.png "Captura de tela da inclusão de membro da equipe")</span><span class="sxs-lookup"><span data-stu-id="8b673-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="8b673-118">Selecione um dos métodos de alocação a seguir para o registrar o recurso:</span><span class="sxs-lookup"><span data-stu-id="8b673-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="8b673-119">**Capacidade completa** registra a capacidade completa de recursos das datas específicas de início e término.</span><span class="sxs-lookup"><span data-stu-id="8b673-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="8b673-120">**Capacidade de porcentagem** registra o recurso para a porcentagem da capacidade do recurso para as datas de início e término.</span><span class="sxs-lookup"><span data-stu-id="8b673-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="8b673-121">**Por horas distribuídas igualmente** registra o recurso de um número de horas específico, distribuindo-os por tempo igualmente por dia nas datas de início e término especificadas.</span><span class="sxs-lookup"><span data-stu-id="8b673-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="8b673-122">**Por horas de distribuição inicial** registra o recurso de um número de horas específico, com distribuição inicial das horas por dia nas datas de início e término especificadas.</span><span class="sxs-lookup"><span data-stu-id="8b673-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="8b673-123">Não selecione **Nenhum** porque ele adiciona o recurso à equipe, mas não cria quaisquer registros que absorvem a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="8b673-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="8b673-124">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="8b673-124">Select **Save**.</span></span>

    <span data-ttu-id="8b673-125">Observe que as horas de registro devem ser suficientes para cobrir as horas de esforço e faixas de data das tarefas as quais você atribui o recurso.</span><span class="sxs-lookup"><span data-stu-id="8b673-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="8b673-126">Se eles não tiverem alinha dos, você não pode atribuir o recurso à tarefa.</span><span class="sxs-lookup"><span data-stu-id="8b673-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="8b673-127">Na estrutura de detalhamento de trabalho (WBS) da tarefa, clique na célula em suspenso.</span><span class="sxs-lookup"><span data-stu-id="8b673-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="8b673-128">Depois:</span><span class="sxs-lookup"><span data-stu-id="8b673-128">Then:</span></span> 

    1. <span data-ttu-id="8b673-129">Selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="8b673-129">Select **Add**.</span></span>
    2. <span data-ttu-id="8b673-130">Selecione os **Recursos** suspensos e selecione o membro de equipe adicionado acima.</span><span class="sxs-lookup"><span data-stu-id="8b673-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="8b673-131">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b673-131">Select **OK**.</span></span> <span data-ttu-id="8b673-132">O membro de equipe agora é atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="8b673-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="8b673-133">![Captura de tela da inclusão de recursos com a WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de tela da inclusão de recursos com a WBS")</span><span class="sxs-lookup"><span data-stu-id="8b673-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="8b673-134">Na grade de membro de equipe, você verá o agregado das horas de recurso atribuídos nas Horas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="8b673-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="8b673-135">Será menor ou igual às horas registradas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="8b673-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="8b673-136">![Captura de tela das horas atribuídas a um recurso](media/FAQ-Resources-to-Tasks2-3.png "Captura de tela das horas atribuídas a um recurso")</span><span class="sxs-lookup"><span data-stu-id="8b673-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="8b673-137">Se a tarefa que você está tentando atribuir ao recurso começa depois da data de término dos registros de recurso, o recurso não aparecerá no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="8b673-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="8b673-138">Observe que é possível atribuir um recurso para mais horas que suas horas registradas se o recurso tiver alguma capacidade restante não atribuída.</span><span class="sxs-lookup"><span data-stu-id="8b673-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="8b673-139">Nesse caso, o recurso será parcialmente atribuído para seus registros.</span><span class="sxs-lookup"><span data-stu-id="8b673-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="8b673-140">Você pode encontrar essas horas de tarefa não atribuídas adicionando a coluna Horas sem recursos à estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b673-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="8b673-141">Se os recursos forem atribuídos a suas horas registradas (suas horas registradas é igual a suas horas atribuídas), você verá a mensagem de erro a seguir quando tentar atribui-los mais tarefas:</span><span class="sxs-lookup"><span data-stu-id="8b673-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="8b673-142">*Impossível atribuir recursos a tarefa - Os recursos a seguir não têm horas suficientes registradas para o projeto.*</span><span class="sxs-lookup"><span data-stu-id="8b673-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="8b673-143">Além disso, o membro da equipe de gerente de projeto adicionado à equipe quando você cria o projeto é adicionado sem quaisquer registros e não pode ser atribuído a qualquer tarefa.</span><span class="sxs-lookup"><span data-stu-id="8b673-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="8b673-144">Eles não aparecerão no menu suspenso de recurso das tarefas.</span><span class="sxs-lookup"><span data-stu-id="8b673-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="8b673-145">Se você quiser atribuir esse recurso, é preciso removê-los da equipe e depois readicioná-los com um método de alocação diferente de Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8b673-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="8b673-146">Eles são adicionados à equipe quando o projeto é criado para que o projeto tenha, pelo menos, um aprovador de projeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="8b673-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="8b673-147">Crie um membro de equipe genérico por meio da atribuição de função nas tarefas</span><span class="sxs-lookup"><span data-stu-id="8b673-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="8b673-148">Este método assegura que que os recursos possuem registros suficientes para tarefas.</span><span class="sxs-lookup"><span data-stu-id="8b673-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="8b673-149">Primeiro, você cria um recurso de espaço reservado ou genérico que descreve as características do recurso nomeado que você deseja usar nas tarefas gerando uma equipe após atribuir funções às tarefas.</span><span class="sxs-lookup"><span data-stu-id="8b673-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="8b673-150">Veja como você faz isso:</span><span class="sxs-lookup"><span data-stu-id="8b673-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="8b673-151">Na estrutura de detalhamento de trabalho, selecione uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="8b673-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="8b673-152">Selecione o ícone suspenso **Função atribuída** na célula de recurso.</span><span class="sxs-lookup"><span data-stu-id="8b673-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="8b673-153">Selecione o menu suspenso **Função** e selecione a função do recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="8b673-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="8b673-154">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b673-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="8b673-155">![Captura de tela do uso da WBS para incluir recurso](media/FAQ-Resources-to-Tasks2-4.png "Captura de tela do uso da WBS para incluir recurso")</span><span class="sxs-lookup"><span data-stu-id="8b673-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="8b673-156">Depois de ter concluído a atribuição de tarefas na WBS, selecione **Gerar equipe de projeto**.</span><span class="sxs-lookup"><span data-stu-id="8b673-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="8b673-157">O Project Service cria o número mínimo de membros de equipe genérico baseado nas funções, unidades de organização de recurso, e calendário de projeto agregando as atribuições de tarefa.</span><span class="sxs-lookup"><span data-stu-id="8b673-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="8b673-158">![Captura de tela da geração da equipe de projeto](media/FAQ-Resources-to-Tasks2-5.png "Captura de tela da geração da equipe de projeto")</span><span class="sxs-lookup"><span data-stu-id="8b673-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="8b673-159">Na grade Membro de equipe, você verá recursos do tipo Recurso genético com a função e nome da posição.</span><span class="sxs-lookup"><span data-stu-id="8b673-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="8b673-160">Se dois recursos são necessários para uma função completar o trabalho, o recurso Gerar equipe cria dois membros de equipe e usa o nome de posição para defini-los separadamente.</span><span class="sxs-lookup"><span data-stu-id="8b673-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="8b673-161">![Captura de tela da inclusão de dois recursos genéricos](media/FAQ-Resources-to-Tasks2-6.png "Captura de tela da inclusão de dois recursos genéricos")</span><span class="sxs-lookup"><span data-stu-id="8b673-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="8b673-162">Você pode abrir o requisito de recurso de backup para o membro de equipe genérico selecionando o link em Requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="8b673-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="8b673-163">![Captura de tela da abertura do requisito de recurso de backup](media/FAQ-Resources-to-Tasks2-7.png "Captura de tela da abertura do requisito de recurso de backup")</span><span class="sxs-lookup"><span data-stu-id="8b673-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="8b673-164">Selecione **Livro** para o recurso genérico, e depois você pode usar o painel de agendamento para encontrar e registrar um recurso real.</span><span class="sxs-lookup"><span data-stu-id="8b673-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="8b673-165">Você também pode enviar o requisito para preenchimento por um gerente de recurso selecionando **Enviar solicitação**.</span><span class="sxs-lookup"><span data-stu-id="8b673-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="8b673-166">Quando o recurso genérico é preenchido com um recurso nomeado, o recurso genérico é removido da equipe e as atribuições de tarefa do recurso genérico são atribuídas ao recurso nomeado que preencheu o requisito de recurso do recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="8b673-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

