---
title: Configurar materiais não estocados e faturas de fornecedor pendentes
description: Este tópico explica como habilitar materiais não estocados e faturas de fornecedor pendentes.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a84245a246f49ab69466aba0fec332f0489eec6c
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880619"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a><span data-ttu-id="8d8ee-103">Configurar materiais não estocados e faturas de fornecedor pendentes</span><span class="sxs-lookup"><span data-stu-id="8d8ee-103">Configure non-stocked materials and pending vendor invoices</span></span>

<span data-ttu-id="8d8ee-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="8d8ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="minimum-version-requirement"></a><span data-ttu-id="8d8ee-105">Requisição de versão mínima</span><span class="sxs-lookup"><span data-stu-id="8d8ee-105">Minimum version requirement</span></span>

<span data-ttu-id="8d8ee-106">O uso de materiais não estocados e faturas de fornecedores pendentes para cenários não estocados/baseados em recursos do Dynamics 365 Project Operations exige as seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="8d8ee-106">Using non-stocked materials and pending vendor invoices for Dynamics 365 Project Operations non-stocked/resource based scenarios requires the following versions:</span></span>

<span data-ttu-id="8d8ee-107">Soluções do Dynamics 365 Dataverse:</span><span class="sxs-lookup"><span data-stu-id="8d8ee-107">Dynamics 365 Dataverse solutions:</span></span>

- <span data-ttu-id="8d8ee-108">Project Operations – 4.9.0.221 ou superior</span><span class="sxs-lookup"><span data-stu-id="8d8ee-108">Project Operations – 4.9.0.221 or higher</span></span>
- <span data-ttu-id="8d8ee-109">Solução de orquestração de aplicativo de gravação dupla - 2.2.2.23 ou superior</span><span class="sxs-lookup"><span data-stu-id="8d8ee-109">Dual-write application orchestration solution - 2.2.2.23 or higher</span></span>

<span data-ttu-id="8d8ee-110">Dynamics 365 Finance:</span><span class="sxs-lookup"><span data-stu-id="8d8ee-110">Dynamics 365 Finance:</span></span>
- <span data-ttu-id="8d8ee-111">10.0.18 (10.0.793.52) ou superior.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-111">10.0.18 (10.0.793.52) or higher.</span></span> <span data-ttu-id="8d8ee-112">Verifique se o ambiente do Finance está atualizado e se todas as atualizações de qualidade são aplicadas para atender aos requisitos mínimos de versão.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-112">Make sure that your Finance environment is current and all quality updates are applied to meet the minimum version requirements.</span></span>

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a><span data-ttu-id="8d8ee-113">Execute mapas de gravação dupla para materiais não estocados e integração de fatura do fornecedor</span><span class="sxs-lookup"><span data-stu-id="8d8ee-113">Run Dual-write maps for non-stocked materials and vendor invoice integration</span></span>

<span data-ttu-id="8d8ee-114">Esta seção fornece informações sobre os mapas específicos necessários para materiais não estocados e faturas de fornecedores.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-114">This section provides information about specific the maps required for non-stocked materials and vendor invoices.</span></span> <span data-ttu-id="8d8ee-115">Verifique se os mapas de pré-requisitos listados no tópico [Provisione um novo ambiente](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) estão em execução em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-115">Verify that the prerequisite maps listed in the [Provision a new environment](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) topic are running on your environment.</span></span>

1. <span data-ttu-id="8d8ee-116">Acesse Lifecycle Services (LCS), navegue até o projeto LCS e acesse a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-116">Go to Lifecycle Services (LCS), navigate to your LCS project, and go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8d8ee-117">Na seção **Informações de ambiente do Common Data Service**, selecione **Link para CDS para Aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-117">In the **Common Data Service Environment Information** section, select **Link to CDS for Apps**.</span></span> <span data-ttu-id="8d8ee-118">Depois de selecionar o link, você será redirecionado para a lista de entidades nos mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-118">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="8d8ee-119">Verifique se os mapas a seguir estão em execução.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-119">Make sure the following maps are running.</span></span> <span data-ttu-id="8d8ee-120">Se eles não estiverem em execução, inicie-os e inclua todos os mapas de tabela relacionados.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-120">If they aren't running, start them and make sure to include all related table maps.</span></span>

    - <span data-ttu-id="8d8ee-121">O CDS lançou produtos distintos (produtos)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-121">CDS released distinct products (products)</span></span>
    - <span data-ttu-id="8d8ee-122">Fornecedores v2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-122">Vendors v2 (msdyn_vendors)</span></span>
    - <span data-ttu-id="8d8ee-123">Tabela do Project Operations para estimativas de material (msdyn_estimatelines)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-123">Project Operations table for material estimates (msdyn_estimatelines)</span></span>
    - <span data-ttu-id="8d8ee-124">Entidade de exportação de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoices)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-124">Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)</span></span>
    - <span data-ttu-id="8d8ee-125">Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoicelines)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-125">Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)</span></span>
    - <span data-ttu-id="8d8ee-126">Dados reais da integração do Project Operations (msdyn_actuals).</span><span class="sxs-lookup"><span data-stu-id="8d8ee-126">Project Operations integration actuals (msdyn_actuals).</span></span> <span data-ttu-id="8d8ee-127">Verifique se você está executando a versão do mapa 1.0.0.14 ou superior.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-127">Make sure you are running map version 1.0.0.14 or higher.</span></span> <span data-ttu-id="8d8ee-128">É possível ver a versão ativa do mapa na coluna **Versão** na página **Gravação Dupla**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-128">You can see the active version of the map in the **Version** column on the **Dual Write** page.</span></span> <span data-ttu-id="8d8ee-129">Você pode ativar uma nova versão do mapa selecionando **Versão do mapa de tabela** e salvando a versão selecionada.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-129">You can activate a new version of the map by selecting **Table map version** and then saving the selected version.</span></span>

<span data-ttu-id="8d8ee-130">Se você estiver usando dados de demonstração padrão, talvez também precise parar e reiniciar os seguintes mapas de entidade com a sincronização inicial:</span><span class="sxs-lookup"><span data-stu-id="8d8ee-130">If you are using standard demo data, you might also need to stop and restart the following entity maps with initial sync:</span></span>
  - <span data-ttu-id="8d8ee-131">Dias de pagamento CDS V2 (msdyn_paymentdays)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-131">Payment days CDS V2 (msdyn_paymentdays)</span></span>
  - <span data-ttu-id="8d8ee-132">Agenda de pagamentos (msdyn_paymentschedules)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-132">Payment schedule (msdyn_paymentschedules)</span></span>
  - <span data-ttu-id="8d8ee-133">Condições de pagamento (msdyn_paymentterms)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-133">Terms of payment (msdyn_paymentterms)</span></span>
  - <span data-ttu-id="8d8ee-134">Grupos de fornecedores (msdyn_vendorgroups)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-134">Vendor groups (msdyn_vendorgroups)</span></span>
  - <span data-ttu-id="8d8ee-135">Unidades (uom)</span><span class="sxs-lookup"><span data-stu-id="8d8ee-135">Units (uom)</span></span>

> [!NOTE]
> <span data-ttu-id="8d8ee-136">A sincronização inicial para grupos e unidades de fornecedores pode falhar para alguns registros no conjunto de dados de demonstração existente.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-136">The initial sync for vendor groups and units might fail for a few records in the existing demo data set.</span></span> <span data-ttu-id="8d8ee-137">Você pode ignorar as falhas, pois elas não o impedirão de usar dados de demonstração com o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-137">You can ignore the failures as they won't prevent you from using demo data with Project Operations.</span></span>

## <a name="configure-prerequisites-in-dataverse"></a><span data-ttu-id="8d8ee-138">Configurar pré-requisitos no Dataverse</span><span class="sxs-lookup"><span data-stu-id="8d8ee-138">Configure prerequisites in Dataverse</span></span>

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a><span data-ttu-id="8d8ee-139">Ative o fluxo de trabalho para criar contas com base na entidade do fornecedor</span><span class="sxs-lookup"><span data-stu-id="8d8ee-139">Activate workflow to create accounts based on vendor entity</span></span>

<span data-ttu-id="8d8ee-140">A solução Dual Write Orchestration fornece [Integração mestre de fornecedores](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping).</span><span class="sxs-lookup"><span data-stu-id="8d8ee-140">The Dual Write Orchestration solution provides [Vendors master integration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping).</span></span> <span data-ttu-id="8d8ee-141">Como pré-requisito para este recurso, os dados do fornecedor devem ser criados na entidade **Contas**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-141">As a prerequisite for this feature, vendor data must be created in the **Accounts** entity.</span></span> <span data-ttu-id="8d8ee-142">Ative um processo de fluxo de trabalho de modelo para criar fornecedores na tabela **Contas**, conforme descrito em [Alternar entre designs de fornecedores](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type).</span><span class="sxs-lookup"><span data-stu-id="8d8ee-142">Activate a template workflow process to create vendors in the **Accounts** table as described in [Switch between vendor designs](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type).</span></span>

### <a name="set-products-to-be-created-as-active"></a><span data-ttu-id="8d8ee-143">Definir produtos a serem criados como ativos</span><span class="sxs-lookup"><span data-stu-id="8d8ee-143">Set products to be created as active</span></span>

<span data-ttu-id="8d8ee-144">Os materiais não estocados devem ser configurados como **Produtos liberados** no Finance.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-144">Non-stocked materials must be configured as **Released products** in Finance.</span></span> <span data-ttu-id="8d8ee-145">A solução Dual Write Orchestration oferece uma [Integração pronta para o uso de produtos liberados para o catálogo de produtos do Dataverse](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping).</span><span class="sxs-lookup"><span data-stu-id="8d8ee-145">The Dual Write Orchestration solution provides an out-of-the-box [Released products integration to Dataverse Product catalog](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping).</span></span> <span data-ttu-id="8d8ee-146">Por padrão, os produtos do Finance são sincronizados para o Dataverse em estado de rascunho.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-146">By default, products from Finance are synchronized to Dataverse in a draft state.</span></span> <span data-ttu-id="8d8ee-147">Para sincronizar o produto para um estado ativo para que possa ser usado diretamente em documentos de uso de material ou faturas de fornecedores pendentes, acesse **Sistema** > **Administração** > **Administração do sistema** > **Configurações do sistema** e, na guia **Vendas**, defina **Criar produtos no estado ativo** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-147">To synchronize the product to an active state so that it can be directly used in material usage documents or pending vendor invoices, go to **System** > **Administration** > **System administration** > **System settings**, and on the **Sales** tab, set **Create products in active state** to **Yes**.</span></span>

## <a name="configure-prerequisites-in-finance"></a><span data-ttu-id="8d8ee-148">Configurar pré-requisitos no Finance</span><span class="sxs-lookup"><span data-stu-id="8d8ee-148">Configure prerequisites in Finance</span></span>

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a><span data-ttu-id="8d8ee-149">Habilite a chave do recurso para faturas de fornecedores pendentes</span><span class="sxs-lookup"><span data-stu-id="8d8ee-149">Enable the feature key for pending vendor invoices</span></span>

<span data-ttu-id="8d8ee-150">Conclua as etapas a seguir para habilitar a funcionalidade de adicionar detalhes do projeto em linhas de fatura de fornecedores pendentes.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-150">Complete the following steps to enable functionality to add project details on pending vendor invoice lines.</span></span>

1. <span data-ttu-id="8d8ee-151">No Finance, acesse o espaço de trabalho **Gerenciamento de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-151">In Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="8d8ee-152">Na lista de recursos, encontre o recurso **Habilite faturas de fornecedores pendentes no Project Operations para cenários baseados em recursos/não estocados** e selecione **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-152">In the feature list, find **Enable pending vendor invoices on Project Operations for resource based/non-stocked scenarios** feature and select **Enable**.</span></span>

### <a name="define-category-groups-and-project-categories-for-items"></a><span data-ttu-id="8d8ee-153">Definir grupos de categorias e categorias de projetos para itens</span><span class="sxs-lookup"><span data-stu-id="8d8ee-153">Define category groups and project categories for items</span></span>

<span data-ttu-id="8d8ee-154">Configure pelo menos um grupo de categorias para o tipo de transação **Item** e pelo menos uma categoria de projeto usando este grupo.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-154">Configure at least one category group for the **Item** transaction type , and at least one project category using this group.</span></span> <span data-ttu-id="8d8ee-155">Para obter mais informações, consulte [Configurar categorias de projeto](../project-accounting/configure-project-categories.md#category-groups).</span><span class="sxs-lookup"><span data-stu-id="8d8ee-155">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md#category-groups).</span></span>

<span data-ttu-id="8d8ee-156">Revise os perfis de custo e receita do projeto e configure a configuração de lançamento contábil para transações de itens.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-156">Review the project cost and revenue profiles, and configure ledger posting setup for item transactions.</span></span> <span data-ttu-id="8d8ee-157">Para obter mais informações, consulte [Configure a contabilidade para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md).</span><span class="sxs-lookup"><span data-stu-id="8d8ee-157">For more information, see [Configure accounting for billable projects](../project-accounting/configure-accounting-billable-projects.md).</span></span>

### <a name="set-up-a-write-in-product"></a><span data-ttu-id="8d8ee-158">Configurar um produto fora do catálogo</span><span class="sxs-lookup"><span data-stu-id="8d8ee-158">Set up a write-in product</span></span>

<span data-ttu-id="8d8ee-159">No Project Operations, você pode registrar estimativas de material e uso para produtos do catálogo que estão configurados no catálogo de produtos liberados e para produtos fora do catálogo.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-159">In Project Operations, you can record material estimates and usage for catalog products that are configured in the released product catalog and for write-in products.</span></span> <span data-ttu-id="8d8ee-160">O uso de produtos fora do catálogo exige um único produto liberado que seja configurado no Finance para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-160">Using write-in products requires a single released product that's configured in Finance for this purpose.</span></span> <span data-ttu-id="8d8ee-161">Conclua as etapas a seguir para configurar um produto fora do catálogo.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-161">Complete the following steps to configure a write-in product.</span></span> <span data-ttu-id="8d8ee-162">Repita essas etapas em cada entidade legal que está usando o Project Operations para cenários de recursos/sem estoque.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-162">Repeat these steps in each legal entity that is using Project Operations for resource/non-stocked scenarios.</span></span>

1. <span data-ttu-id="8d8ee-163">No Finance, acesse **Gerenciamento de informações do produto** > **Produtos** > **Produtos liberados** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-163">In Finance, go to **Product Information Management** > **Products** > **Released products**, and select **New**.</span></span>
2. <span data-ttu-id="8d8ee-164">No campo **Tipo de produto**, selecione **Item**; no campo **Subtipo de produto**, selecione **Produto**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-164">In the **Product type** field, select **Item** and in the **Product subtype** field, select **Product**.</span></span>
3. <span data-ttu-id="8d8ee-165">Insira o número do produto (WRITEIN) e o nome do produto (Produto Fora do Catálogo).</span><span class="sxs-lookup"><span data-stu-id="8d8ee-165">Enter the product number (WRITEIN) and the product name (Write-in Product).</span></span>
4. <span data-ttu-id="8d8ee-166">Selecione o grupo de modelos de itens.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-166">Select  the item model group.</span></span> <span data-ttu-id="8d8ee-167">Verifique se o grupo de modelos de itens que você selecionou tem o campo **Política de estoque - Produto em estoque** definido como **Falso**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-167">Make sure that the item model group you select has the **Inventory policy Stocked product** field set to **False**.</span></span>
5. <span data-ttu-id="8d8ee-168">Selecione valores nos campos **Grupo de itens**, **Grupo de dimensão de armazenamento** e **Grupo de dimensão de rastreamento**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-168">Select values in the **Item group**, **Storage dimension group**, and **Tracking dimension group** fields.</span></span> <span data-ttu-id="8d8ee-169">Use **Dimensão de armazenamento** apenas para **Local** e não defina dimensões de acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-169">Use the **Storage dimension** for **Site** only, and do not set any tracking dimensions.</span></span>
6. <span data-ttu-id="8d8ee-170">Selecione valores nos campos **Unidade de estoque**, **Unidade de compra** e **Unidade de vendas**. Em seguida, salve as alterações.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-170">Select values in the **Inventory unit**, **Purchase unit**, and **Sales unit** field, and then save your changes.</span></span>
7. <span data-ttu-id="8d8ee-171">Na guia **Plano**, defina as configurações de ordem padrão e no guia **Estoque**, defina o site e o depósito padrão.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-171">In the **Plan** tab, set the default order settings, and on the **Inventory** tab, set the default site and warehouse.</span></span>
8. <span data-ttu-id="8d8ee-172">Acesse **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto** e abra **Project Operations no Dynamics 365 Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-172">Go to **Project management and accounting** > **Setup** > **Project management and accounting parameters** and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
9. <span data-ttu-id="8d8ee-173">Na guia **Materiais**, no campo **Produto fora do catálogo**, selecione o produto que você criou.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-173">On the **Materials** tab, in the **Write-in product** field, select the product you created.</span></span>
10. <span data-ttu-id="8d8ee-174">Na ambiente Dataverse, no mapa do site, abra a entidade **Produtos** e encontre o registro do produto fora do catálogo.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-174">In your Dataverse environment, in the site map, open the **Products** entity and find the write-in product record.</span></span> 
11. <span data-ttu-id="8d8ee-175">Abra os detalhes do registro e defina o estado do produto como **Aposentado**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-175">Open the record details and set product state to **Retired**.</span></span> <span data-ttu-id="8d8ee-176">Este estado do produto evita que alguém acidentalmente use este registro diretamente em estimativas de material e documentos de uso.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-176">This product state prevents anyone from accidentally using this record directly in material estimates and usage documents.</span></span>

### <a name="set-up-a-procurement-integration-account"></a><span data-ttu-id="8d8ee-177">Configure uma conta de integração de compras</span><span class="sxs-lookup"><span data-stu-id="8d8ee-177">Set up a procurement integration account</span></span>

<span data-ttu-id="8d8ee-178">A conta de integração de compras é usada como conta de compensação ao lançar uma fatura de fornecedores pendentes com linhas atribuídas a um projeto.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-178">The procurement integration account is used as a clearing account when posting a pending vendor invoice with lines attributed to a project.</span></span>

<span data-ttu-id="8d8ee-179">Quando o sistema posta uma fatura de fornecedor pendente, esta conta é usada para o valor de custo do projeto.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-179">When the system posts a pending vendor invoice, this account is used for the project cost amount.</span></span> <span data-ttu-id="8d8ee-180">Os detalhes da fatura do fornecedor são processados no Dataverse e um projeto real correspondente é criado.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-180">The vendor invoice details are processed in Dataverse, and a corresponding project actual is created.</span></span> <span data-ttu-id="8d8ee-181">As informações do projeto real são adicionadas ao diário de integração do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-181">The information from the project actual is added to the Project Operations Integration journal.</span></span> <span data-ttu-id="8d8ee-182">Quando você posta o diário de integração, o valor é compensado da conta de integração de compras e registrado no custo do projeto.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-182">When you post the integration journal, the amount is cleared from the procurement integration account and recorded to the project cost.</span></span>

1. <span data-ttu-id="8d8ee-183">Para configurar a conta de integração de compras, acesse **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto** e abra **Project Operations no Dynamics 365 Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-183">To set up the procurement integration account, go to **Project management and accounting** > **Setup** > **Project management and accounting parameters**, and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
2. <span data-ttu-id="8d8ee-184">Selecione a guia **Materiais** e selecione um valor no campo **Conta de integração de compras**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-184">Select the **Materials** tab, and select a value in the **Procurement integration account** field.</span></span>

#### <a name="set-up-project-category-defaults-for-an-item"></a><span data-ttu-id="8d8ee-185">Configurar padrões de categoria de projeto para um item</span><span class="sxs-lookup"><span data-stu-id="8d8ee-185">Set up project category defaults for an item</span></span>

1. <span data-ttu-id="8d8ee-186">No Finance, acesse **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto** e abra **Project Operations no Dynamics 365 Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-186">In Finance, go to **Project management and accounting** > **Setup** > **Project management and accounting parameters**, and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
2. <span data-ttu-id="8d8ee-187">Na guia **Padrões de categoria de projeto**, no campo **Item**, selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-187">On the **Project category defaults** tab, in the **Item** field, select a value.</span></span> <span data-ttu-id="8d8ee-188">Esta categoria de projeto será usada para transações de material se a categoria do projeto não tiver sido definida no registro de dados reais do projeto.</span><span class="sxs-lookup"><span data-stu-id="8d8ee-188">This project category is used for material transactions if the project category wasn't set on the project actuals record.</span></span>