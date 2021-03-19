---
title: Manter membros da equipe
description: Este tópico fornece informações sobre como reservar recursos nomeados para equipes de projeto e atribuí-los a tarefas.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286819"
---
# <a name="maintain-team-members"></a><span data-ttu-id="2f73c-103">Manter membros da equipe</span><span class="sxs-lookup"><span data-stu-id="2f73c-103">Maintain team members</span></span>

<span data-ttu-id="2f73c-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="2f73c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2f73c-105">Você pode adicionar um recurso nomeado à equipe do projeto reservando-o diretamente na equipe.</span><span class="sxs-lookup"><span data-stu-id="2f73c-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="2f73c-106">No Dynamics 365 Project Operations, vá para **Projetos** e abra o projeto para o qual está fazendo a reserva.</span><span class="sxs-lookup"><span data-stu-id="2f73c-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="2f73c-107">Na página **Projetos**, na guia **Equipe**, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2f73c-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="2f73c-108">Na caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto**, selecione o recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="2f73c-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="2f73c-109">O campo **Função** será preenchido com a função padrão do recurso, caso tenha uma atribuída.</span><span class="sxs-lookup"><span data-stu-id="2f73c-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="2f73c-110">Você pode alterar a função.</span><span class="sxs-lookup"><span data-stu-id="2f73c-110">You can change the role.</span></span> 
4. <span data-ttu-id="2f73c-111">Selecione o intervalo de datas em que o recurso será necessário e o método de alocação da capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="2f73c-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="2f73c-112">Se quiser que o membro da equipe seja um aprovador de projeto, selecione **Sim** no campo **Aprovador do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="2f73c-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="2f73c-113">O membro da equipe pode aprovar as entradas de despesa e tempo enviadas para esse projeto.</span><span class="sxs-lookup"><span data-stu-id="2f73c-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="2f73c-114">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="2f73c-114">Select **Save**.</span></span>

<span data-ttu-id="2f73c-115">Agora é possível atribuir o recurso reservado a tarefas no projeto.</span><span class="sxs-lookup"><span data-stu-id="2f73c-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="2f73c-116">Na página **Projeto**, na guia **Agendar**, atribua tarefas ao novo recurso.</span><span class="sxs-lookup"><span data-stu-id="2f73c-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="2f73c-117">O seletor de recurso que é iniciado no campo **Recursos** na grade da tarefa mostrará os membros da equipe que podem ser selecionados.</span><span class="sxs-lookup"><span data-stu-id="2f73c-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="2f73c-118">Em Project Operations, as reservas de recursos e as atribuições de tarefas não estão estreitamente associadas.</span><span class="sxs-lookup"><span data-stu-id="2f73c-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="2f73c-119">Quando você usar o seletor de recurso na agenda, será possível atribuir tarefas aos membros da equipe para mais horas do que as cobertas na reserva do projeto.</span><span class="sxs-lookup"><span data-stu-id="2f73c-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="2f73c-120">As diferenças entre as reservas e atribuições dos membros da equipe são mostradas nas guias **Equipe** e **Reconciliação de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="2f73c-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="2f73c-121">Você também pode reconciliar as diferenças entre reservas e atribuições de recursos em um nível mais detalhado.</span><span class="sxs-lookup"><span data-stu-id="2f73c-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="2f73c-122">Use o seletor de recurso na guia **Agendar** para pesquisar e selecionar recursos reserváveis que não fazem parte da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="2f73c-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="2f73c-123">Esses recursos são mostrado no seletor de recurso como **Outros Recursos**.</span><span class="sxs-lookup"><span data-stu-id="2f73c-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="2f73c-124">Quando você faz uma seleção, o recurso é adicionado à equipe do projeto e atribuído à tarefa, mas não são geradas reservas.</span><span class="sxs-lookup"><span data-stu-id="2f73c-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="2f73c-125">É possível usar o recurso de extensão da guia **Reconciliação** ou **Quadro de Agendamento** para reservar a capacidade do recurso para o projeto.</span><span class="sxs-lookup"><span data-stu-id="2f73c-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="2f73c-126">Depois que um membro da equipe é reservado no projeto, você pode usar o recurso **Manter reservas** ou o **Quadro de agendamento** diretamente para gerenciar as reservas dele.</span><span class="sxs-lookup"><span data-stu-id="2f73c-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]