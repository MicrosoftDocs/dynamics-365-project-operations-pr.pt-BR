---
title: Provisionar um novo ambiente
description: Este tópico fornece informações sobre como provisionar um novo ambiente do Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949348"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="a0673-103">Provisionar um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="a0673-103">Provision a new environment</span></span>

<span data-ttu-id="a0673-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="a0673-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a0673-105">Este tópico fornece informações sobre como provisionar um novo ambiente do Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.</span><span class="sxs-lookup"><span data-stu-id="a0673-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="a0673-106">Habilitar o provisionamento automatizado do Project Operations em um projeto do LCS</span><span class="sxs-lookup"><span data-stu-id="a0673-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="a0673-107">Use as etapas a seguir para habilitar o fluxo de provisionamento automatizado do Project Operations para seu projeto do LCS.</span><span class="sxs-lookup"><span data-stu-id="a0673-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="a0673-108">Acesse [LCS](https://lcs.dynamics.com/v2) e selecione o bloco **Gerenciamento versão prévia do recurso**.</span><span class="sxs-lookup"><span data-stu-id="a0673-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="a0673-109">Na lista **Versão prévia do recurso**, selecione **Project Operations** e **Versão prévia do recurso habilitada** para habilitar o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a0673-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="a0673-110">Esta etapa é realizada apenas uma vez por projeto do LCS.</span><span class="sxs-lookup"><span data-stu-id="a0673-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="a0673-111">Provisionar um ambiente do Project Operations</span><span class="sxs-lookup"><span data-stu-id="a0673-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="a0673-112">Abra uma nova implantação de [ambiente de demonstração](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ou [área restrita/ambiente de produção](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a0673-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="a0673-113">Siga o assistente de **Provisionamento de ambiente**.</span><span class="sxs-lookup"><span data-stu-id="a0673-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="a0673-114">Certifique-se de que a versão do aplicativo selecionado seja 10.0.13 ou superior.</span><span class="sxs-lookup"><span data-stu-id="a0673-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="a0673-115">Para provisionar o Project Operations, em **Configurações avançadas**, selecione **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="a0673-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="a0673-116">Habilite a **Configuração do Common Data Service** selecionando **Sim** e insira as informações nos campos obrigatórios:</span><span class="sxs-lookup"><span data-stu-id="a0673-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="a0673-117">Nome</span><span class="sxs-lookup"><span data-stu-id="a0673-117">Name</span></span>
  - <span data-ttu-id="a0673-118">Região</span><span class="sxs-lookup"><span data-stu-id="a0673-118">Region</span></span>
  - <span data-ttu-id="a0673-119">Linguagem</span><span class="sxs-lookup"><span data-stu-id="a0673-119">Language</span></span>
  - <span data-ttu-id="a0673-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="a0673-120">Currency</span></span>
 
5. <span data-ttu-id="a0673-121">No campo **Modelo do Common Data Service**, selecione **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="a0673-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="a0673-122">Selecione o tipo de ambiente para sua implantação.</span><span class="sxs-lookup"><span data-stu-id="a0673-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="a0673-123">Uma avaliação baseada em subscrição permitirá que você implante um ambiente CDS por 30 dias.</span><span class="sxs-lookup"><span data-stu-id="a0673-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configurações da implantação](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="a0673-125">Selecione **Concordo** para aceitar os termos de serviço e, em seguida, **Concluído** para retornar às configurações de implantação.</span><span class="sxs-lookup"><span data-stu-id="a0673-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentimento de Implantação](./media/2DeploymentConsent.png)

7. <span data-ttu-id="a0673-127">Preencha os campos obrigatórios restantes no assistente e confirme a implantação.</span><span class="sxs-lookup"><span data-stu-id="a0673-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="a0673-128">O tempo de provisionamento do ambiente varia de acordo com o tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="a0673-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="a0673-129">O provisionamento pode levar até seis horas.</span><span class="sxs-lookup"><span data-stu-id="a0673-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="a0673-130">Depois que a implantação for concluída com sucesso, o ambiente será exibido como **Implantado**.</span><span class="sxs-lookup"><span data-stu-id="a0673-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="a0673-131">Para confirmar se o ambiente foi implantado com sucesso, selecione **Logon** e faça logon no ambiente para confirmar.</span><span class="sxs-lookup"><span data-stu-id="a0673-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalhes do ambiente do ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="a0673-133">Aplicar no Project Operations os dados de demonstração do Finance (etapa opcional)</span><span class="sxs-lookup"><span data-stu-id="a0673-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="a0673-134">Aplique no Project Operations os dados de demonstração do Finance ao ambiente hospedado na nuvem da versão de serviço 10.0.13, conforme descrito [neste artigo](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="a0673-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="a0673-135">Aplicar atualizações ao ambiente do Finance</span><span class="sxs-lookup"><span data-stu-id="a0673-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="a0673-136">O Project Operations requer um ambiente do Finance com aplicativo versão **10.0.13 (10.0.569.20009)** ou superior.</span><span class="sxs-lookup"><span data-stu-id="a0673-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="a0673-137">Poderá ser necessário aplicar atualizações de qualidade ao seu ambiente do Finance para receber esta versão.</span><span class="sxs-lookup"><span data-stu-id="a0673-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="a0673-138">No LCS, na página **Detalhes do ambiente**, na seção **Atualizações Disponíveis**, selecione **Exibir Atualização**.</span><span class="sxs-lookup"><span data-stu-id="a0673-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Exibir Atualizações](./media/5ViewUpdates.png)

2. <span data-ttu-id="a0673-140">Na página **Atualizações de binário**, selecione **Salvar pacote**.</span><span class="sxs-lookup"><span data-stu-id="a0673-140">On the **Binary updates** page, select **Save package.**</span></span>

![Salvar pacote](./media/6SavePackage.png)

3. <span data-ttu-id="a0673-142">Clique em **Selecionar tudo** e selecione **Salvar pacote**.</span><span class="sxs-lookup"><span data-stu-id="a0673-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar e salvar atualizações](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="a0673-144">Insira um nome e uma descrição do pacote e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="a0673-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="a0673-145">Dependendo da conexão com a Internet, esse processo pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="a0673-145">Depending on the internet connection, this process might take some time.</span></span>

![Carregar pacote para Biblioteca de Ativos](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="a0673-147">Depois que o pacote for salvo, selecione **Concluído** e salve esse pacote na Biblioteca de Ativos em seu projeto do LCS.</span><span class="sxs-lookup"><span data-stu-id="a0673-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="a0673-148">Salvar e validar o pacote pode levar cerca de 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="a0673-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="a0673-149">Para aplicar a atualização, navegue até a página **Detalhes do ambiente** no LCS e selecione **Manter** > **Aplicar atualizações**.</span><span class="sxs-lookup"><span data-stu-id="a0673-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Manter Ambientes](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="a0673-151">Na lista de atualizações, selecione o pacote que você criou e **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="a0673-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar Atualizações](./media/10ApplyUpdates.png)

<span data-ttu-id="a0673-153">A manutenção do ambiente levará algum tempo.</span><span class="sxs-lookup"><span data-stu-id="a0673-153">Environment servicing will take some time.</span></span> <span data-ttu-id="a0673-154">Após a conclusão, o ambiente retornará ao estado implantado.</span><span class="sxs-lookup"><span data-stu-id="a0673-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ambiente Implantado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="a0673-156">Estabelecer uma conexão de Gravação Dupla</span><span class="sxs-lookup"><span data-stu-id="a0673-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="a0673-157">Em seu projeto do LCS, acesse a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="a0673-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="a0673-158">Em **Informações do ambiente do Common Data Service**, selecione **Link para o CDS para aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="a0673-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="a0673-159">Depois que o link for concluído, selecione novamente **Link para o CDS para aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="a0673-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="a0673-160">Você será redirecionado para Gravação Dupla no Finance.</span><span class="sxs-lookup"><span data-stu-id="a0673-160">You will be redirected to Dual Write in Finance.</span></span>

![Link para o CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="a0673-162">Selecione **Aplicar Solução** para acessar as entidades que serão mapeadas na integração.</span><span class="sxs-lookup"><span data-stu-id="a0673-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar Soluções](./media/13ApplySolutions.png)

5. <span data-ttu-id="a0673-164">Selecione ambas as soluções, **Mapa de Entidades de Gravação Dupla do Dynamics 365 Finance and Operations** e **Mapas de Entidades de Gravação Dupla do Dynamics 365 Project Operations** e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="a0673-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar Soluções](./media/14ConfirmSolutions.png)

<span data-ttu-id="a0673-166">Depois que as soluções forem aplicadas, as entidades de Gravação Dupla serão aplicadas ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="a0673-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicar Soluções](./media/15ApplyingSolutions.png)

<span data-ttu-id="a0673-168">Depois que as entidades forem aplicadas, todos os mapeamentos disponíveis serão listados no ambiente.</span><span class="sxs-lookup"><span data-stu-id="a0673-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapas de Gravação Dupla](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="a0673-170">Atualizar as entidades de dados após a atualização</span><span class="sxs-lookup"><span data-stu-id="a0673-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="a0673-171">No Finance, acesse o espaço de trabalho de **Gerenciamento de dados**.</span><span class="sxs-lookup"><span data-stu-id="a0673-171">In Finance, go to the **Data management** workspace.</span></span>

![Espaço de trabalho de Gerenciamento de Dados](./media/16DataManagement.png)

2. <span data-ttu-id="a0673-173">Selecione o bloco **Parâmetros da estrutura**.</span><span class="sxs-lookup"><span data-stu-id="a0673-173">Select the **Framework parameters** tile.</span></span>

![Parâmetros da Estrutura](./media/17FrameworkParameters.png)

3. <span data-ttu-id="a0673-175">Na página **Configurações de entidade**, selecione **Atualizar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="a0673-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Atualizar Lista de Entidades](./media/18RefreshEntityList.png)

<span data-ttu-id="a0673-177">A atualização levará aproximadamente 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="a0673-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="a0673-178">Você receberá um alerta quando ela for concluída.</span><span class="sxs-lookup"><span data-stu-id="a0673-178">You will receive an alert when it is complete.</span></span>

![Atualizar Confirmação](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="a0673-180">Executar Mapas de Gravação Dupla do Project Operations</span><span class="sxs-lookup"><span data-stu-id="a0673-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="a0673-181">Em seu projeto do LCS, acesse a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="a0673-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="a0673-182">Em **Informações do ambiente do Common Data Service**, selecione **Link para o CDS para aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="a0673-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="a0673-183">Depois de selecionar o link, você será redirecionado para a lista de entidades nos mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="a0673-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="a0673-184">Inicie os mapas conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a0673-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="a0673-185">Certifique-se de seguir a sequência listada.</span><span class="sxs-lookup"><span data-stu-id="a0673-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="a0673-186">**Mapa de Entidade**</span><span class="sxs-lookup"><span data-stu-id="a0673-186">**Entity Map**</span></span> | <span data-ttu-id="a0673-187">**Atualizar entidade**</span><span class="sxs-lookup"><span data-stu-id="a0673-187">**Refresh entity**</span></span> | <span data-ttu-id="a0673-188">**Sincronização inicial**</span><span class="sxs-lookup"><span data-stu-id="a0673-188">**Initial sync**</span></span> | <span data-ttu-id="a0673-189">**Mestre para sincronização inicial**</span><span class="sxs-lookup"><span data-stu-id="a0673-189">**Master for initial sync**</span></span> | <span data-ttu-id="a0673-190">**Executar pré-requisitos**</span><span class="sxs-lookup"><span data-stu-id="a0673-190">**Run prerequisites**</span></span> | <span data-ttu-id="a0673-191">**Sincronização inicial dos pré-requisitos**</span><span class="sxs-lookup"><span data-stu-id="a0673-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="a0673-192">**Funções de Recursos do Projeto para Todas as Empresas (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="a0673-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="a0673-193">No</span><span class="sxs-lookup"><span data-stu-id="a0673-193">No</span></span> | <span data-ttu-id="a0673-194">Sim</span><span class="sxs-lookup"><span data-stu-id="a0673-194">Yes</span></span> | <span data-ttu-id="a0673-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a0673-195">Common Data Service</span></span> | <span data-ttu-id="a0673-196">No</span><span class="sxs-lookup"><span data-stu-id="a0673-196">No</span></span> | <span data-ttu-id="a0673-197">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-197">N\A</span></span> |
| <span data-ttu-id="a0673-198">**Entidades legais (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="a0673-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="a0673-199">No</span><span class="sxs-lookup"><span data-stu-id="a0673-199">No</span></span> | <span data-ttu-id="a0673-200">Sim</span><span class="sxs-lookup"><span data-stu-id="a0673-200">Yes</span></span> | <span data-ttu-id="a0673-201">Aplicativos do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0673-201">Finance and Operations apps</span></span> | <span data-ttu-id="a0673-202">No</span><span class="sxs-lookup"><span data-stu-id="a0673-202">No</span></span> | <span data-ttu-id="a0673-203">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-203">N\A</span></span> |
| <span data-ttu-id="a0673-204">**Valores reais da integração do Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="a0673-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="a0673-205">No</span><span class="sxs-lookup"><span data-stu-id="a0673-205">No</span></span> | <span data-ttu-id="a0673-206">No</span><span class="sxs-lookup"><span data-stu-id="a0673-206">No</span></span> | <span data-ttu-id="a0673-207">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-207">N\A</span></span> | <span data-ttu-id="a0673-208">Sim</span><span class="sxs-lookup"><span data-stu-id="a0673-208">Yes</span></span> | <span data-ttu-id="a0673-209">No</span><span class="sxs-lookup"><span data-stu-id="a0673-209">No</span></span> |
| <span data-ttu-id="a0673-210">**Linhas de contrato do projeto (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="a0673-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="a0673-211">No</span><span class="sxs-lookup"><span data-stu-id="a0673-211">No</span></span> | <span data-ttu-id="a0673-212">No</span><span class="sxs-lookup"><span data-stu-id="a0673-212">No</span></span> | <span data-ttu-id="a0673-213">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-213">N\A</span></span> | <span data-ttu-id="a0673-214">No</span><span class="sxs-lookup"><span data-stu-id="a0673-214">No</span></span> | <span data-ttu-id="a0673-215">No</span><span class="sxs-lookup"><span data-stu-id="a0673-215">No</span></span> |
| <span data-ttu-id="a0673-216">**Entidade de integração para relacionamentos de transações do projeto (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="a0673-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="a0673-217">No</span><span class="sxs-lookup"><span data-stu-id="a0673-217">No</span></span> | <span data-ttu-id="a0673-218">No</span><span class="sxs-lookup"><span data-stu-id="a0673-218">No</span></span> | <span data-ttu-id="a0673-219">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-219">N\A</span></span> | <span data-ttu-id="a0673-220">No</span><span class="sxs-lookup"><span data-stu-id="a0673-220">No</span></span> | <span data-ttu-id="a0673-221">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-221">N\A</span></span> |
| <span data-ttu-id="a0673-222">**Marcos da linha do contrato de integração do Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="a0673-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="a0673-223">No</span><span class="sxs-lookup"><span data-stu-id="a0673-223">No</span></span> | <span data-ttu-id="a0673-224">No</span><span class="sxs-lookup"><span data-stu-id="a0673-224">No</span></span> | <span data-ttu-id="a0673-225">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-225">N\A</span></span> | <span data-ttu-id="a0673-226">No</span><span class="sxs-lookup"><span data-stu-id="a0673-226">No</span></span> | <span data-ttu-id="a0673-227">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-227">N\A</span></span> |
| <span data-ttu-id="a0673-228">**Entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="a0673-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="a0673-229">No</span><span class="sxs-lookup"><span data-stu-id="a0673-229">No</span></span> | <span data-ttu-id="a0673-230">No</span><span class="sxs-lookup"><span data-stu-id="a0673-230">No</span></span> | <span data-ttu-id="a0673-231">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-231">N\A</span></span> | <span data-ttu-id="a0673-232">No</span><span class="sxs-lookup"><span data-stu-id="a0673-232">No</span></span> | <span data-ttu-id="a0673-233">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-233">N\A</span></span> |
| <span data-ttu-id="a0673-234">**Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="a0673-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="a0673-235">No</span><span class="sxs-lookup"><span data-stu-id="a0673-235">No</span></span> | <span data-ttu-id="a0673-236">No</span><span class="sxs-lookup"><span data-stu-id="a0673-236">No</span></span> | <span data-ttu-id="a0673-237">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-237">N\A</span></span> | <span data-ttu-id="a0673-238">No</span><span class="sxs-lookup"><span data-stu-id="a0673-238">No</span></span> | <span data-ttu-id="a0673-239">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-239">N\A</span></span> |
| <span data-ttu-id="a0673-240">**Entidade de exportação de despesas do projeto de integração do Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="a0673-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="a0673-241">Sim</span><span class="sxs-lookup"><span data-stu-id="a0673-241">Yes</span></span> | <span data-ttu-id="a0673-242">No</span><span class="sxs-lookup"><span data-stu-id="a0673-242">No</span></span> | <span data-ttu-id="a0673-243">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-243">N\A</span></span> | <span data-ttu-id="a0673-244">No</span><span class="sxs-lookup"><span data-stu-id="a0673-244">No</span></span> | <span data-ttu-id="a0673-245">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-245">N\A</span></span> |
| <span data-ttu-id="a0673-246">**Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="a0673-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="a0673-247">Sim</span><span class="sxs-lookup"><span data-stu-id="a0673-247">Yes</span></span> | <span data-ttu-id="a0673-248">No</span><span class="sxs-lookup"><span data-stu-id="a0673-248">No</span></span> | <span data-ttu-id="a0673-249">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-249">N\A</span></span> | <span data-ttu-id="a0673-250">No</span><span class="sxs-lookup"><span data-stu-id="a0673-250">No</span></span> | <span data-ttu-id="a0673-251">N/A</span><span class="sxs-lookup"><span data-stu-id="a0673-251">N\A</span></span> |

4. <span data-ttu-id="a0673-252">Para atualizar a entidade, selecione o nome do mapa e, em seguida, **Atualizar entidades**.</span><span class="sxs-lookup"><span data-stu-id="a0673-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="a0673-253">Continue executando o mapa depois que a atualização for concluída.</span><span class="sxs-lookup"><span data-stu-id="a0673-253">Proceed with running the map after the refresh is complete.</span></span>

![Atualizar Mapa](./media/20RefreshMapping.png)

<span data-ttu-id="a0673-255">Antes de habilitar o próximo mapa, verifique se o mapa na tabela está em um estado **Em Execução**.</span><span class="sxs-lookup"><span data-stu-id="a0673-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="a0673-256">Executar mapas com um número maior de pré-requisitos pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="a0673-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="a0673-257">Para executar um mapa com pré-requisitos, habilite o botão de alternância **Exibir mapas de entidades relacionadas**.</span><span class="sxs-lookup"><span data-stu-id="a0673-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="a0673-258">Se a tabela indicar que **Sincronização inicial do pré-requisito** é **Não**, verifique se o indicador **Sincronização inicial** é **Desativado** em todos os mapas de pré-requisitos antes de executá-lo.</span><span class="sxs-lookup"><span data-stu-id="a0673-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Executar Mapa](./media/21RunMap.png)

6. <span data-ttu-id="a0673-260">Verifique se todos os mapas relacionados ao projeto estão no estado em execução.</span><span class="sxs-lookup"><span data-stu-id="a0673-260">Validate all project related maps are in the running state.</span></span>

![Todos os Mapas em Execução](./media/22AllMapsRunning.png)

<span data-ttu-id="a0673-262">Seu ambiente do Project Operations agora está provisionado e configurado.</span><span class="sxs-lookup"><span data-stu-id="a0673-262">Your Project Operations environment is now provisioned and configured.</span></span>
