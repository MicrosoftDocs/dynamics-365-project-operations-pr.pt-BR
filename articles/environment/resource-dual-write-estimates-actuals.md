---
title: Integração de estimativas e dados reais do projeto
description: Este tópico fornece informações sobre a integração de gravação dupla do Project Operations para estimativas e dados reais do projeto.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955700"
---
# <a name="project-estimates-and-actuals-integration"></a><span data-ttu-id="1b743-103">Integração de estimativas e dados reais do projeto</span><span class="sxs-lookup"><span data-stu-id="1b743-103">Project estimates and actuals integration</span></span>

<span data-ttu-id="1b743-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="1b743-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1b743-105">Este tópico fornece informações sobre a integração de gravação dupla do Project Operations para estimativas e dados reais do projeto.</span><span class="sxs-lookup"><span data-stu-id="1b743-105">This topic provides information about Project Operations dual-write integration for project estimates and actuals.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="1b743-106">Estimativas do projeto</span><span class="sxs-lookup"><span data-stu-id="1b743-106">Project estimates</span></span>

<span data-ttu-id="1b743-107">As estimativas de mão de obra, despesas e material do projeto são criadas e mantidas no Microsoft Dataverse e sincronizada com aplicativos do Finance and Operations para fins contábeis.</span><span class="sxs-lookup"><span data-stu-id="1b743-107">Project labor, expense, and material estimates are created and maintained in Microsoft Dataverse and synchronized to Finance and Operations apps for accounting purposes.</span></span> <span data-ttu-id="1b743-108">As operações de criação, atualização e exclusão não têm suporte de aplicativos do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b743-108">Create, update, and delete operations aren't supported through the Finance and Operations apps.</span></span>

<span data-ttu-id="1b743-109">A criação de estimativas exige uma configuração de contabilidade válida para o projeto.</span><span class="sxs-lookup"><span data-stu-id="1b743-109">Creating estimates requires a valid accounting configuration for the project.</span></span> <span data-ttu-id="1b743-110">Os projetos associados a linhas de contrato devem ter um perfil de custo e receita de projeto válido definido nas regras de perfil de custo e receita do projeto.</span><span class="sxs-lookup"><span data-stu-id="1b743-110">Projects that are associated with contract lines must have a valid project cost and revenue profile defined in the Project cost and revenue profile rules.</span></span> <span data-ttu-id="1b743-111">Para obter mais informações, consulte [Configure a contabilidade para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).</span><span class="sxs-lookup"><span data-stu-id="1b743-111">For more information, see [Configure accounting for billable projects](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).</span></span>

## <a name="labor-estimates"></a><span data-ttu-id="1b743-112">Estimativas de mão de obra</span><span class="sxs-lookup"><span data-stu-id="1b743-112">Labor estimates</span></span>

<span data-ttu-id="1b743-113">Estimativas de mão de obra são criadas pelo Project Manager ou pelo gerente de recursos que também atribui um recurso genérico ou nomeado à tarefa do projeto.</span><span class="sxs-lookup"><span data-stu-id="1b743-113">Labor estimates are created by the Project Manager or Resource manager who also assigns a generic or named resource to the project task.</span></span> <span data-ttu-id="1b743-114">Os registros de atribuição de recursos podem ser revisados na guia **Atribuições de recursos** na página **Detalhes do Projeto** no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1b743-114">Resource assignment records can be reviewed on the **Resource Assignments** tab on the **Project Details** page in Dataverse.</span></span> <span data-ttu-id="1b743-115">Registros de atribuição de recursos no Dataverse criam registros de previsão de horas em aplicativos do Finance and Operations usando **Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)**.</span><span class="sxs-lookup"><span data-stu-id="1b743-115">Resource assignment records in Dataverse create hour forecast records in Finance and Operations apps using **Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**.</span></span>

   ![Integração de estimativas de mão de obra](./Media/DW4LaborEstimates.png)

<span data-ttu-id="1b743-117">A gravação dupla sincroniza registros de atribuição de recursos com a tabela de preparo (**ProjCDSEstimateHoursImport**) e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de horas (**ProjForecastEmpl**).</span><span class="sxs-lookup"><span data-stu-id="1b743-117">Dual-write synchronizes resource assignment records to the staging table (**ProjCDSEstimateHoursImport**), and then uses business logic to create and update hour forecast records (**ProjForecastEmpl**).</span></span>

<span data-ttu-id="1b743-118">O contador do projeto revisa registros de previsão de horas criados em aplicativos do Finance and Operations ao acessar **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Plano** > **Previsões de horas**.</span><span class="sxs-lookup"><span data-stu-id="1b743-118">The Project accountant reviews forecast hour records created in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Plan** > **Hour forecasts**.</span></span>

## <a name="expense-estimates"></a><span data-ttu-id="1b743-119">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="1b743-119">Expense estimates</span></span>

<span data-ttu-id="1b743-120">As estimativas de despesas são criadas pelo gerente de projeto na guia **Estimativas de Despesas** na página **Detalhes do Projeto** no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1b743-120">Expense estimates are created by the Project manager on the **Expense Estimates** tab on the **Project Details** page in Dataverse.</span></span> <span data-ttu-id="1b743-121">Os registros de estimativa de despesas são armazenados na entidade **Linha de Estimativa** no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1b743-121">Expense estimate records are stored in the **Estimate Line** entity in Dataverse.</span></span> <span data-ttu-id="1b743-122">Esses registros de estimativa têm classe de transação, **Despesa** e são sincronizados com os registros de previsão de despesas em aplicativos do Finance and Operations usando **Entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimatelines)**.</span><span class="sxs-lookup"><span data-stu-id="1b743-122">These estimate records have transaction class, **Expense** and are synchronized to expense forecast records in Finance and Operations apps using **Project Operations integration entity for expense estimates (msdyn\_estimatelines)**.</span></span>

   ![Integração de estimativas de despesas](./Media/DW4ExpenseEstimates.png)

<span data-ttu-id="1b743-124">A gravação dupla sincroniza registros de estimativas de despesas para a tabela de preparo **ProjCDSEstimateExpenseImport** e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de despesas (**ProjForecastCost**).</span><span class="sxs-lookup"><span data-stu-id="1b743-124">Dual-write synchronizes expense estimate records to the staging table, **ProjCDSEstimateExpenseImport)** and then uses business logic to create and update expense forecast records (**ProjForecastCost**).</span></span> <span data-ttu-id="1b743-125">As linhas de estimativa armazenam a estimativa de vendas e os registros de estimativa de custo separadamente.</span><span class="sxs-lookup"><span data-stu-id="1b743-125">Estimate lines store sales estimate and cost estimate records separately.</span></span> <span data-ttu-id="1b743-126">A lógica de negócios em aplicativos do Finance and Operations preenche um único registro de previsão de despesas usando esse detalhe na tabela de preparo.</span><span class="sxs-lookup"><span data-stu-id="1b743-126">The business logic in Finance and Operations apps populates a single Expense forecast record using this detail in the staging table.</span></span>

<span data-ttu-id="1b743-127">O contador do projeto pode revisar registros de previsão de despesas em aplicativos do Finance and Operations ao acessar **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Plano** > **Previsões de despesas**.</span><span class="sxs-lookup"><span data-stu-id="1b743-127">The Project accountant can review expense forecast records in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Plan** > **Expense forecasts**.</span></span>

## <a name="material-estimates"></a><span data-ttu-id="1b743-128">Estimativas de material</span><span class="sxs-lookup"><span data-stu-id="1b743-128">Material estimates</span></span>

<span data-ttu-id="1b743-129">As estimativas de material são criadas pelo gerente de projeto na guia **Estimativas de material** na página **Detalhes do Projeto** no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1b743-129">Material estimates are created by the Project manager on the **Material Estimates** tab on the **Project Details** page in Dataverse.</span></span> <span data-ttu-id="1b743-130">Os registros de estimativa de material são armazenados na entidade **Linha de Estimativa** no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1b743-130">Material estimate records are stored in the **Estimate Line** entity in Dataverse.</span></span> <span data-ttu-id="1b743-131">Esses registros de estimativa têm a classe de transação, **Material** e são sincronizados com os registros de previsão de itens em aplicativos do Finance and Operations usando **Tabela de integração de projeto para estimativas de material (msdyn\_estimatelines)**.</span><span class="sxs-lookup"><span data-stu-id="1b743-131">These estimate records have the transaction class, **Material** and are synchronized to item forecast records in Finance and Operations apps using **Project integration table for material estimates (msdyn\_estimatelines)**.</span></span>

   ![Integração de estimativas de material](./Media/DW4MaterialEstimates.png)

<span data-ttu-id="1b743-133">A gravação dupla sincroniza registros de estimativas de material para a tabela de preparo, **ProjForecastSalesImpor** e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de itens (**ForecastSales**).</span><span class="sxs-lookup"><span data-stu-id="1b743-133">Dual-write synchronizes material estimate records to the staging table **ProjForecastSalesImpor**, and then uses business logic to create and update item forecast records (**ForecastSales**).</span></span> <span data-ttu-id="1b743-134">As linhas de estimativa armazenam a estimativa de vendas e os registros de estimativa de custo separadamente.</span><span class="sxs-lookup"><span data-stu-id="1b743-134">Estimate lines store sales estimate and cost estimate records separately.</span></span> <span data-ttu-id="1b743-135">A lógica de negócios em aplicativos do Finance and Operations preenche um único registro de previsão de itens usando esse detalhe na tabela de preparo.</span><span class="sxs-lookup"><span data-stu-id="1b743-135">The business logic in Finance and Operations apps populates a single Item forecast record using this detail in the staging table.</span></span>

<span data-ttu-id="1b743-136">O contador do projeto pode revisar registros de previsão de itens em aplicativos do Finance and Operations ao acessar **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Plano** > **Previsões de itens**.</span><span class="sxs-lookup"><span data-stu-id="1b743-136">The Project accountant can review item forecast records in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Plan** > **Item forecasts**.</span></span>

## <a name="project-actuals"></a><span data-ttu-id="1b743-137">Dados reais do projeto</span><span class="sxs-lookup"><span data-stu-id="1b743-137">Project actuals</span></span>

<span data-ttu-id="1b743-138">Os dados reais do projeto são criados no Dataverse, com base em tempo, despesas, material e atividade de cobrança.</span><span class="sxs-lookup"><span data-stu-id="1b743-138">Project actuals are created in Dataverse, based on time, expense, material, and billing activity.</span></span> <span data-ttu-id="1b743-139">Todos os atributos operacionais dessas transações, incluindo quantidade, preço de custo, preço de venda e projeto são capturados nesta entidade do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1b743-139">All operational attributes of these transactions including quantity, cost price, sales price, and project are captured in this Dataverse entity.</span></span> <span data-ttu-id="1b743-140">Para obter mais informações, consulte [Dados reais](../actuals/actuals-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1b743-140">For more information, see [Actuals](../actuals/actuals-overview.md).</span></span> <span data-ttu-id="1b743-141">Os registros de dados reais são sincronizados com aplicativos do Finance and Operations usando o mapa da tabela de gravação dupla **Dados reais de integração do Project Operations (msdyn\_actuals)** para contabilidade derivada.</span><span class="sxs-lookup"><span data-stu-id="1b743-141">Actual records are synchronized to Finance and Operations apps using the dual-write table map **Project Operations integration actuals (msdyn\_actuals)** for downstream accounting.</span></span>

   ![Integração de dados reais](./Media/DW4Actuals.png)

<span data-ttu-id="1b743-143">O mapa de tabela **Dados reais de integração do Project Operations** sincroniza todos os registros da entidade **Dados Reais** no Dataverse, com o atributo **Ignorar Sincronização (apenas para uso interno)** definido como **Falso**.</span><span class="sxs-lookup"><span data-stu-id="1b743-143">The **Project Operations integration actuals** table map synchronizes all the records from the **Actuals** entity in Dataverse, with the attribute **Skip Sync (internal use only)** set to **False**.</span></span> <span data-ttu-id="1b743-144">Este valor de atributo é definido no Dataverse automaticamente quando o registro é criado.</span><span class="sxs-lookup"><span data-stu-id="1b743-144">This attribute value is set in Dataverse automatically when the record is created.</span></span> <span data-ttu-id="1b743-145">Exemplos em que este atributo é definido como **Verdadeiro**:</span><span class="sxs-lookup"><span data-stu-id="1b743-145">Examples where this attribute is set to **True** are:</span></span>

  - <span data-ttu-id="1b743-146">Dados reais de custo do projeto para transações intercompanhia.</span><span class="sxs-lookup"><span data-stu-id="1b743-146">Project cost actuals for intercompany transactions.</span></span> <span data-ttu-id="1b743-147">Para obter mais informações, consulte [Criar transações intercompanhia](../project-accounting/create-intercompany-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="1b743-147">For more information, see [Create intercompany transactions](../project-accounting/create-intercompany-transactions.md).</span></span> <span data-ttu-id="1b743-148">Esses registros são ignorados porque o sistema recria os dados reais de custo do projeto em aplicativos do Finance and Operations quando a fatura do fornecedor intercompanhia é postada.</span><span class="sxs-lookup"><span data-stu-id="1b743-148">These records are skipped because the system recreates the project cost actual in Finance and Operations apps when the intercompany vendor invoice is posted.</span></span>
  - <span data-ttu-id="1b743-149">Registros negativos de vendas não cobradas criados quando a fatura pro forma é confirmada.</span><span class="sxs-lookup"><span data-stu-id="1b743-149">Negative unbilled sales records created when the proforma invoice is confirmed.</span></span> <span data-ttu-id="1b743-150">Esses registros são ignorados porque o razão auxiliar do projeto em aplicativos do Finance and Operations não reverte o registro de vendas não cobradas no faturamento, mas altera o status para totalmente faturado.</span><span class="sxs-lookup"><span data-stu-id="1b743-150">These records are skipped because the project subledger in Finance and Operations apps doesn't reverse the unbilled sales record at invoicing but changes the status to fully invoiced.</span></span>

<span data-ttu-id="1b743-151">O mapa da tabela de gravação dupla sincroniza os registros de dados reais com a tabela de preparo, **ProjCDSActualsImport**.</span><span class="sxs-lookup"><span data-stu-id="1b743-151">The dual-write table map synchronizes the actuals records to the staging table, **ProjCDSActualsImport**.</span></span> <span data-ttu-id="1b743-152">Esses registros são processados pelo processo periódico **Importar da tabela de preparo** ao criar linhas de diário de integração do Project Operations e linhas de proposta de fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="1b743-152">These records are processed by the periodic process **Import from staging table** when creating Project Operations integration journal lines and project invoice proposal lines.</span></span> <span data-ttu-id="1b743-153">Para obter mais informações, consulte [Diário de integração no Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="1b743-153">For more information, see [Integration journal in Project Operations](../project-accounting/project-operations-integration-journal.md).</span></span>

<span data-ttu-id="1b743-154">O Dataverse também captura os links entre as transações reais do projeto na entidade **Conexão de transação**.</span><span class="sxs-lookup"><span data-stu-id="1b743-154">Dataverse also captures the links between the project actual transactions in the **Transaction connection** entity.</span></span> <span data-ttu-id="1b743-155">Para obter mais informações, consulte [Vincule dados reais a registros originais](../actuals/linkingactuals.md).</span><span class="sxs-lookup"><span data-stu-id="1b743-155">For more information, see [Link actuals to original records](../actuals/linkingactuals.md).</span></span> <span data-ttu-id="1b743-156">Links entre transações reais também são sincronizados com aplicativos do Finance and Operations usando o mapa de tabela de gravação dupla, **Entidade de integração para relacionamentos de transação do projeto (msdyn\_transactionconnections)**.</span><span class="sxs-lookup"><span data-stu-id="1b743-156">Links between actual transactions are also synchronized to Finance and Operations apps using the dual-write table map, **Integration entity for project transaction relationships (msdyn\_transactionconnections)**.</span></span> <span data-ttu-id="1b743-157">Esses registros são usados pelo processo periódico, **Importar da tabela de preparo**, ao criar linhas de diário de integração do Project Operations e linhas de proposta de fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="1b743-157">These records are used by the periodic process, **Import from staging table** when creating Project Operations integration journal lines and Project invoice proposal lines.</span></span>

<span data-ttu-id="1b743-158">Postar um diário de integração do Project Operations e uma proposta de fatura de projeto dispara uma atualização nos respectivos registros na tabela de preparo, **ProjCDSActualsImport**.</span><span class="sxs-lookup"><span data-stu-id="1b743-158">Posting a Project Operations integration journal and a project invoice proposal triggers an update in respective records in the staging table, **ProjCDSActualsImport**.</span></span> <span data-ttu-id="1b743-159">O sistema captura e registra os seguintes atributos de contabilidade para transações de dados reais:</span><span class="sxs-lookup"><span data-stu-id="1b743-159">The system captures and records the following accounting attributes for actuals transactions:</span></span>

- <span data-ttu-id="1b743-160">Valor da moeda contábil</span><span class="sxs-lookup"><span data-stu-id="1b743-160">Accounting currency amount</span></span>
- <span data-ttu-id="1b743-161">Taxa de câmbio</span><span class="sxs-lookup"><span data-stu-id="1b743-161">Exchange rate</span></span>
- <span data-ttu-id="1b743-162">Número do comprovante</span><span class="sxs-lookup"><span data-stu-id="1b743-162">Voucher number</span></span>
- <span data-ttu-id="1b743-163">Valor do imposto</span><span class="sxs-lookup"><span data-stu-id="1b743-163">Sales tax amount</span></span>

<span data-ttu-id="1b743-164">O mapa de tabela **Dados reais de integração do Project Operations** atualiza os respectivos registros de dados reais no Dataverse com essas informações.</span><span class="sxs-lookup"><span data-stu-id="1b743-164">The **Project Operations integration actuals** table map updates respective actuals records in Dataverse with this information.</span></span>