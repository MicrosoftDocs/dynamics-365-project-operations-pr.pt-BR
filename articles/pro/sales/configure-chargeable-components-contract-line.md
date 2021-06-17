---
title: Configurar componentes passíveis de cobrança de uma linha de contrato baseada em projeto
description: Este tópico fornece informações sobre como adicionar componentes passíveis de cobrança às linhas de contrato no Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003707"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="90d1e-103">Configurar componentes passíveis de cobrança de uma linha de contrato baseada em projeto</span><span class="sxs-lookup"><span data-stu-id="90d1e-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="90d1e-104">_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma, Project Operations para cenários com base em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="90d1e-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="90d1e-105">Uma linha de contrato com base em projeto tem componentes *incluídos* e componentes *passíveis de cobrança*.</span><span class="sxs-lookup"><span data-stu-id="90d1e-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="90d1e-106">Os componentes incluídos são componentes que estão sujeitos a:</span><span class="sxs-lookup"><span data-stu-id="90d1e-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="90d1e-107">Método de cobrança e divisões do cliente</span><span class="sxs-lookup"><span data-stu-id="90d1e-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="90d1e-108">Limites máximos</span><span class="sxs-lookup"><span data-stu-id="90d1e-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="90d1e-109">Configurações de frequência de fatura definidas na linha de contrato com base em projeto</span><span class="sxs-lookup"><span data-stu-id="90d1e-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="90d1e-110">Um subconjunto dos componentes incluídos pode ser marcado como cobrável usando o campo **Tipo de Cobrança**.</span><span class="sxs-lookup"><span data-stu-id="90d1e-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="90d1e-111">O campo **Tipo de Cobrança** é um conjunto de opções que permite os seguintes valores no contexto de uma linha de contrato:</span><span class="sxs-lookup"><span data-stu-id="90d1e-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="90d1e-112">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-112">Chargeable</span></span>
  - <span data-ttu-id="90d1e-113">Não Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-113">Non-chargeable</span></span>

<span data-ttu-id="90d1e-114">Os componentes passíveis de cobrança podem ser definidos em tarefas, funções e categorias de transação.</span><span class="sxs-lookup"><span data-stu-id="90d1e-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="90d1e-115">Os encargos são definidos nas tarefas para uma linha de contrato do projeto e se aplicam a todas as classes de transação incluídas na linha.</span><span class="sxs-lookup"><span data-stu-id="90d1e-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="90d1e-116">Se o campo **Incluir Tarefas** em uma linha de contrato estiver em branco ou definido como **Projeto inteiro**, a guia **Tarefas passíveis de cobrança** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="90d1e-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="90d1e-117">Os encargos definidos em funções para uma linha de contrato do projeto só se aplicam à classe de transação **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="90d1e-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="90d1e-118">Se o campo **Incluir Tempo** em uma linha de contrato estiver definido como **Não**, a guia **Funções passíveis de cobrança** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="90d1e-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="90d1e-119">Os encargos são definidos em categorias de transação para uma linha de contrato do projeto e só se aplicam à classe de transação **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="90d1e-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="90d1e-120">Se o campo **Incluir Despesas** estiver definido como **Não**, a guia **Categorias Passíveis de Cobrança** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="90d1e-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="90d1e-121">Atualizar uma tarefa de projeto como passível de cobrança ou não passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="90d1e-122">Uma tarefa de projeto pode ser passível de cobrança ou não passível de cobrança em uma linha de contrato específica, o que torna possível a seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="90d1e-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="90d1e-123">Se uma linha de contrato com base em projeto incluir **Tempo** e uma determinada tarefa, **T1** estará associado a ela como passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="90d1e-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="90d1e-124">Se houver uma segunda linha de contrato que inclua **Despesa**, você poderá associar a tarefa T1 na linha de contrato como não passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="90d1e-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="90d1e-125">O resultado é que todo o tempo registrado na tarefa é passível de cobrança e todas as despesas não são passíveis de cobrança.</span><span class="sxs-lookup"><span data-stu-id="90d1e-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="90d1e-126">O tipo de faturamento de uma tarefa pode ser configurado na guia **Tarefas Passíveis de Cobrança** da linha do contrato atualizando o campo **Tipo de Cobrança** na subgrade de tarefas da linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="90d1e-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="90d1e-127">Como alternativa, você pode atualizar o campo **Tipo de Cobrança** na subgrade da tarefa Configuração de Faturamento de um projeto que mostra as linhas de contrato associadas a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="90d1e-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="90d1e-128">Atualizar uma função como passível de cobrança ou não passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="90d1e-129">Uma função pode ser passível de cobrança ou não passível de cobrança em uma linha de contrato específica.</span><span class="sxs-lookup"><span data-stu-id="90d1e-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="90d1e-130">O tipo de cobrança de uma função pode ser configurado na guia **Funções Passíveis de Cobrança** de uma linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="90d1e-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="90d1e-131">Para fazer isso, atualize o campo **Tipo de Cobrança** na subgrade **Funções Passíveis de Cobrança**.</span><span class="sxs-lookup"><span data-stu-id="90d1e-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="90d1e-132">Atualizar uma categoria de transação como passível de cobrança ou não passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="90d1e-133">Uma categoria de transação pode ser passível de cobrança ou não passível de cobrança em uma linha de contrato específica.</span><span class="sxs-lookup"><span data-stu-id="90d1e-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="90d1e-134">O tipo de cobrança de uma transação pode ser configurado na guia **Categorias Passíveis de Cobrança** de uma linha de contrato com base em projeto.</span><span class="sxs-lookup"><span data-stu-id="90d1e-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="90d1e-135">Para fazer isso, atualize o campo **Tipo de Cobrança** na subgrade **Categorias Passíveis de Cobrança**.</span><span class="sxs-lookup"><span data-stu-id="90d1e-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="90d1e-136">Resolver os encargos</span><span class="sxs-lookup"><span data-stu-id="90d1e-136">Resolve chargeability</span></span>

<span data-ttu-id="90d1e-137">Uma estimativa ou dados reais criados para tempo são considerados passíveis de cobrança se:</span><span class="sxs-lookup"><span data-stu-id="90d1e-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="90d1e-138">**Tempo** estiver incluído na linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="90d1e-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="90d1e-139">**Função** estiver configurado como passível de cobrança na linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="90d1e-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="90d1e-140">**Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="90d1e-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="90d1e-141">Se esses três itens forem verdadeiros, a tarefa será configurada como passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="90d1e-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="90d1e-142">Uma estimativa ou dados reais criados para despesas são considerados passíveis de cobrança se:</span><span class="sxs-lookup"><span data-stu-id="90d1e-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="90d1e-143">**Despesa** está incluído na linha de contrato</span><span class="sxs-lookup"><span data-stu-id="90d1e-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="90d1e-144">**Categoria da transação** estiver configurado como passível de cobrança na linha do contrato</span><span class="sxs-lookup"><span data-stu-id="90d1e-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="90d1e-145">**Tarefas Incluídas** estiver configurado como **Tarefa selecionada** na linha do contrato</span><span class="sxs-lookup"><span data-stu-id="90d1e-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="90d1e-146">Se esses três itens forem verdadeiros, a **Tarefa** será configurada como passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="90d1e-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="90d1e-147">Uma estimativa ou dados reais criados para material são considerados passíveis de cobrança se:</span><span class="sxs-lookup"><span data-stu-id="90d1e-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="90d1e-148">**Materiais** estiver incluído na linha de contrato</span><span class="sxs-lookup"><span data-stu-id="90d1e-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="90d1e-149">**Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha do contrato</span><span class="sxs-lookup"><span data-stu-id="90d1e-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="90d1e-150">Se esses dois itens forem verdadeiros, a **Tarefa** será configurada como passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="90d1e-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="90d1e-151">
                    <strong>Inclui Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="90d1e-152">
                    <strong>Inclui Despesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="90d1e-153">
                    <strong>Inclui Materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="90d1e-154">
                    <strong>Tarefas Incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-155">
                    <strong>Função</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90d1e-156">
                    <strong>Categoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-157">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="90d1e-158">
                    <strong>Impacto de encargos</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-159">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-160">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-161">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-162">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="90d1e-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-163">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-164">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-165">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-166">Cobrança em um tempo real: <strong>Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-167">Tipo de cobrança em uma despesa real: <strong>Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-168">Tipo de cobrança em um material real: <strong>Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-169">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-170">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-171">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-172">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="90d1e-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-173">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-174">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-175">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-176">Cobrança em um tempo real: <strong>Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-177">Tipo de cobrança em uma despesa real: <strong>Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-178">Tipo de cobrança em um material real: <strong>Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-179">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-180">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-181">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-182">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="90d1e-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-183">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-184">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-185">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-186">Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-187">Tipo de cobrança em uma despesa real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90d1e-188">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-189">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-190">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-191">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-192">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="90d1e-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-193">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-194">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-195">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-196">Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-197">Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-198">Tipo de cobrança em um material real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-199">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-200">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-201">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-202">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="90d1e-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-203">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-204">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-205">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-206">Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-207">Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-208">Tipo de cobrança em um material real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-209">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-210">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-211">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-212">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="90d1e-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-213">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90d1e-214">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-215">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-216">Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-217">Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-218">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="90d1e-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-220">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-221">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-222">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="90d1e-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-223">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90d1e-224">
                    <strong>Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-225">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-226">Cobrança em um tempo real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-227">Tipo de cobrança em uma despesa real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90d1e-228">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="90d1e-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-230">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-231">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-232">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="90d1e-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-233">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90d1e-234">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-235">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-236">Cobrança em um tempo real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-237">Tipo de cobrança em despesa real: <strong>Não passível de cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-238">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-239">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="90d1e-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-241">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-242">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="90d1e-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-243">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-244">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-245">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-246">Cobrança em um tempo real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90d1e-247">Tipo de cobrança em despesa real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-248">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-249">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="90d1e-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="90d1e-251">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-252">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="90d1e-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-253">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-254">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-255">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-256">Cobrança em um tempo real: <strong>Não passível de cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-257">Tipo de cobrança em despesa real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-258">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-259">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-260">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="90d1e-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-262">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="90d1e-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-263">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-264">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-265">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-266">Cobrança em um tempo real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90d1e-267">Tipo de cobrança em uma despesa real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="90d1e-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="90d1e-268">Tipo de cobrança em material real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="90d1e-269">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="90d1e-270">Sim</span><span class="sxs-lookup"><span data-stu-id="90d1e-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="90d1e-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="90d1e-272">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="90d1e-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="90d1e-273">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="90d1e-274">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="90d1e-275">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="90d1e-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="90d1e-276">Cobrança em um tempo real: <strong>Não passível de cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-277">Tipo de cobrança em despesa real: <strong>Não passível de cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="90d1e-278">Tipo de cobrança em material real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="90d1e-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
