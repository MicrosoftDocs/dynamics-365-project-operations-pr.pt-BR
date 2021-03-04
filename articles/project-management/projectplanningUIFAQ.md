---
title: Solucionar problemas de trabalho na grade de Tarefas
description: Este tópico fornece informações de solução de problemas necessárias ao trabalhar na grade de Tarefas.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031523"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="b837d-103">Solucionar problemas de trabalho na grade de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b837d-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="b837d-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="b837d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b837d-105">Este tópico descreve como corrigir problemas que você pode encontrar ao trabalhar com gerenciamento de custos.</span><span class="sxs-lookup"><span data-stu-id="b837d-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="b837d-106">Ativar cookies</span><span class="sxs-lookup"><span data-stu-id="b837d-106">Enable cookies</span></span>

<span data-ttu-id="b837d-107">O Project Operations exige que os cookies de terceiros sejam habilitados para processar a estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b837d-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="b837d-108">Quando os cookies de terceiros não estão habilitados, em vez de ver as tarefas, você verá uma página em branco ao selecionar a guia **Tarefas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="b837d-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Guia em branco quando os cookies de terceiros não estão habilitados](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="b837d-110">Solução alternativa</span><span class="sxs-lookup"><span data-stu-id="b837d-110">Workaround</span></span>
<span data-ttu-id="b837d-111">Para os navegadores Microsoft Edge ou Google Chrome, os procedimentos a seguir descrevem como atualizar a configuração do seu navegador para habilitar cookies de terceiros.</span><span class="sxs-lookup"><span data-stu-id="b837d-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="b837d-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b837d-112">Microsoft Edge</span></span>

1. <span data-ttu-id="b837d-113">Abra o navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b837d-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="b837d-114">No canto superior direito, selecione as **reticências** (...) e, em seguida, **Configurações**.</span><span class="sxs-lookup"><span data-stu-id="b837d-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="b837d-115">Em **Cookies e permissões de site**, selecione **Cookies e dados do site**.</span><span class="sxs-lookup"><span data-stu-id="b837d-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="b837d-116">Desative **Bloquear cookies de terceiros**.</span><span class="sxs-lookup"><span data-stu-id="b837d-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="b837d-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="b837d-117">Google Chrome</span></span>

1. <span data-ttu-id="b837d-118">Abra o navegador Chrome.</span><span class="sxs-lookup"><span data-stu-id="b837d-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="b837d-119">No canto superior direito, selecione os três pontos verticais e depois selecione **Configurações**.</span><span class="sxs-lookup"><span data-stu-id="b837d-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="b837d-120">Em **Privacidade e segurança**, selecione **Cookies e outros dados do site**.</span><span class="sxs-lookup"><span data-stu-id="b837d-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="b837d-121">Selecione **Permitir todos os cookies**.</span><span class="sxs-lookup"><span data-stu-id="b837d-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b837d-122">Se você bloquear cookies de terceiros, todos os cookies e dados de sites de outros sites serão bloqueados, mesmo se o site for permitido em sua lista de exceções.</span><span class="sxs-lookup"><span data-stu-id="b837d-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="b837d-123">Ponto de Extremidade PEX</span><span class="sxs-lookup"><span data-stu-id="b837d-123">PEX Endpoint</span></span>

<span data-ttu-id="b837d-124">O Project Operations exige que um parâmetro do projeto faça referência ao Ponto de Extremidade PEX.</span><span class="sxs-lookup"><span data-stu-id="b837d-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="b837d-125">Esse ponto de extremidade é necessário para se comunicar com o serviço usado para processar a estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b837d-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="b837d-126">Se o parâmetro não estiver habilitado, você receberá o erro "O parâmetro do projeto não é válido".</span><span class="sxs-lookup"><span data-stu-id="b837d-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="b837d-127">Solução alternativa</span><span class="sxs-lookup"><span data-stu-id="b837d-127">Workaround</span></span>
 ![Campo Ponto de Extremidade PEX no parâmetro do projeto](media/projectparameter.png)

1. <span data-ttu-id="b837d-129">Adicione o campo **Ponto de Extremidade PEX** à página **Parâmetros do projeto**.</span><span class="sxs-lookup"><span data-stu-id="b837d-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="b837d-130">Atualize o campo com o seguinte valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="b837d-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="b837d-131">Remova o campo da página **Parâmetros do projeto**.</span><span class="sxs-lookup"><span data-stu-id="b837d-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="b837d-132">Privilégios para projeto para a Web</span><span class="sxs-lookup"><span data-stu-id="b837d-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="b837d-133">O Project Operations conta com um serviço de agendamento externo.</span><span class="sxs-lookup"><span data-stu-id="b837d-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="b837d-134">O serviço requer que um usuário tenha várias funções atribuídas para ler e gravar em entidades relacionadas à estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b837d-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="b837d-135">Essas entidades incluem tarefas de projeto, atribuições de recursos e dependências de tarefas.</span><span class="sxs-lookup"><span data-stu-id="b837d-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="b837d-136">Se um usuário não puder renderizar a estrutura de detalhamento de trabalho quando for para a guia **Tarefas**, provavelmente é porque o projeto para o Project Operations não foi habilitado.</span><span class="sxs-lookup"><span data-stu-id="b837d-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="b837d-137">Um usuário pode receber um erro de direito de acesso ou um erro relacionado a uma negação de acesso.</span><span class="sxs-lookup"><span data-stu-id="b837d-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="b837d-138">Solução alternativa</span><span class="sxs-lookup"><span data-stu-id="b837d-138">Workaround</span></span>

1. <span data-ttu-id="b837d-139">Vá para **Configurações > Segurança > Usuários > Usuários do Aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="b837d-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Leitor de aplicativo](media/applicationuser.jpg)
   
2. <span data-ttu-id="b837d-141">Clique duas vezes no nome de inscrição para verificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b837d-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="b837d-142">O usuário tem acesso ao projeto:</span><span class="sxs-lookup"><span data-stu-id="b837d-142">The user has access to the project.</span></span> <span data-ttu-id="b837d-143">Essa verificação normalmente é feita garantindo que o usuário tenha o direito de acesso **Gerente de projeto**.</span><span class="sxs-lookup"><span data-stu-id="b837d-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="b837d-144">O usuário do aplicativo Microsoft Project existe e está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="b837d-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="b837d-145">Se este usuário não existir, você poderá criar um novo registro de usuário.</span><span class="sxs-lookup"><span data-stu-id="b837d-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="b837d-146">Selecionar **Novos usuários**.</span><span class="sxs-lookup"><span data-stu-id="b837d-146">Select **New Users**.</span></span> <span data-ttu-id="b837d-147">Altere o formulário de inscrição para **Usuário do aplicativo** e, em seguida, adicione o **ID do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="b837d-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detalhes do usuário de inscrição](media/applicationuserdetails.jpg)

4. <span data-ttu-id="b837d-149">Verifique se o usuário recebeu a licença correta e se o serviço está habilitado nos detalhes dos planos de serviço da licença.</span><span class="sxs-lookup"><span data-stu-id="b837d-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="b837d-150">Verifique se o usuário consegue abrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="b837d-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="b837d-151">Verifique por meio dos parâmetros do projeto se o sistema está apontando para o ponto de extremidade correto do projeto.</span><span class="sxs-lookup"><span data-stu-id="b837d-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="b837d-152">Verifique se o usuário de inscrição do projeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="b837d-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="b837d-153">Aplique os seguintes direitos de acesso ao usuário:</span><span class="sxs-lookup"><span data-stu-id="b837d-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="b837d-154">Usuário do Dataverse</span><span class="sxs-lookup"><span data-stu-id="b837d-154">Dataverse User</span></span>
  - <span data-ttu-id="b837d-155">Sistema do Project Operations</span><span class="sxs-lookup"><span data-stu-id="b837d-155">Project Operations System</span></span>
  - <span data-ttu-id="b837d-156">Sistema do projeto</span><span class="sxs-lookup"><span data-stu-id="b837d-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="b837d-157">Erro ao atualizar a estrutura de detalhamento de trabalho</span><span class="sxs-lookup"><span data-stu-id="b837d-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="b837d-158">Quando uma ou mais atualizações são feitas na estrutura de detalhamento de trabalho, as alterações eventualmente falham e não são salvas.</span><span class="sxs-lookup"><span data-stu-id="b837d-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="b837d-159">Ocorre um erro na grade de agendamento, observando que "Não foi possível salvar as alterações recentes feitas por você."</span><span class="sxs-lookup"><span data-stu-id="b837d-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="b837d-160">Solução alternativa</span><span class="sxs-lookup"><span data-stu-id="b837d-160">Workaround</span></span>

1. <span data-ttu-id="b837d-161">Verifique se o usuário recebeu a licença correta e se o serviço está habilitado nos detalhes dos planos de serviço da licença.</span><span class="sxs-lookup"><span data-stu-id="b837d-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="b837d-162">Verifique se o usuário consegue abrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="b837d-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="b837d-163">Verifique se o sistema está apontando para o ponto de extremidade correto do projeto,.</span><span class="sxs-lookup"><span data-stu-id="b837d-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="b837d-164">Verifique se o usuário de inscrição do projeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="b837d-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="b837d-165">Aplique os seguintes direitos de acesso ao usuário:</span><span class="sxs-lookup"><span data-stu-id="b837d-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="b837d-166">Usuário ou usuário base do Dataverse</span><span class="sxs-lookup"><span data-stu-id="b837d-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="b837d-167">Sistema do Project Operations</span><span class="sxs-lookup"><span data-stu-id="b837d-167">Project Operations System</span></span>
  - <span data-ttu-id="b837d-168">Sistema do projeto</span><span class="sxs-lookup"><span data-stu-id="b837d-168">Project System</span></span>
  - <span data-ttu-id="b837d-169">Sistema de gravação dupla do Project Operations (Esta função é necessária se você estiver implantando o cenário baseado em recursos/sem estoque do Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="b837d-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
