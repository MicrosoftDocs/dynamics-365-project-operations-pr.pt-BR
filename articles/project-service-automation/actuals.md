---
title: Dados Efetivos
description: Este tópico fornece informações sobre dados reais do projeto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749137"
---
# <a name="actuals"></a><span data-ttu-id="aa049-103">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="aa049-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aa049-104">Os dados reais são o volume de trabalho que foi concluído em um projeto.</span><span class="sxs-lookup"><span data-stu-id="aa049-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="aa049-105">Os dados reais do projeto podem ser rastreados para seus documentos de origem.</span><span class="sxs-lookup"><span data-stu-id="aa049-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="aa049-106">Esses documentos de origem incluem hora, despesa e entradas de diário, além de faturas.</span><span class="sxs-lookup"><span data-stu-id="aa049-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Como os dados reais do projeto são rastreados para documentos de origem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="aa049-108">Enviando uma entrada de hora</span><span class="sxs-lookup"><span data-stu-id="aa049-108">Submitting a time entry</span></span>

<span data-ttu-id="aa049-109">No PSA, quando uma entrada de hora é enviada para um projeto que está mapeado para uma linha de contrato de tempo e materiais, são criadas duas linhas de diário.</span><span class="sxs-lookup"><span data-stu-id="aa049-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="aa049-110">Uma linha destinada ao custo e a outra às vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="aa049-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="aa049-111">Quando uma entrada de hora é enviada para um projeto que está mapeado para uma linha de contrato de preço fixo, uma linha do diário é criada apenas para custo.</span><span class="sxs-lookup"><span data-stu-id="aa049-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="aa049-112">A lógica para inserir preços padrão reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="aa049-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="aa049-113">Todos os valores de campo de uma entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="aa049-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="aa049-114">Esses campos incluem a data da transação, a linha de contrato para a qual o projeto está mapeado e o resultado da moeda na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="aa049-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="aa049-115">Os campos que afetam preços padrão, como **Função** e **Unidades Organizacional**, fazem com que um preço apropriado seja inserido por padrão na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="aa049-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="aa049-116">Se você adicionar um campo personalizado na entrada de hora e quiser que o valor do campo seja propagado para os dados reais, crie o campo na entidade Dados Reais e use mapeamentos de campo para copiar o campo da entrada de hora para os dados reais.</span><span class="sxs-lookup"><span data-stu-id="aa049-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="aa049-117">Enviando uma entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="aa049-117">Submitting an expense entry</span></span>

<span data-ttu-id="aa049-118">No PSA, quando uma entrada de despesa é enviada para um projeto que está mapeado para uma linha de contrato de tempo e materiais, são criadas duas linhas de diário.</span><span class="sxs-lookup"><span data-stu-id="aa049-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="aa049-119">Uma linha destinada ao custo e a outra às vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="aa049-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="aa049-120">Quando uma entrada de despesa é enviada para um projeto que está mapeado para uma linha de contrato de preço fixo, uma linha do diário é criada apenas para custo.</span><span class="sxs-lookup"><span data-stu-id="aa049-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="aa049-121">A lógica para inserir preços padrão para despesas se baseia na categoria da despesa que é selecionada na página **Entrada de despesa**.</span><span class="sxs-lookup"><span data-stu-id="aa049-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="aa049-122">A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada.</span><span class="sxs-lookup"><span data-stu-id="aa049-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="aa049-123">No entanto, para o preço em si, o valor que o usuário inseriu é definido diretamente nas linhas de diário da despesa relacionadas para custo e vendas por padrão.</span><span class="sxs-lookup"><span data-stu-id="aa049-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="aa049-124">Na versão atual do PSA, a entrada baseada em categoria dos preços padrão por unidade nas entradas de despesa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="aa049-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="aa049-125">Usando diários para registrar custos</span><span class="sxs-lookup"><span data-stu-id="aa049-125">Using journals to record costs</span></span>

<span data-ttu-id="aa049-126">No PSA, os diários permitem registrar custo ou receita nas classes de material, valor, hora, despesa ou transação de imposto.</span><span class="sxs-lookup"><span data-stu-id="aa049-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="aa049-127">Um diário possui um cabeçalho, linhas e uma ação **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="aa049-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="aa049-128">Veja a seguir alguns cenários onde você pode usar um diário:</span><span class="sxs-lookup"><span data-stu-id="aa049-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="aa049-129">Você deve registrar os custos reais de material e as vendas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="aa049-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="aa049-130">Você deve mover dados reais da transação de outro sistema para o PSA.</span><span class="sxs-lookup"><span data-stu-id="aa049-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="aa049-131">Você deve registrar os custos que ocorreram em outro sistema, como custos de aquisição ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="aa049-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="aa049-132">Registrando dados reais baseados em eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-132">Recording actuals based on project events</span></span>

<span data-ttu-id="aa049-133">Os PSA registra as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="aa049-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="aa049-134">Essas transações são registradas como **dados reais**.</span><span class="sxs-lookup"><span data-stu-id="aa049-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="aa049-135">As tabelas a seguir mostram os diferentes tipos de dados reais que são criados de acordo com o tipo de projeto; se é de preço fixo ou de tempo e materiais, se está no estágio da venda ou se está em um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="aa049-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="aa049-136">**O recurso pertence à mesma unidade organizacional que a unidade de contratação do projeto**</span><span class="sxs-lookup"><span data-stu-id="aa049-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="aa049-137">Evento</span><span class="sxs-lookup"><span data-stu-id="aa049-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="aa049-138">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="aa049-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="aa049-139">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="aa049-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="aa049-140">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="aa049-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="aa049-141">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="aa049-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="aa049-142">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="aa049-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="aa049-143">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="aa049-143">Actuals</span></span></th>
<th><span data-ttu-id="aa049-144">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="aa049-144">Transaction currency</span></span></th>
<th><span data-ttu-id="aa049-145">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="aa049-145">Fixed price</span></span></th>
<th><span data-ttu-id="aa049-146">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="aa049-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aa049-147">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="aa049-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="aa049-148">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="aa049-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-149">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="aa049-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="aa049-150">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="aa049-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="aa049-151">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="aa049-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="aa049-152">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-152">Cost actual</span></span></td>
<td><span data-ttu-id="aa049-153">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-154">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-155">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="aa049-156">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-157">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-158">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="aa049-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="aa049-159">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="aa049-160">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="aa049-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="aa049-161">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-161">Cost actual</span></span></td>
<td><span data-ttu-id="aa049-162">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-163">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-164">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-165">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-166">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-167">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="aa049-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="aa049-168">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-169">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="aa049-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="aa049-170">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="aa049-171">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="aa049-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="aa049-172">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="aa049-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="aa049-173">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-174">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="aa049-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-175">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-176">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-177">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-178">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="aa049-178">Billed sales</span></span></td>
<td><span data-ttu-id="aa049-179">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="aa049-180">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="aa049-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="aa049-181">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="aa049-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="aa049-182">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-183">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-184">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-185">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-187">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="aa049-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="aa049-188">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-189">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="aa049-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="aa049-190">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="aa049-191">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="aa049-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="aa049-192">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="aa049-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="aa049-193">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="aa049-194">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="aa049-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="aa049-195">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="aa049-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="aa049-196">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="aa049-197">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="aa049-198">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-199">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="aa049-199">Billed sales</span></span></td>
<td><span data-ttu-id="aa049-200">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="aa049-201">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="aa049-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="aa049-202">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="aa049-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="aa049-203">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-204">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="aa049-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="aa049-205">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-206">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="aa049-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="aa049-207">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aa049-208">**O recurso pertence à uma unidade organizacional que é diferente da unidade de contratação do projeto**</span><span class="sxs-lookup"><span data-stu-id="aa049-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="aa049-209">Evento</span><span class="sxs-lookup"><span data-stu-id="aa049-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="aa049-210">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="aa049-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="aa049-211">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="aa049-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="aa049-212">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="aa049-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="aa049-213">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="aa049-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="aa049-214">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="aa049-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="aa049-215">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="aa049-215">Actuals</span></span></th>
<th><span data-ttu-id="aa049-216">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="aa049-216">Transaction currency</span></span></th>
<th><span data-ttu-id="aa049-217">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="aa049-217">Fixed price</span></span></th>
<th><span data-ttu-id="aa049-218">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="aa049-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aa049-219">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="aa049-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="aa049-220">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="aa049-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-221">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="aa049-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="aa049-222">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="aa049-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="aa049-223">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="aa049-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="aa049-224">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-224">Cost actual</span></span></td>
<td><span data-ttu-id="aa049-225">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="aa049-226">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="aa049-227">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="aa049-228">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="aa049-229">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-230">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="aa049-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="aa049-231">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-232">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="aa049-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="aa049-233">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="aa049-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-234">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="aa049-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="aa049-235">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="aa049-236">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="aa049-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="aa049-237">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-237">Cost actual</span></span></td>
<td><span data-ttu-id="aa049-238">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="aa049-239">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="aa049-240">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="aa049-241">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="aa049-242">Custo real</span><span class="sxs-lookup"><span data-stu-id="aa049-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-243">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="aa049-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="aa049-244">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="aa049-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-245">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="aa049-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="aa049-246">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="aa049-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-247">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="aa049-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="aa049-248">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-249">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="aa049-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="aa049-250">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="aa049-251">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="aa049-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="aa049-252">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="aa049-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="aa049-253">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-254">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="aa049-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-255">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-256">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="aa049-257">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-258">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="aa049-258">Billed sales</span></span></td>
<td><span data-ttu-id="aa049-259">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="aa049-260">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="aa049-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="aa049-261">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="aa049-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="aa049-262">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-263">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-264">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-265">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="aa049-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-267">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="aa049-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="aa049-268">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-269">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="aa049-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="aa049-270">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="aa049-271">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="aa049-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="aa049-272">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="aa049-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="aa049-273">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="aa049-274">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="aa049-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="aa049-275">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="aa049-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="aa049-276">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="aa049-277">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="aa049-278">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="aa049-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-279">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="aa049-279">Billed sales</span></span></td>
<td><span data-ttu-id="aa049-280">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="aa049-281">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="aa049-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="aa049-282">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="aa049-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="aa049-283">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-284">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="aa049-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="aa049-285">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa049-286">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="aa049-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="aa049-287">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="aa049-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
