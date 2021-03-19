---
title: Atribuir um recurso a uma tarefa
description: Este tópico fornece informações sobre como atribuir recursos a tarefas.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286234"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="e998f-103">Atribuir um recurso a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="e998f-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e998f-104">Há três maneiras de atribuir um recurso a uma tarefa no Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e998f-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="e998f-105">Reservar um recurso como um membro da equipe e atribuí-lo a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="e998f-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="e998f-106">É possível adicionar um recurso à equipe do projeto e atribuí-lo a tarefas na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="e998f-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="e998f-107">Na guia **Membro da Equipe**, adicione um novo membro da equipe selecionando **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e998f-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="e998f-108">O painel **Criação Rápida de Membro de Equipe** é aberto, onde você pode selecionar o nome do recurso reservável e definir uma função.</span><span class="sxs-lookup"><span data-stu-id="e998f-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="e998f-109">Selecione um dos seguintes métodos de alocação para a reserva do recurso:</span><span class="sxs-lookup"><span data-stu-id="e998f-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="e998f-110">**Capacidade completa** registra a capacidade completa de recursos das datas específicas de início e término.</span><span class="sxs-lookup"><span data-stu-id="e998f-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e998f-111">**Capacidade de porcentagem** registra o recurso para a porcentagem da capacidade do recurso para as datas de início e término.</span><span class="sxs-lookup"><span data-stu-id="e998f-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e998f-112">**Por Horas Distribuídas Igualmente** reserva o recurso por um número de horas específico, distribuindo-as igualmente por dia pelo intervalo de datas especificado.</span><span class="sxs-lookup"><span data-stu-id="e998f-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="e998f-113">**Por horas de distribuição inicial** registra o recurso de um número de horas específico, com distribuição inicial das horas por dia nas datas de início e término especificadas.</span><span class="sxs-lookup"><span data-stu-id="e998f-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="e998f-114">**Nenhum** adiciona o recurso à equipe, mas não cria quaisquer registros que absorvem sua capacidade.</span><span class="sxs-lookup"><span data-stu-id="e998f-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="e998f-115">Na grade **Agendar** de uma tarefa, selecione o ícone **Recurso** na célula do recurso e, em **Membros da Equipe**, selecione o membro da equipe que acabou de adicionar.</span><span class="sxs-lookup"><span data-stu-id="e998f-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="e998f-116">Nas guias **Membro da Equipe** e **Reconciliação**, o recurso mostra as horas reservadas e atribuídas.</span><span class="sxs-lookup"><span data-stu-id="e998f-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="e998f-117">As horas devem ser as mesmas, mas não é obrigatório, pois as reservas e atribuições não são rigidamente combinadas.</span><span class="sxs-lookup"><span data-stu-id="e998f-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="e998f-118">A guia **Reconciliação** fornece detalhes quando elas são diferentes, como quando você atribui a um recurso mais horas do que as que foram reservadas.</span><span class="sxs-lookup"><span data-stu-id="e998f-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="e998f-119">Se necessário, você pode corrigir as informações estendendo as reservas ou alterando a atribuição do recurso.</span><span class="sxs-lookup"><span data-stu-id="e998f-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="e998f-120">Criar um membro da equipe genérico por meio da atribuição de tarefa</span><span class="sxs-lookup"><span data-stu-id="e998f-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="e998f-121">Ao criar um membro da equipe genérico por meio da atribuição de tarefa, você cria um espaço reservado ou recurso genérico que descreve as características do recurso nomeado que deseja usar nas tarefas.</span><span class="sxs-lookup"><span data-stu-id="e998f-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="e998f-122">Em seguida, você gera um requisito (ou envia uma solicitação usando o requisito) que é usado para procurar e reservar o recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="e998f-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="e998f-123">Na grade **Agendar** de uma tarefa, selecione o ícone **Recurso** na célula do recurso.</span><span class="sxs-lookup"><span data-stu-id="e998f-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="e998f-124">Digite um nome para servir como o nome do recurso do espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="e998f-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="e998f-125">Por exemplo, Gerente de Programa.</span><span class="sxs-lookup"><span data-stu-id="e998f-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="e998f-126">Selecione **Criar** e, no campo **Criação Rápida: Membro da Equipe do Projeto**, defina a função para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e998f-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="e998f-127">Você pode continuar atribuindo tarefas a esse recurso de espaço reservado selecionando o recurso no **Seletor de Recursos** da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e998f-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="e998f-128">Eles são listado em **Membros da Equipe**.</span><span class="sxs-lookup"><span data-stu-id="e998f-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="e998f-129">Quando terminar de atribuir o recurso genérico, selecione o recurso genérico na guia **Equipe** e, em seguida, selecione **Gerar Requisito** de modo a criar um requisito de recurso para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e998f-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="e998f-130">Selecione **Registrar** para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e998f-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="e998f-131">É possível usar o Quadro de Agendamento para encontrar e reservar um recurso real.</span><span class="sxs-lookup"><span data-stu-id="e998f-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="e998f-132">Você também pode enviar o requisito para preenchimento por um gerente de recurso.</span><span class="sxs-lookup"><span data-stu-id="e998f-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="e998f-133">Quando o recurso genérico é preenchido com um recurso nomeado, o recurso genérico é removido da equipe e as atribuições de tarefa do recurso genérico são atribuídas ao recurso nomeado que preencheu o requisito de recurso do recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e998f-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="e998f-134">Atribuir um recurso nomeado usando a lista de todos os recursos reserváveis</span><span class="sxs-lookup"><span data-stu-id="e998f-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="e998f-135">Você pode usar uma caixa de pesquisa no **Seletor de Recursos** para procurar todos os recursos reserváveis e atribui-los à uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e998f-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="e998f-136">Os recursos atribuídos dessa maneira são adicionados à equipe sem nenhuma reserva.</span><span class="sxs-lookup"><span data-stu-id="e998f-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="e998f-137">É como adicionar um membro da equipe e selecionar Nenhum como o método de alocação.</span><span class="sxs-lookup"><span data-stu-id="e998f-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="e998f-138">O recurso é exibido nas guias **Equipe** e **Reconciliação** como recursos apenas com atribuições e um déficit de reserva.</span><span class="sxs-lookup"><span data-stu-id="e998f-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="e998f-139">Registre-os se quiser usar sua disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e998f-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="e998f-140">Na grade **Agendar** de uma tarefa, selecione o ícone **Recurso** na célula do recurso.</span><span class="sxs-lookup"><span data-stu-id="e998f-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="e998f-141">Comece a digitar um nome.</span><span class="sxs-lookup"><span data-stu-id="e998f-141">Start typing a name.</span></span> <span data-ttu-id="e998f-142">Os resultados da pesquisa para o nome são exibidos no **Seletor de Recursos** em **Outros Recursos**.</span><span class="sxs-lookup"><span data-stu-id="e998f-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="e998f-143">Selecione o recurso que deseja atribuir à tarefa.</span><span class="sxs-lookup"><span data-stu-id="e998f-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]