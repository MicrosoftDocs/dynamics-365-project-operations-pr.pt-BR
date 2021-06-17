---
title: Configurar os componentes passíveis de cobrança de uma linha de cotação
description: Este tópico fornece informações sobre a configuração de componentes passíveis de cobrança e não passíveis de cobrança em uma linha de cotação com base em projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003752"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="c58d7-103">Configurar os componentes passíveis de cobrança de uma linha de cotação</span><span class="sxs-lookup"><span data-stu-id="c58d7-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="c58d7-104">_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma, Project Operations para cenários com base em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="c58d7-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c58d7-105">Uma linha de cotação com base em projeto tem o conceito de componentes *incluídos* e componentes *passíveis de cobrança*.</span><span class="sxs-lookup"><span data-stu-id="c58d7-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="c58d7-106">Os componentes incluídos estão sujeitos a:</span><span class="sxs-lookup"><span data-stu-id="c58d7-106">Included components are subject to:</span></span>

  - <span data-ttu-id="c58d7-107">Método de cobrança e divisões do cliente</span><span class="sxs-lookup"><span data-stu-id="c58d7-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="c58d7-108">Limites máximos</span><span class="sxs-lookup"><span data-stu-id="c58d7-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="c58d7-109">Configurações de frequência de fatura definidas na linha de cotação com base em projeto</span><span class="sxs-lookup"><span data-stu-id="c58d7-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="c58d7-110">Um subconjunto dos componentes incluídos pode ser marcado como cobrável usando o campo **Tipo de Cobrança**.</span><span class="sxs-lookup"><span data-stu-id="c58d7-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="c58d7-111">O campo **Tipo de Cobrança** é um conjunto de opções que permite os seguintes valores no contexto de uma linha de cotação:</span><span class="sxs-lookup"><span data-stu-id="c58d7-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="c58d7-112">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-112">Chargeable</span></span>
  - <span data-ttu-id="c58d7-113">Não Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-113">Non-chargeable</span></span>

<span data-ttu-id="c58d7-114">Os componentes passíveis de cobrança podem ser definidos em tarefas, funções e categorias de transação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="c58d7-115">Os encargos são definidos nas tarefas para uma linha de cotação e se aplicam a todas as classes de transação incluídas nessa linha.</span><span class="sxs-lookup"><span data-stu-id="c58d7-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="c58d7-116">Se o campo **Incluir Tarefas** estiver definido como **Projeto inteiro** ou tiver sido deixado em branco, a guia **Tarefas Passíveis de Cobrança** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="c58d7-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="c58d7-117">Os encargos são definidos nas funções para uma linha de cotação e só se aplicam à classe de transação **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="c58d7-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="c58d7-118">Se o campo **Incluir Tempo** estiver definido como **Não** na linha de cotação de projeto, a guia **Funções Passíveis de Cobrança** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="c58d7-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="c58d7-119">Os encargos são definidos em categorias de transação para uma linha de cotação e só se aplicam à classe de transação **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="c58d7-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="c58d7-120">Se o campo **Incluir Despesas** estiver definido como **Não** na linha de cotação de projeto, a guia **Categorias Passíveis de Cobrança** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="c58d7-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="c58d7-121">Atualizar uma tarefa de projeto para passível de cobrança ou não passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="c58d7-122">Uma tarefa de projeto pode ser passível de cobrança ou não passível de cobrança no contexto de uma linha de cotação com base em projeto, o que torna possível a seguinte configuração.</span><span class="sxs-lookup"><span data-stu-id="c58d7-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="c58d7-123">Se uma linha de cotação com base em projeto incluir **Tempo** e a tarefa **T1**, a tarefa será associada à linha de cotação como passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c58d7-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="c58d7-124">Se houver uma segunda linha de cotação que inclua **Despesas**, você poderá associar a tarefa **T1** na linha de cotação como não passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c58d7-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="c58d7-125">O resultado é que todo o tempo registrado na tarefa é passível de cobrança e todas as despesas registradas na tarefa não são passíveis de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c58d7-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="c58d7-126">O tipo de faturamento de uma tarefa pode ser configurado na guia **Tarefas Passíveis de Cobrança** de uma linha de cotação baseada no projeto atualizando o campo **Tipo de Cobrança** na subgrade **Tarefas da Linha de Cotação**.</span><span class="sxs-lookup"><span data-stu-id="c58d7-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="c58d7-127">Como alternativa, você pode atualizar o tipo de faturamento de uma tarefa do projeto no campo **Tipo de Cobrança** na subgrade na configuração de faturamento da tarefa de um projeto que mostra as linhas da cotação associadas a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="c58d7-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="c58d7-128">Atualizar uma função para passível de cobrança ou não passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="c58d7-129">Uma função pode ser passível de cobrança ou não passível de cobrança no contexto de uma linha de cotação com base em projeto específica.</span><span class="sxs-lookup"><span data-stu-id="c58d7-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="c58d7-130">O tipo de faturamento de uma função pode ser configurado na guia **Funções Passíveis de Cobrança** de uma linha da cotação atualizando o campo **Tipo de Faturamento** na subgrade **Funções Passíveis de Cobrança**.</span><span class="sxs-lookup"><span data-stu-id="c58d7-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="c58d7-131">Atualizar uma categoria de transação para passível de cobrança ou não passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="c58d7-132">Uma categoria de transação pode ser passível de cobrança ou não passível de cobrança em uma linha de cotação específica.</span><span class="sxs-lookup"><span data-stu-id="c58d7-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="c58d7-133">O tipo de faturamento de uma transação pode ser configurado na guia **Categorias Passíveis de Cobrança** de uma linha da cotação atualizando o campo **Tipo de Faturamento** na subgrade **Categorias Passíveis de Cobrança**.</span><span class="sxs-lookup"><span data-stu-id="c58d7-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="c58d7-134">Resolver os encargos</span><span class="sxs-lookup"><span data-stu-id="c58d7-134">Resolve chargeability</span></span>
<span data-ttu-id="c58d7-135">Uma estimativa ou dados reais criados para tempo serão considerados passíveis de cobrança se:</span><span class="sxs-lookup"><span data-stu-id="c58d7-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="c58d7-136">**Tempo** estiver incluído na linha da cotação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="c58d7-137">**Função** for configurada como passível de cobrança na linha da cotação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="c58d7-138">**Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha da cotação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="c58d7-139">Se esses três itens forem verdadeiros, a **Tarefa** também será configurada como passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c58d7-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="c58d7-140">Uma estimativa ou dados reais criados para despesas são considerados passíveis de cobrança se:</span><span class="sxs-lookup"><span data-stu-id="c58d7-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="c58d7-141">**Despesa** estiver incluída na linha da cotação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="c58d7-142">**Categoria da transação** estiver configurado como passível de cobrança na linha da cotação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="c58d7-143">**Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha da cotação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="c58d7-144">Se esses três itens forem verdadeiros, a **Tarefa** também será configurada como passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c58d7-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="c58d7-145">Uma estimativa ou dados reais criados para material serão considerados passíveis de cobrança se:</span><span class="sxs-lookup"><span data-stu-id="c58d7-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="c58d7-146">**Materiais** estiver incluído na linha da cotação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="c58d7-147">**Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha da cotação.</span><span class="sxs-lookup"><span data-stu-id="c58d7-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="c58d7-148">Se esses dois itens forem verdadeiros, a **Tarefa** também deverá ser configurada como passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c58d7-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="c58d7-149">
                    <strong>Inclui Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="c58d7-150">
                    <strong>Inclui Despesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="c58d7-151">
                    <strong>Inclui Materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="c58d7-152">
                    <strong>Tarefas Incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-153">
                    <strong>Função</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c58d7-154">
                    <strong>Categoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-155">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="c58d7-156">
                    <strong>Impacto de encargos</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-157">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-158">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-159">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-160">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="c58d7-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-161">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-162">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-163">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-164">Cobrança em um tempo real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-165">Tipo de cobrança em uma despesa real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-166">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-167">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-168">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-169">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-170">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="c58d7-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-171">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-172">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-173">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-174">Cobrança em um tempo real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-175">Tipo de cobrança em uma despesa real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-176">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-177">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-178">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-179">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-180">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="c58d7-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-181">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-182">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-183">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-184">Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-185">Tipo de cobrança em uma despesa real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-186">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-187">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-188">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-189">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-190">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="c58d7-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-191">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-192">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-193">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-194">Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-195">Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-196">Tipo de cobrança em um material real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-197">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-198">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-199">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-200">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="c58d7-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-201">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-202">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-203">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-204">Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-205">Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-206">Tipo de cobrança em um material real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-207">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-208">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-209">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-210">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="c58d7-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-211">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c58d7-212">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-213">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-214">Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-215">Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-216">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="c58d7-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-218">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-219">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-220">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="c58d7-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-221">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c58d7-222">
                    <strong>Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-223">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-224">Cobrança em um tempo real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-225">Tipo de cobrança em uma despesa real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-226">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="c58d7-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-228">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-229">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-230">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="c58d7-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-231">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c58d7-232">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-233">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-234">Cobrança em um tempo real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-235">Tipo de cobrança em despesa real: <strong>Não passível de cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-236">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-237">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="c58d7-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-239">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-240">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="c58d7-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-241">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-242">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-243">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-244">Cobrança em um tempo real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-245">Tipo de cobrança em despesa real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-246">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-247">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="c58d7-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="c58d7-249">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-250">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="c58d7-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-251">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-252">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-253">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-254">Cobrança em um tempo real: <strong>Não passível de cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-255">Tipo de cobrança em despesa real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-256">Tipo de cobrança em um material real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-257">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-258">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="c58d7-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-260">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="c58d7-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-261">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-262">Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-263">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-264">Cobrança em um tempo real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-265">Tipo de cobrança em uma despesa real: Passível de Cobrança</span><span class="sxs-lookup"><span data-stu-id="c58d7-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="c58d7-266">Tipo de cobrança em material real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="c58d7-267">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="c58d7-268">Sim</span><span class="sxs-lookup"><span data-stu-id="c58d7-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="c58d7-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="c58d7-270">Projeto Inteiro</span><span class="sxs-lookup"><span data-stu-id="c58d7-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="c58d7-271">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="c58d7-272">
                    <strong>Não Passível de Cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="c58d7-273">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="c58d7-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="c58d7-274">Cobrança em um tempo real: <strong>Não passível de cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-275">Tipo de cobrança em despesa real: <strong>Não passível de cobrança</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="c58d7-276">Tipo de cobrança em material real: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c58d7-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
