---
title: Sincronizar estimativas de projetos diretamente do Project Service Automation para o Finance and Operations
description: Este tópico descreve os modelos e as tarefas subjacentes usados para sincronizar as estimativas de horas e de despesas do projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071556"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="7695a-103">Sincronizar estimativas de projetos diretamente do Project Service Automation para o Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7695a-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7695a-104">Este tópico descreve os modelos e as tarefas subjacentes usados para sincronizar as estimativas de horas e de despesas do projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7695a-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="7695a-105">Integração de tarefas do projeto, categorias de transações de despesas, estimativas de horas, estimativas de despesas e bloqueio de funcionalidade estão disponíveis na versão 8.0.</span><span class="sxs-lookup"><span data-stu-id="7695a-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="7695a-106">A integração dos valores reais está disponível na versão 8.0.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7695a-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="7695a-107">Fluxo de dados do Project Service Automation para o Finance</span><span class="sxs-lookup"><span data-stu-id="7695a-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="7695a-108">A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Project Service Automation e do Finance.</span><span class="sxs-lookup"><span data-stu-id="7695a-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="7695a-109">Os modelos de integração disponíveis com o recurso de integração de dados permitem transferir dados sobre estimativas de horas e de despesas do projeto do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="7695a-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7695a-110">A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="7695a-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="7695a-111">[![Fluxo de dados para a integração do Project Service Automation ao Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="7695a-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="7695a-112">Estimativas de horas do projeto</span><span class="sxs-lookup"><span data-stu-id="7695a-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7695a-113">Modelo e tarefas</span><span class="sxs-lookup"><span data-stu-id="7695a-113">Template and tasks</span></span>

<span data-ttu-id="7695a-114">Para acessar os modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="7695a-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7695a-115">O seguinte modelo e as tarefas subjacentes são usados para sincronizar estimativas de horas do projeto do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="7695a-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7695a-116">**Nome do modelo na integração de dados:** Estimativas de horas do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="7695a-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7695a-117">**Nome das tarefas no projeto:**</span><span class="sxs-lookup"><span data-stu-id="7695a-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7695a-118">Relacionamentos de transações</span><span class="sxs-lookup"><span data-stu-id="7695a-118">Transaction relationships</span></span>
    - <span data-ttu-id="7695a-119">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="7695a-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7695a-120">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="7695a-120">Entity set</span></span>

| <span data-ttu-id="7695a-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7695a-121">Project Service Automation</span></span> | <span data-ttu-id="7695a-122">Financeiro</span><span class="sxs-lookup"><span data-stu-id="7695a-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="7695a-123">Tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="7695a-123">Project tasks</span></span>              | <span data-ttu-id="7695a-124">Entidade de integração para estimativas de horas do projeto</span><span class="sxs-lookup"><span data-stu-id="7695a-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="7695a-125">Fluxo da entidade</span><span class="sxs-lookup"><span data-stu-id="7695a-125">Entity flow</span></span>

<span data-ttu-id="7695a-126">As estimativas de horas do projeto são gerenciados no Project Service Automation e são sincronizados com o Finance como previsões de horas do projeto.</span><span class="sxs-lookup"><span data-stu-id="7695a-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7695a-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7695a-127">Prerequisites</span></span>

<span data-ttu-id="7695a-128">Para que a sincronização das estimativas de horas do projeto ocorra, você deve primeiro sincronizar projetos, tarefas do projeto e categorias de transações das despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="7695a-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7695a-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="7695a-129">Power Query</span></span>

<span data-ttu-id="7695a-130">No modelo de estimativas de horas do projeto, você deve usar o Microsoft Power Query para Excel para concluir estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="7695a-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="7695a-131">Definir a ID do modelo de previsão padrão que será usada quando a integração criar novas previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="7695a-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7695a-132">Filtrar todos os registros específicos de recursos na tarefa que terão falha na integração com previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="7695a-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="7695a-133">Filtrar todas as linhas de categoria de transação vazias.</span><span class="sxs-lookup"><span data-stu-id="7695a-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="7695a-134">A falha na conclusão dessa tarefa poderá resultar em previsões de horas incorretas.</span><span class="sxs-lookup"><span data-stu-id="7695a-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7695a-135">Definir a ID do modelo de previsão padrão</span><span class="sxs-lookup"><span data-stu-id="7695a-135">Set the default forecast model ID</span></span>

<span data-ttu-id="7695a-136">Para atualizar a ID do modelo de previsão padrão no modelo, clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="7695a-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7695a-137">Em seguida, selecione o link **Consulta e filtragem avançadas**.</span><span class="sxs-lookup"><span data-stu-id="7695a-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7695a-138">Se você estiver usando o modelo de estimativas de horas do projeto padrão (PSA para Fin and Ops), selecione a **Condição inserida** na lista de **Etapas aplicadas**.</span><span class="sxs-lookup"><span data-stu-id="7695a-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="7695a-139">Na entrada da **Função** , substitua **O\_forecast** pelo nome da ID do modelo de previsão que deve ser usado com a integração.</span><span class="sxs-lookup"><span data-stu-id="7695a-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7695a-140">O modelo padrão tem uma ID do modelo de previsão nos dados de demonstração.</span><span class="sxs-lookup"><span data-stu-id="7695a-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7695a-141">Se estiver criando um novo modelo, você deverá adicionar essa coluna.</span><span class="sxs-lookup"><span data-stu-id="7695a-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7695a-142">Em Power Query, selecione **Adicionar coluna condicional** e insira um nome para a nova coluna, como **IDModelo**.</span><span class="sxs-lookup"><span data-stu-id="7695a-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7695a-143">Insira a condição para a coluna, em que, se a tarefa do projeto não for nula (null), então \<enter the forecast model ID\>; senão nula (null).</span><span class="sxs-lookup"><span data-stu-id="7695a-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="7695a-144">Filtrar registros específicos de recursos</span><span class="sxs-lookup"><span data-stu-id="7695a-144">Filter out resource-specific records</span></span>

<span data-ttu-id="7695a-145">O modelo de estimativas de horas do projeto (PSA para Fin and Ops) tem um filtro padrão que remove todos os registros específicos do recurso.</span><span class="sxs-lookup"><span data-stu-id="7695a-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="7695a-146">Se você criar seu próprio modelo, deverá adicionar esse filtro.</span><span class="sxs-lookup"><span data-stu-id="7695a-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7695a-147">Selecione o link **Consulta e filtragem avançadas** para filtrar na coluna **msdyn\_islinetask** para que apenas registros com resultado **Falso** sejam são incluídos.</span><span class="sxs-lookup"><span data-stu-id="7695a-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="7695a-148">Filtrar linhas de categoria de transação vazias</span><span class="sxs-lookup"><span data-stu-id="7695a-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="7695a-149">Você deve adicionar um filtro para remover todas as linhas que possuem categorias de transação vazias.</span><span class="sxs-lookup"><span data-stu-id="7695a-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="7695a-150">Essa tarefa é necessária, independentemente de você estar usando o modelo padrão ou criando seu próprio modelo.</span><span class="sxs-lookup"><span data-stu-id="7695a-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="7695a-151">Esse filtro remove todas as linhas de resumo do Project Service Automation que possam fazer com que as previsões de horas no Finance fiquem incorretas.</span><span class="sxs-lookup"><span data-stu-id="7695a-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="7695a-152">Selecione o link **Consulta e filtragem avançadas** para filtrar registros nulos na coluna **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="7695a-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7695a-153">Mapeamento de modelos na integração de dados</span><span class="sxs-lookup"><span data-stu-id="7695a-153">Template mapping in Data integration</span></span>

<span data-ttu-id="7695a-154">A ilustração a seguir mostra um exemplo do mapeamento de tarefas do modelo na integração de dados.</span><span class="sxs-lookup"><span data-stu-id="7695a-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="7695a-155">O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="7695a-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7695a-156">[![Mapeamento de tarefa de modelo na integração de dados](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7695a-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="7695a-157">Estimativas de despesas do projeto</span><span class="sxs-lookup"><span data-stu-id="7695a-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7695a-158">Modelo e tarefas</span><span class="sxs-lookup"><span data-stu-id="7695a-158">Template and tasks</span></span>

<span data-ttu-id="7695a-159">O seguinte modelo e as tarefas subjacentes são usados para sincronizar estimativas de despesas do projeto do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="7695a-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7695a-160">**Nome do modelo na integração de dados:** Estimativas de despesas do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="7695a-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7695a-161">**Nome das tarefas no projeto:**</span><span class="sxs-lookup"><span data-stu-id="7695a-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7695a-162">Relacionamentos de transações</span><span class="sxs-lookup"><span data-stu-id="7695a-162">Transaction relationships</span></span> 
    - <span data-ttu-id="7695a-163">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="7695a-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7695a-164">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="7695a-164">Entity set</span></span>

| <span data-ttu-id="7695a-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7695a-165">Project Service Automation</span></span> | <span data-ttu-id="7695a-166">Financeiro</span><span class="sxs-lookup"><span data-stu-id="7695a-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="7695a-167">Conexões da Transação</span><span class="sxs-lookup"><span data-stu-id="7695a-167">Transaction Connections</span></span>    | <span data-ttu-id="7695a-168">Entidade de integração para relacionamentos de transações do projeto</span><span class="sxs-lookup"><span data-stu-id="7695a-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="7695a-169">Linhas de Estimativa</span><span class="sxs-lookup"><span data-stu-id="7695a-169">Estimate Lines</span></span>             | <span data-ttu-id="7695a-170">Entidade de integração para estimativas de despesas do projeto</span><span class="sxs-lookup"><span data-stu-id="7695a-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="7695a-171">Fluxo da entidade</span><span class="sxs-lookup"><span data-stu-id="7695a-171">Entity flow</span></span>

<span data-ttu-id="7695a-172">As estimativas de despesas do projeto são gerenciados no Project Service Automation e são sincronizados com o Finance como previsões de despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="7695a-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7695a-173">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7695a-173">Prerequisites</span></span>

<span data-ttu-id="7695a-174">Para que a sincronização das estimativas de despesas do projeto ocorra, você deve primeiro sincronizar projetos, tarefas do projeto e categorias de transações das despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="7695a-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7695a-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="7695a-175">Power Query</span></span>

<span data-ttu-id="7695a-176">No modelo de estimativas de despesas do projeto, você deve usar o Microsoft Power Query para Excel para concluir estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="7695a-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="7695a-177">Filtrar para incluir apenas registros de linha de estimativas de despesas.</span><span class="sxs-lookup"><span data-stu-id="7695a-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="7695a-178">Definir a ID do modelo de previsão padrão que será usada quando a integração criar novas previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="7695a-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7695a-179">Transformar os tipos de cobrança.</span><span class="sxs-lookup"><span data-stu-id="7695a-179">Transform the billing types.</span></span>
- <span data-ttu-id="7695a-180">Transformar os tipos de transação.</span><span class="sxs-lookup"><span data-stu-id="7695a-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="7695a-181">Filtrar para incluir apenas linhas de estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="7695a-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="7695a-182">O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) tem um filtro padrão que inclui apenas as linhas de despesas na integração.</span><span class="sxs-lookup"><span data-stu-id="7695a-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="7695a-183">Se você criar seu próprio modelo, deverá adicionar esse filtro.</span><span class="sxs-lookup"><span data-stu-id="7695a-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7695a-184">Selecione a tarefa **Relacionamentos de transações** e, em seguida, clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="7695a-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7695a-185">Selecione o link **Consulta e filtragem avançadas**.</span><span class="sxs-lookup"><span data-stu-id="7695a-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="7695a-186">Filtre a coluna **msdyn\_transactiontype1** para que inclua apenas **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="7695a-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7695a-187">Definir a ID do modelo de previsão padrão</span><span class="sxs-lookup"><span data-stu-id="7695a-187">Set the default forecast model ID</span></span>

<span data-ttu-id="7695a-188">Para atualizar a ID do modelo de previsão padrão no modelo, selecione a tarefa **Estimativas de despesas** e, em seguida, clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="7695a-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7695a-189">Selecione o link **Consulta e filtragem avançadas**.</span><span class="sxs-lookup"><span data-stu-id="7695a-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7695a-190">Se você estiver usando o modelo de estimativas de despesas do projeto padrão (PSA para Fin and Ops), no Power Query, selecione a primeira **Condição inserida** na seção **Etapas aplicadas**.</span><span class="sxs-lookup"><span data-stu-id="7695a-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="7695a-191">Na entrada da **Função** , substitua **O\_forecast** pelo nome da ID do modelo de previsão que deve ser usado com a integração.</span><span class="sxs-lookup"><span data-stu-id="7695a-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7695a-192">O modelo padrão tem uma ID do modelo de previsão nos dados de demonstração.</span><span class="sxs-lookup"><span data-stu-id="7695a-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7695a-193">Se estiver criando um novo modelo, você deverá adicionar essa coluna.</span><span class="sxs-lookup"><span data-stu-id="7695a-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7695a-194">Em Power Query, selecione **Adicionar coluna condicional** e insira um nome para a nova coluna, como **IDModelo**.</span><span class="sxs-lookup"><span data-stu-id="7695a-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7695a-195">Insira a condição para a coluna, em que, se a ID de linha da estimativa não for nula (null), então \<enter the forecast model ID\>; senão nula (null).</span><span class="sxs-lookup"><span data-stu-id="7695a-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="7695a-196">Transformar os tipos de cobrança</span><span class="sxs-lookup"><span data-stu-id="7695a-196">Transform the billing types</span></span>

<span data-ttu-id="7695a-197">O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é usada para transformar os tipos de cobrança que são recebidos do Project Service Automation durante a integração.</span><span class="sxs-lookup"><span data-stu-id="7695a-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7695a-198">Se você criar seu próprio modelo, deverá adicionar essa coluna condicional.</span><span class="sxs-lookup"><span data-stu-id="7695a-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7695a-199">Selecione o link **Consulta e filtragem avançadas** e, em seguida, **Adicionar coluna condicional**.</span><span class="sxs-lookup"><span data-stu-id="7695a-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7695a-200">Insira um nome para a nova coluna, como **TipoCobrança**.</span><span class="sxs-lookup"><span data-stu-id="7695a-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="7695a-201">Depois, insira a seguinte condição:</span><span class="sxs-lookup"><span data-stu-id="7695a-201">Then enter the following condition:</span></span>

<span data-ttu-id="7695a-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="7695a-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="7695a-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="7695a-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="7695a-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="7695a-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="7695a-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="7695a-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="7695a-206">Transformar os tipos de transação</span><span class="sxs-lookup"><span data-stu-id="7695a-206">Transform the transaction types</span></span>

<span data-ttu-id="7695a-207">O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é usada para transformar os tipos de transação que são recebidos do Project Service Automation durante a integração.</span><span class="sxs-lookup"><span data-stu-id="7695a-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7695a-208">Se você criar seu próprio modelo, deverá adicionar essa coluna condicional.</span><span class="sxs-lookup"><span data-stu-id="7695a-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7695a-209">Selecione o link **Consulta e filtragem avançadas** e, em seguida, **Adicionar coluna condicional**.</span><span class="sxs-lookup"><span data-stu-id="7695a-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7695a-210">Insira um nome para a nova coluna, como **TipoTransação**.</span><span class="sxs-lookup"><span data-stu-id="7695a-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="7695a-211">Depois, insira a seguinte condição:</span><span class="sxs-lookup"><span data-stu-id="7695a-211">Then enter the following condition:</span></span>

<span data-ttu-id="7695a-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="7695a-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="7695a-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="7695a-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="7695a-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="7695a-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7695a-215">Mapeamento de modelos na integração de dados</span><span class="sxs-lookup"><span data-stu-id="7695a-215">Template mapping in Data integration</span></span>

<span data-ttu-id="7695a-216">As ilustrações a seguir mostram exemplos de mapeamentos de tarefas do modelo na integração de dados.</span><span class="sxs-lookup"><span data-stu-id="7695a-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="7695a-217">O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="7695a-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7695a-218">[![Mapeamento de modelo de transações de estimativa de despesas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7695a-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="7695a-219">[![Mapeamento de modelo de estimativas de despesas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7695a-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
