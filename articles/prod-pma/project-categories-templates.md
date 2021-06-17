---
title: Sincronizar categorias de despesas de projeto entre Finance and Operations e Project Service Automation
description: Este tópico descreve os modelos e as tarefas subjacentes usadas para sincronizar as categorias de despesas de projeto entre o Microsoft Dynamics 365 Finance e o Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999837"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="fa243-103">Sincronizar categorias de despesas de projeto entre Finance and Operations e Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fa243-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fa243-104">Este tópico descreve os modelos e as tarefas subjacentes usadas para sincronizar as categorias de despesas de projeto entre o Dynamics 365 Finance e o Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fa243-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="fa243-105">A integração de tarefas de projeto, as categorias de transação de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.</span><span class="sxs-lookup"><span data-stu-id="fa243-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="fa243-106">A integração dos valores reais está disponível na versão 8.0.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fa243-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="fa243-107">Se você estiver usando a Enterprise Edition 7.3.0, após instalar o KB 4132657 e o KB 4132660, será possível usar os modelos para integrar as tarefas de projeto, as categorias de transação, as estimativas de horas, as estimativas de despesas e os dados reais, além de configurar o bloqueio de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="fa243-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="fa243-108">Caso seja necessário redefinir as distribuições contábeis, recomendamos instalar o KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="fa243-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="fa243-109">Fluxo de dados para Project Service Automation e o Finance</span><span class="sxs-lookup"><span data-stu-id="fa243-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="fa243-110">A solução de integração do Project Service Automation e do Finance usa o recurso de Integração de dados para sincronizar dados em instâncias do Project Service Automation e do Finance.</span><span class="sxs-lookup"><span data-stu-id="fa243-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="fa243-111">Os modelos de integração disponíveis com o recurso de Integração de dados permitem o fluxo de dados sobre categorias de transação de despesas do projeto entre o Finance e o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fa243-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="fa243-112">Se as categorias de despesas do projeto forem masterizadas em Finance, o fluxo de integração será primeiro do Finance para o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fa243-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="fa243-113">A integração de IDs das categorias de despesas do projeto serão atualizadas por meio de sincronização do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="fa243-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="fa243-114">Se as categorias de despesas do projeto forem masterizadas em Project Service Automation, o fluxo de integração será primeiro do serviço de projeto para o Finance.</span><span class="sxs-lookup"><span data-stu-id="fa243-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="fa243-115">As categorias de projeto já devem estar configuradas no Finance antes da sincronização do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fa243-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="fa243-116">Em seguida, sincronize do Finance para o Project Service Automation e depois do Project Service Automation para o Finance novamente.</span><span class="sxs-lookup"><span data-stu-id="fa243-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="fa243-117">Dessa forma, você ajuda a garantir que as categorias sejam vinculadas e que nenhuma duplicata seja criada.</span><span class="sxs-lookup"><span data-stu-id="fa243-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="fa243-118">Normalmente, as categorias de despesas de projeto são masterizadas no Finance.</span><span class="sxs-lookup"><span data-stu-id="fa243-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="fa243-119">No entanto, caso não sejam ou se as categorias de despesas já tiverem sido criadas no Project Service Automation, é necessário sincronizar primeiro usando o modelo de categorias de transação de despesas do Projeto (PSA para Fin e Ops).</span><span class="sxs-lookup"><span data-stu-id="fa243-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="fa243-120">Em seguida, sincronize usando o modelo de categorias de transação de despesas do Projeto (Fin e Ops para PSA).</span><span class="sxs-lookup"><span data-stu-id="fa243-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="fa243-121">Em seguida, é necessário executar a sincronização do Project Service Automation para o Finance mais uma vez.</span><span class="sxs-lookup"><span data-stu-id="fa243-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="fa243-122">Se você sincronizar o Project Service Automation primeiro, os seguintes requisitos devem ser atendidos no Finance antes que a sincronização seja executada:</span><span class="sxs-lookup"><span data-stu-id="fa243-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="fa243-123">A categoria compartilhada que corresponde à categoria do projeto configurada no Project Service Automation deve existir e deve estar habilitada para **Projeto** e **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="fa243-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="fa243-124">Para cada entidade legal do Finance à qual deve estar integrada, as seguintes categorias de projeto devem existir:</span><span class="sxs-lookup"><span data-stu-id="fa243-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="fa243-125">A **Categoria de projeto** existe.</span><span class="sxs-lookup"><span data-stu-id="fa243-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="fa243-126">**Usar em Despesa** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fa243-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="fa243-127">**Ativo no diário** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fa243-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="fa243-128">O **Tipo de transação** está definido como **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="fa243-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="fa243-129">A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="fa243-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="fa243-130">[![Fluxo de dados para a integração do Project Service Automation e o Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="fa243-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="fa243-131">Sincronização de categorias de despesas de projeto do Finance para o Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fa243-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="fa243-132">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="fa243-132">Template and task</span></span>

<span data-ttu-id="fa243-133">Para acessar o modelo, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="fa243-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="fa243-134">O seguinte modelo e a tarefa subjacente são usados para sincronizar as categorias de despesas de projeto do Finance para o Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="fa243-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="fa243-135">**Nome do modelo na Integração de dados:** categorias de transação de despesas do Projeto (Fin e Ops para PSA)</span><span class="sxs-lookup"><span data-stu-id="fa243-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="fa243-136">**Nome da tarefa raiz no projeto:** sincronizar categorias com o PSA</span><span class="sxs-lookup"><span data-stu-id="fa243-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="fa243-137">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="fa243-137">Entity set</span></span>

| <span data-ttu-id="fa243-138">Financeiro</span><span class="sxs-lookup"><span data-stu-id="fa243-138">Finance</span></span>                           | <span data-ttu-id="fa243-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fa243-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="fa243-140">Entidade da integração para categorias</span><span class="sxs-lookup"><span data-stu-id="fa243-140">Integration entity for categories</span></span> | <span data-ttu-id="fa243-141">Categorias de transação</span><span class="sxs-lookup"><span data-stu-id="fa243-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="fa243-142">Fluxo de entidade</span><span class="sxs-lookup"><span data-stu-id="fa243-142">Entity flow</span></span>

<span data-ttu-id="fa243-143">As categorias de despesas de projeto são gerenciadas em Finance e podem ser sincronizadas com o Project Service Automation como categorias de transação.</span><span class="sxs-lookup"><span data-stu-id="fa243-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="fa243-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="fa243-144">Power Query</span></span>

<span data-ttu-id="fa243-145">Quando estiver sincronizando com o Project Service Automation, é necessário usar o Microsoft Power Query para Excel para definir o tipo de faturamento da categoria de transação.</span><span class="sxs-lookup"><span data-stu-id="fa243-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="fa243-146">O modelo de categorias de transação de despesas do Projeto (Fin e Ops para PSA) oferece um mapeamento e uma coluna padrão.</span><span class="sxs-lookup"><span data-stu-id="fa243-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="fa243-147">Se você criar seu próprio modelo, é necessário adicionar uma coluna condicional no Power Query.</span><span class="sxs-lookup"><span data-stu-id="fa243-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="fa243-148">Siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="fa243-148">Follow these steps.</span></span>

1. <span data-ttu-id="fa243-149">Clique na seta para abrir o mapeamento da tarefa de categorias de despesas de projeto no modelo de categorias de transação de despesas do Projeto (Fin e Ops para PSA).</span><span class="sxs-lookup"><span data-stu-id="fa243-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="fa243-150">Clique no link **Avançar Consulta e Filtragem** para abrir o Power Query.</span><span class="sxs-lookup"><span data-stu-id="fa243-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="fa243-151">Selecione **Adicionar Coluna Condicional**.</span><span class="sxs-lookup"><span data-stu-id="fa243-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="fa243-152">Insira um nome para a nova coluna, como **TipoCobrança**.</span><span class="sxs-lookup"><span data-stu-id="fa243-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="fa243-153">Insira a seguinte condição: **se CATEGORYID não for igual a nulo, ele será 19235001; caso contrário, ele será nulo**.</span><span class="sxs-lookup"><span data-stu-id="fa243-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="fa243-154">Clique em **OK** na coluna.</span><span class="sxs-lookup"><span data-stu-id="fa243-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="fa243-155">Certifique-se de mapear essa nova coluna na página de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="fa243-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="fa243-156">A ilustração a seguir mostra um exemplo do mapeamento de tarefas do modelo na integração de dados.</span><span class="sxs-lookup"><span data-stu-id="fa243-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="fa243-157">O mapeamento mostra as informações de campo que serão sincronizadas do Finance para o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fa243-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="fa243-158">[![Categoria de despesas do projeto para mapeamento de modelo do Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="fa243-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="fa243-159">Sincronização de categorias de despesas de projeto do Project Service Automation para o Finance</span><span class="sxs-lookup"><span data-stu-id="fa243-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="fa243-160">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="fa243-160">Template and task</span></span>

<span data-ttu-id="fa243-161">O seguinte modelo e a tarefa subjacente são usados para sincronizar as categorias de despesas de projeto do Project Service Automation para o Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="fa243-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="fa243-162">**Nome do modelo na Integração de dados:** categorias de transação de despesas do Projeto (PSA para Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="fa243-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="fa243-163">**Nome da tarefa raiz no projeto:** sincronizar categorias com o Fin Ops</span><span class="sxs-lookup"><span data-stu-id="fa243-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="fa243-164">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="fa243-164">Entity set</span></span>

| <span data-ttu-id="fa243-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fa243-165">Project Service Automation</span></span> | <span data-ttu-id="fa243-166">Financeiro</span><span class="sxs-lookup"><span data-stu-id="fa243-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="fa243-167">Categorias de transação</span><span class="sxs-lookup"><span data-stu-id="fa243-167">Transaction categories</span></span>     | <span data-ttu-id="fa243-168">Entidade da integração para categorias</span><span class="sxs-lookup"><span data-stu-id="fa243-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="fa243-169">Fluxo de entidade</span><span class="sxs-lookup"><span data-stu-id="fa243-169">Entity flow</span></span>

<span data-ttu-id="fa243-170">As categorias de despesas de projeto são gerenciadas em Finance e podem ser sincronizadas com o Project Service Automation como categorias de transação.</span><span class="sxs-lookup"><span data-stu-id="fa243-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="fa243-171">A nova sincronização para o Finance atualiza a categoria do projeto no Finance com a ID de integração do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fa243-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fa243-172">Mapeamento de modelos na integração de dados</span><span class="sxs-lookup"><span data-stu-id="fa243-172">Template mapping in Data integration</span></span>

<span data-ttu-id="fa243-173">A ilustração a seguir mostra um exemplo do mapeamento de tarefas do modelo na integração de dados.</span><span class="sxs-lookup"><span data-stu-id="fa243-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="fa243-174">O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="fa243-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="fa243-175">[![Mapeamento de modelo do Project Service Automation ao Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="fa243-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]