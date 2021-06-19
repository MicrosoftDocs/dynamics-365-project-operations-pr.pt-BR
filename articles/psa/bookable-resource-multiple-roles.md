---
title: Estimar vendas e custos do projeto quando um recurso reservável preencher várias funções para um projeto
description: Este tópico fornece informações sobre como as dimensões de preços podem ser usadas para oferecer suporte a preços e custos de um recurso que preenche várias funções em um projeto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013247"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="95b44-103">Estimar vendas e custos do projeto quando um recurso reservável preencher várias funções para um projeto</span><span class="sxs-lookup"><span data-stu-id="95b44-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="95b44-104">As empresas que têm como base projetos frequentemente precisam de um recurso para realizar várias funções em um projeto.</span><span class="sxs-lookup"><span data-stu-id="95b44-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="95b44-105">Cada uma dessas funções pode ter um preço e um custo diferentes, o que significa que a hora do mesmo recurso no projeto pode ter uma estimativa financeira diferente, dependendo da cobrança e das taxas de custo de cada uma das funções.</span><span class="sxs-lookup"><span data-stu-id="95b44-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="95b44-106">O Project Service Automation permite a configuração dos valores no registro do membro da equipe para o recurso nomeado e permite diferentes substituições em cada uma das tarefas às quais o membro da equipe está atribuído.</span><span class="sxs-lookup"><span data-stu-id="95b44-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="95b44-107">O exemplo a seguir explica como a substituição simples desse valor permite que um recurso tenha várias funções em um projeto com diferentes custos e taxas de cobrança.</span><span class="sxs-lookup"><span data-stu-id="95b44-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="95b44-108">Criar tarefas</span><span class="sxs-lookup"><span data-stu-id="95b44-108">Create tasks</span></span>
<span data-ttu-id="95b44-109">Crie duas tarefas de projeto de 40 horas cada, Tarefa A e Tarefa B. Selecione a Tarefa A como predecessora da Tarefa B.</span><span class="sxs-lookup"><span data-stu-id="95b44-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="95b44-110">Configurar a Função e a Unidade Organizacional para um membro genérico da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="95b44-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="95b44-111">Na página **Agenda**, selecione a linha **Tarefa** para a Tarefa A.</span><span class="sxs-lookup"><span data-stu-id="95b44-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="95b44-112">No campo **Recursos**, selecione **Criar** na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="95b44-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="95b44-113">Na página **Criação Rápida de Membro de Equipe**, especifique os atributos do membro genérico da equipe que poderá executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="95b44-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="95b44-114">Selecione a função e a unidade organizacional apropriadas e, em seguida, selecione **Salvar e Fechar**.</span><span class="sxs-lookup"><span data-stu-id="95b44-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="95b44-115">Um membro genérico da equipe é criado e atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="95b44-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="95b44-116">Repita estas etapas para a Tarefa B e certifique-se de que a função e a unidade organizacional no membro genérico da equipe criado para a Tarefa B sejam diferentes da Tarefa A.</span><span class="sxs-lookup"><span data-stu-id="95b44-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="95b44-117">Configurar a função e a unidade organizacional para uma tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="95b44-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="95b44-118">Depois de criar a Tarefa A, selecione a tarefa e, em seguida, selecione **Editar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="95b44-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="95b44-119">Na página **Detalhes da Tarefa**, localize os campos **Função** e **Unidade Organizacional**, adicione os valores exigidos de um recurso que executaria esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="95b44-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="95b44-120">Se você estiver concluindo estes cenários usando dados de demonstração do Project Service Automation, selecione **Líder de Consultoria** como a função e **Fabrikam US** como a unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="95b44-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="95b44-121">Selecione a Tarefa B e, em seguida, **Editar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="95b44-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="95b44-122">Na página **Detalhes da Tarefa**, localize os campos **Função** e **Unidade Organizacional**, adicione os valores exigidos de um recurso que executaria esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="95b44-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="95b44-123">Certifique-se de que os valores nos campos **Função** e **Unidade organizacional** sejam diferentes entre a Tarefa B e a Tarefa A.</span><span class="sxs-lookup"><span data-stu-id="95b44-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="95b44-124">Se você estiver concluindo estes cenários usando dados de demonstração do Project Service Automation, selecione **Técnico de Rede** como a função e **Fabrikam US** como a unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="95b44-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="95b44-125">Salve e feche a página **Detalhes da Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="95b44-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="95b44-126">Membro da equipe e comportamento de estimativas</span><span class="sxs-lookup"><span data-stu-id="95b44-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="95b44-127">Na página **Detalhes da Tarefa**, em **Membro da Equipe**, selecione os dois Membros genéricos da equipe e, em seguida, selecione **Gerar Requisitos**.</span><span class="sxs-lookup"><span data-stu-id="95b44-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="95b44-128">Selecione a linha do membro da equipe de **Líder de Consultoria** e então selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="95b44-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="95b44-129">O quadro de horários é aberto e reserva um recurso para esse requisito.</span><span class="sxs-lookup"><span data-stu-id="95b44-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="95b44-130">Selecione a linha do membro da equipe de **Técnico de Rede** e então selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="95b44-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="95b44-131">O quadro de horários é aberto e reserva o mesmo recurso nesse requisito.</span><span class="sxs-lookup"><span data-stu-id="95b44-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="95b44-132">Grade Membro da Equipe</span><span class="sxs-lookup"><span data-stu-id="95b44-132">Team Member grid</span></span> 
<span data-ttu-id="95b44-133">Na grade **Membro da Equipe**, observe que os dois registros genéricos do membro da equipe foram excluídos e um recurso foi substituído.</span><span class="sxs-lookup"><span data-stu-id="95b44-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="95b44-134">Há um conjunto de valores para esse recurso que mostra um conjunto padrão de valores para **Função** e **Unidade Organizacional**.</span><span class="sxs-lookup"><span data-stu-id="95b44-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="95b44-135">Ao expandir a linha desse registro Membro da Equipe, você poderá ver atribuições distintas no registro do membro da equipe para ambas as tarefas.</span><span class="sxs-lookup"><span data-stu-id="95b44-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="95b44-136">Cada linha de atribuição tem valores específicos de tarefa para **Função** e **Unidade Organizacional**.</span><span class="sxs-lookup"><span data-stu-id="95b44-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="95b44-137">Grade Estimativas</span><span class="sxs-lookup"><span data-stu-id="95b44-137">Estimates grid</span></span> 
<span data-ttu-id="95b44-138">Quando navegar para a grade **Estimativas**, você notará que ambas as atribuições para o mesmo recurso têm preços diferentes.</span><span class="sxs-lookup"><span data-stu-id="95b44-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="95b44-139">O preço da atribuição para o recurso na Tarefa A foi estimado usando o valor do atributo **Função** de **Líder de Consultoria**.</span><span class="sxs-lookup"><span data-stu-id="95b44-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="95b44-140">O preço da atribuição para o mesmo recurso na Tarefa B foi estimado usando o valor do atributo **Função** de **Técnico de Rede**.</span><span class="sxs-lookup"><span data-stu-id="95b44-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]