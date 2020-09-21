---
title: Sincronizar estimativas de projetos diretamente do Project Service Automation para o Finance and Operations
description: Este tópico descreve os modelos e as tarefas subjacentes usados para sincronizar as estimativas de horas e de despesas do projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: KimANelson
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749063"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="2c70e-103">Sincronizar estimativas de projetos diretamente do Project Service Automation para o Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2c70e-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2c70e-104">Este tópico descreve os modelos e as tarefas subjacentes usados para sincronizar as estimativas de horas e de despesas do projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2c70e-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="2c70e-105">Integração de tarefas do projeto, categorias de transações de despesas, estimativas de horas, estimativas de despesas e bloqueio de funcionalidade estão disponíveis na versão 8.0.</span><span class="sxs-lookup"><span data-stu-id="2c70e-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="2c70e-106">A integração dos valores reais está disponível na versão 8.0.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2c70e-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="2c70e-107">Fluxo de dados do Project Service Automation para o Finance</span><span class="sxs-lookup"><span data-stu-id="2c70e-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="2c70e-108">A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Project Service Automation e do Finance.</span><span class="sxs-lookup"><span data-stu-id="2c70e-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="2c70e-109">Os modelos de integração disponíveis com o recurso de integração de dados permitem transferir dados sobre estimativas de horas e de despesas do projeto do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="2c70e-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="2c70e-110">A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="2c70e-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="2c70e-111">[![Fluxo de dados para a integração do Project Service Automation ao Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="2c70e-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="2c70e-112">Estimativas de horas do projeto</span><span class="sxs-lookup"><span data-stu-id="2c70e-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="2c70e-113">Modelo e tarefas</span><span class="sxs-lookup"><span data-stu-id="2c70e-113">Template and tasks</span></span>

<span data-ttu-id="2c70e-114">Para acessar os modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="2c70e-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="2c70e-115">O seguinte modelo e as tarefas subjacentes são usados para sincronizar estimativas de horas do projeto do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="2c70e-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="2c70e-116">**Nome do modelo na integração de dados:** Estimativas de horas do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="2c70e-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="2c70e-117">**Nome das tarefas no projeto:**</span><span class="sxs-lookup"><span data-stu-id="2c70e-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="2c70e-118">Relacionamentos de transações</span><span class="sxs-lookup"><span data-stu-id="2c70e-118">Transaction relationships</span></span>
    - <span data-ttu-id="2c70e-119">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="2c70e-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="2c70e-120">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="2c70e-120">Entity set</span></span>

| <span data-ttu-id="2c70e-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2c70e-121">Project Service Automation</span></span> | <span data-ttu-id="2c70e-122">Financeiro</span><span class="sxs-lookup"><span data-stu-id="2c70e-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="2c70e-123">Tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="2c70e-123">Project tasks</span></span>              | <span data-ttu-id="2c70e-124">Entidade de integração para estimativas de horas do projeto</span><span class="sxs-lookup"><span data-stu-id="2c70e-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="2c70e-125">Fluxo da entidade</span><span class="sxs-lookup"><span data-stu-id="2c70e-125">Entity flow</span></span>

<span data-ttu-id="2c70e-126">As estimativas de horas do projeto são gerenciados no Project Service Automation e são sincronizados com o Finance como previsões de horas do projeto.</span><span class="sxs-lookup"><span data-stu-id="2c70e-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="2c70e-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2c70e-127">Prerequisites</span></span>

<span data-ttu-id="2c70e-128">Para que a sincronização das estimativas de horas do projeto ocorra, você deve primeiro sincronizar projetos, tarefas do projeto e categorias de transações das despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="2c70e-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="2c70e-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="2c70e-129">Power Query</span></span>

<span data-ttu-id="2c70e-130">No modelo de estimativas de horas do projeto, você deve usar o Microsoft Power Query para Excel para concluir estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="2c70e-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="2c70e-131">Definir a ID do modelo de previsão padrão que será usada quando a integração criar novas previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="2c70e-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="2c70e-132">Filtrar todos os registros específicos de recursos na tarefa que terão falha na integração com previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="2c70e-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="2c70e-133">Filtrar todas as linhas de categoria de transação vazias.</span><span class="sxs-lookup"><span data-stu-id="2c70e-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="2c70e-134">A falha na conclusão dessa tarefa poderá resultar em previsões de horas incorretas.</span><span class="sxs-lookup"><span data-stu-id="2c70e-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="2c70e-135">Definir a ID do modelo de previsão padrão</span><span class="sxs-lookup"><span data-stu-id="2c70e-135">Set the default forecast model ID</span></span>

<span data-ttu-id="2c70e-136">Para atualizar a ID do modelo de previsão padrão no modelo, clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="2c70e-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="2c70e-137">Em seguida, selecione o link **Consulta e filtragem avançadas**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="2c70e-138">Se você estiver usando o modelo de estimativas de horas do projeto padrão (PSA para Fin and Ops), selecione a **Condição inserida** na lista de **Etapas aplicadas**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="2c70e-139">Na entrada da **Função**, substitua **O\_forecast** pelo nome da ID do modelo de previsão que deve ser usado com a integração.</span><span class="sxs-lookup"><span data-stu-id="2c70e-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="2c70e-140">O modelo padrão tem uma ID do modelo de previsão nos dados de demonstração.</span><span class="sxs-lookup"><span data-stu-id="2c70e-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="2c70e-141">Se estiver criando um novo modelo, você deverá adicionar essa coluna.</span><span class="sxs-lookup"><span data-stu-id="2c70e-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="2c70e-142">Em Power Query, selecione **Adicionar coluna condicional** e insira um nome para a nova coluna, como **IDModelo**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="2c70e-143">Insira a condição para a coluna, em que, if Tarefa do projeto is not null, then \<insira a ID do modelo de previsão\>; else null.</span><span class="sxs-lookup"><span data-stu-id="2c70e-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="2c70e-144">Filtrar registros específicos de recursos</span><span class="sxs-lookup"><span data-stu-id="2c70e-144">Filter out resource-specific records</span></span>

<span data-ttu-id="2c70e-145">O modelo de estimativas de horas do projeto (PSA para Fin and Ops) tem um filtro padrão que remove todos os registros específicos do recurso.</span><span class="sxs-lookup"><span data-stu-id="2c70e-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="2c70e-146">Se você criar seu próprio modelo, deverá adicionar esse filtro.</span><span class="sxs-lookup"><span data-stu-id="2c70e-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="2c70e-147">Selecione o link **Consulta e filtragem avançadas** para filtrar na coluna **msdyn\_islinetask** para que apenas registros com resultado **Falso** sejam são incluídos.</span><span class="sxs-lookup"><span data-stu-id="2c70e-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="2c70e-148">Filtrar linhas de categoria de transação vazias</span><span class="sxs-lookup"><span data-stu-id="2c70e-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="2c70e-149">Você deve adicionar um filtro para remover todas as linhas que possuem categorias de transação vazias.</span><span class="sxs-lookup"><span data-stu-id="2c70e-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="2c70e-150">Essa tarefa é necessária, independentemente de você estar usando o modelo padrão ou criando seu próprio modelo.</span><span class="sxs-lookup"><span data-stu-id="2c70e-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="2c70e-151">Esse filtro remove todas as linhas de resumo do Project Service Automation que possam fazer com que as previsões de horas no Finance fiquem incorretas.</span><span class="sxs-lookup"><span data-stu-id="2c70e-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="2c70e-152">Selecione o link **Consulta e filtragem avançadas** para filtrar registros nulos na coluna **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2c70e-153">Mapeamento de modelos na integração de dados</span><span class="sxs-lookup"><span data-stu-id="2c70e-153">Template mapping in Data integration</span></span>

<span data-ttu-id="2c70e-154">A ilustração a seguir mostra um exemplo do mapeamento de tarefas do modelo na integração de dados.</span><span class="sxs-lookup"><span data-stu-id="2c70e-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="2c70e-155">O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="2c70e-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="2c70e-156">[![Mapeamento de modelos](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="2c70e-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="2c70e-157">Estimativas de despesas do projeto</span><span class="sxs-lookup"><span data-stu-id="2c70e-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="2c70e-158">Modelo e tarefas</span><span class="sxs-lookup"><span data-stu-id="2c70e-158">Template and tasks</span></span>

<span data-ttu-id="2c70e-159">O seguinte modelo e as tarefas subjacentes são usados para sincronizar estimativas de despesas do projeto do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="2c70e-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="2c70e-160">**Nome do modelo na integração de dados:** Estimativas de despesas do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="2c70e-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="2c70e-161">**Nome das tarefas no projeto:**</span><span class="sxs-lookup"><span data-stu-id="2c70e-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="2c70e-162">Relacionamentos de transações</span><span class="sxs-lookup"><span data-stu-id="2c70e-162">Transaction relationships</span></span> 
    - <span data-ttu-id="2c70e-163">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="2c70e-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="2c70e-164">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="2c70e-164">Entity set</span></span>

| <span data-ttu-id="2c70e-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2c70e-165">Project Service Automation</span></span> | <span data-ttu-id="2c70e-166">Financeiro</span><span class="sxs-lookup"><span data-stu-id="2c70e-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="2c70e-167">Conexões da Transação</span><span class="sxs-lookup"><span data-stu-id="2c70e-167">Transaction Connections</span></span>    | <span data-ttu-id="2c70e-168">Entidade de integração para relacionamentos de transações do projeto</span><span class="sxs-lookup"><span data-stu-id="2c70e-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="2c70e-169">Linhas de Estimativa</span><span class="sxs-lookup"><span data-stu-id="2c70e-169">Estimate Lines</span></span>             | <span data-ttu-id="2c70e-170">Entidade de integração para estimativas de despesas do projeto</span><span class="sxs-lookup"><span data-stu-id="2c70e-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="2c70e-171">Fluxo da entidade</span><span class="sxs-lookup"><span data-stu-id="2c70e-171">Entity flow</span></span>

<span data-ttu-id="2c70e-172">As estimativas de despesas do projeto são gerenciados no Project Service Automation e são sincronizados com o Finance como previsões de despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="2c70e-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="2c70e-173">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2c70e-173">Prerequisites</span></span>

<span data-ttu-id="2c70e-174">Para que a sincronização das estimativas de despesas do projeto ocorra, você deve primeiro sincronizar projetos, tarefas do projeto e categorias de transações das despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="2c70e-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="2c70e-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="2c70e-175">Power Query</span></span>

<span data-ttu-id="2c70e-176">No modelo de estimativas de despesas do projeto, você deve usar o Microsoft Power Query para Excel para concluir estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="2c70e-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="2c70e-177">Filtrar para incluir apenas registros de linha de estimativas de despesas.</span><span class="sxs-lookup"><span data-stu-id="2c70e-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="2c70e-178">Definir a ID do modelo de previsão padrão que será usada quando a integração criar novas previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="2c70e-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="2c70e-179">Transformar os tipos de cobrança.</span><span class="sxs-lookup"><span data-stu-id="2c70e-179">Transform the billing types.</span></span>
- <span data-ttu-id="2c70e-180">Transformar os tipos de transação.</span><span class="sxs-lookup"><span data-stu-id="2c70e-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="2c70e-181">Filtrar para incluir apenas linhas de estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="2c70e-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="2c70e-182">O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) tem um filtro padrão que inclui apenas as linhas de despesas na integração.</span><span class="sxs-lookup"><span data-stu-id="2c70e-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="2c70e-183">Se você criar seu próprio modelo, deverá adicionar esse filtro.</span><span class="sxs-lookup"><span data-stu-id="2c70e-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="2c70e-184">Selecione a tarefa **Relacionamentos de transações** e, em seguida, clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="2c70e-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="2c70e-185">Selecione o link **Consulta e filtragem avançadas**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="2c70e-186">Filtre a coluna **msdyn\_transactiontype1** para que inclua apenas **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="2c70e-187">Definir a ID do modelo de previsão padrão</span><span class="sxs-lookup"><span data-stu-id="2c70e-187">Set the default forecast model ID</span></span>

<span data-ttu-id="2c70e-188">Para atualizar a ID do modelo de previsão padrão no modelo, selecione a tarefa **Estimativas de despesas** e, em seguida, clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="2c70e-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="2c70e-189">Selecione o link **Consulta e filtragem avançadas**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="2c70e-190">Se você estiver usando o modelo de estimativas de despesas do projeto padrão (PSA para Fin and Ops), no Power Query, selecione a primeira **Condição inserida** na seção **Etapas aplicadas**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="2c70e-191">Na entrada da **Função**, substitua **O\_forecast** pelo nome da ID do modelo de previsão que deve ser usado com a integração.</span><span class="sxs-lookup"><span data-stu-id="2c70e-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="2c70e-192">O modelo padrão tem uma ID do modelo de previsão nos dados de demonstração.</span><span class="sxs-lookup"><span data-stu-id="2c70e-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="2c70e-193">Se estiver criando um novo modelo, você deverá adicionar essa coluna.</span><span class="sxs-lookup"><span data-stu-id="2c70e-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="2c70e-194">Em Power Query, selecione **Adicionar coluna condicional** e insira um nome para a nova coluna, como **IDModelo**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="2c70e-195">Insira a condição para a coluna, em que, if ID de linha da estimativa is not null, then \<insira a ID do modelo de previsão\>; else null.</span><span class="sxs-lookup"><span data-stu-id="2c70e-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="2c70e-196">Transformar os tipos de cobrança</span><span class="sxs-lookup"><span data-stu-id="2c70e-196">Transform the billing types</span></span>

<span data-ttu-id="2c70e-197">O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é usada para transformar os tipos de cobrança que são recebidos do Project Service Automation durante a integração.</span><span class="sxs-lookup"><span data-stu-id="2c70e-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="2c70e-198">Se você criar seu próprio modelo, deverá adicionar essa coluna condicional.</span><span class="sxs-lookup"><span data-stu-id="2c70e-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="2c70e-199">Selecione o link **Consulta e filtragem avançadas** e, em seguida, **Adicionar coluna condicional**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="2c70e-200">Insira um nome para a nova coluna, como **TipoCobrança**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="2c70e-201">Depois, insira a seguinte condição:</span><span class="sxs-lookup"><span data-stu-id="2c70e-201">Then enter the following condition:</span></span>

<span data-ttu-id="2c70e-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="2c70e-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="2c70e-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="2c70e-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="2c70e-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="2c70e-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="2c70e-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="2c70e-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="2c70e-206">Transformar os tipos de transação</span><span class="sxs-lookup"><span data-stu-id="2c70e-206">Transform the transaction types</span></span>

<span data-ttu-id="2c70e-207">O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é usada para transformar os tipos de transação que são recebidos do Project Service Automation durante a integração.</span><span class="sxs-lookup"><span data-stu-id="2c70e-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="2c70e-208">Se você criar seu próprio modelo, deverá adicionar essa coluna condicional.</span><span class="sxs-lookup"><span data-stu-id="2c70e-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="2c70e-209">Selecione o link **Consulta e filtragem avançadas** e, em seguida, **Adicionar coluna condicional**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="2c70e-210">Insira um nome para a nova coluna, como **TipoTransação**.</span><span class="sxs-lookup"><span data-stu-id="2c70e-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="2c70e-211">Depois, insira a seguinte condição:</span><span class="sxs-lookup"><span data-stu-id="2c70e-211">Then enter the following condition:</span></span>

<span data-ttu-id="2c70e-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="2c70e-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="2c70e-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="2c70e-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="2c70e-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="2c70e-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2c70e-215">Mapeamento de modelos na integração de dados</span><span class="sxs-lookup"><span data-stu-id="2c70e-215">Template mapping in Data integration</span></span>

<span data-ttu-id="2c70e-216">As ilustrações a seguir mostram exemplos de mapeamentos de tarefas do modelo na integração de dados.</span><span class="sxs-lookup"><span data-stu-id="2c70e-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="2c70e-217">O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="2c70e-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="2c70e-218">[![Mapeamento de modelos](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="2c70e-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="2c70e-219">[![Mapeamento de modelos](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="2c70e-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
