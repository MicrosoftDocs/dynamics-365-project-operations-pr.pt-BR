---
title: Provisionar um novo ambiente
description: Este tópico fornece informações sobre como provisionar um novo ambiente do Project Operations.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995472"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="89cfd-103">Provisionar um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="89cfd-103">Provision a new environment</span></span>

<span data-ttu-id="89cfd-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="89cfd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="89cfd-105">Este tópico fornece informações sobre como provisionar um novo ambiente do Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.</span><span class="sxs-lookup"><span data-stu-id="89cfd-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="89cfd-106">Habilitar o provisionamento automatizado do Project Operations em um projeto do LCS</span><span class="sxs-lookup"><span data-stu-id="89cfd-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="89cfd-107">Use as etapas a seguir para habilitar o fluxo de provisionamento automatizado do Project Operations para seu projeto do LCS.</span><span class="sxs-lookup"><span data-stu-id="89cfd-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="89cfd-108">Acesse [LCS](https://lcs.dynamics.com/v2) e selecione o bloco **Gerenciamento versão prévia do recurso**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="89cfd-109">Na lista **Versão prévia do recurso**, selecione o **Recurso Project Operations** e **Versão prévia do recurso habilitada** para habilitar o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="89cfd-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="89cfd-110">Esta etapa é realizada apenas uma vez por projeto do LCS.</span><span class="sxs-lookup"><span data-stu-id="89cfd-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="89cfd-111">Provisionar um ambiente do Project Operations</span><span class="sxs-lookup"><span data-stu-id="89cfd-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="89cfd-112">Abra uma nova implantação de [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ou [área restrita/ambiente de produção](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="89cfd-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="89cfd-113">Siga o assistente de **Provisionamento de ambiente**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="89cfd-114">Certifique-se de que a versão do aplicativo selecionado seja 10.0.13 ou superior.</span><span class="sxs-lookup"><span data-stu-id="89cfd-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="89cfd-115">Para provisionar o Project Operations, em **Configurações avançadas**, selecione **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="89cfd-116">Habilite a **Configuração do Common Data Service** selecionando **Sim** e insira as informações nos campos obrigatórios:</span><span class="sxs-lookup"><span data-stu-id="89cfd-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="89cfd-117">Nome</span><span class="sxs-lookup"><span data-stu-id="89cfd-117">Name</span></span>
  - <span data-ttu-id="89cfd-118">Região</span><span class="sxs-lookup"><span data-stu-id="89cfd-118">Region</span></span>
  - <span data-ttu-id="89cfd-119">Linguagem</span><span class="sxs-lookup"><span data-stu-id="89cfd-119">Language</span></span>
  - <span data-ttu-id="89cfd-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="89cfd-120">Currency</span></span>
 
5. <span data-ttu-id="89cfd-121">No campo **Modelo do Common Data Service**, selecione **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="89cfd-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="89cfd-122">Selecione o tipo de ambiente para sua implantação.</span><span class="sxs-lookup"><span data-stu-id="89cfd-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="89cfd-123">Uma avaliação baseada em subscrição permitirá que você implante um ambiente CDS por 30 dias.</span><span class="sxs-lookup"><span data-stu-id="89cfd-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configurações da implantação](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="89cfd-125">Selecione **Concordo** para aceitar os termos de serviço e, em seguida, **Concluído** para retornar às configurações de implantação.</span><span class="sxs-lookup"><span data-stu-id="89cfd-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentimento de Implantação](./media/2DeploymentConsent.png)

7. <span data-ttu-id="89cfd-127">Opcional - Aplique dados de demonstração ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="89cfd-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="89cfd-128">Vá para **Configurações avançadas**, selecione **Personalizar a configuração do banco de dados SQL** e defina **Especificar um conjunto de dados para o banco de dados do aplicativo** como **Demonstração**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="89cfd-129">Preencha os campos obrigatórios restantes no assistente e confirme a implantação.</span><span class="sxs-lookup"><span data-stu-id="89cfd-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="89cfd-130">O tempo para provisionar o ambiente varia de acordo com o tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="89cfd-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="89cfd-131">O provisionamento pode levar até seis horas.</span><span class="sxs-lookup"><span data-stu-id="89cfd-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="89cfd-132">Depois que a implantação for concluída com sucesso, o ambiente será exibido como **Implantado**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="89cfd-133">Para confirmar que o ambiente foi implantado com sucesso, selecione **Entrar** e faça login no ambiente para confirmar.</span><span class="sxs-lookup"><span data-stu-id="89cfd-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalhes do ambiente do ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="89cfd-135">Aplicar atualizações ao ambiente do Finance</span><span class="sxs-lookup"><span data-stu-id="89cfd-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="89cfd-136">O Project Operations requer um ambiente do Finance com aplicativo versão **10.0.13 (10.0.569.20009)** ou superior.</span><span class="sxs-lookup"><span data-stu-id="89cfd-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="89cfd-137">Poderá ser necessário aplicar atualizações de qualidade ao seu ambiente do Finance para receber esta versão.</span><span class="sxs-lookup"><span data-stu-id="89cfd-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="89cfd-138">No LCS, na página **Detalhes do ambiente**, na seção **Atualizações Disponíveis**, selecione **Exibir Atualização**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Exibir Atualizações](./media/5ViewUpdates.png)

2. <span data-ttu-id="89cfd-140">Na página **Atualizações de binário**, selecione **Salvar pacote**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-140">On the **Binary updates** page, select **Save package.**</span></span>

![Salvar pacote](./media/6SavePackage.png)

3. <span data-ttu-id="89cfd-142">Clique em **Selecionar tudo** e selecione **Salvar pacote**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar e salvar atualizações](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="89cfd-144">Insira um nome e uma descrição do pacote e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="89cfd-145">Dependendo da conexão com a Internet, esse processo pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="89cfd-145">Depending on the internet connection, this process might take some time.</span></span>

![Carregar pacote para Biblioteca de Ativos](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="89cfd-147">Depois que o pacote for salvo, selecione **Concluído** e salve esse pacote na Biblioteca de Ativos em seu projeto do LCS.</span><span class="sxs-lookup"><span data-stu-id="89cfd-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="89cfd-148">Salvar e validar o pacote pode levar cerca de 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="89cfd-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="89cfd-149">Para aplicar a atualização, navegue até a página **Detalhes do ambiente** no LCS e selecione **Manter** > **Aplicar atualizações**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Manter Ambientes](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="89cfd-151">Na lista de atualizações, selecione o pacote que você criou e **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar Atualizações](./media/10ApplyUpdates.png)

<span data-ttu-id="89cfd-153">A manutenção do ambiente levará algum tempo.</span><span class="sxs-lookup"><span data-stu-id="89cfd-153">Environment servicing will take some time.</span></span> <span data-ttu-id="89cfd-154">Após a conclusão, o ambiente retornará ao estado implantado.</span><span class="sxs-lookup"><span data-stu-id="89cfd-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ambiente Implantado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="89cfd-156">Estabelecer uma conexão de Gravação Dupla</span><span class="sxs-lookup"><span data-stu-id="89cfd-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="89cfd-157">Em seu projeto do LCS, acesse a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="89cfd-158">Em **Informações do ambiente do Common Data Service**, selecione **Link para o CDS para aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="89cfd-159">Depois que o link for concluído, selecione novamente **Link para o CDS para aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="89cfd-160">Você será redirecionado para Gravação Dupla no Finance.</span><span class="sxs-lookup"><span data-stu-id="89cfd-160">You will be redirected to Dual Write in Finance.</span></span>

![Link para o CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="89cfd-162">Selecione **Aplicar Solução** para acessar as entidades que serão mapeadas na integração.</span><span class="sxs-lookup"><span data-stu-id="89cfd-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar Soluções](./media/13ApplySolutions.png)

5. <span data-ttu-id="89cfd-164">Selecione ambas as soluções, **Mapa de entidade de gravação dupla do Dynamics 365 Finance and Operations** e **Mapas de entidades de gravação dupla do Dynamics 365 Project Operations** e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar Soluções](./media/14ConfirmSolutions.png)

<span data-ttu-id="89cfd-166">Depois que as soluções forem aplicadas, as entidades de Gravação Dupla serão aplicadas ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="89cfd-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicar Soluções](./media/15ApplyingSolutions.png)

<span data-ttu-id="89cfd-168">Depois que as entidades forem aplicadas, todos os mapeamentos disponíveis serão listados no ambiente.</span><span class="sxs-lookup"><span data-stu-id="89cfd-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapas de Gravação Dupla](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="89cfd-170">Atualizar as entidades de dados após a atualização</span><span class="sxs-lookup"><span data-stu-id="89cfd-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="89cfd-171">No Finance, acesse o espaço de trabalho de **Gerenciamento de dados**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-171">In Finance, go to the **Data management** workspace.</span></span>

![Espaço de trabalho de Gerenciamento de Dados](./media/16DataManagement.png)

2. <span data-ttu-id="89cfd-173">Selecione o bloco **Parâmetros da estrutura**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-173">Select the **Framework parameters** tile.</span></span>

![Parâmetros da Estrutura](./media/17FrameworkParameters.png)

3. <span data-ttu-id="89cfd-175">Na página **Configurações de entidade**, selecione **Atualizar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Atualizar Lista de Entidades](./media/18RefreshEntityList.png)

<span data-ttu-id="89cfd-177">A atualização levará aproximadamente 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="89cfd-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="89cfd-178">Você receberá um alerta quando ela for concluída.</span><span class="sxs-lookup"><span data-stu-id="89cfd-178">You will receive an alert when it is complete.</span></span>

![Atualizar Confirmação](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="89cfd-180">Atualizar as configurações de segurança nas Project Operations no Dataverse</span><span class="sxs-lookup"><span data-stu-id="89cfd-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="89cfd-181">Vá para o Project Operations no seu ambiente do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="89cfd-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="89cfd-182">Vá para **Configurações** > **Segurança** > **Direitos de Acesso**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="89cfd-183">Na página **Direitos de acesso**, na lista de direitos, selecione **usuário de aplicativo de gravação dupla** e selecione a guia **Entidades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="89cfd-184">Verifique se o direito tem permissões para **Ler** e **Anexar a** para:</span><span class="sxs-lookup"><span data-stu-id="89cfd-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="89cfd-185">**Tipo da taxa de câmbio de moeda**</span><span class="sxs-lookup"><span data-stu-id="89cfd-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="89cfd-186">**Tabela de contas**</span><span class="sxs-lookup"><span data-stu-id="89cfd-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="89cfd-187">**Calendário fiscal**</span><span class="sxs-lookup"><span data-stu-id="89cfd-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="89cfd-188">**Razão**</span><span class="sxs-lookup"><span data-stu-id="89cfd-188">**Ledger**</span></span>

5. <span data-ttu-id="89cfd-189">Depois que o direito de acesso for atualizado, vá para **Configurações** > **Segurança** > **Equipes** e selecione a equipe padrão na exibição de equipe **Proprietário de empresa local**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="89cfd-190">Selecione **Gerenciar funções** e verifique se o privilégio de segurança **usuário de aplicativo de gravação dupla** está aplicado a essa equipe.</span><span class="sxs-lookup"><span data-stu-id="89cfd-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="89cfd-191">Executar Mapas de Gravação Dupla do Project Operations</span><span class="sxs-lookup"><span data-stu-id="89cfd-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="89cfd-192">Em seu projeto do LCS, acesse a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="89cfd-193">Em **Informações do ambiente do Common Data Service**, selecione **Link para o CDS para aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="89cfd-194">Depois de selecionar o link, você será redirecionado para a lista de entidades nos mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="89cfd-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="89cfd-195">Inicie os mapas conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="89cfd-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="89cfd-196">Certifique-se de seguir a sequência listada.</span><span class="sxs-lookup"><span data-stu-id="89cfd-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="89cfd-197">**Mapa de Entidade**</span><span class="sxs-lookup"><span data-stu-id="89cfd-197">**Entity Map**</span></span> | <span data-ttu-id="89cfd-198">**Atualizar entidade**</span><span class="sxs-lookup"><span data-stu-id="89cfd-198">**Refresh entity**</span></span> | <span data-ttu-id="89cfd-199">**Sincronização inicial**</span><span class="sxs-lookup"><span data-stu-id="89cfd-199">**Initial sync**</span></span> | <span data-ttu-id="89cfd-200">**Mestre para sincronização inicial**</span><span class="sxs-lookup"><span data-stu-id="89cfd-200">**Master for initial sync**</span></span> | <span data-ttu-id="89cfd-201">**Executar pré-requisitos**</span><span class="sxs-lookup"><span data-stu-id="89cfd-201">**Run prerequisites**</span></span> | <span data-ttu-id="89cfd-202">**Sincronização inicial dos pré-requisitos**</span><span class="sxs-lookup"><span data-stu-id="89cfd-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="89cfd-203">**Funções de Recursos do Projeto para Todas as Empresas (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="89cfd-204">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-204">No</span></span> | <span data-ttu-id="89cfd-205">Sim</span><span class="sxs-lookup"><span data-stu-id="89cfd-205">Yes</span></span> | <span data-ttu-id="89cfd-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="89cfd-206">Common Data Service</span></span> | <span data-ttu-id="89cfd-207">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-207">No</span></span> | <span data-ttu-id="89cfd-208">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-208">N\A</span></span> |
| <span data-ttu-id="89cfd-209">**Entidades legais (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="89cfd-210">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-210">No</span></span> | <span data-ttu-id="89cfd-211">Sim</span><span class="sxs-lookup"><span data-stu-id="89cfd-211">Yes</span></span> | <span data-ttu-id="89cfd-212">Aplicativos do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="89cfd-212">Finance and Operations apps</span></span> | <span data-ttu-id="89cfd-213">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-213">No</span></span> | <span data-ttu-id="89cfd-214">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-214">N\A</span></span> |
| <span data-ttu-id="89cfd-215">**Contabilidade (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="89cfd-216">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-216">No</span></span> | <span data-ttu-id="89cfd-217">Sim</span><span class="sxs-lookup"><span data-stu-id="89cfd-217">Yes</span></span> | <span data-ttu-id="89cfd-218">Aplicativos do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="89cfd-218">Finance and Operations apps</span></span> | <span data-ttu-id="89cfd-219">Sim</span><span class="sxs-lookup"><span data-stu-id="89cfd-219">Yes</span></span> | <span data-ttu-id="89cfd-220">Sim, aplicativos do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="89cfd-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="89cfd-221">**Valores reais da integração do Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="89cfd-222">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-222">No</span></span> | <span data-ttu-id="89cfd-223">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-223">No</span></span> | <span data-ttu-id="89cfd-224">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-224">N\A</span></span> | <span data-ttu-id="89cfd-225">Sim</span><span class="sxs-lookup"><span data-stu-id="89cfd-225">Yes</span></span> | <span data-ttu-id="89cfd-226">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-226">No</span></span> |
| <span data-ttu-id="89cfd-227">**Linhas de contrato do projeto (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="89cfd-228">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-228">No</span></span> | <span data-ttu-id="89cfd-229">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-229">No</span></span> | <span data-ttu-id="89cfd-230">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-230">N\A</span></span> | <span data-ttu-id="89cfd-231">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-231">No</span></span> | <span data-ttu-id="89cfd-232">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-232">No</span></span> |
| <span data-ttu-id="89cfd-233">**Entidade de integração para relacionamentos de transações do projeto (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="89cfd-234">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-234">No</span></span> | <span data-ttu-id="89cfd-235">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-235">No</span></span> | <span data-ttu-id="89cfd-236">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-236">N\A</span></span> | <span data-ttu-id="89cfd-237">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-237">No</span></span> | <span data-ttu-id="89cfd-238">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-238">N\A</span></span> |
| <span data-ttu-id="89cfd-239">**Marcos da linha do contrato de integração do Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="89cfd-240">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-240">No</span></span> | <span data-ttu-id="89cfd-241">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-241">No</span></span> | <span data-ttu-id="89cfd-242">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-242">N\A</span></span> | <span data-ttu-id="89cfd-243">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-243">No</span></span> | <span data-ttu-id="89cfd-244">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-244">N\A</span></span> |
| <span data-ttu-id="89cfd-245">**Entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="89cfd-246">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-246">No</span></span> | <span data-ttu-id="89cfd-247">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-247">No</span></span> | <span data-ttu-id="89cfd-248">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-248">N\A</span></span> | <span data-ttu-id="89cfd-249">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-249">No</span></span> | <span data-ttu-id="89cfd-250">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-250">N\A</span></span> |
| <span data-ttu-id="89cfd-251">**Entidade de exportação de categorias de despesas do projeto de integração do Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="89cfd-252">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-252">No</span></span> | <span data-ttu-id="89cfd-253">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-253">No</span></span> | <span data-ttu-id="89cfd-254">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-254">N\A</span></span> | <span data-ttu-id="89cfd-255">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-255">No</span></span> | <span data-ttu-id="89cfd-256">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-256">N\A</span></span> |
| <span data-ttu-id="89cfd-257">**Entidade de exportação de despesas do projeto de integração do Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="89cfd-258">Sim</span><span class="sxs-lookup"><span data-stu-id="89cfd-258">Yes</span></span> | <span data-ttu-id="89cfd-259">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-259">No</span></span> | <span data-ttu-id="89cfd-260">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-260">N\A</span></span> | <span data-ttu-id="89cfd-261">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-261">No</span></span> | <span data-ttu-id="89cfd-262">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-262">N\A</span></span> |
| <span data-ttu-id="89cfd-263">**Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="89cfd-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="89cfd-264">Sim</span><span class="sxs-lookup"><span data-stu-id="89cfd-264">Yes</span></span> | <span data-ttu-id="89cfd-265">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-265">No</span></span> | <span data-ttu-id="89cfd-266">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-266">N\A</span></span> | <span data-ttu-id="89cfd-267">No</span><span class="sxs-lookup"><span data-stu-id="89cfd-267">No</span></span> | <span data-ttu-id="89cfd-268">N/A</span><span class="sxs-lookup"><span data-stu-id="89cfd-268">N\A</span></span> |


4. <span data-ttu-id="89cfd-269">Para atualizar a entidade, selecione o nome do mapa e, em seguida, **Atualizar entidades**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Atualizar Mapa](./media/20RefreshMapping.png)

5. <span data-ttu-id="89cfd-271">Depois que a atualização for concluída, execute o mapa.</span><span class="sxs-lookup"><span data-stu-id="89cfd-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="89cfd-272">Antes de habilitar o próximo mapa, verifique se o mapa na tabela está em um estado **Em Execução**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="89cfd-273">Executar mapas com um número maior de pré-requisitos pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="89cfd-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="89cfd-274">Para executar um mapa com pré-requisitos, habilite o botão de alternância **Exibir mapas de entidades relacionadas**.</span><span class="sxs-lookup"><span data-stu-id="89cfd-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="89cfd-275">Se a tabela indicar que **Sincronização inicial do pré-requisito** é **Não**, verifique se o indicador **Sincronização inicial** é **Desativado** em todos os mapas de pré-requisitos antes de executá-lo.</span><span class="sxs-lookup"><span data-stu-id="89cfd-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Executar Mapa](./media/21RunMap.png)

6. <span data-ttu-id="89cfd-277">Verifique se todos os mapas relacionados ao projeto estão no estado em execução.</span><span class="sxs-lookup"><span data-stu-id="89cfd-277">Validate all project related maps are in the running state.</span></span>

![Todos os Mapas em Execução](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="89cfd-279">Aplicar dados de configuração no CDS para o Project Operations (opcional)</span><span class="sxs-lookup"><span data-stu-id="89cfd-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="89cfd-280">Se você aplicou dados de demonstração ao ambiente do Finance, consulte [Configurar e aplicar dados de configuração no Common Data Service para Project Operations](resource-apply-pro-setup-config-data.md) para aplicar dados de demonstração ao ambiente CDS.</span><span class="sxs-lookup"><span data-stu-id="89cfd-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="89cfd-281">Seu ambiente do Project Operations agora está provisionado e configurado.</span><span class="sxs-lookup"><span data-stu-id="89cfd-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]