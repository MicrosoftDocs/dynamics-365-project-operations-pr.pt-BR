---
title: Integração com o Microsoft Project Client
description: O planejamento e a manutenção da agenda de um projeto podem ser complexos; portanto, os gerentes de projeto precisam usar ferramentas que os ajudem a gerenciar essa tarefa. A integração com o Microsoft Project Client fornece suporte para abrir e gerenciar uma estrutura de detalhamento de trabalho do projeto.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289310"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="9c769-104">Integração com o Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9c769-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c769-105">O planejamento e a manutenção da agenda de um projeto podem ser complexos; portanto, os gerentes de projeto precisam usar ferramentas que os ajudem a gerenciar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="9c769-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="9c769-106">A integração com o Microsoft Project Client fornece suporte para abrir e gerenciar uma estrutura de detalhamento de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="9c769-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="9c769-107">O gerente de projeto pode publicar quaisquer alterações de volta na estrutura de detalhamento de trabalho do projeto do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9c769-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="9c769-108">Se estiver usando a atualização de julho (versão 10.0.4), você deverá instalar o KB 4054797 e 4055884.</span><span class="sxs-lookup"><span data-stu-id="9c769-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="9c769-109">Configurar o suplemento do Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9c769-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="9c769-110">Para habilitar a integração com o Microsoft Project Client, um suplemento do Microsoft Dynamics 365 deverá ser instalado no aplicativo cliente do Microsoft Project do usuário.</span><span class="sxs-lookup"><span data-stu-id="9c769-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="9c769-111">Isso é feito abrindo o **Espaço de trabalho de gerenciamento de projetos**.</span><span class="sxs-lookup"><span data-stu-id="9c769-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="9c769-112">•   Clique em **Configurar o suplemento de cliente do projeto** na seção **Links** > **Configuração** do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9c769-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="9c769-113">•   Clique em **Abrir** e, em seguida, em **Executar** quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="9c769-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="9c769-114">Abrir e editar um rascunho existente da estrutura de detalhamento de trabalho no Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9c769-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="9c769-115">Se um projeto no Dynamics 365 Finance já tiver uma estrutura de detalhamento de trabalho criada, ela poderá ser aberta no aplicativo Microsoft Project Client, caso esteja no status de rascunho.</span><span class="sxs-lookup"><span data-stu-id="9c769-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="9c769-116">Para abrir na página **Projeto**, clique no link **Abrir no Microsoft Project** na guia **Planejar**. Essa página também pode ser aberta no aplicativo Microsoft Project Client clicando em **Abrir** na guia **Microsoft Dynamics 365**. Selecione **Entidade legal** e **Projeto** na lista.</span><span class="sxs-lookup"><span data-stu-id="9c769-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="9c769-117">Se você estiver usando o Internet Explorer como navegador, precisará clicar em **Salvar** para abrir manualmente a partir do local em que o arquivo foi baixado.</span><span class="sxs-lookup"><span data-stu-id="9c769-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="9c769-118">Ou clique em **Salvar e abrir** para abrir o arquivo no Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9c769-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="9c769-119">Não mude o nome do arquivo ao salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="9c769-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="9c769-120">Antes de fazer qualquer edição no arquivo usando o Microsoft Project Client, você precisa fazer o check-out dele. Clique em **Check-out** na guia **Microsoft Dynamics 365**. Isso impedirá que outros usuários editem ao mesmo tempo a estrutura de detalhamento de trabalho no Finance.</span><span class="sxs-lookup"><span data-stu-id="9c769-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="9c769-121">Para publicar a estrutura de detalhamento de trabalho após concluir as edições, clique em **Check-in** na guia **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9c769-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="9c769-122">Se uma equipe de projeto já tiver sido adicionada ao projeto no Finance, a lista de recursos será preenchida com os membros da equipe.</span><span class="sxs-lookup"><span data-stu-id="9c769-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="9c769-123">Se uma equipe de projeto ainda não tiver sido adicionada ao projeto, você poderá selecionar recursos e criar a equipe dentro do Microsoft Project Client clicando no botão **Recursos** na guia **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9c769-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="9c769-124">Os dados a seguir serão sincronizados de volta com o Finance como parte do processo de check-in:</span><span class="sxs-lookup"><span data-stu-id="9c769-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="9c769-125">•   Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="9c769-125">•   Task name</span></span>

<span data-ttu-id="9c769-126">•   Data de início</span><span class="sxs-lookup"><span data-stu-id="9c769-126">•   Start date</span></span>

<span data-ttu-id="9c769-127">•   Data de término</span><span class="sxs-lookup"><span data-stu-id="9c769-127">•   Finish date</span></span>

<span data-ttu-id="9c769-128">•   Antecessores</span><span class="sxs-lookup"><span data-stu-id="9c769-128">•   Predecessors</span></span>

<span data-ttu-id="9c769-129">•   Nomes dos recursos</span><span class="sxs-lookup"><span data-stu-id="9c769-129">•   Resource names</span></span>

<span data-ttu-id="9c769-130">•   Categoria</span><span class="sxs-lookup"><span data-stu-id="9c769-130">•   Category</span></span>

<span data-ttu-id="9c769-131">•   Categoria do recurso</span><span class="sxs-lookup"><span data-stu-id="9c769-131">•   Resource category</span></span>

<span data-ttu-id="9c769-132">•   Horas de trabalho</span><span class="sxs-lookup"><span data-stu-id="9c769-132">•   Work hours</span></span>

<span data-ttu-id="9c769-133">•   Observações</span><span class="sxs-lookup"><span data-stu-id="9c769-133">•   Notes</span></span>

<span data-ttu-id="9c769-134">•   Prioridade</span><span class="sxs-lookup"><span data-stu-id="9c769-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="9c769-135">Se você adicionar quaisquer outras colunas ao arquivo do Microsoft Project Client, elas não serão salvas no arquivo e não serão exibidas quando o arquivo for aberto novamente.</span><span class="sxs-lookup"><span data-stu-id="9c769-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="9c769-136">Criar a estrutura de detalhamento de trabalho para um projeto existente usando o Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9c769-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="9c769-137">Siga estas etapas para criar uma nova estrutura de detalhamento de trabalho usando o Microsoft Project Client:</span><span class="sxs-lookup"><span data-stu-id="9c769-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="9c769-138">Abra o Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9c769-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9c769-139">Na guia **Microsoft Dynamics 365**, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="9c769-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="9c769-140">Selecione a **Entidade legal** para o projeto.</span><span class="sxs-lookup"><span data-stu-id="9c769-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="9c769-141">Selecione o **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c769-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="9c769-142">Clique em **Check-out** na guia **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9c769-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="9c769-143">Quando estiver pronto para publicar no Finance, clique em **Check-in** na guia **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9c769-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="9c769-144">Substituir a estrutura de detalhamento de trabalho existente de um projeto existente usando o Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9c769-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="9c769-145">Para criar uma nova estrutura de detalhamento de trabalho usando o Microsoft Project Client e substituir uma estrutura existente para um projeto existente, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9c769-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="9c769-146">Abra o Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9c769-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9c769-147">Crie a agenda no Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9c769-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="9c769-148">Na guia **Microsoft Dynamics 365**, clique em **Salvar alterações** > **Substituir projeto existente**.</span><span class="sxs-lookup"><span data-stu-id="9c769-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="9c769-149">Selecione a **Entidade legal** para o projeto.</span><span class="sxs-lookup"><span data-stu-id="9c769-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="9c769-150">Selecione o **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c769-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="9c769-151">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c769-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="9c769-152">Criar um novo projeto de dentro do Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9c769-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="9c769-153">Abra o Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9c769-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9c769-154">Crie a agenda no Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9c769-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="9c769-155">Na guia **Microsoft Dynamics 365**, clique em **Salvar alterações** > **Salvar em novo projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c769-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="9c769-156">Selecione a **Entidade legal** para o projeto.</span><span class="sxs-lookup"><span data-stu-id="9c769-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="9c769-157">Insira a **ID do projeto**, se necessário.</span><span class="sxs-lookup"><span data-stu-id="9c769-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="9c769-158">Informe o **Nome do projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c769-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="9c769-159">Selecione o **Tipo de projeto**, o **Grupo do projeto** e a **ID do contrato de projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c769-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="9c769-160">Também é possível criar um novo contrato de projeto clicando em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="9c769-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="9c769-161">Selecione o **Calendário** a ser usado para obter recursos.</span><span class="sxs-lookup"><span data-stu-id="9c769-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="9c769-162">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c769-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]