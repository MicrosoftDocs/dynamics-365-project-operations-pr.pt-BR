---
title: Espaço de trabalho móvel de entrada de hora de projeto
description: Esse tópico fornece informações sobre o espaço de trabalho móvel da entrada de hora de projeto. Este espaço de trabalho permite que os usuários entrem e economizem tempo em um projeto usando seu dispositivo móvel.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eae471cf42f02e64844a4682cc8ed02cbb14c34
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288860"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="599ee-104">Espaço de trabalho móvel de entrada de hora de projeto</span><span class="sxs-lookup"><span data-stu-id="599ee-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="599ee-105">Esse tópico fornece informações sobre o espaço de trabalho móvel da **entrada de hora de projeto**.</span><span class="sxs-lookup"><span data-stu-id="599ee-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="599ee-106">Este espaço de trabalho permite que os usuários entrem e economizem tempo em um projeto usando seu dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="599ee-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="599ee-107">Esse espaço de trabalho móvel deve ser usado com o aplicativo móvel Dynamics 365 Unified Ops.</span><span class="sxs-lookup"><span data-stu-id="599ee-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="599ee-108">Visão Geral</span><span class="sxs-lookup"><span data-stu-id="599ee-108">Overview</span></span>
<span data-ttu-id="599ee-109">Como parte de seu trabalho diário, os recursos do projeto costumam estar no local ou em viagem.</span><span class="sxs-lookup"><span data-stu-id="599ee-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="599ee-110">O espaço de trabalho móvel **Entrada de tempo do projeto** permite que os usuários insiram seu tempo faturável ou não faturável em um projeto no dispositivo móvel de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="599ee-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="599ee-111">Portanto, os recursos do projeto podem registrar entradas de tempo a qualquer hora e em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="599ee-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="599ee-112">Eles também podem ver as entradas de tempo que já foram registradas.</span><span class="sxs-lookup"><span data-stu-id="599ee-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="599ee-113">Especificamente, no espaço de trabalho móvel **Entrada de tempo do projeto**, os usuários podem executar estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="599ee-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="599ee-114">Para qualquer data selecionada, insira o número de horas que você gastou em uma tarefa específica.</span><span class="sxs-lookup"><span data-stu-id="599ee-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="599ee-115">Pesquise por nome do projeto ou cliente para encontrar o projeto para o qual inserir o tempo.</span><span class="sxs-lookup"><span data-stu-id="599ee-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="599ee-116">Especifique a categoria e atividade para o tempo que você gastou.</span><span class="sxs-lookup"><span data-stu-id="599ee-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="599ee-117">Registre o tempo como faturável ou não faturável para o projeto.</span><span class="sxs-lookup"><span data-stu-id="599ee-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="599ee-118">Opcionalmente, insira qualquer comentário externo ou interno.</span><span class="sxs-lookup"><span data-stu-id="599ee-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="599ee-119">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="599ee-119">Prerequisites</span></span>
<span data-ttu-id="599ee-120">Os pré-requisitos diferem, com base na versão do Microsoft Dynamics 365 que foi implantado para sua organização.</span><span class="sxs-lookup"><span data-stu-id="599ee-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="599ee-121">Pré-requisitos se você usar Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="599ee-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="599ee-122">Se o Finance foi implantado para sua organização, o administrador do sistema deve publicar o espaço de trabalho móvel **Entrada de tempo do projeto**.</span><span class="sxs-lookup"><span data-stu-id="599ee-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="599ee-123">Para obter instruções, veja [Publicar um espaço de trabalho móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="599ee-123">For instructions, see [Publish a mobile workspace](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="599ee-124">Pré-requisitos se você usar a versão 1611 com atualização de plataforma 3 ou posterior</span><span class="sxs-lookup"><span data-stu-id="599ee-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="599ee-125">Se a versão 1611 com atualização da plataforma 3 ou posterior foi implantada para sua organização, o administrador do sistema deve preencher os seguintes pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="599ee-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="599ee-126">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="599ee-126">Prerequisite</span></span></th>
<th><span data-ttu-id="599ee-127">Função</span><span class="sxs-lookup"><span data-stu-id="599ee-127">Role</span></span></th>
<th><span data-ttu-id="599ee-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="599ee-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="599ee-129">Implemente o KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="599ee-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="599ee-130">Administrador do sistema</span><span class="sxs-lookup"><span data-stu-id="599ee-130">System administrator</span></span></td>
<td><span data-ttu-id="599ee-131">KB 4018050 é uma atualização X++ ou hotfix de metadados que contém o espaço de trabalho móvel <strong>Entrada de tempo do projeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="599ee-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="599ee-132">Para implementar o KB 4018050, o administrador do sistema deve seguir estas etapas.</span><span class="sxs-lookup"><span data-stu-id="599ee-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="599ee-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Baixe o hotfix de metadados de Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="599ee-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="599ee-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instale o hotfix de metadados</a>.</span><span class="sxs-lookup"><span data-stu-id="599ee-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="599ee-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Crie um pacote implantável</a> que contém os modelos <strong>ApplicationSuite</strong> e <strong>ProjectMobile</strong> e, em seguida, carregue o pacote implantável no LCS.</span><span class="sxs-lookup"><span data-stu-id="599ee-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="599ee-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplique o pacote implantável</a>.</span><span class="sxs-lookup"><span data-stu-id="599ee-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="599ee-137">Publicar o Espaço de trabalho móvel de <strong>entrada de hora de projeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="599ee-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="599ee-138">Administrador do sistema</span><span class="sxs-lookup"><span data-stu-id="599ee-138">System administrator</span></span></td>
<td><span data-ttu-id="599ee-139">Consulte <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar um espaço de trabalho móvel</a>.</span><span class="sxs-lookup"><span data-stu-id="599ee-139">See <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="599ee-140">Baixe e instale o aplicativo móvel</span><span class="sxs-lookup"><span data-stu-id="599ee-140">Download and install the mobile app</span></span>

<span data-ttu-id="599ee-141">Baixe e instale o aplicativo móvel Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="599ee-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="599ee-142">Para telefones Android</span><span class="sxs-lookup"><span data-stu-id="599ee-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="599ee-143">Para iPhones</span><span class="sxs-lookup"><span data-stu-id="599ee-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="599ee-144">Entre no aplicativo móvel</span><span class="sxs-lookup"><span data-stu-id="599ee-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="599ee-145">Inicie o aplicativo no dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="599ee-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="599ee-146">Insira o URL do Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="599ee-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="599ee-147">Na primeira vez que você efetuar login, será solicitado seu nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="599ee-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="599ee-148">Insira suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="599ee-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="599ee-149">Depois de fazer login, os espaços de trabalho disponíveis para sua empresa são mostrados.</span><span class="sxs-lookup"><span data-stu-id="599ee-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="599ee-150">Observe que se o administrador do sistema publicar uma nova área de trabalho posteriormente, você terá que atualizar a lista de áreas de trabalho móveis.</span><span class="sxs-lookup"><span data-stu-id="599ee-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="599ee-151">[![Deslizar para atualizar](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="599ee-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="599ee-152">Insira o tempo usando o espaço de trabalho móvel de entrada de tempo do projeto</span><span class="sxs-lookup"><span data-stu-id="599ee-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="599ee-153">No seu dispositivo móvel, selecione o espaço de trabalho **Entrada de tempo do projeto**.</span><span class="sxs-lookup"><span data-stu-id="599ee-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="599ee-154">Selecione **Entrada de hora**.</span><span class="sxs-lookup"><span data-stu-id="599ee-154">Select **Time entry**.</span></span> <span data-ttu-id="599ee-155">As datas do calendário para a semana atual serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="599ee-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="599ee-156">Para uma data selecionada, selecione **Ações** &gt; **Nova entrada**.</span><span class="sxs-lookup"><span data-stu-id="599ee-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="599ee-157">Insira o número de horas para registrar.</span><span class="sxs-lookup"><span data-stu-id="599ee-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="599ee-158">Selecione o projeto para a entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="599ee-158">Select the project for the time entry.</span></span> <span data-ttu-id="599ee-159">Uma lista mostra os projetos que são carregados em seu aplicativo para uso offline.</span><span class="sxs-lookup"><span data-stu-id="599ee-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="599ee-160">Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número.</span><span class="sxs-lookup"><span data-stu-id="599ee-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="599ee-161">Para obter mais informações, consulte [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="599ee-161">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="599ee-162">Se o seu projeto não estiver na lista, selecione **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="599ee-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="599ee-163">Pesquise por nome ou alterne para pesquisar por nome de projeto ou cliente.</span><span class="sxs-lookup"><span data-stu-id="599ee-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="599ee-164">Selecionar uma categoria.</span><span class="sxs-lookup"><span data-stu-id="599ee-164">Select a category.</span></span> <span data-ttu-id="599ee-165">Uma lista mostra as categorias que são carregadas em seu aplicativo para uso offline.</span><span class="sxs-lookup"><span data-stu-id="599ee-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="599ee-166">Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número.</span><span class="sxs-lookup"><span data-stu-id="599ee-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="599ee-167">Para obter mais informações, consulte [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="599ee-167">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="599ee-168">Se a sua categoria não estiver na lista, selecione **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="599ee-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="599ee-169">Pesquise por categoria ou mude para pesquisar por nome de categoria.</span><span class="sxs-lookup"><span data-stu-id="599ee-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="599ee-170">Selecione uma atividade.</span><span class="sxs-lookup"><span data-stu-id="599ee-170">Select an activity.</span></span> <span data-ttu-id="599ee-171">Uma lista mostra as atividades que são carregadas em seu aplicativo para uso offline.</span><span class="sxs-lookup"><span data-stu-id="599ee-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="599ee-172">Por padrão, 50 itens são carregados, mas um desenvolvedor pode alterar esse número.</span><span class="sxs-lookup"><span data-stu-id="599ee-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="599ee-173">Para obter mais informações, consulte [Plataforma móvel](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="599ee-173">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="599ee-174">Se a sua atividade não estiver na lista, selecione **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="599ee-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="599ee-175">Pesquise por número de atividade ou alterne para pesquisar por objetivo.</span><span class="sxs-lookup"><span data-stu-id="599ee-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="599ee-176">Selecione a propriedade de linha.</span><span class="sxs-lookup"><span data-stu-id="599ee-176">Select the line property.</span></span>
12. <span data-ttu-id="599ee-177">Opcional: insira quaisquer comentários externos e internos.</span><span class="sxs-lookup"><span data-stu-id="599ee-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="599ee-178">Escolha **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="599ee-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]