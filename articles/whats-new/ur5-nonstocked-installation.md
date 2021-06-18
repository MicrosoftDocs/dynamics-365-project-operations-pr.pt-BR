---
title: Atualizar o Project Operations em seu ambiente do Finance
description: Este tópico fornece informações sobre como atualizar o Project Operations no seu ambiente do Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011042"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="f7268-103">Atualizar o Project Operations em seu ambiente do Finance</span><span class="sxs-lookup"><span data-stu-id="f7268-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="f7268-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="f7268-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="f7268-105">Este tópico fornece informações sobre como atualizar o Dynamics 365 Project Operations no seu ambiente do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f7268-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="f7268-106">Existem três procedimentos necessários para atualizar o Project Operations para a Atualização 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="f7268-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="f7268-107">Importar o pacote para o seu projeto de versão preliminar</span><span class="sxs-lookup"><span data-stu-id="f7268-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="f7268-108">Aplicar a atualização</span><span class="sxs-lookup"><span data-stu-id="f7268-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="f7268-109">Atualizar seu ambiente do Dataverse</span><span class="sxs-lookup"><span data-stu-id="f7268-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="f7268-110">Importar o pacote para o seu projeto do LCS</span><span class="sxs-lookup"><span data-stu-id="f7268-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="f7268-111">Entre no [Lifecycle Services (LCS)](https://lcs.dynamics.com/) como proprietário do projeto ou gerente de ambiente.</span><span class="sxs-lookup"><span data-stu-id="f7268-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="f7268-112">Na lista de projetos, selecione seu projeto do LCS.</span><span class="sxs-lookup"><span data-stu-id="f7268-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="f7268-113">Na página **Projeto**, no grupo **Ambientes**, abra o ambiente que deseja atualizar.</span><span class="sxs-lookup"><span data-stu-id="f7268-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="f7268-114">Verifique se o ambiente está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="f7268-114">Verify that the environment is running.</span></span> <span data-ttu-id="f7268-115">Se não tiver sido iniciado, inicie o ambiente.</span><span class="sxs-lookup"><span data-stu-id="f7268-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="f7268-116">Na seção **Nova versão** em **Atualizações disponíveis**, selecione **Ver atualização** para 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="f7268-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Botão Visualizar atualização](media/view-update.png)

6. <span data-ttu-id="f7268-118">Na página **Atualizações de binário**, selecione **Salvar pacote**.</span><span class="sxs-lookup"><span data-stu-id="f7268-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="f7268-119">Na página **Revisar e salvar atualizações**, selecione **Salvar pacote**.</span><span class="sxs-lookup"><span data-stu-id="f7268-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="f7268-120">No painel **Salvar pacote na biblioteca de ativos** que abrir, digite o nome do pacote e selecione **Salvar pacote**.</span><span class="sxs-lookup"><span data-stu-id="f7268-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="f7268-121">Quando o LCS terminar de salvar o pacote, o botão **Concluído** será habilitado.</span><span class="sxs-lookup"><span data-stu-id="f7268-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="f7268-122">Selecione **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="f7268-122">Select **Done**.</span></span> <span data-ttu-id="f7268-123">O LCS irá verificar o pacote.</span><span class="sxs-lookup"><span data-stu-id="f7268-123">LCS will verify the package.</span></span> <span data-ttu-id="f7268-124">A verificação pode levar alguns minutos ou até uma hora.</span><span class="sxs-lookup"><span data-stu-id="f7268-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="f7268-125">Aplicar a atualização de pacote</span><span class="sxs-lookup"><span data-stu-id="f7268-125">Apply the package update</span></span>

1. <span data-ttu-id="f7268-126">No LCS, na página **Detalhes do ambiente**, selecione **Manter** > **Aplicar atualizações**.</span><span class="sxs-lookup"><span data-stu-id="f7268-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="f7268-127">Na lista, selecione o pacote que você salvou anteriormente e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="f7268-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="f7268-128">Selecione **Sim** para confirmar que deseja implantar o pacote.</span><span class="sxs-lookup"><span data-stu-id="f7268-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Confirmar a caixa de diálogo de implantação do pacote](media/confirm-package-deployment.png)

4. <span data-ttu-id="f7268-130">Selecione **Sim** para confirmar que deseja atualizar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7268-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Confirmar a caixa de diálogo de atualização do aplicativo](media/confirm-application-update.png)

<span data-ttu-id="f7268-132">A implantação e atualização do aplicativo serão iniciadas.</span><span class="sxs-lookup"><span data-stu-id="f7268-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="f7268-133">Na página **Detalhes do ambiente**, no canto superior direito, o status do ambiente será atualizado para **Manutenção**.</span><span class="sxs-lookup"><span data-stu-id="f7268-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="f7268-134">Em aproximadamente duas horas, a atualização estará concluída.</span><span class="sxs-lookup"><span data-stu-id="f7268-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="f7268-135">As informações de versão do aplicativo serão atualizadas para **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** e o status do ambiente será atualizado para **Implantado**.</span><span class="sxs-lookup"><span data-stu-id="f7268-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="f7268-136">Atualizar seu ambiente do Dataverse</span><span class="sxs-lookup"><span data-stu-id="f7268-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="f7268-137">Entre no [centro de administração da Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="f7268-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="f7268-138">Na lista, encontre e abra o ambiente que você usou para instalar o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f7268-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="f7268-139">Na página **Ambientes**, selecione **Recurso** > **Aplicativos do Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f7268-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="f7268-140">Na lista, localize **Microsoft Dynamics 365 Project Operations**, e na coluna **Status**, selecione **Atualização disponível**.</span><span class="sxs-lookup"><span data-stu-id="f7268-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="f7268-141">Selecione a caixa de seleção **Eu aceito os termos de serviço**, em seguida, selecione **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="f7268-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="f7268-142">A versão mais recente da solução será instalada.</span><span class="sxs-lookup"><span data-stu-id="f7268-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="f7268-143">Após a conclusão da instalação, você terá a versão 4.5.0.134 instalada.</span><span class="sxs-lookup"><span data-stu-id="f7268-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="f7268-144">Configurar novos recursos</span><span class="sxs-lookup"><span data-stu-id="f7268-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="f7268-145">Habilitar mapeamento de gravação dupla</span><span class="sxs-lookup"><span data-stu-id="f7268-145">Enable dual-write mapping</span></span>

<span data-ttu-id="f7268-146">Depois de concluir a atualização nos ambientes do Finance e Dataverse, você pode ativar os mapeamentos de gravação dupla necessários.</span><span class="sxs-lookup"><span data-stu-id="f7268-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="f7268-147">Conclua os seguintes procedimentos para habilitar mapeamentos de gravação dupla.</span><span class="sxs-lookup"><span data-stu-id="f7268-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="f7268-148">Atualizar as configurações de segurança no ambiente do Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="f7268-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="f7268-149">Atualizar entidades de dados</span><span class="sxs-lookup"><span data-stu-id="f7268-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="f7268-150">Atualizar e executar os mapeamentos de gravação dupla</span><span class="sxs-lookup"><span data-stu-id="f7268-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="f7268-151">Atualizar as configurações de segurança no ambiente do Dataverse</span><span class="sxs-lookup"><span data-stu-id="f7268-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="f7268-152">As seguintes atualizações para os privilégios de segurança para entidades são necessárias como parte da atualização para UR5.</span><span class="sxs-lookup"><span data-stu-id="f7268-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="f7268-153">No seu ambiente do Dataverse, vá para **Configurações** e no grupo **Sistema**, selecione **Segurança**.</span><span class="sxs-lookup"><span data-stu-id="f7268-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Configurações do ambiente do Dataverse](media/Picture21.png)

2. <span data-ttu-id="f7268-155">Selecione **Direitos de Acesso**.</span><span class="sxs-lookup"><span data-stu-id="f7268-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="f7268-156">Na lista de direitos, selecione **usuário de aplicativo de gravação dupla** e selecione a guia **Entidades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="f7268-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="f7268-157">Verifique se o direito tem permissões para **Ler** e **Anexar a** para:</span><span class="sxs-lookup"><span data-stu-id="f7268-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="f7268-158">**Tipo da taxa de câmbio de moeda**</span><span class="sxs-lookup"><span data-stu-id="f7268-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="f7268-159">**Tabela de contas**</span><span class="sxs-lookup"><span data-stu-id="f7268-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="f7268-160">**Calendário fiscal**</span><span class="sxs-lookup"><span data-stu-id="f7268-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="f7268-161">**Razão**</span><span class="sxs-lookup"><span data-stu-id="f7268-161">**Ledger**</span></span>

5. <span data-ttu-id="f7268-162">Depois que o direito de acesso for atualizado, vá para **Configurações** > **Segurança** > **Equipes**.</span><span class="sxs-lookup"><span data-stu-id="f7268-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="f7268-163">Verifique se a função **usuário de aplicativo de gravação dupla** foi aplicada à equipe.</span><span class="sxs-lookup"><span data-stu-id="f7268-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="f7268-164">Atualizar entidades de dados com base na atualização</span><span class="sxs-lookup"><span data-stu-id="f7268-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="f7268-165">Em seu ambiente do Finance, abra o espaço de trabalho **Gerenciamento de dados** e, em seguida, abra a página **Parâmetros da estrutura**.</span><span class="sxs-lookup"><span data-stu-id="f7268-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="f7268-166">Na guia **Configurações de entidade**, selecione **Atualizar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="f7268-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="f7268-167">Selecione **Fechar** para confirmar a atualização da entidade.</span><span class="sxs-lookup"><span data-stu-id="f7268-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="f7268-168">Esse processo levará aproximadamente 20 minutos para ser concluído.</span><span class="sxs-lookup"><span data-stu-id="f7268-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="f7268-169">Você será notificado quando a atualização for concluída.</span><span class="sxs-lookup"><span data-stu-id="f7268-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="f7268-170">Atualizar mapeamentos de gravação dupla</span><span class="sxs-lookup"><span data-stu-id="f7268-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="f7268-171">No espaço de trabalho **Gerenciamento de dados**, selecione **Gravação dupla**.</span><span class="sxs-lookup"><span data-stu-id="f7268-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="f7268-172">Selecione **Aplicar soluções**, selecione ambas as soluções na lista e, em seguida, selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="f7268-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="f7268-173">Na página **Gravação dupla**, selecione os seguintes mapas de tabela e, em seguida, selecione **Parar**.</span><span class="sxs-lookup"><span data-stu-id="f7268-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="f7268-174">**Valores reais da integração do Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="f7268-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="f7268-175">**Categorias de despesas do projeto de integração do Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="f7268-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="f7268-176">**Entidade de exportação de despesas do projeto dados reais de integração do Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="f7268-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="f7268-177">Na página **Versão do mapa de tabela**, aplique uma nova versão do mapa a cada uma das três entidades.</span><span class="sxs-lookup"><span data-stu-id="f7268-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="f7268-178">Na página **Gravação dupla**, selecione executar para reiniciar os mapas.</span><span class="sxs-lookup"><span data-stu-id="f7268-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="f7268-179">Na lista de mapas, selecione o mapa **Razão (msdyn_ledgers)** com todos os pré-requisitos e marque a caixa de seleção **Sincronização inicial**.</span><span class="sxs-lookup"><span data-stu-id="f7268-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="f7268-180">No campo **Mestre para sincronização inicial**, selecione **Aplicativos Finance and Operations** e então selecione **Executar**.</span><span class="sxs-lookup"><span data-stu-id="f7268-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sincronização de mapa de razão](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]