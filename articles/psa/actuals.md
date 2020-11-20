---
title: Visão geral dos dados reais
description: Este tópico fornece informações sobre dados reais do projeto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129754"
---
# <a name="actuals-overview"></a><span data-ttu-id="d4add-103">Visão geral dos dados reais</span><span class="sxs-lookup"><span data-stu-id="d4add-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d4add-104">Os dados reais são o volume de trabalho que foi concluído em um projeto.</span><span class="sxs-lookup"><span data-stu-id="d4add-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d4add-105">Os dados reais do projeto podem ser rastreados para seus documentos de origem.</span><span class="sxs-lookup"><span data-stu-id="d4add-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="d4add-106">Esses documentos de origem incluem hora, despesa e entradas de diário, além de faturas.</span><span class="sxs-lookup"><span data-stu-id="d4add-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Como os dados reais do projeto são rastreados para documentos de origem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="d4add-108">Enviando uma entrada de hora</span><span class="sxs-lookup"><span data-stu-id="d4add-108">Submitting a time entry</span></span>

<span data-ttu-id="d4add-109">No PSA, quando uma entrada de hora é enviada para um projeto que está mapeado para uma linha de contrato de tempo e materiais, são criadas duas linhas de diário.</span><span class="sxs-lookup"><span data-stu-id="d4add-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d4add-110">Uma linha destinada ao custo e a outra às vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="d4add-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d4add-111">Quando uma entrada de hora é enviada para um projeto que está mapeado para uma linha de contrato de preço fixo, uma linha do diário é criada apenas para custo.</span><span class="sxs-lookup"><span data-stu-id="d4add-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="d4add-112">A lógica para inserir preços padrão reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="d4add-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="d4add-113">Todos os valores de campo de uma entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="d4add-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="d4add-114">Esses campos incluem a data da transação, a linha de contrato para a qual o projeto está mapeado e o resultado da moeda na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="d4add-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="d4add-115">Os campos que afetam preços padrão, como **Função** e **Unidades Organizacional**, fazem com que um preço apropriado seja inserido por padrão na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="d4add-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="d4add-116">Se você adicionar um campo personalizado na entrada de hora e quiser que o valor do campo seja propagado para os dados reais, crie o campo na entidade Dados Reais e use mapeamentos de campo para copiar o campo da entrada de hora para os dados reais.</span><span class="sxs-lookup"><span data-stu-id="d4add-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="d4add-117">Enviando uma entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="d4add-117">Submitting an expense entry</span></span>

<span data-ttu-id="d4add-118">No PSA, quando uma entrada de despesa é enviada para um projeto que está mapeado para uma linha de contrato de tempo e materiais, são criadas duas linhas de diário.</span><span class="sxs-lookup"><span data-stu-id="d4add-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d4add-119">Uma linha destinada ao custo e a outra às vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="d4add-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d4add-120">Quando uma entrada de despesa é enviada para um projeto que está mapeado para uma linha de contrato de preço fixo, uma linha do diário é criada apenas para custo.</span><span class="sxs-lookup"><span data-stu-id="d4add-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="d4add-121">A lógica para inserir preços padrão para despesas se baseia na categoria da despesa que é selecionada na página **Entrada de despesa**.</span><span class="sxs-lookup"><span data-stu-id="d4add-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="d4add-122">A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada.</span><span class="sxs-lookup"><span data-stu-id="d4add-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d4add-123">No entanto, para o preço em si, o valor que o usuário inseriu é definido diretamente nas linhas de diário da despesa relacionadas para custo e vendas por padrão.</span><span class="sxs-lookup"><span data-stu-id="d4add-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="d4add-124">Na versão atual do PSA, a entrada baseada em categoria dos preços padrão por unidade nas entradas de despesa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="d4add-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="d4add-125">Usando Diários de entrada para registrar custos</span><span class="sxs-lookup"><span data-stu-id="d4add-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="d4add-126">No PSA, os Diários de entrada permitem registrar o custo ou a receita nas classes de material, valor, hora, despesa ou transação de imposto.</span><span class="sxs-lookup"><span data-stu-id="d4add-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d4add-127">Um diário possui um cabeçalho, linhas e uma ação **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="d4add-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="d4add-128">Veja a seguir alguns cenários onde você pode usar um diário:</span><span class="sxs-lookup"><span data-stu-id="d4add-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="d4add-129">Você deve registrar os custos reais de material e as vendas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="d4add-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="d4add-130">Você deve mover dados reais da transação de outro sistema para o PSA.</span><span class="sxs-lookup"><span data-stu-id="d4add-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="d4add-131">Você deve registrar os custos que ocorreram em outro sistema, como custos de aquisição ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="d4add-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4add-132">O uso de Diários de entrada para criar dados reais deve ser realizado somente por um usuário totalmente ciente do impacto contábil que os Dados reais têm no projeto.</span><span class="sxs-lookup"><span data-stu-id="d4add-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="d4add-133">Isso ocorre porque o aplicativo não valida o tipo de linha do diário, ou o preço relacionado inserido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="d4add-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d4add-134">Devido ao impacto desse tipo de diário, é necessário ter cautela ao determinar para quem conceder acesso para a criação de Diários de entrada.</span><span class="sxs-lookup"><span data-stu-id="d4add-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="d4add-135">Registrando dados reais baseados em eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-135">Recording actuals based on project events</span></span>

<span data-ttu-id="d4add-136">Os PSA registra as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="d4add-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d4add-137">Essas transações são registradas como **dados reais**.</span><span class="sxs-lookup"><span data-stu-id="d4add-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="d4add-138">As tabelas a seguir mostram os diferentes tipos de dados reais que são criados de acordo com o tipo de projeto; se é de preço fixo ou de tempo e materiais, se está no estágio da venda ou se está em um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="d4add-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="d4add-139">**O recurso pertence à mesma unidade organizacional que a unidade de contratação do projeto**</span><span class="sxs-lookup"><span data-stu-id="d4add-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d4add-140">Evento</span><span class="sxs-lookup"><span data-stu-id="d4add-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d4add-141">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="d4add-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d4add-142">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="d4add-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d4add-143">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="d4add-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d4add-144">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="d4add-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d4add-145">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d4add-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d4add-146">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="d4add-146">Actuals</span></span></th>
<th><span data-ttu-id="d4add-147">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="d4add-147">Transaction currency</span></span></th>
<th><span data-ttu-id="d4add-148">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d4add-148">Fixed price</span></span></th>
<th><span data-ttu-id="d4add-149">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="d4add-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4add-150">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="d4add-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d4add-151">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="d4add-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-152">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="d4add-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d4add-153">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="d4add-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4add-154">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="d4add-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d4add-155">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-155">Cost actual</span></span></td>
<td><span data-ttu-id="d4add-156">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-157">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-158">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d4add-159">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-160">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-161">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="d4add-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d4add-162">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4add-163">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="d4add-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d4add-164">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-164">Cost actual</span></span></td>
<td><span data-ttu-id="d4add-165">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-166">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-167">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-168">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-169">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-170">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d4add-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d4add-171">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-172">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="d4add-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4add-173">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4add-174">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="d4add-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d4add-175">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="d4add-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d4add-176">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-177">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="d4add-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-178">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-179">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-180">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-181">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="d4add-181">Billed sales</span></span></td>
<td><span data-ttu-id="d4add-182">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4add-183">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="d4add-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d4add-184">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="d4add-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d4add-185">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-187">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-188">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-189">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-190">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d4add-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d4add-191">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-192">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="d4add-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4add-193">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4add-194">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="d4add-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d4add-195">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="d4add-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d4add-196">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d4add-197">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="d4add-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d4add-198">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="d4add-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d4add-199">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d4add-200">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d4add-201">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-202">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="d4add-202">Billed sales</span></span></td>
<td><span data-ttu-id="d4add-203">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4add-204">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="d4add-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d4add-205">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="d4add-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d4add-206">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-207">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d4add-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d4add-208">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-209">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="d4add-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4add-210">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4add-211">**O recurso pertence à uma unidade organizacional que é diferente da unidade de contratação do projeto**</span><span class="sxs-lookup"><span data-stu-id="d4add-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d4add-212">Evento</span><span class="sxs-lookup"><span data-stu-id="d4add-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d4add-213">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="d4add-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d4add-214">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="d4add-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d4add-215">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="d4add-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d4add-216">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="d4add-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d4add-217">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d4add-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d4add-218">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="d4add-218">Actuals</span></span></th>
<th><span data-ttu-id="d4add-219">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="d4add-219">Transaction currency</span></span></th>
<th><span data-ttu-id="d4add-220">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d4add-220">Fixed price</span></span></th>
<th><span data-ttu-id="d4add-221">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="d4add-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4add-222">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="d4add-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d4add-223">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="d4add-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-224">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="d4add-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d4add-225">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="d4add-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d4add-226">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="d4add-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d4add-227">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-227">Cost actual</span></span></td>
<td><span data-ttu-id="d4add-228">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d4add-229">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d4add-230">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d4add-231">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d4add-232">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-233">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="d4add-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d4add-234">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-235">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d4add-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d4add-236">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d4add-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-237">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="d4add-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d4add-238">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d4add-239">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="d4add-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d4add-240">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-240">Cost actual</span></span></td>
<td><span data-ttu-id="d4add-241">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d4add-242">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d4add-243">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d4add-244">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d4add-245">Custo real</span><span class="sxs-lookup"><span data-stu-id="d4add-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-246">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d4add-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d4add-247">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d4add-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-248">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="d4add-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d4add-249">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d4add-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-250">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d4add-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d4add-251">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-252">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="d4add-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4add-253">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4add-254">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="d4add-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d4add-255">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="d4add-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d4add-256">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-257">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="d4add-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-258">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-259">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d4add-260">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-261">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="d4add-261">Billed sales</span></span></td>
<td><span data-ttu-id="d4add-262">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4add-263">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="d4add-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d4add-264">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="d4add-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d4add-265">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-267">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-268">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4add-269">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-270">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d4add-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d4add-271">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-272">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="d4add-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4add-273">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4add-274">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="d4add-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d4add-275">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="d4add-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d4add-276">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d4add-277">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="d4add-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d4add-278">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="d4add-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d4add-279">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d4add-280">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d4add-281">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d4add-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-282">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="d4add-282">Billed sales</span></span></td>
<td><span data-ttu-id="d4add-283">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4add-284">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="d4add-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d4add-285">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="d4add-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d4add-286">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-287">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d4add-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d4add-288">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4add-289">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="d4add-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4add-290">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="d4add-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
