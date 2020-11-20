---
title: Considerações de upgrade - Microsoft Dynamics 365 Project Service Automation versão 2.x ou 1.x para a versão 3
description: Este tópico fornece informações sobre as considerações que você deve fazer ao fazer upgrade da versão 2.x ou 1.x para a versão 3 do Project Service Automation.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3c51726f71cfd0d4be98982d6a02268d64a70b91
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121699"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a><span data-ttu-id="efd70-103">Considerações de atualização - PSA versão 2.x ou 1.x para a versão 3</span><span class="sxs-lookup"><span data-stu-id="efd70-103">Upgrade considerations - PSA version 2.x or 1.x to version 3</span></span>
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a><span data-ttu-id="efd70-104">Project Service Automation e Field Service</span><span class="sxs-lookup"><span data-stu-id="efd70-104">Project Service Automation and Field Service</span></span>
<span data-ttu-id="efd70-105">O Dynamics 365 Project Service Automation e o Dynamics 365 Field Service usam a solução URS (Universal Resourcing Scheduling) para agendamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="efd70-105">Both Dynamics 365 Project Service Automation and Dynamics 365 Field Service use the Universal Resourcing Scheduling (URS) solution for resource scheduling.</span></span> <span data-ttu-id="efd70-106">Se você tiver o Project Service Automation e o Field Service em sua instância, planeje fazer upgrade das duas soluções para a versão mais recente (versão 3.x para o Project Service Automation, versão 8.x para o Field Service).</span><span class="sxs-lookup"><span data-stu-id="efd70-106">If you have both Project Service Automation and Field Service in your instance, you should plan on upgrading both solutions to the latest version (version 3.x for Project Service Automation, version 8.x for Field Service).</span></span> <span data-ttu-id="efd70-107">A atualização do Project Service Automation ou do Field Service instalará a versão mais recente do URS, o que significa que poderá ocorrer um comportamento inconsistente se as soluções Project Service Automation e Field Service na mesma instância não forem atualizadas para a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="efd70-107">Upgrading Project Service Automation or Field Service will install the latest version of URS, which means that inconsistent behavior is possible if both Project Service Automation and Field Service solutions in the same instance aren’t upgraded to the latest version.</span></span>

## <a name="resource-assignments"></a><span data-ttu-id="efd70-108">Atribuições de recursos</span><span class="sxs-lookup"><span data-stu-id="efd70-108">Resource assignments</span></span>
<span data-ttu-id="efd70-109">No Project Service Automation versão 2 e versão 1, as atribuições de tarefas eram armazenadas como tarefas filho (também chamadas de tarefas de linha) na **entidade Tarefa** e estavam indiretamente relacionadas à entidade **Atribuição de Recurso**.</span><span class="sxs-lookup"><span data-stu-id="efd70-109">In Project Service Automation version 2 and version 1, task assignments were stored as child tasks (also called line tasks) in the **Task entity**, and indirectly related to the **Resource Assignment** entity.</span></span> <span data-ttu-id="efd70-110">A tarefa de linha ficava visível na janela pop-up de atribuição da WBS (estrutura de detalhamento de trabalho).</span><span class="sxs-lookup"><span data-stu-id="efd70-110">The line task was visible in the assignment pop-up window on the Work Breakdown Structure (WBS).</span></span>

![Linha de tarefas na WBS no Project Service Automation versão 2 e versão 1](media/upgrade-line-task-01.png)

<span data-ttu-id="efd70-112">Na versão 3 do Project Service Automation, o esquema subjacente de atribuição de recursos reserváveis às tarefas foi alterado.</span><span class="sxs-lookup"><span data-stu-id="efd70-112">In version 3 of Project Service Automation, the underlying schema of assigning bookable resources to tasks has changed.</span></span> <span data-ttu-id="efd70-113">A tarefa de linha foi preterida e há um relacionamento 1:1 direto entre a tarefa na **entidade Tarefa** e o membro da equipe na entidade **Atribuição de Recurso**.</span><span class="sxs-lookup"><span data-stu-id="efd70-113">The line task has been deprecated and there is a direct 1:1 relationship between the task in the **Task entity** and the team member in the **Resource Assignment** entity.</span></span> <span data-ttu-id="efd70-114">As tarefas atribuídas a um membro da equipe do projeto agora são armazenadas diretamente na entidade Atribuição de Recurso.</span><span class="sxs-lookup"><span data-stu-id="efd70-114">Tasks that are assigned to a project team member are now stored directly in the Resource Assignment entity.</span></span>  

<span data-ttu-id="efd70-115">Essas alterações causam impacto na atualização dos projetos existentes que possuem atribuições de recursos para recursos reserváveis nomeados e recursos genéricos em uma equipe de projeto.</span><span class="sxs-lookup"><span data-stu-id="efd70-115">These changes impact the upgrade of any existing projects that have resource assignments for named bookable resources and generic resources on a project team.</span></span> <span data-ttu-id="efd70-116">Este tópico descreve as considerações que você deve fazer em relação aos projetos ao atualizar para a versão 3.</span><span class="sxs-lookup"><span data-stu-id="efd70-116">This topic provides the considerations that you will need to take into account for your projects when you upgrade to version 3.</span></span> 

### <a name="tasks-assigned-to-named-resources"></a><span data-ttu-id="efd70-117">Tarefas atribuídas a recursos nomeados</span><span class="sxs-lookup"><span data-stu-id="efd70-117">Tasks assigned to named resources</span></span>
<span data-ttu-id="efd70-118">Ao usar a entidade de tarefa subjacente, as tarefas na versão 2 e na versão 1 permitem que os membros da equipe desempenhem uma função diferente de suas funções padrão definidas.</span><span class="sxs-lookup"><span data-stu-id="efd70-118">Using the underlying task entity, tasks in version 2 and version 1 allowed team members to portray a role other than their default defined role.</span></span> <span data-ttu-id="efd70-119">Por exemplo, Clara Gomes, que recebeu, por padrão, a função de Gerente de Programa, pode receber a atribuição de uma tarefa com a função de Desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="efd70-119">For example, Gracie George, who’s by default assigned the role of Program Manager, could be assigned to a task with the role of Developer.</span></span> <span data-ttu-id="efd70-120">Na versão 3, a função dos membros de uma equipe nomeada é sempre o padrão, de modo que qualquer tarefa que seja atribuída a Clara Gomes use sua função padrão de Gerente de Programa.</span><span class="sxs-lookup"><span data-stu-id="efd70-120">In version 3, the role of a named team member is always the default, so any task that Gracie George is assigned to uses her default role of Program Manager.</span></span>

<span data-ttu-id="efd70-121">Se tiver atribuído a um recurso uma tarefa fora de sua função padrão nas versões 2 e 1, ao atualizar, a função padrão será atribuída ao recurso nomeado para todas as atribuições de tarefas, independentemente da atribuição de função na versão 2.</span><span class="sxs-lookup"><span data-stu-id="efd70-121">If you have assigned a resource to a task outside of their default role in version 2 and version 1, when you upgrade, the named resource will be assigned the default role for all task assignments, regardless of role assignment in version 2.</span></span> <span data-ttu-id="efd70-122">Isso resultará em diferenças nas estimativas calculadas da versão 2 ou versão 1 em relação à versão 3, pois as estimativas são calculadas com base na função do recurso, e não na atribuição da tarefa de linha.</span><span class="sxs-lookup"><span data-stu-id="efd70-122">This will result in differences in the calculated estimates from version 2 or version 1 to version 3 because estimates are calculated based on the role of the resource and not the line task assignment.</span></span> <span data-ttu-id="efd70-123">Por exemplo, na versão 2, duas tarefas foram atribuídas a Vitória Cavalcante.</span><span class="sxs-lookup"><span data-stu-id="efd70-123">For example, in version 2, two tasks have been assigned to Ashley Chinn.</span></span> <span data-ttu-id="efd70-124">A função na tarefa de linha da tarefa 1 era Desenvolvedor e, na tarefa 2, Gerente de Programa.</span><span class="sxs-lookup"><span data-stu-id="efd70-124">The role on the line task for task 1 is Developer and for task 2, Program Manager.</span></span> <span data-ttu-id="efd70-125">A função padrão de Vitória Cavalcante é Gerente de Programa.</span><span class="sxs-lookup"><span data-stu-id="efd70-125">Ashley Chinn has the default role of Program Manager.</span></span>

![Várias funções atribuídas a um recurso](media/upgrade-multiple-roles-02.png)

<span data-ttu-id="efd70-127">Como as funções de Desenvolvedor e Gerente de Programa são diferentes, as estimativas de custo e vendas são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="efd70-127">Because the roles of Developer and Program Manager differ, the cost and sales estimates are as follows:</span></span>

![Estimativas de custo para as funções do recurso](media/upggrade-cost-estimates-03.png)

![Estimativas de vendas para as funções do recurso](media/upgrade-sales-estimates-04.png)

<span data-ttu-id="efd70-130">Ao atualizar para a versão 3, as tarefas de linha são substituídas por atribuições de recursos na tarefa do membro da equipe de recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="efd70-130">When you upgrade to version 3, line tasks are replaced with resource assignments on the task of the bookable resource team member.</span></span> <span data-ttu-id="efd70-131">A atribuição usará a função padrão do recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="efd70-131">The assignment will use the default role of the bookable resource.</span></span> <span data-ttu-id="efd70-132">Na imagem a seguir, Vitória Cavalcante, que possui a função de Gerente de Programa, é o recurso.</span><span class="sxs-lookup"><span data-stu-id="efd70-132">In the following graphic, Ashley Chinn who has a role of Program Manager, is the resource.</span></span>

![Atribuições de recursos](media/resource-assignment-v2-05.png)

<span data-ttu-id="efd70-134">Como as estimativas baseiam-se na função padrão do recurso, as estimativas de custo e vendas podem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="efd70-134">Because the estimates are based on the default role for the resource, the sales and cost estimates may change.</span></span> <span data-ttu-id="efd70-135">Observe que, na imagem a seguir, a função **Desenvolvedor** não é mais exibida, pois a função agora é obtida da função padrão do recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="efd70-135">Note that in the following graphic, you no longer see the **Developer** role as the role is now taken from the bookable resource’s default role.</span></span>

<span data-ttu-id="efd70-136">![Estimativas de custo para funções padrão](media/resource-assignment-cost-estimate-06.png)
![Estimativas de vendas para funções padrão](media/resource-assignment-sales-estimate-07.png)</span><span class="sxs-lookup"><span data-stu-id="efd70-136">![Cost estimates for default roles](media/resource-assignment-cost-estimate-06.png)
![Sales estimate for default roles](media/resource-assignment-sales-estimate-07.png)</span></span>

<span data-ttu-id="efd70-137">Depois que a atualização for concluída, você poderá editar a função de um membro da equipe como algo diferente do padrão atribuído.</span><span class="sxs-lookup"><span data-stu-id="efd70-137">After upgrade is complete, you can edit a team member's role to be something other than the assigned default.</span></span> <span data-ttu-id="efd70-138">Entretanto, se você modificar a função de membros da equipe, ela será alterada em todas as suas tarefas atribuídas, pois não é mais permitido atribuir várias funções aos membros da equipe na versão 3.</span><span class="sxs-lookup"><span data-stu-id="efd70-138">However, if you change a team members role, it will be changed on all of their assigned tasks because team members are no longer allowed to be assigned multiple roles in version 3.</span></span>

![Atualizando uma função de recurso](media/resource-role-assignment-08.png)

<span data-ttu-id="efd70-140">Isso também é válido para as tarefas de linha atribuídas a recursos nomeados quando você altera a unidade organizacional do recurso de padrão para outra unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="efd70-140">This is also true for line tasks that were assigned to named resources when you change the resource’s organization unit from the default to another organization unit.</span></span> <span data-ttu-id="efd70-141">Após a conclusão da atualização da versão 3, a atribuição usará a unidade organizacional padrão do recurso, em vez da unidade definida na tarefa de linha.</span><span class="sxs-lookup"><span data-stu-id="efd70-141">After the version 3 upgrade is complete, the assignment will use the resource’s default organization unit instead of the one set on the line task.</span></span>

### <a name="tasks-assigned-to-generic-resources"></a><span data-ttu-id="efd70-142">Tarefas atribuídas a recursos genéricos</span><span class="sxs-lookup"><span data-stu-id="efd70-142">Tasks assigned to generic resources</span></span>
<span data-ttu-id="efd70-143">Na versão 2 e na versão 1, você pode definir a função e a unidade organizacional em uma tarefa e, depois, usar o recurso **Gerar equipe** para gerar recursos genéricos com base nos atributos definidos na tarefa.</span><span class="sxs-lookup"><span data-stu-id="efd70-143">In version 2 and version 1, you can set the role and org unit on a task and then use the **Generate team** feature to generate generic resources based on the attributes set on the task.</span></span> <span data-ttu-id="efd70-144">Na versão 3, você cria os membros da equipe genéricos com função e unidade organizacional e, em seguida, atribua os membros da equipe às tarefas.</span><span class="sxs-lookup"><span data-stu-id="efd70-144">In version 3, you create the generic team members with role and org unit, and then assign the team members to tasks.</span></span>

<span data-ttu-id="efd70-145">Na versão 2 e na versão 1, os projetos com recursos genéricos podem estar em dois estados ou em uma combinação de ambos no nível da tarefa.</span><span class="sxs-lookup"><span data-stu-id="efd70-145">In version 2 and version 1, projects with generic resources can be in two states, or a mix of both at the task level.</span></span> <span data-ttu-id="efd70-146">Por exemplo, é possível ter os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="efd70-146">For example, you can have the following scenarios:</span></span>

- <span data-ttu-id="efd70-147">Tarefas com funções e unidades organizacionais definidas, mas nenhuma atribuição de recurso afiliado foi gerada.</span><span class="sxs-lookup"><span data-stu-id="efd70-147">Tasks with roles and org units set, but no affiliated resource assignment has been generated.</span></span>
- <span data-ttu-id="efd70-148">Tarefas com recursos de membros da equipe genéricos atribuídos por meio da criação de um recurso genérico usando o recurso **Gerar equipe**.</span><span class="sxs-lookup"><span data-stu-id="efd70-148">Tasks with generic team member resource assignments that were assigned by creating generic resource using the **Generate team** feature.</span></span>

<span data-ttu-id="efd70-149">Antes de iniciar a atualização, é recomendável gerar novamente a equipe para cada projeto que possui tarefas atribuídas a recursos genéricos ou que ainda tem de executar o processo nelas.</span><span class="sxs-lookup"><span data-stu-id="efd70-149">Before you begin your upgrade, we recommend that you re-generate the team for each project that has tasks assigned to generic resources or has yet to have the generate team process run on them.</span></span>

<span data-ttu-id="efd70-150">Para as tarefas atribuídas a membros da equipe genéricos que foram gerados usando **Gerar equipe**, a atualização irá manter o recurso genérico na equipe e, também, a atribuição a esse membro da equipe genérico.</span><span class="sxs-lookup"><span data-stu-id="efd70-150">For tasks that are assigned to generic team members that were generated with **Generate Team**, the upgrade will leave the generic resource on the team and leave the assignment to that generic team member.</span></span> <span data-ttu-id="efd70-151">Recomendamos que você gere o requisito de recurso para o membro da equipe genérico após a atualização, mas antes de reservar ou enviar uma solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="efd70-151">We recommend that you generate the resource requirement for the generic team member after the upgrade but before you book or submit a resource request.</span></span> <span data-ttu-id="efd70-152">Isso preservará todas as atribuições de unidade organizacional dos membros da equipe genéricos que forem diferentes da unidade organizacional de contratação do projeto.</span><span class="sxs-lookup"><span data-stu-id="efd70-152">This will preserve any org unit assignments on the generic team members that are different than the project’s contracting org unit.</span></span>

<span data-ttu-id="efd70-153">Por exemplo, no projeto Projeto Z, a unidade organizacional de contratação é a unidade Cabral US.</span><span class="sxs-lookup"><span data-stu-id="efd70-153">For example, in the Project Z project, the contracting org unit is Contoso US.</span></span> <span data-ttu-id="efd70-154">No plano de projeto, a função Consultor Técnico foi atribuída às tarefas de teste da fase de implementação, e a unidade organizacional atribuída é a unidade Cabral India.</span><span class="sxs-lookup"><span data-stu-id="efd70-154">In the project plan, testing tasks within the Implementation phase have been assigned the role Technical Consultant and the assigned org unit is Contoso India.</span></span>

![Atribuição de organização na fase de implementação](media/org-unit-assignment-09.png)

<span data-ttu-id="efd70-156">Após a fase de implementação, a tarefa de teste de integração é atribuída à função Consultor Técnico, mas a organização é definida como Cabral US.</span><span class="sxs-lookup"><span data-stu-id="efd70-156">After the implementation phase, the integration test task is assigned to the role Technical consultant, but the org is set to Contoso US.</span></span>  

![Atribuição de organização da tarefa de teste de integração](media/org-unit-generate-team-10.png)

<span data-ttu-id="efd70-158">Ao gerar uma equipe para o projeto, dois membros da equipe genéricos são criados devido às unidades organizacionais diferentes nas tarefas.</span><span class="sxs-lookup"><span data-stu-id="efd70-158">When you generate a team for the project, two generic team members are created due to the different org units on the tasks.</span></span> <span data-ttu-id="efd70-159">As tarefas da unidade Cabral India serão atribuídas ao Consultor técnico 1 e o Consultor técnico 2 receberá as tarefas da unidade Cabral US.</span><span class="sxs-lookup"><span data-stu-id="efd70-159">Technical consultant 1 will be assigned the Contoso India tasks and Technical consultant 2 will have the Contoso US tasks.</span></span>  

![Membros da equipe genéricos gerados](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> <span data-ttu-id="efd70-161">No Project Service Automation versões 2 e 1, o membro da equipe não mantém a unidade organizacional, ela é mantida na tarefa de linha.</span><span class="sxs-lookup"><span data-stu-id="efd70-161">In Project Service Automation version 2 and version 1, the team member does not hold the organization unit, that is maintained on the line task.</span></span>

![Tarefas de linha de versão 2 e da versão 1 no Project Service Automation](media/line-tasks-12.png)

<span data-ttu-id="efd70-163">Você pode ver a unidade organizacional no modo de exibição de estimativas.</span><span class="sxs-lookup"><span data-stu-id="efd70-163">You can see the organization unit on the estimates view.</span></span> 

![Estimativas da unidade organizacional](media/org-unit-estimates-view-13.png)
 
<span data-ttu-id="efd70-165">Quando a atualização é concluída, a unidade organizacional na tarefa de linha que corresponde ao membro da equipe genérico é adicionada a esse membro e a tarefa de linha é removida.</span><span class="sxs-lookup"><span data-stu-id="efd70-165">When the upgrade is complete, the organization unit on the line task that corresponds to the generic team member is added to the generic team member and the line task is removed.</span></span> <span data-ttu-id="efd70-166">Por isso, recomendamos que, antes de atualizar, você gere a equipe em cada projeto que contém recursos genéricos, ou gere-a novamente.</span><span class="sxs-lookup"><span data-stu-id="efd70-166">Because of this, we recommend that before you upgrade, you generate or re-generate the team on each project that contains generic resources.</span></span>

<span data-ttu-id="efd70-167">Para as tarefas atribuídas a uma função com uma unidade organizacional diferente daquela do projeto de contratação e sem uma equipe gerada, a atualização criará um membro da equipe genérico para a função, mas usará a unidade de contratação do projeto para a unidade organizacional do membro da equipe.</span><span class="sxs-lookup"><span data-stu-id="efd70-167">For tasks that are assigned to a role with an org unit that differs from the org unit of the contracting project, and a team has not been generated, upgrade will create a generic team member for the role, but will use the contracting unit of the project for the team member's org unit.</span></span> <span data-ttu-id="efd70-168">Voltando ao exemplo do Projeto Z, isso significa que a função Consultor Técnico foi atribuída à unidade organizacional de contratação Cabral US e às tarefas de teste de plano do projeto na fase de implementação com a unidade organizacional atribuída à Cabral India.</span><span class="sxs-lookup"><span data-stu-id="efd70-168">Referring back to the example with Project Z, this means that the contracting org unit Contoso US, and the project plan testing tasks within the Implementation phase have been assigned the role Technical Consultant with the org unit assigned to Contoso India.</span></span> <span data-ttu-id="efd70-169">A tarefa de teste de integração concluída após a fase de implementação foi atribuída à função Consultor Técnico.</span><span class="sxs-lookup"><span data-stu-id="efd70-169">The Integration test task that is completed after the Implementation phase has been assigned to the role Technical consultant.</span></span> <span data-ttu-id="efd70-170">A unidade organizacional é a unidade Cabral US e uma equipe não foi gerada.</span><span class="sxs-lookup"><span data-stu-id="efd70-170">The org unit is Contoso US and a team has not been generated.</span></span> <span data-ttu-id="efd70-171">A atualização criará um membro da equipe genérico, um Consultor técnico que possui as horas atribuídas das três tarefas e uma unidade organizacional da unidade Cabral US, a unidade organizacional de contratação do projeto.</span><span class="sxs-lookup"><span data-stu-id="efd70-171">Upgrade will create one generic team member, a Technical consultant that has the assigned hours of all three tasks, and an org unit of Contoso US, the project’s contracting org unit.</span></span>   
 
<span data-ttu-id="efd70-172">Alteração no padrão de unidades organizacionais de recursos diferentes em membros de equipe não gerados é o motivo pelo qual recomendamos que você gere a equipe em cada projeto que contém recursos genéricos antes da atualização, de modo que as atribuições da unidade organizacional não sejam perdidas.</span><span class="sxs-lookup"><span data-stu-id="efd70-172">Changing the default of the different resourcing org units on un-generated team members is the reason we recommend that you generate or re-generate the team on each project that contains generic resources prior to the upgrade so that the org unit assignments are not lost.</span></span>
