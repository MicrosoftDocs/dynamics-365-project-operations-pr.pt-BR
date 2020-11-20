---
title: Gerenciar recursos
description: Este tópico fornece informações sobre como você pode gerenciar recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132319"
---
# <a name="manage-resources"></a><span data-ttu-id="e40d4-103">Gerenciar recursos</span><span class="sxs-lookup"><span data-stu-id="e40d4-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e40d4-104">O Dynamics 365 Project Service Automation inclui um painel de gerente de recursos que fornece uma visão geral visual da demanda e horas trabalhadas do recurso em toda a organização.</span><span class="sxs-lookup"><span data-stu-id="e40d4-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="e40d4-105">Você pode usar os gráficos desse painel para visualizar as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="e40d4-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="e40d4-106">**Demanda do recurso** – o gráfico **Solicitação de Recurso Ativa** mostra os recursos que foram enviados.</span><span class="sxs-lookup"><span data-stu-id="e40d4-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="e40d4-107">Os recursos são agregados pela função ou pelo projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="e40d4-108">**Demanda de recurso não enviada** – o gráfico **Demanda de Recurso Não Atribuída** mostra todos os requisitos de recurso que não foram enviados.</span><span class="sxs-lookup"><span data-stu-id="e40d4-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="e40d4-109">Ele ajuda os gerenciadores de recursos a verem a demanda que não está confirmada e pode ser enviada por meio de uma solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="e40d4-110">**Horas trabalhadas faturáveis para a semana passada** – o gráfico **Horas trabalhadas por Função** mostra a porcentagem das horas trabalhadas faturáveis por função de dados reais da organização em relação às suas horas trabalhadas faturáveis de destino por função.</span><span class="sxs-lookup"><span data-stu-id="e40d4-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e40d4-111">Para disponibilizar o gráfico **Horas Trabalhadas por Função**, crie um trabalho que execute o fluxo de trabalho UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="e40d4-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="e40d4-112">Esse trabalho recorrente é executado a cada sete dias para calcular as horas trabalhadas faturáveis para os sete dias anteriores.</span><span class="sxs-lookup"><span data-stu-id="e40d4-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="e40d4-113">Os resultados são agregados por função.</span><span class="sxs-lookup"><span data-stu-id="e40d4-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="e40d4-114">Gerenciar membros da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="e40d4-114">Manage project team members</span></span>

<span data-ttu-id="e40d4-115">Os gerentes de projeto podem usar o painel do gerente de recursos para gerenciar os recursos em projetos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="e40d4-116">Por exemplo, eles podem adicionar um membro da equipe diretamente a um projeto e reservar um membro da equipe para atender aos requisitos de recurso que foram capturados por um recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="e40d4-117">Adicionar um membro da equipe diretamente a um projeto</span><span class="sxs-lookup"><span data-stu-id="e40d4-117">Add a team member directly to a project</span></span>

<span data-ttu-id="e40d4-118">Para adicionar um membro da equipe diretamente a um projeto, na página **Projetos**, na guia **Equipe**, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="e40d4-119">A caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto** é exibida.</span><span class="sxs-lookup"><span data-stu-id="e40d4-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="e40d4-120">Nessa caixa de diálogo, você pode executar estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="e40d4-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="e40d4-121">**Reservar um recurso nomeado** – no campo **Recurso Reservável**, selecione o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="e40d4-122">Em seguida, selecione a função, defina o período e selecione um método de alocação.</span><span class="sxs-lookup"><span data-stu-id="e40d4-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="e40d4-123">O recurso nomeado que você selecionou é adicionado ao projeto usando o método de alocação selecionado e o calendário de recursos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="e40d4-124">**Adicionar um recurso genérico** – deixe o campo **Recurso reservável** em branco, selecione a função, defina o período e selecione o método de alocação de preferência.</span><span class="sxs-lookup"><span data-stu-id="e40d4-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="e40d4-125">Um recurso genérico é adicionado à equipe como um espaço reservado de modo a manter o padrão de demanda que é usado para reservar recursos nomeados na equipe.</span><span class="sxs-lookup"><span data-stu-id="e40d4-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="e40d4-126">O requisito é feito de acordo com o calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="e40d4-127">**Adicionar um recurso nomeado à equipe sem consumir capacidade do recurso** – no campo **Recurso Reservável**, selecione um recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="e40d4-128">Em seguida, selecione o período e **Nenhum** como o método de alocação.</span><span class="sxs-lookup"><span data-stu-id="e40d4-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="e40d4-129">O recurso é adicionado à equipe, mas a capacidade do recurso não é consumida por meio de uma reserva.</span><span class="sxs-lookup"><span data-stu-id="e40d4-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="e40d4-130">Reservar um membro da equipe para atender aos requisitos de um recurso genérico</span><span class="sxs-lookup"><span data-stu-id="e40d4-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="e40d4-131">No PSA, você pode reservar um recurso genérico em uma equipe de projeto, bem como especificar a função, a capacidade necessária e como essa capacidade é distribuída.</span><span class="sxs-lookup"><span data-stu-id="e40d4-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="e40d4-132">No requisito do recurso, é possível especificar atributos que são associados ao recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="e40d4-133">Esses atributos incluem habilidades necessárias, além da unidade organizacional e dos recursos de preferência.</span><span class="sxs-lookup"><span data-stu-id="e40d4-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="e40d4-134">Siga estas etapas para especificar as habilidades necessárias em um recurso genérico para um desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="e40d4-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="e40d4-135">Na página **Projetos**, na guia **Equipe**, selecione **Novo** para reservar um recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Recurso genérico reservado na equipe](media/Resource-Management-image9.png)

2. <span data-ttu-id="e40d4-137">Na exibição **Todos os Membros da Equipe**, na coluna **Requisito de Recurso**, selecione o link de modo a adicionar habilidades necessárias para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Link do requisito](media/Resource-Management-image10.png)

3. <span data-ttu-id="e40d4-139">Na página **Requisito de Recurso** que é exibida, na grade **Habilidades**, selecione as reticências (**...**) e, em seguida, **Adicionar Novas Características de Requisito** para adicionar as habilidades necessárias para seu desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="e40d4-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Comando Adicionar Novas Características de Requisito](media/Resource-Management-image11.png)

4. <span data-ttu-id="e40d4-141">Na caixa de diálogo **Criação Rápida: Característica de Requisito** que é exibida, no campo **Característica**, selecione a habilidade necessária.</span><span class="sxs-lookup"><span data-stu-id="e40d4-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="e40d4-142">Em seguida, no campo **Valor de classificação**, selecione o nível de proficiência para essa habilidade.</span><span class="sxs-lookup"><span data-stu-id="e40d4-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="e40d4-143">Por fim, no campo **Requisito de Recurso**, defina o requisito para dar origem a recursos, partindo de unidades organizacionais ou, até mesmo, de recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="e40d4-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="e40d4-144">Ao concluir, selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-144">When you've finished, select **Save**.</span></span>

    ![Caixa de diálogo Criação Rápida: Característica de Requisito](media/Resource-Management-image12.png)

5. <span data-ttu-id="e40d4-146">Na página **Requisito de Recurso**, selecione **Reservar** para atender ao requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Botão Reservar na página Requisito de Recurso](media/Resource-Management-image13.png)

    <span data-ttu-id="e40d4-148">Você também pode selecionar o recurso genérico na grade **Todos os Membros da Equipe** e selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Botão Reservar acima da grade Todos os Membros da Equipe](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="e40d4-150">Neste exemplo, há mais de 40 horas necessárias, mas nenhuma hora reservada, pois os recursos genéricos não têm reservas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="e40d4-151">Além disso, não há horas atribuídas, pois o recurso genérico foi adicionado diretamente à equipe.</span><span class="sxs-lookup"><span data-stu-id="e40d4-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="e40d4-152">Ele não foi adicionado usando a atribuição de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="e40d4-153">Na página **Assistente de Agendamento**, é possível filtrar os recursos disponíveis pelos requisitos que são especificados no requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="e40d4-154">Os recursos são classificados de acordo com os parâmetros de classificação que são especificados no Quadro de Agendamento.</span><span class="sxs-lookup"><span data-stu-id="e40d4-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Página Assistente de Agendamento](media/Resource-Management-image15.png)

    <span data-ttu-id="e40d4-156">Veja a seguir alguns filtros que são usados frequentemente:</span><span class="sxs-lookup"><span data-stu-id="e40d4-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="e40d4-157">**Características com uma classificação** – filtre por habilidades, certificações e outras qualidades do recurso, além de classificações de proficiência.</span><span class="sxs-lookup"><span data-stu-id="e40d4-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="e40d4-158">**Funções** – filtre por funções padrão que são atribuídas a recursos reserváveis.</span><span class="sxs-lookup"><span data-stu-id="e40d4-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="e40d4-159">**Unidades organizacionais** – filtre recursos reserváveis pelas unidades organizacionais às quais eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="e40d4-160">Se não estiver satisfeito com os resultados da pesquisa inicial de requisito, você poderá alterar os critérios de filtro.</span><span class="sxs-lookup"><span data-stu-id="e40d4-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="e40d4-161">Expanda o painel **Filtrar Exibição** à esquerda e selecione **Pesquisar** para encontrar recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="e40d4-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Painel Filtrar Exibição](media/Resource-Management-image16.png)

7. <span data-ttu-id="e40d4-163">Para alterar como os resultados são classificados, selecione **Classificar**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Comando Classificar](media/Resource-Management-image17.png)

8. <span data-ttu-id="e40d4-165">Selecione recursos de acordo com a demanda que é especificada no requisito, conforme indicado no topo da grade.</span><span class="sxs-lookup"><span data-stu-id="e40d4-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="e40d4-166">Você pode limpar a seleção das células na grade e deixar a capacidade do recurso em aberto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="e40d4-167">Somente um recurso por vez pode ser selecionado como reservado.</span><span class="sxs-lookup"><span data-stu-id="e40d4-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="e40d4-168">Selecione **Reservar** para reservar o recurso selecionado e deixar o Quadro de Agendamento em aberto, de modo que você possa selecionar recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="e40d4-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="e40d4-169">Como alternativa, selecione **Reservar e Sair** para reservar o recurso selecionado e fechar o Quadro de Agendamento.</span><span class="sxs-lookup"><span data-stu-id="e40d4-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Recurso a ser reservado](media/Resource-Management-image19.png)

    <span data-ttu-id="e40d4-171">Você recebe uma notificação sobre as horas reservadas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="e40d4-172">Os indicadores de demanda mostram quanto do requisito de reserva foi atendido e quanto ainda falta.</span><span class="sxs-lookup"><span data-stu-id="e40d4-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="e40d4-173">Também é possível ver o quanto é consumido da capacidade do recurso selecionado.</span><span class="sxs-lookup"><span data-stu-id="e40d4-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="e40d4-174">Selecione **Expandir** para exibir mais detalhes sobre reservas do recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="e40d4-175">Retorne à exibição **Todos os Membros da Equipe**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="e40d4-176">Na grade, observe que o recurso genérico foi substituído pelo recurso nomeado, e as 40 horas são listadas como reservadas para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Grade Todos os Membros da Equipe atualizada](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="e40d4-178">Nenhuma hora atribuída é mostrada, pois foram reservadas diretamente na equipe.</span><span class="sxs-lookup"><span data-stu-id="e40d4-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="e40d4-179">Elas não foram reservadas usando a atribuição de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="e40d4-180">Atribuir recursos genéricos a tarefas e gerar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="e40d4-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="e40d4-181">No PSA, você pode criar tarefas e atribuir recursos genéricos a elas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="e40d4-182">Desse modo, a demanda do recurso pode ser representada pelos espaços reservados enquanto você estima sua agenda e seus números financeiros.</span><span class="sxs-lookup"><span data-stu-id="e40d4-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="e40d4-183">É possível gerar requisitos para recursos genéricos e atendê-los.</span><span class="sxs-lookup"><span data-stu-id="e40d4-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="e40d4-184">Na página **Projetos**, na guia **Agendar**, selecione **Adicionar** para criar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e40d4-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Nova tarefa criada](media/Resource-Management-image21.png)

2. <span data-ttu-id="e40d4-186">No campo **Recursos**, selecione o símbolo **Seletor de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="e40d4-187">O Seletor de Recursos aparece e mostra membros da equipe existentes para o projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Seletor de Recursos](media/Resource-Management-image22.png)

3. <span data-ttu-id="e40d4-189">Digite o novo nome do novo recurso genérico e selecione **Criar**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Nome de um novo recurso genérico inserido](media/Resource-Management-image23.png)

4. <span data-ttu-id="e40d4-191">Na caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto** exibida, no campo **Função**, selecione a função para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="e40d4-192">No campo **Unidade de Recursos**, selecione a unidade organizacional para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="e40d4-193">Em seguida, selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-193">Then select **Save**.</span></span>

    ![Caixa de diálogo Criação Rápida: Membro da Equipe do Projeto](media/Resource-Management-image24.png)

    <span data-ttu-id="e40d4-195">O membro da equipe genérico agora é atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="e40d4-195">The generic team member is now assigned to the task.</span></span>

    ![Membro da equipe genérico atribuído à tarefa](media/Resource-Management-image25.png)

    <span data-ttu-id="e40d4-197">Na guia **Equipe**, você verá o novo membro da equipe genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="e40d4-198">Observe que ele tem apenas horas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="e40d4-199">Essas horas são a soma de todas as tarefas que são atribuídas ao membro da equipe genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="e40d4-200">O membro da equipe genérico ainda não tem horas exigidas nem um requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Membro da equipe genérico na guia Equipe](media/Resource-Management-image26.png)

5. <span data-ttu-id="e40d4-202">Agora você pode atribuir o membro da equipe genérico a outras tarefas usando o Seletor de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Membro da equipe genérico no Seletor de Recursos](media/Resource-Management-image27.png)

    <span data-ttu-id="e40d4-204">Ao terminar de atribuir o recurso genérico às tarefas, você poderá gerar um requisito para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="e40d4-205">Na guia **Equipe**, selecione o recurso genérico e selecione **Gerar Requisito**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Comando Gerar Requisito](media/Resource-Management-image28.png)

    <span data-ttu-id="e40d4-207">Quando o requisito for gerado, o membro da equipe genérico terá horas exigidas e um link para o requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Link Requisito de recurso](media/Resource-Management-image29.png)

    <span data-ttu-id="e40d4-209">Após reserva de um recurso nomeado, o recurso genérico é removido da equipe e substituído pelo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="e40d4-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Recurso genérico substituído pelo recurso nomeado](media/Resource-Management-image30.png)

    <span data-ttu-id="e40d4-211">Na guia **Agendar**, as atribuições de recurso genérico são removidas e substituídas pelo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="e40d4-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Atribuições de recurso genérico substituídas pelo recurso nomeado na guia Agendar](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="e40d4-213">Esse comportamento ocorre apenas quando um recurso é totalmente reservado para o requisito de recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="e40d4-214">Quando um recurso nomeado substitui parcialmente o requisito de recurso genérico ou vários recursos nomeados substituem o requisito de recurso genérico, este permanece atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="e40d4-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="e40d4-215">Na ilustração a seguir, uma tarefa de 80 horas foi planejada para uma duração de cinco dias (16 horas por dia por cinco dias) e atribuída ao recurso genérico denominado **Funcional**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Tarefa de oitenta horas e cinco dias para o recurso genérico Funcional](media/Resource-Management-image32.png)

    <span data-ttu-id="e40d4-217">Quando você gera o requisito, é para 80 horas por cinco dias.</span><span class="sxs-lookup"><span data-stu-id="e40d4-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Requisito gerado para 80 horas por cinco dias](media/Resource-Management-image33.png)

    <span data-ttu-id="e40d4-219">Como os recursos disponíveis funcionam somente oito horas por dia, dois recursos são necessário para atender ao requisito.</span><span class="sxs-lookup"><span data-stu-id="e40d4-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Segundo recurso](media/Resource-Management-image35.png)

    <span data-ttu-id="e40d4-221">Na guia **Equipe**, agora é possível ver que o recurso genérico não tenha horas exigidas, mas as horas atribuídas ainda aparecem com os dois recursos nomeados que compõem o atendimento.</span><span class="sxs-lookup"><span data-stu-id="e40d4-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dois recursos nomeados na guia Equipe](media/Resource-Management-image36.png)

    <span data-ttu-id="e40d4-223">Na guia **Agendar**, o recurso genérico permanece atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="e40d4-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Recursos genéricos na guia Agendar](media/Resource-Management-image37.png)

<span data-ttu-id="e40d4-225">O PSA não atribui ambos os recursos à tarefa, pois esse comportamento geraria uma agenda menos previsível.</span><span class="sxs-lookup"><span data-stu-id="e40d4-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="e40d4-226">Neste exemplos simples, é fácil dividir as horas igualmente entre dois recursos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="e40d4-227">No entanto, em cenários mais complexos que envolvem várias tarefas e vários recursos, o PSA teria que supor como deve alocar as reservas que são recebidas para vários recursos em várias tarefas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="e40d4-228">Portanto, nesses cenários, o gerente de projeto é responsável por analisar as várias reservas e atribuí-las conforme a necessidade.</span><span class="sxs-lookup"><span data-stu-id="e40d4-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="e40d4-229">Para alocar as reservas, o gerente de projeto atribui as tarefas dos recursos genéricos aos recursos nomeados e usa a exibição **Reconciliação** para garantir que a alocação funcione com as reservas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="e40d4-230">Editar um requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="e40d4-230">Edit a resource requirement</span></span>

<span data-ttu-id="e40d4-231">Depois que um requisito de recurso tiver sido criado, um gerente de projeto ou gerente de recursos pode querer editar os detalhes para refinar os critérios de pesquisa quando o Quadro de Agendamento é usado.</span><span class="sxs-lookup"><span data-stu-id="e40d4-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="e40d4-232">Para editar o requisito de recurso, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="e40d4-233">Na página **Projetos**, na guia **Equipe**, selecione o link para qualquer requisito em um recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="e40d4-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="e40d4-234">Na página **Requisito de Recurso** que é exibida, você pode atualizar vários atributos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="e40d4-235">Veja alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="e40d4-235">Here are some examples:</span></span>

    - <span data-ttu-id="e40d4-236">Nome</span><span class="sxs-lookup"><span data-stu-id="e40d4-236">Name</span></span>
    - <span data-ttu-id="e40d4-237">Data Inicial</span><span class="sxs-lookup"><span data-stu-id="e40d4-237">From Date</span></span>
    - <span data-ttu-id="e40d4-238">Data Final</span><span class="sxs-lookup"><span data-stu-id="e40d4-238">To Date</span></span>
    - <span data-ttu-id="e40d4-239">Duração</span><span class="sxs-lookup"><span data-stu-id="e40d4-239">Duration</span></span>
    - <span data-ttu-id="e40d4-240">Tipo de Recurso</span><span class="sxs-lookup"><span data-stu-id="e40d4-240">Resource Type</span></span>

<span data-ttu-id="e40d4-241">Na página **Requisito de Recurso**, o gerente de projeto ou gerente de recursos também pode definir as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="e40d4-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="e40d4-242">Habilidades</span><span class="sxs-lookup"><span data-stu-id="e40d4-242">Skills</span></span>
- <span data-ttu-id="e40d4-243">Funções</span><span class="sxs-lookup"><span data-stu-id="e40d4-243">Roles</span></span>
- <span data-ttu-id="e40d4-244">Preferências de recurso</span><span class="sxs-lookup"><span data-stu-id="e40d4-244">Resource preferences</span></span>
- <span data-ttu-id="e40d4-245">Unidades organizacionais preferenciais</span><span class="sxs-lookup"><span data-stu-id="e40d4-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="e40d4-246">Atualizar reservas do recurso depois que ele é reservado em um projeto</span><span class="sxs-lookup"><span data-stu-id="e40d4-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="e40d4-247">Depois de adicionar um recurso genérico ou nomeado a uma equipe de projeto, você pode alterar as reservas do recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="e40d4-248">Na página **Projetos**, na guia **Equipe**, selecione um membro da equipe e, por fim, selecione **Manter Registros**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Quadro de Agendamento aberto para o membro da equipe selecionado](media/Resource-Management-image40.png)

    <span data-ttu-id="e40d4-250">O Quadro de Agendamento aparece e mostra as reservas do membro da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="e40d4-251">Expanda o registro do membro da equipe para exibir as horas que foram reservadas em relação a esse projeto e outros projetos que estão consumindo a capacidade do membro da equipe.</span><span class="sxs-lookup"><span data-stu-id="e40d4-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="e40d4-252">Selecione e arrastre a reserva para estendê-la ou encurtá-la.</span><span class="sxs-lookup"><span data-stu-id="e40d4-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="e40d4-253">Uma caixa de diálogo **Criar Reserva de Recursos** aparece e permite ajustar a reserva.</span><span class="sxs-lookup"><span data-stu-id="e40d4-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Caixa de diálogo Criar Reserva de Recursos](media/Resource-Management-image41.png)

3. <span data-ttu-id="e40d4-255">Clique com o botão direito do mouse na reserva.</span><span class="sxs-lookup"><span data-stu-id="e40d4-255">Right-click the booking.</span></span> <span data-ttu-id="e40d4-256">É possível usar o menu de atalho para concluir as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="e40d4-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="e40d4-257">Alterar o status da reserva.</span><span class="sxs-lookup"><span data-stu-id="e40d4-257">Change the booking status.</span></span>
    - <span data-ttu-id="e40d4-258">Editar a reserva.</span><span class="sxs-lookup"><span data-stu-id="e40d4-258">Edit the booking.</span></span>
    - <span data-ttu-id="e40d4-259">Substituir um recurso na equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="e40d4-260">Alterar o status da reserva</span><span class="sxs-lookup"><span data-stu-id="e40d4-260">Change the booking status</span></span>

<span data-ttu-id="e40d4-261">Você pode alterar qualquer status de reserva padrão ou personalizada.</span><span class="sxs-lookup"><span data-stu-id="e40d4-261">You can change any default or custom booking status.</span></span>

![Comando Alterar Status](media/Resource-Management-image42.png)

<span data-ttu-id="e40d4-263">Os seguintes status são incluídos no PSA:</span><span class="sxs-lookup"><span data-stu-id="e40d4-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="e40d4-264">**Cancelado** – esse status cancela uma reserva do recurso e libera a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="e40d4-265">**Reserva Fixa** – esse status consome a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="e40d4-266">Geralmente, uma reserva tem esse status quando você abre **Manter Reservas** na grade **Todos os Membros da Equipe** na página **Projetos**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="e40d4-267">**Reserva Flexível** – esse status adiciona um recurso a uma equipe, mas não consome a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="e40d4-268">Ele indica que o recurso foi reservado para trabalho potencial, mas ainda tem capacidade se for necessário para outros trabalhos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="e40d4-269">Na exibição da disponibilidade geral do recurso, as reservas flexíveis têm um status diferente de reservas fixas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="e40d4-270">**Proposto** – esse status representa uma proposta do gerente de recursos ou gerente de projeto para um recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="e40d4-271">As propostas não consomem a capacidade de um recurso, e o recurso não é adicionado à equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="e40d4-272">Para fazer uma reserva fixa do recurso na equipe, o gerente de projeto deve aceitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="e40d4-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="e40d4-273">Enviar solicitações de recursos</span><span class="sxs-lookup"><span data-stu-id="e40d4-273">Submit resource requests</span></span>

<span data-ttu-id="e40d4-274">As solicitações de recurso são usadas para transmitir a demanda (requisito de recurso) que deve ser atendida por um gerente de recursos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="e40d4-275">Para um recurso genérico que já está na equipe, você pode enviar uma solicitação de recurso diretamente.</span><span class="sxs-lookup"><span data-stu-id="e40d4-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="e40d4-276">Uma solicitação de recurso pode ser atendida de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="e40d4-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="e40d4-277">O gerente de recursos atende à solicitação diretamente.</span><span class="sxs-lookup"><span data-stu-id="e40d4-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="e40d4-278">Nesse caso, o recurso genérico é substituído por uma reserva fixa que tem um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="e40d4-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="e40d4-279">O gerente de recursos propõe um recurso para o gerente de projeto, e o gerente de projeto aprova ou rejeita o recurso proposto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="e40d4-280">Atendimento direto das solicitações de recurso</span><span class="sxs-lookup"><span data-stu-id="e40d4-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="e40d4-281">Quando um requisito de recurso é gerado, um gerente de projeto pode enviar uma solicitação de recurso para um recurso genérico selecionando o recurso e **Enviar Solicitação**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Botão Enviar Solicitação](media/Resource-Management-image45.png)

<span data-ttu-id="e40d4-283">Os comentários sobre o recurso podem ser fornecidos ao gerente de recursos que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="e40d4-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="e40d4-284">Depois que a solicitação é enviada, o campo **Status** do membro da equipe é alterado para **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Inserindo comentários opcionais](media/Resource-Management-image46.png)

<span data-ttu-id="e40d4-286">Quando o gerente de recursos atende à solicitação, o membro da equipe genérico é substituído pelo recurso nomeado na grade **Todos os Membros da Equipe**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Membro da equipe genérico substituído pelo recurso nomeado na grade Todos os Membros da Equipe](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="e40d4-288">Usar uma proposta de recurso para solicitações de recurso</span><span class="sxs-lookup"><span data-stu-id="e40d4-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="e40d4-289">Em vez de reservar diretamente um recurso em uma solicitação de recurso, um gerente de recursos pode propor um recurso ao gerente de projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="e40d4-290">Um gerente de recursos pode usar essa opção quando uma correspondência exata para os requisitos não está disponível.</span><span class="sxs-lookup"><span data-stu-id="e40d4-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="e40d4-291">Quando um gerente de recursos propõe um recurso, o gerente de projeto vê se o campo **Status** para o membro da equipe genérico foi alterado para **Precisa de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Status do membro da equipe genérico alterado para Precisa de Revisão](media/Resource-Management-image48.png)

<span data-ttu-id="e40d4-293">Para exibir o recurso proposto com uma visualização do efeito da reserva da proposta, clique duas vezes no membro da equipe que tem um status de **Precisa de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="e40d4-294">Em seguida, selecione a guia **Recursos Propostos**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-294">Then select the **Proposed Resources** tab.</span></span>

![Guia Recursos Propostos](media/Resource-Management-image49.png)

<span data-ttu-id="e40d4-296">Selecione **Aceitar Todas as Propostas** para aceitar todos os recursos propostos ou **Rejeitar Todas as Propostas** para rejeitá-las.</span><span class="sxs-lookup"><span data-stu-id="e40d4-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="e40d4-297">Se você aceitar os recursos propostos, eles serão reservados fixamente no projeto como membros da equipe e substituirão os recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="e40d4-298">Você deve aceitar ou rejeitar todos os recursos propostos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="e40d4-299">Não é possível aceitá-los ou rejeitá-los parcialmente.</span><span class="sxs-lookup"><span data-stu-id="e40d4-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="e40d4-300">Substituir um recurso na equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="e40d4-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="e40d4-301">Às vezes, o gerente de projeto deve substituir um membro da equipe registrado em um projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="e40d4-302">Na página **Projetos**, na guia **Equipe**, selecione o recurso que precisa de um substituto e selecione **Manter Reservas**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="e40d4-303">Expanda o recurso para exibir os projetos aos quais ele está atribuído.</span><span class="sxs-lookup"><span data-stu-id="e40d4-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Recurso expandido para mostrar projetos atribuídos](media/Resource-Management-image50.png)

3. <span data-ttu-id="e40d4-305">Clique com o botão direito do mouse no projeto e selecione **Substituir Recurso**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="e40d4-306">Se você souber o recurso que deseja substituir para o recurso atual, selecione ou digite o nome e selecione **Reatribuir**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Especificando um recurso substituto](media/Resource-Management-image51.png)

    <span data-ttu-id="e40d4-308">Se preferir, siga estas etapas para procurar um recurso:</span><span class="sxs-lookup"><span data-stu-id="e40d4-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="e40d4-309">Selecione **Localizar Substituição**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-309">Select **Find Substitution**.</span></span>

        ![Procurando um recurso substituto](media/Resource-Management-image52.png)

        <span data-ttu-id="e40d4-311">O Assistente de Agendamento retorna uma lista de substitutos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e40d4-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="e40d4-312">No Assistente de Agendamento, você ainda pode filtrar os recursos disponíveis para localizar um substituto adequado.</span><span class="sxs-lookup"><span data-stu-id="e40d4-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Lista de substitutos disponíveis](media/Resource-Management-image53.png)

    2. <span data-ttu-id="e40d4-314">Para substituir o recurso, selecione o recurso desejado e, em seguida, **Substituto**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Recurso substituto selecionado](media/Resource-Management-image54.png)

    <span data-ttu-id="e40d4-316">As reservas e atribuições são substituídas pelo novo recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Reservas e atribuições substituídas pelo novo recurso](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="e40d4-318">Reconciliar reservas e atribuições do membro da equipe</span><span class="sxs-lookup"><span data-stu-id="e40d4-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="e40d4-319">Para membros da equipe, reservas e atribuições são livremente combinadas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="e40d4-320">Em outras palavras, os recursos podem ter atribuições, mas nenhuma reserva, ou podem ter reservas, mas nenhuma atribuição.</span><span class="sxs-lookup"><span data-stu-id="e40d4-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="e40d4-321">De maneira ideal, reservas e atribuições devem ser alinhadas para que os recursos tenham capacidade confirmada para executar as atribuições de tarefa.</span><span class="sxs-lookup"><span data-stu-id="e40d4-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="e40d4-322">No entanto, as reservas podem ser baseadas na disponibilidade e as durações das tarefas podem ser alteradas conforme o projeto continua.</span><span class="sxs-lookup"><span data-stu-id="e40d4-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="e40d4-323">Portanto, a livre combinação de reservas e atribuições proporciona flexibilidade.</span><span class="sxs-lookup"><span data-stu-id="e40d4-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="e40d4-324">O PSA tem uma guia **Reconciliação** que permite aos gerentes de projeto reconciliar reservas dos membros da equipe e suas atribuições para equipes de projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Guia Reconciliação](media/Resource-Management-image56.png)

<span data-ttu-id="e40d4-326">A guia **Reconciliação** mostra reservas e atribuições até o nível da atribuição de tarefas individual para cada membro da equipe.</span><span class="sxs-lookup"><span data-stu-id="e40d4-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="e40d4-327">Ela mostra horas em células que representam períodos, desde meses até dias.</span><span class="sxs-lookup"><span data-stu-id="e40d4-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="e40d4-328">A guia também mostra um total líquido geral para o projeto com uma coluna de total.</span><span class="sxs-lookup"><span data-stu-id="e40d4-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="e40d4-329">Para cada recurso, a guia calcula a diferença entre as reservas do membro da equipe e um valor acumulado das atribuições de tarefas do membro da equipe.</span><span class="sxs-lookup"><span data-stu-id="e40d4-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="e40d4-330">O ideal é que essa diferença seja 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e40d4-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="e40d4-331">Em outras palavras, não deve haver diferença entre as reservas e as atribuições.</span><span class="sxs-lookup"><span data-stu-id="e40d4-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="e40d4-332">As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:</span><span class="sxs-lookup"><span data-stu-id="e40d4-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="e40d4-333">**Falta de reserva** – a falta de reserva ocorre quando um recurso tem mais atribuições do que reservas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="e40d4-334">Como essa capacidade não foi reservada, um gerente de projeto pode querer corrigir essa condição estendendo as reservas do recurso para cobrir o déficit.</span><span class="sxs-lookup"><span data-stu-id="e40d4-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="e40d4-335">**Reservas em excesso** – ocorrem quando um recurso é reservado para o projeto, mas não é atribuído a tarefas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="e40d4-336">Essa condição pode ser aceitável nos casos onde o recurso foi reservado para o projeto antes da atribuição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e40d4-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="e40d4-337">No entanto, em outros casos, o recurso não foi planejado para ser atribuído a tarefas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="e40d4-338">Nesses casos, o gerente de projetos deve considerar o cancelamento das reservas do recurso, para que a capacidade possa ser usada em outro projeto.</span><span class="sxs-lookup"><span data-stu-id="e40d4-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="e40d4-339">Em alguns casos, quando você exibe tempo em um nível mais alto do que o nível de dia (por exemplo, o nível de mês), é possível ver uma diferença líquida de zero para um recurso (em outras palavras, reservas = atribuições).</span><span class="sxs-lookup"><span data-stu-id="e40d4-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="e40d4-340">No entanto, se você exibir o tempo no nível de semana, será possível ver que há atribuições de zero horas e reservas de 40 horas na primeira semana, mas as atribuições de 40 horas e reservas de zero horas na segunda semana.</span><span class="sxs-lookup"><span data-stu-id="e40d4-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="e40d4-341">De modo geral, as reservas e atribuições são reconciliadas, mas elas diferem de uma semana para a outra.</span><span class="sxs-lookup"><span data-stu-id="e40d4-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="e40d4-342">Ao exibir tempo em níveis mais altos, as células na guia **Reconciliação** têm um indicador para informar que há diferenças em níveis mais baixos.</span><span class="sxs-lookup"><span data-stu-id="e40d4-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="e40d4-343">Ao clicar duas vezes em uma célula, você pode ampliar para exibir a diferença.</span><span class="sxs-lookup"><span data-stu-id="e40d4-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="e40d4-344">É possível clicar com o botão direito do mouse para reduzir. Ao selecionar um recurso e usar o controle **Próxima diferença** na barra de ferramentas da grade, você pode ir para a próxima diferença entre reservas e atribuições para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="e40d4-345">Você pode usar o controle **Diferença anterior** para voltar.</span><span class="sxs-lookup"><span data-stu-id="e40d4-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="e40d4-346">Também é possível desativar o indicador de diferença e o comportamento da navegação em **Configurações**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Indicador de diferença](media/Resource-Management-image57.png)

<span data-ttu-id="e40d4-348">Se você tiver atribuições de tarefa para um recurso, mas nenhuma reserva, na página **Projetos**, na guia **Reconciliação**, selecione a falta de reserva e, em seguida, **Estender Reserva**.</span><span class="sxs-lookup"><span data-stu-id="e40d4-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="e40d4-349">A caixa de diálogo **Estender Reserva** aparece e mostra a reserva que é necessária para suprir a falta do recurso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="e40d4-350">Ela também mostra as reservas existentes do recurso em todos os projetos ou outras entidades que podem ser agendadas.</span><span class="sxs-lookup"><span data-stu-id="e40d4-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="e40d4-351">Se você selecionar **OK** a fim de criar a reserva para o recurso, independentemente da disponibilidade desse recurso, é possível haver reservas em excesso.</span><span class="sxs-lookup"><span data-stu-id="e40d4-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Caixa de diálogo Estender Reserva](media/Resource-Management-image58.png)

<span data-ttu-id="e40d4-353">O gerente de projeto ou o gerente de recursos pode usar o Quadro de Agendamento para gerenciar situações em que um recurso é reservado em excesso além de sua capacidade.</span><span class="sxs-lookup"><span data-stu-id="e40d4-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
