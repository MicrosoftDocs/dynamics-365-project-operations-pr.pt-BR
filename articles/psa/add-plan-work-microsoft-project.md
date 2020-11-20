---
title: Usar o Suplemento do Project Service para planejar seu trabalho no Microsoft Project | MicrosoftDocs
description: Este tópico fornece informações sobre como adicionar, configurar e usar o suplemento do Microsoft Project para o Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071558"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="489ad-103">Usar o Suplemento do Project Service Automation para planejar seu trabalho no Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="489ad-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="489ad-104">Com o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], é mais fácil realizar o planejamento de projetos, incluindo estimativas.</span><span class="sxs-lookup"><span data-stu-id="489ad-104">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="489ad-105">Você pode definir o trabalho para que os custos, o esforço e o valor de venda estejam claros quando a proposta final for enviada.</span><span class="sxs-lookup"><span data-stu-id="489ad-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="489ad-106">Agora você pode instalar o [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] e fazer o seu trabalho de planejamento no ambiente familiar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="489ad-107">Use os sólidos recursos de planejamento e gerenciamento do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e atualize seu plano de projeto no Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="489ad-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="489ad-108">Para usar o gerenciamento de documentos do SharePoint para armazenar os arquivos [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para projetos do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o administrador do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] precisará ativar o gerenciamento de documentos.</span><span class="sxs-lookup"><span data-stu-id="489ad-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="489ad-109">O [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] é compatível apenas com o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="489ad-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="489ad-110">Baixar e instalar o suplemento</span><span class="sxs-lookup"><span data-stu-id="489ad-110">Download and install the add-in</span></span>  
 <span data-ttu-id="489ad-111">Prepare suas informações de suplemento do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="489ad-112">Você precisará dessas informações para se conectar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="489ad-113">No Centro de Download, você pode baixar o suplemento para a versão compatível do Project Service, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ou [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="489ad-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="489ad-114">Clique no link do download.</span><span class="sxs-lookup"><span data-stu-id="489ad-114">Click the download link.</span></span>  

3.  <span data-ttu-id="489ad-115">Quando o download estiver concluído, clique em **Sim** para instalar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="489ad-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="489ad-116">Configurar o suplemento</span><span class="sxs-lookup"><span data-stu-id="489ad-116">Configure the add-in</span></span>  

1. <span data-ttu-id="489ad-117">Abra o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e clique na guia **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="489ad-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="489ad-118">Clique em **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="489ad-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="489ad-119">Insira as informações do seu suplemento e, em seguida, clique em **Entrar**.</span><span class="sxs-lookup"><span data-stu-id="489ad-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="489ad-120">Agora você pode começar a usar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="489ad-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="489ad-121">Ler de um modelo</span><span class="sxs-lookup"><span data-stu-id="489ad-121">Read from a template</span></span>  
 <span data-ttu-id="489ad-122">Ler usando um modelo que você criou no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copie para [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para iniciar o planejamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="489ad-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="489ad-123">[Criar um modelo de projeto (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="489ad-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="489ad-124">Na guia **Project Service** , clique em **Ler** > **Modelo de projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="489ad-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="489ad-125">Selecione um modelo de projeto na lista e depois clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="489ad-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="489ad-126">Por padrão, as tarefas que são copiadas do modelo no Project são definidas como agendadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="489ad-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="489ad-127">Atribuir funções de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] aos recursos do projeto</span><span class="sxs-lookup"><span data-stu-id="489ad-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="489ad-128">Abra um projeto e clique na faixa de opções **Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="489ad-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="489ad-129">Clique no menu **Gráfico de Gantt** e depois selecione **Planilha de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="489ad-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="489ad-130">Na Planilha de Recursos, clique no menu suspenso **Função de Recurso do Project Service** e selecione uma função do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="489ad-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="489ad-131">Obter recursos para seu projeto</span><span class="sxs-lookup"><span data-stu-id="489ad-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="489ad-132">Na guia Project Service, selecione uma linha e clique em **Encontrar Recursos**.</span><span class="sxs-lookup"><span data-stu-id="489ad-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="489ad-133">Na tela **Reservar Recurso** , selecione o recurso que deseja usar no projeto.</span><span class="sxs-lookup"><span data-stu-id="489ad-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="489ad-134">Clique em **Reservar** e depois clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="489ad-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="489ad-135">Publicar seu projeto</span><span class="sxs-lookup"><span data-stu-id="489ad-135">Publish your project</span></span>  
<span data-ttu-id="489ad-136">Após a conclusão do seu planejamento de projeto, o próximo passo é importar e publicar o projeto na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="489ad-137">O projeto será importado para a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="489ad-138">Os preços e o processo de geração de equipe serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="489ad-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="489ad-139">Abra o projeto no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para verificar se a equipe, as estimativas de projeto e a estrutura de detalhamento de trabalho foram gerados.</span><span class="sxs-lookup"><span data-stu-id="489ad-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="489ad-140">A seguinte tabela mostra onde encontrar os resultados:</span><span class="sxs-lookup"><span data-stu-id="489ad-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="489ad-141">**Gráfico de Gantt**</span><span class="sxs-lookup"><span data-stu-id="489ad-141">**Gantt Chart**</span></span>   | <span data-ttu-id="489ad-142">Importa na tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estrutura de Detalhamento de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="489ad-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="489ad-143">**Planilha de Recursos**</span><span class="sxs-lookup"><span data-stu-id="489ad-143">**Resource Sheet**</span></span> |   <span data-ttu-id="489ad-144">Importa na tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Membros da Equipe do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="489ad-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="489ad-145">**Uso**</span><span class="sxs-lookup"><span data-stu-id="489ad-145">**Use Usage**</span></span>    |    <span data-ttu-id="489ad-146">Importa na tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estimativas do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="489ad-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="489ad-147">**Para importar e publicar seu projeto**</span><span class="sxs-lookup"><span data-stu-id="489ad-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="489ad-148">Na guia **Project Service** , clique em **Publicar** > **Novo Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="489ad-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="489ad-149">Na caixa de diálogo **Publicar para um novo projeto no Project Service** , insira o **Nome do Projeto** e selecione o **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="489ad-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="489ad-150">Opcionalmente, verifique a opção **Vincular plano de projeto ao Project Service Automation** para vincular o arquivo do Project do plano ao Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="489ad-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="489ad-151">Clique em **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="489ad-151">Click **Publish**.</span></span>  

   <span data-ttu-id="489ad-152">Vincular o arquivo do Project ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] torna o arquivo do Project o mestre e define a estrutura de detalhamento de trabalho no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="489ad-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="489ad-153">Para fazer alterações no plano de projeto, você precisa fazê-las no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicá-las como atualizações para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="489ad-154">Editar um projeto que foi importado</span><span class="sxs-lookup"><span data-stu-id="489ad-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="489ad-155">Para fazer alterações em um plano de projeto que foi importado para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], você tem duas opções:</span><span class="sxs-lookup"><span data-stu-id="489ad-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="489ad-156">Abra o arquivo mestre e edite-o no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="489ad-157">Desvincule o arquivo e edite-o diretamente no Project Service.</span><span class="sxs-lookup"><span data-stu-id="489ad-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="489ad-158">Por padrão, um projeto que foi carregado do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] é bloqueado e só pode ser editado em Projeto.</span><span class="sxs-lookup"><span data-stu-id="489ad-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="489ad-159">Para editar o arquivo no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o arquivo precisa estar desvinculado.</span><span class="sxs-lookup"><span data-stu-id="489ad-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="489ad-160">Edite no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="489ad-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="489ad-161">No menu principal, clique em **Project Service** > **Projetos**.</span><span class="sxs-lookup"><span data-stu-id="489ad-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="489ad-162">Na lista de projetos, abra aquele que você criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="489ad-163">Clique em **Abrir no MS Project** na faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="489ad-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="489ad-164">Isso abrirá o arquivo mestre vinculado no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="489ad-165">Desvincule um arquivo e edite no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="489ad-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="489ad-166">No menu principal, clique em **Project Service** > **Projetos**.</span><span class="sxs-lookup"><span data-stu-id="489ad-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="489ad-167">Na lista de projetos, abra aquele que você criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="489ad-168">Clique em **Desvincular do MS Project** na faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="489ad-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="489ad-169">Carregar um arquivo do Project no SharePoint ou Grupos do Office</span><span class="sxs-lookup"><span data-stu-id="489ad-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="489ad-170">É possível carregar seu arquivo do Project no SharePoint e encontrá-lo nos Documentos Associados do seu projeto do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="489ad-171">É preciso que o administrador configure o gerenciamento de documentos do SharePoint e ative-o para a entidade Projeto.</span><span class="sxs-lookup"><span data-stu-id="489ad-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="489ad-172">Você também pode carregar seu arquivo do projeto para [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se tiver Grupos do Office configurados.</span><span class="sxs-lookup"><span data-stu-id="489ad-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="489ad-173">Carregar um arquivo para SharePoint</span><span class="sxs-lookup"><span data-stu-id="489ad-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="489ad-174">No menu principal, clique em **Project Service** > **Carregar**.</span><span class="sxs-lookup"><span data-stu-id="489ad-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="489ad-175">Selecione **Para Documentos do Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="489ad-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="489ad-176">Na caixa de diálogo **Permitir Abertura no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , selecione **Sim** ou **Não**.</span><span class="sxs-lookup"><span data-stu-id="489ad-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="489ad-177">Se clicar em **Sim** , você poderá selecionar o botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation, iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o arquivo do Project da biblioteca de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="489ad-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="489ad-178">Se clicar em **Não** , o link do botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.</span><span class="sxs-lookup"><span data-stu-id="489ad-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="489ad-179">O arquivo do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto específico do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="489ad-180">Carregar um arquivo para Grupos do Office</span><span class="sxs-lookup"><span data-stu-id="489ad-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="489ad-181">No menu principal, clique em **Project Service** > **Carregar**.</span><span class="sxs-lookup"><span data-stu-id="489ad-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="489ad-182">Selecione **Para Documentos do Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="489ad-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="489ad-183">Na caixa de diálogo **Permitir Abertura no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , selecione **Sim** ou **Não**.</span><span class="sxs-lookup"><span data-stu-id="489ad-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="489ad-184">Se clicar em **Sim** , você poderá selecionar o botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation, iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o arquivo do Project da biblioteca de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="489ad-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="489ad-185">Se clicar em **Não** , o link do botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.</span><span class="sxs-lookup"><span data-stu-id="489ad-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="489ad-186">O arquivo do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto específico do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="489ad-187">Publicar seu projeto como modelo</span><span class="sxs-lookup"><span data-stu-id="489ad-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="489ad-188">Você pode salvar seu projeto e reutilizá-lo salvando-o como modelo de projeto no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="489ad-189">Os modelos de projeto são planos de projeto reutilizáveis no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="489ad-190">[Criar um modelo de projeto (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="489ad-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="489ad-191">Na guia **Project Service** , clique em **Publicar** > **Novo Modelo de Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="489ad-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="489ad-192">Na caixa de diálogo **Publicar para um novo projeto no modelo de Project Service** , insira o **Nome de modelo do projeto**.</span><span class="sxs-lookup"><span data-stu-id="489ad-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="489ad-193">Opcionalmente, clique em **Vincular plano de projeto ao Project Service Automation** para vincular o arquivo do Project ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="489ad-194">Clique em **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="489ad-194">Click **Publish**.</span></span>  

<span data-ttu-id="489ad-195">Vincular o arquivo do Project ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] torna o arquivo do Project o mestre e define a estrutura de detalhamento de trabalho no modelo do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="489ad-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="489ad-196">Para fazer alterações no plano de projeto, você precisa fazê-las no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicá-las como atualizações para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="489ad-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="489ad-197">Consulte também</span><span class="sxs-lookup"><span data-stu-id="489ad-197">See Also</span></span>  
 [<span data-ttu-id="489ad-198">Guia do gerente de projeto</span><span class="sxs-lookup"><span data-stu-id="489ad-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)