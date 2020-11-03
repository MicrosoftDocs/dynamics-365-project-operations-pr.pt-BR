---
title: Dados reais
description: Este tópico fornece informações sobre como trabalhar com dados reais no Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071418"
---
# <a name="actuals"></a><span data-ttu-id="c9ded-103">Dados reais</span><span class="sxs-lookup"><span data-stu-id="c9ded-103">Actuals</span></span> 

<span data-ttu-id="c9ded-104">_**Aplicável a: Project Operations para cenários baseados em recursos/sem estoque**_</span><span class="sxs-lookup"><span data-stu-id="c9ded-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c9ded-105">Os dados reais são o volume de trabalho que foi concluído em um projeto.</span><span class="sxs-lookup"><span data-stu-id="c9ded-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="c9ded-106">Eles são criados como resultado de entradas de hora e despesas e entradas de diário e faturas.</span><span class="sxs-lookup"><span data-stu-id="c9ded-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="c9ded-107">Linhas do diário e envio de horas</span><span class="sxs-lookup"><span data-stu-id="c9ded-107">Journal lines and time submission</span></span>

<span data-ttu-id="c9ded-108">Para obter mais informações sobre a entrada de hora, consulte [Visão geral de entrada de hora](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c9ded-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="c9ded-109">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="c9ded-109">Time and materials</span></span>

<span data-ttu-id="c9ded-110">Quando uma entrada de hora enviada está vinculada a um projeto mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas de diário, uma para custo e a outra para vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="c9ded-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="c9ded-111">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="c9ded-111">Fixed price</span></span>

<span data-ttu-id="c9ded-112">Quando uma entrada enviada está vinculada a um projeto que está mapeado para uma linha de contrato de preço fixo, o sistema cria uma linha de diário para custo.</span><span class="sxs-lookup"><span data-stu-id="c9ded-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="c9ded-113">Preço padrão</span><span class="sxs-lookup"><span data-stu-id="c9ded-113">Default pricing</span></span>

<span data-ttu-id="c9ded-114">A lógica para criar preços padrão reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="c9ded-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="c9ded-115">Os valores de campo da entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="c9ded-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="c9ded-116">Esses valores incluem a data da transação, a linha de contrato para a qual o projeto está mapeado e o resultado da moeda na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="c9ded-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="c9ded-117">Os campos que afetam preços padrão, como **Função** e **Unidades Organizacional** , são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="c9ded-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="c9ded-118">Você pode adicionar um campo personalizado à entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="c9ded-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="c9ded-119">Se você quiser que o valor do campo seja propagado para os dados reais, crie o campo na entidade Dados Reais e use mapeamentos de campo para copiar o campo da entrada de hora para os dados reais.</span><span class="sxs-lookup"><span data-stu-id="c9ded-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="c9ded-120">Linhas de diário e envio de despesas básicas</span><span class="sxs-lookup"><span data-stu-id="c9ded-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="c9ded-121">Para obter mais informações sobre a entrada de despesa, consulte [Visão geral de despesas](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c9ded-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="c9ded-122">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="c9ded-122">Time and materials</span></span>

<span data-ttu-id="c9ded-123">Quando uma entrada de despesa básica enviada está vinculada a um projeto mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas de diário, uma para custo e a outra para vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="c9ded-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="c9ded-124">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="c9ded-124">Fixed price</span></span>

<span data-ttu-id="c9ded-125">Quando uma entrada de despesa básica enviada está vinculada a um projeto que está mapeado para uma linha de contrato de preço fixo, o sistema cria uma linha de diário para custo.</span><span class="sxs-lookup"><span data-stu-id="c9ded-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="c9ded-126">Preço padrão</span><span class="sxs-lookup"><span data-stu-id="c9ded-126">Default pricing</span></span>

<span data-ttu-id="c9ded-127">A lógica para inserir preços padrão para despesas é baseada na categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="c9ded-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="c9ded-128">A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada.</span><span class="sxs-lookup"><span data-stu-id="c9ded-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="c9ded-129">No entanto, por padrão, o valor inserido para o preço em si é definido diretamente nas linhas de diário da despesa relacionadas para custo e vendas.</span><span class="sxs-lookup"><span data-stu-id="c9ded-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="c9ded-130">A entrada baseada em categoria dos preços padrão por unidade nas entradas de despesa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="c9ded-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="c9ded-131">Usar diários de entrada para registrar custos</span><span class="sxs-lookup"><span data-stu-id="c9ded-131">Use entry journals to record costs</span></span>

<span data-ttu-id="c9ded-132">Você pode usar diários de entrada para registrar o custo ou receita nas classes de material, valor, hora, despesa ou transação de imposto.</span><span class="sxs-lookup"><span data-stu-id="c9ded-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="c9ded-133">Os diários podem ser usados para as seguintes finalidades:</span><span class="sxs-lookup"><span data-stu-id="c9ded-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="c9ded-134">Registrar o custo real dos materiais e as vendas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="c9ded-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="c9ded-135">Mover dados reais de outro sistema para o Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c9ded-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="c9ded-136">Registre os custos que ocorreram em outro sistema.</span><span class="sxs-lookup"><span data-stu-id="c9ded-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="c9ded-137">Esses custos podem incluir custos de aquisição ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="c9ded-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9ded-138">O aplicativo não valida o tipo de linha do diário ou o preço relacionado inserido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="c9ded-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="c9ded-139">Portanto, somente um usuário que está totalmente ciente do impacto contábil que os dados reais têm no projeto devem usar diários de entrada para criar os dados reais.</span><span class="sxs-lookup"><span data-stu-id="c9ded-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="c9ded-140">Devido ao impacto deste tipo de diário, é necessário escolher cuidadosamente quem tem acesso para criar diários de entrada.</span><span class="sxs-lookup"><span data-stu-id="c9ded-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="c9ded-141">Registrar dados reais baseados em eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-141">Record actuals based on project events</span></span>

<span data-ttu-id="c9ded-142">O Project Operations registra as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="c9ded-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="c9ded-143">Essas transações são registradas como dados reais.</span><span class="sxs-lookup"><span data-stu-id="c9ded-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="c9ded-144">As tabelas a seguir mostram os diferentes tipos de dados reais que são criados de acordo com o tipo de projeto; se é de preço fixo ou de tempo e materiais, se está no estágio da venda ou se está em um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="c9ded-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="c9ded-145">O recurso pertence à mesma unidade organizacional que a unidade de contratação do projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c9ded-146">Evento</span><span class="sxs-lookup"><span data-stu-id="c9ded-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c9ded-147">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="c9ded-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c9ded-148">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="c9ded-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c9ded-149">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="c9ded-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c9ded-150">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="c9ded-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c9ded-151">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="c9ded-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c9ded-152">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="c9ded-152">Actuals</span></span></th>
<th><span data-ttu-id="c9ded-153">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="c9ded-153">Transaction currency</span></span></th>
<th><span data-ttu-id="c9ded-154">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="c9ded-154">Fixed price</span></span></th>
<th><span data-ttu-id="c9ded-155">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="c9ded-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9ded-156">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="c9ded-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c9ded-157">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="c9ded-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-158">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="c9ded-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c9ded-159">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="c9ded-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c9ded-160">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="c9ded-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c9ded-161">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-161">Cost actual</span></span></td>
<td><span data-ttu-id="c9ded-162">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-163">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-164">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="c9ded-165">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-166">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-167">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="c9ded-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c9ded-168">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9ded-169">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="c9ded-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c9ded-170">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-170">Cost actual</span></span></td>
<td><span data-ttu-id="c9ded-171">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-172">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-173">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-174">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-175">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-176">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="c9ded-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c9ded-177">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-178">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="c9ded-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c9ded-179">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c9ded-180">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="c9ded-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c9ded-181">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="c9ded-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c9ded-182">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-183">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="c9ded-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-184">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-185">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-187">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="c9ded-187">Billed sales</span></span></td>
<td><span data-ttu-id="c9ded-188">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9ded-189">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="c9ded-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c9ded-190">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="c9ded-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c9ded-191">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-192">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-193">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-194">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-195">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-196">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="c9ded-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c9ded-197">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-198">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="c9ded-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c9ded-199">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c9ded-200">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c9ded-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c9ded-201">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="c9ded-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c9ded-202">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c9ded-203">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="c9ded-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c9ded-204">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="c9ded-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c9ded-205">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c9ded-206">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c9ded-207">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-208">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="c9ded-208">Billed sales</span></span></td>
<td><span data-ttu-id="c9ded-209">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9ded-210">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c9ded-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c9ded-211">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="c9ded-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c9ded-212">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-213">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="c9ded-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c9ded-214">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-215">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="c9ded-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c9ded-216">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="c9ded-217">O recurso pertence à uma unidade organizacional que é diferente da unidade de contratação do projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c9ded-218">Evento</span><span class="sxs-lookup"><span data-stu-id="c9ded-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c9ded-219">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="c9ded-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c9ded-220">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="c9ded-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c9ded-221">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="c9ded-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c9ded-222">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="c9ded-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c9ded-223">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="c9ded-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c9ded-224">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="c9ded-224">Actuals</span></span></th>
<th><span data-ttu-id="c9ded-225">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="c9ded-225">Transaction currency</span></span></th>
<th><span data-ttu-id="c9ded-226">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="c9ded-226">Fixed price</span></span></th>
<th><span data-ttu-id="c9ded-227">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="c9ded-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9ded-228">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="c9ded-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c9ded-229">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="c9ded-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-230">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="c9ded-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c9ded-231">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="c9ded-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="c9ded-232">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="c9ded-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c9ded-233">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-233">Cost actual</span></span></td>
<td><span data-ttu-id="c9ded-234">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c9ded-235">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c9ded-236">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c9ded-237">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c9ded-238">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-239">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="c9ded-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c9ded-240">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-241">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="c9ded-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c9ded-242">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="c9ded-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-243">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="c9ded-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c9ded-244">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c9ded-245">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="c9ded-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c9ded-246">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-246">Cost actual</span></span></td>
<td><span data-ttu-id="c9ded-247">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c9ded-248">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c9ded-249">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c9ded-250">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c9ded-251">Custo real</span><span class="sxs-lookup"><span data-stu-id="c9ded-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-252">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="c9ded-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c9ded-253">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="c9ded-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-254">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="c9ded-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c9ded-255">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="c9ded-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-256">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="c9ded-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c9ded-257">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-258">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="c9ded-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c9ded-259">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c9ded-260">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="c9ded-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c9ded-261">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="c9ded-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c9ded-262">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-263">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="c9ded-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-264">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-265">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c9ded-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-267">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="c9ded-267">Billed sales</span></span></td>
<td><span data-ttu-id="c9ded-268">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9ded-269">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="c9ded-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c9ded-270">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="c9ded-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c9ded-271">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-272">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-273">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-274">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c9ded-275">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-276">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="c9ded-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c9ded-277">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-278">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="c9ded-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c9ded-279">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c9ded-280">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c9ded-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c9ded-281">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="c9ded-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c9ded-282">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c9ded-283">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="c9ded-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c9ded-284">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="c9ded-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c9ded-285">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c9ded-286">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c9ded-287">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="c9ded-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-288">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="c9ded-288">Billed sales</span></span></td>
<td><span data-ttu-id="c9ded-289">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c9ded-290">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c9ded-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c9ded-291">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="c9ded-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c9ded-292">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-293">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="c9ded-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c9ded-294">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9ded-295">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="c9ded-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c9ded-296">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="c9ded-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
