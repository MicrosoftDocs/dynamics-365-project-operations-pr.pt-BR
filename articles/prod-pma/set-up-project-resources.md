---
title: Configurar recursos do projeto
description: Este tópico fornece informações sobre como configurar ou solicitar recursos do projeto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997677"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="250e9-103">Configurar recursos do projeto</span><span class="sxs-lookup"><span data-stu-id="250e9-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="250e9-104">Você deve configurar um calendário e associá-lo a um funcionário ou colaborador.</span><span class="sxs-lookup"><span data-stu-id="250e9-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="250e9-105">O calendário é usado para agendar o projeto e o horário de trabalho dos recursos reservados para o projeto.</span><span class="sxs-lookup"><span data-stu-id="250e9-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="250e9-106">Durante a configuração do calendário, os gerentes de projeto podem fazer o nivelamento de recursos como parte da otimização de recursos.</span><span class="sxs-lookup"><span data-stu-id="250e9-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="250e9-107">Com base na agenda do calendário, podem ser colocadas restrições aos recursos.</span><span class="sxs-lookup"><span data-stu-id="250e9-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="250e9-108">Você pode configurar um calendário na página **Calendários**.</span><span class="sxs-lookup"><span data-stu-id="250e9-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="250e9-109">Ao configurar um funcionário como recurso do projeto, você pode selecionar entre os funcionários que trabalham na empresa para a qual você está configurando os recursos.</span><span class="sxs-lookup"><span data-stu-id="250e9-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="250e9-110">Você também pode selecionar funcionários de outras empresas em sua organização.</span><span class="sxs-lookup"><span data-stu-id="250e9-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="250e9-111">Esses funcionários são conhecidos como recursos intercompanhia.</span><span class="sxs-lookup"><span data-stu-id="250e9-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="250e9-112">Os procedimentos a seguir explicam como configurar um funcionário como um recurso de projeto na sua empresa e como configurar um recurso de projeto intercompanhia.</span><span class="sxs-lookup"><span data-stu-id="250e9-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="250e9-113">Configurar um funcionário como um recurso do projeto</span><span class="sxs-lookup"><span data-stu-id="250e9-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="250e9-114">Na página **Funcionários**, na lista **Funcionários**, selecione o funcionário que você está adicionando como um recurso de projeto e abra o registro dele.</span><span class="sxs-lookup"><span data-stu-id="250e9-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="250e9-115">No Painel de ação, selecione **Projeto** &gt; **Configuração** &gt; **Configuração do projeto**.</span><span class="sxs-lookup"><span data-stu-id="250e9-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="250e9-116">Selecione um calendário e feche a página.</span><span class="sxs-lookup"><span data-stu-id="250e9-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="250e9-117">Você também pode especificar projetos padrão para um recurso como um tipo de atribuição prévia.</span><span class="sxs-lookup"><span data-stu-id="250e9-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="250e9-118">As atribuições prévias podem ser usadas quando o gerente de recursos ou de projeto sabe com antecedência em quais projetos o recurso estará trabalhando.</span><span class="sxs-lookup"><span data-stu-id="250e9-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="250e9-119">As atribuições prévias também podem ser baseadas na solicitação de um patrocinador ou cliente do projeto.</span><span class="sxs-lookup"><span data-stu-id="250e9-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="250e9-120">Para fazer a atribuição prévia de um projeto, na página **Atribuir projetos**, na guia **Projetos**, na lista **Projetos pendentes**, selecione o projeto apropriado.</span><span class="sxs-lookup"><span data-stu-id="250e9-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="250e9-121">Configurar um recurso intercompanhia</span><span class="sxs-lookup"><span data-stu-id="250e9-121">Set up an intercompany resource</span></span>

<span data-ttu-id="250e9-122">Ao configurar um funcionário como um recurso intercompanhia, você deve concluir a configuração na empresa que faz e na que toma o empréstimo.</span><span class="sxs-lookup"><span data-stu-id="250e9-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="250e9-123">Na empresa que faz o empréstimo</span><span class="sxs-lookup"><span data-stu-id="250e9-123">In the lending company</span></span>

1. <span data-ttu-id="250e9-124">No Finance, verifique se a empresa que faz o empréstimo está selecionada e conclua o procedimento da seção anterior, "Configurar um funcionário como um recurso do projeto".</span><span class="sxs-lookup"><span data-stu-id="250e9-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="250e9-125">Na página **Contabilidade intercompanhia**, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="250e9-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="250e9-126">No campo **ID de entidade legal**, selecione a empresa que faz o empréstimo.</span><span class="sxs-lookup"><span data-stu-id="250e9-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="250e9-127">Preencha os campos restantes conforme apropriado e, em seguida, selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="250e9-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="250e9-128">Na página **Preço de transferência**, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="250e9-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="250e9-129">No campo **Entidade legal que toma o empréstimo**, selecione a empresa apropriada.</span><span class="sxs-lookup"><span data-stu-id="250e9-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="250e9-130">Para emprestar à empresa que toma o empréstimo apenas o recurso que você criou no início desta seção, no campo **Recurso**, selecione o nome do recurso que você criou.</span><span class="sxs-lookup"><span data-stu-id="250e9-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="250e9-131">Para colocar todos os recursos da empresa que faz o empréstimo à disposição da empresa que o toma, deixe o campo **Recurso** em branco.</span><span class="sxs-lookup"><span data-stu-id="250e9-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="250e9-132">Na página **Parâmetros de gerenciamento e contabilidade de projeto**, na guia **Intercompanhia**, defina a opção **Habilitar quadro de horários e agendamento de recursos intercompanhia** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="250e9-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="250e9-133">Na empresa que toma o empréstimo</span><span class="sxs-lookup"><span data-stu-id="250e9-133">In the borrowing company</span></span>

- <span data-ttu-id="250e9-134">Na página **Lista de recursos**, no filtro de pesquisa, insira o nome do recurso que você criou para a empresa que faz o empréstimo para verificar se o nome está incluído na lista de recursos para a empresa que o toma.</span><span class="sxs-lookup"><span data-stu-id="250e9-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="250e9-135">Solicitar recursos do projeto</span><span class="sxs-lookup"><span data-stu-id="250e9-135">Request project resources</span></span>
<span data-ttu-id="250e9-136">A funcionalidade de agendamento de recursos do projeto permite apenas que os gerentes de recursos distribuam recursos de equipe em compromissos ou projetos.</span><span class="sxs-lookup"><span data-stu-id="250e9-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="250e9-137">Para ativar essa funcionalidade, conclua as seguintes tarefas ou verifique se elas foram concluídas:</span><span class="sxs-lookup"><span data-stu-id="250e9-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="250e9-138">Configurar sequências numéricas.</span><span class="sxs-lookup"><span data-stu-id="250e9-138">Set up number sequences.</span></span>
- <span data-ttu-id="250e9-139">Configurar fluxos de trabalho de gerenciamento e contabilidade de projeto.</span><span class="sxs-lookup"><span data-stu-id="250e9-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="250e9-140">Habilite fluxos de trabalho de solicitação de recursos.</span><span class="sxs-lookup"><span data-stu-id="250e9-140">Enable resource request workflows.</span></span>

<span data-ttu-id="250e9-141">Após a conclusão das tarefas anteriores, você poderá concluir as seguintes tarefas conforme necessário:</span><span class="sxs-lookup"><span data-stu-id="250e9-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="250e9-142">Criar uma solicitação de recurso a partir de um recurso em equipe com reserva flexível.</span><span class="sxs-lookup"><span data-stu-id="250e9-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="250e9-143">Monitorar as solicitações de recursos.</span><span class="sxs-lookup"><span data-stu-id="250e9-143">Monitor resource requests.</span></span>
- <span data-ttu-id="250e9-144">Preencher solicitações de recursos.</span><span class="sxs-lookup"><span data-stu-id="250e9-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="250e9-145">Solicitar um recurso de equipe de uma WBS.</span><span class="sxs-lookup"><span data-stu-id="250e9-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="250e9-146">Reservar recursos para um projeto sem ter uma solicitação de um recurso de equipe.</span><span class="sxs-lookup"><span data-stu-id="250e9-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]