---
title: Criar uma equipe de projeto
description: Este tópico fornece informações sobre como criar e gerenciar equipes de projeto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071593"
---
# <a name="create-a-project-team"></a><span data-ttu-id="c818b-103">Criar uma equipe de projeto</span><span class="sxs-lookup"><span data-stu-id="c818b-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c818b-104">Para usar as funções que foram configuradas anteriormente em um projeto, um gerente de projeto deve associar as funções ao projeto.</span><span class="sxs-lookup"><span data-stu-id="c818b-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="c818b-105">Várias funções podem ser atribuídas a um projeto.</span><span class="sxs-lookup"><span data-stu-id="c818b-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="c818b-106">Para evitar confusão, essas funções são automaticamente rotuladas durante a reserva.</span><span class="sxs-lookup"><span data-stu-id="c818b-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="c818b-107">Por exemplo, se o gerente de projeto precisa de três engenheiros de software, três funções de engenheiro de software com os rótulos **engenheiro de software 1** , **engenheiro de software 2** e **engenheiro de software 3** serão geradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c818b-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1** , **software engineer 2** , and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="c818b-108">Se as características da função foram definidas anteriormente para a função, elas são aplicadas como um filtro durante as pesquisas de um recurso.</span><span class="sxs-lookup"><span data-stu-id="c818b-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="c818b-109">Características adicionais podem ser adicionadas conforme necessário para refinar ainda mais a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c818b-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="c818b-110">As configurações de exibição também podem ser personalizadas para exibir melhor a disponibilidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="c818b-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="c818b-111">Existem opções para mostrar a disponibilidade horária, diária, semanal, mensal, trimestral e anual.</span><span class="sxs-lookup"><span data-stu-id="c818b-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="c818b-112">Também há uma opção para mostrar a capacidade disponível e restante dos recursos.</span><span class="sxs-lookup"><span data-stu-id="c818b-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="c818b-113">Essa opção é útil para gerenciamento de horas, ao estimar o tempo disponível para atividades ou disponibilidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="c818b-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="c818b-114">O gerente de projeto pode selecionar uma função na página e, em seguida, se houver um recurso disponível que atenda ao requisito, selecionar para reservar um recurso para preencher a função.</span><span class="sxs-lookup"><span data-stu-id="c818b-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="c818b-115">Observe que os recursos não precisam ser reservados nesse ponto do estágio de planejamento.</span><span class="sxs-lookup"><span data-stu-id="c818b-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="c818b-116">Ao criar uma WBS, você pode substituir funções por recursos de equipe para o projeto.</span><span class="sxs-lookup"><span data-stu-id="c818b-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="c818b-117">Se as funções forem substituídas por recursos de equipe na WBS, a configuração do recurso atualiza automaticamente o agendamento e a lista da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="c818b-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="c818b-118">[![Lista da equipe do projeto que inclui funções e recursos reais](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="c818b-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="c818b-119">O gerente de projeto tem várias opções para reservar um recurso para um projeto, como **Capacidade restante** , **Capacidade total** , **Porcentagem de capacidade** e **Especificar horas**.</span><span class="sxs-lookup"><span data-stu-id="c818b-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity** , **Full capacity** , **Capacity percentage** , and **Specify hours**.</span></span> <span data-ttu-id="c818b-120">Essas opções de reserva podem ser canceladas a qualquer momento se as atribuições de recursos forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="c818b-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="c818b-121">Dois tipos de reserva são compatíveis:</span><span class="sxs-lookup"><span data-stu-id="c818b-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="c818b-122">**Reserva fixa** : a reserva de recurso foi aprovada e confirmada para trabalhar no compromisso pelo período especificado.</span><span class="sxs-lookup"><span data-stu-id="c818b-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="c818b-123">**Reserva flexível** : a reserva de recurso foi configurada para tentar trabalhar no compromisso pelo período especificado.</span><span class="sxs-lookup"><span data-stu-id="c818b-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="c818b-124">O seguinte procedimento explica como criar uma equipe de projeto.</span><span class="sxs-lookup"><span data-stu-id="c818b-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="c818b-125">Criar uma equipe de projeto</span><span class="sxs-lookup"><span data-stu-id="c818b-125">Create a project team</span></span>

1. <span data-ttu-id="c818b-126">Na página de lista **Todos os projetos** , selecione um projeto e, em seguida, **Editar**.</span><span class="sxs-lookup"><span data-stu-id="c818b-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="c818b-127">Na guia **Equipe do projeto e agendamento** , no campo **Data de término do agendamento** , insira a data de início do agendamento mais um mês.</span><span class="sxs-lookup"><span data-stu-id="c818b-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="c818b-128">Por exemplo, se a data de início do agendamento for 24 de junho de 2017 (24/06/2017), insira **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="c818b-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="c818b-129">Selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="c818b-129">Select **Add**.</span></span>
4. <span data-ttu-id="c818b-130">No painel **Adicionar funções ao projeto** , no campo **Função** , selecione **Gerente de projeto sênior**.</span><span class="sxs-lookup"><span data-stu-id="c818b-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="c818b-131">Selecione **Competências necessárias**.</span><span class="sxs-lookup"><span data-stu-id="c818b-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="c818b-132">Na página **Escolher características** , as características que você configurou anteriormente para a função de gerente de projeto sênior são selecionadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="c818b-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="c818b-133">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="c818b-133">Select **OK**.</span></span>
7. <span data-ttu-id="c818b-134">Na página **Adicionar funções ao projeto** , no campo **Número de recursos** , digite **1**.</span><span class="sxs-lookup"><span data-stu-id="c818b-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="c818b-135">No campo **Recurso** , a pesquisa mostra todos os recursos que possuem as competências necessárias.</span><span class="sxs-lookup"><span data-stu-id="c818b-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="c818b-136">Selecione **Daniel Goldschmidt** e, em seguida, **Criar**.</span><span class="sxs-lookup"><span data-stu-id="c818b-136">Select **Daniel Goldschmidt** , and then select **Create**.</span></span>
9. <span data-ttu-id="c818b-137">Na página **Projeto** , selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="c818b-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="c818b-138">No painel **Adicionar funções ao projeto** , no campo **Função** , selecione **Membro da equipe**.</span><span class="sxs-lookup"><span data-stu-id="c818b-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="c818b-139">No campo **Número de recursos** , insira **5**.</span><span class="sxs-lookup"><span data-stu-id="c818b-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="c818b-140">Selecione **Criar**.</span><span class="sxs-lookup"><span data-stu-id="c818b-140">Select **Create**.</span></span>
12. <span data-ttu-id="c818b-141">Na página **Projetos** , selecione **Preencher recurso**.</span><span class="sxs-lookup"><span data-stu-id="c818b-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="c818b-142">Monitorar equipes de projeto</span><span class="sxs-lookup"><span data-stu-id="c818b-142">Monitor project teams</span></span>
1. <span data-ttu-id="c818b-143">Na página **Todos os projetos** , selecione o link da **ID do projeto** para o projeto **Atualização do XYZ fase 2**.</span><span class="sxs-lookup"><span data-stu-id="c818b-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="c818b-144">Na FastTab **Equipe do projeto e agendamento** , verifique se os recursos do projeto listados estão corretos.</span><span class="sxs-lookup"><span data-stu-id="c818b-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>