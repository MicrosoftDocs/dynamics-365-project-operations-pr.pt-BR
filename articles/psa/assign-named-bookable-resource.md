---
title: Reservar recursos reserváveis nomeados a uma equipe de projeto e atribuir tarefas
description: Este tópico fornece informações sobre como reservar recursos indicados para equipes de projeto e atribuí-los a tarefas.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009332"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="b1228-103">Reservar recursos reserváveis nomeados a uma equipe de projeto e atribuir tarefas</span><span class="sxs-lookup"><span data-stu-id="b1228-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b1228-104">Você pode adicionar um recurso nomeado à equipe do projeto reservando-o diretamente na equipe.</span><span class="sxs-lookup"><span data-stu-id="b1228-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="b1228-105">Para fazer isso, execute estas etapas.</span><span class="sxs-lookup"><span data-stu-id="b1228-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="b1228-106">No Project Service Automation, vá para **Projetos** e abra o projeto para o qual está fazendo a reserva.</span><span class="sxs-lookup"><span data-stu-id="b1228-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="b1228-107">Na página **Projetos**, na guia **Equipe**, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="b1228-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Adicionando um membro da equipe pela guia de equipe](media/RM-how-to-1.png)

3. <span data-ttu-id="b1228-109">Na caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto**, selecione o recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="b1228-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="b1228-110">O campo **Função** será preenchido com a função padrão do recurso, caso tenha uma atribuída.</span><span class="sxs-lookup"><span data-stu-id="b1228-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="b1228-111">Você pode alterar a função, se necessário.</span><span class="sxs-lookup"><span data-stu-id="b1228-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="b1228-112">Selecione o intervalo de datas em que o recurso será necessário e o método de alocação da capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="b1228-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="b1228-113">Se quiser que o membro da equipe seja um aprovador de projeto, selecione **Sim** no campo **Aprovador do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="b1228-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="b1228-114">Isso significa que o membro da equipe pode aprovar as entradas de despesa e tempo enviadas para esse projeto.</span><span class="sxs-lookup"><span data-stu-id="b1228-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="b1228-115">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="b1228-115">Click **Save**.</span></span>

![Adicionando um membro da equipe no formulário de criação rápida](media/RM-how-to-2.png)


<span data-ttu-id="b1228-117">Agora é possível atribuir o recurso reservado a tarefas no projeto.</span><span class="sxs-lookup"><span data-stu-id="b1228-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="b1228-118">Na página **Projeto**, clique na guia **Agendar** para atribuir atarefas ao novo recurso.</span><span class="sxs-lookup"><span data-stu-id="b1228-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="b1228-119">O seletor de recurso que é iniciado no campo **Recursos** na grade da tarefa mostrará os membros da equipe que podem ser selecionados.</span><span class="sxs-lookup"><span data-stu-id="b1228-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Atribuindo um membro da equipe a uma tarefa na guia de agendamento](media/RM-how-to-3.png)

<span data-ttu-id="b1228-121">Na versão 3 do PSA (Project Service Automation), reservas de recurso e atribuições de tarefa não são rigidamente acopladas.</span><span class="sxs-lookup"><span data-stu-id="b1228-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="b1228-122">Isso significa que quando você usar o seletor de recurso na agenda, será possível atribuir tarefas aos membros da equipe para mais horas do que as cobertas na reserva do projeto.</span><span class="sxs-lookup"><span data-stu-id="b1228-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="b1228-123">É possível ver as diferenças entre atribuições e reservas do membro da equipe na guia **Equipe** ou na guia **Reconciliação de Recursos**. Você também pode reconciliar as diferenças entre reservas e atribuições para recursos em um nível mais detalhado.</span><span class="sxs-lookup"><span data-stu-id="b1228-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Guia Reconciliação de recursos](media/RM-how-to-4.png)

<span data-ttu-id="b1228-125">Você também pode usar o seletor de recurso na guia **Agendar** para pesquisar e selecionar recursos reserváveis que não fazem parte da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="b1228-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="b1228-126">Eles são mostrado no seletor de recurso como **Outros Recursos**.</span><span class="sxs-lookup"><span data-stu-id="b1228-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Atribuindo um recurso de membro que não faz parte da equipe a uma tarefa](media/RM-how-to-5.png)

<span data-ttu-id="b1228-128">Ao fazer isso, o recurso é adicionado à equipe do projeto e atribuído à tarefa, mas não são geradas reservas.</span><span class="sxs-lookup"><span data-stu-id="b1228-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Membro da equipe com atribuições e sem reservas](media/RM-how-to-6.png)

<span data-ttu-id="b1228-130">É possível usar o recurso de extensão da guia **Reconciliação** ou **Quadro de Agendamento** para reservar a capacidade do recurso para o projeto.</span><span class="sxs-lookup"><span data-stu-id="b1228-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Estendendo reservas para um membro da equipe na guia de reconciliação de recursos](media/RM-how-to-7.png)

<span data-ttu-id="b1228-132">Depois que um membro da equipe é reservado no projeto, você pode usar o recurso de manter reservas ou o Quadro de Agendamento diretamente para gerenciar as reservas dele.</span><span class="sxs-lookup"><span data-stu-id="b1228-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]