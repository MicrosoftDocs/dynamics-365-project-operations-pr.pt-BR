---
title: Visão geral dos dados reais
description: Este tópico fornece informações sobre dados reais do projeto.
author: rumant
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
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014642"
---
# <a name="actuals-overview"></a><span data-ttu-id="74675-103">Visão geral dos dados reais</span><span class="sxs-lookup"><span data-stu-id="74675-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="74675-104">Os dados reais são o volume de trabalho que foi concluído em um projeto.</span><span class="sxs-lookup"><span data-stu-id="74675-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="74675-105">Os dados reais do projeto podem ser rastreados para seus documentos de origem.</span><span class="sxs-lookup"><span data-stu-id="74675-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="74675-106">Esses documentos de origem incluem hora, despesa e entradas de diário, além de faturas.</span><span class="sxs-lookup"><span data-stu-id="74675-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Como os dados reais do projeto são rastreados para documentos de origem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="74675-108">Enviando uma entrada de hora</span><span class="sxs-lookup"><span data-stu-id="74675-108">Submitting a time entry</span></span>

<span data-ttu-id="74675-109">No PSA, quando uma entrada de hora é enviada para um projeto que está mapeado para uma linha de contrato de tempo e materiais, são criadas duas linhas de diário.</span><span class="sxs-lookup"><span data-stu-id="74675-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="74675-110">Uma linha destinada ao custo e a outra às vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="74675-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="74675-111">Quando uma entrada de hora é enviada para um projeto que está mapeado para uma linha de contrato de preço fixo, uma linha do diário é criada apenas para custo.</span><span class="sxs-lookup"><span data-stu-id="74675-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="74675-112">A lógica para inserir preços padrão reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="74675-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="74675-113">Todos os valores de campo de uma entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="74675-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="74675-114">Esses campos incluem a data da transação, a linha de contrato para a qual o projeto está mapeado e o resultado da moeda na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="74675-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="74675-115">Os campos que afetam preços padrão, como **Função** e **Unidades Organizacional**, fazem com que um preço apropriado seja inserido por padrão na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="74675-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="74675-116">Se você adicionar um campo personalizado na entrada de hora e quiser que o valor do campo seja propagado para os dados reais, crie o campo na entidade Dados Reais e use mapeamentos de campo para copiar o campo da entrada de hora para os dados reais.</span><span class="sxs-lookup"><span data-stu-id="74675-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="74675-117">Enviando uma entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="74675-117">Submitting an expense entry</span></span>

<span data-ttu-id="74675-118">No PSA, quando uma entrada de despesa é enviada para um projeto que está mapeado para uma linha de contrato de tempo e materiais, são criadas duas linhas de diário.</span><span class="sxs-lookup"><span data-stu-id="74675-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="74675-119">Uma linha destinada ao custo e a outra às vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="74675-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="74675-120">Quando uma entrada de despesa é enviada para um projeto que está mapeado para uma linha de contrato de preço fixo, uma linha do diário é criada apenas para custo.</span><span class="sxs-lookup"><span data-stu-id="74675-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="74675-121">A lógica para inserir preços padrão para despesas se baseia na categoria da despesa que é selecionada na página **Entrada de despesa**.</span><span class="sxs-lookup"><span data-stu-id="74675-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="74675-122">A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada.</span><span class="sxs-lookup"><span data-stu-id="74675-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="74675-123">No entanto, para o preço em si, o valor que o usuário inseriu é definido diretamente nas linhas de diário da despesa relacionadas para custo e vendas por padrão.</span><span class="sxs-lookup"><span data-stu-id="74675-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="74675-124">Na versão atual do PSA, a entrada baseada em categoria dos preços padrão por unidade nas entradas de despesa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="74675-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="74675-125">Usando Diários de entrada para registrar custos</span><span class="sxs-lookup"><span data-stu-id="74675-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="74675-126">No PSA, os Diários de entrada permitem registrar o custo ou a receita nas classes de material, valor, hora, despesa ou transação de imposto.</span><span class="sxs-lookup"><span data-stu-id="74675-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="74675-127">Um diário possui um cabeçalho, linhas e uma ação **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="74675-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="74675-128">Veja a seguir alguns cenários onde você pode usar um diário:</span><span class="sxs-lookup"><span data-stu-id="74675-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="74675-129">Você deve registrar os custos reais de material e as vendas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="74675-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="74675-130">Você deve mover dados reais da transação de outro sistema para o PSA.</span><span class="sxs-lookup"><span data-stu-id="74675-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="74675-131">Você deve registrar os custos que ocorreram em outro sistema, como custos de aquisição ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="74675-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74675-132">O uso de Diários de entrada para criar dados reais deve ser realizado somente por um usuário totalmente ciente do impacto contábil que os Dados reais têm no projeto.</span><span class="sxs-lookup"><span data-stu-id="74675-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="74675-133">Isso ocorre porque o aplicativo não valida o tipo de linha do diário, ou o preço relacionado inserido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="74675-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="74675-134">Devido ao impacto desse tipo de diário, é necessário ter cautela ao determinar para quem conceder acesso para a criação de Diários de entrada.</span><span class="sxs-lookup"><span data-stu-id="74675-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="74675-135">Registrando dados reais baseados em eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="74675-135">Recording actuals based on project events</span></span>

<span data-ttu-id="74675-136">Os PSA registra as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="74675-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="74675-137">Essas transações são registradas como **dados reais**.</span><span class="sxs-lookup"><span data-stu-id="74675-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="74675-138">As tabelas a seguir mostram os diferentes tipos de dados reais que são criados de acordo com o tipo de projeto; se é de preço fixo ou de tempo e materiais, se está no estágio da venda ou se está em um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="74675-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="74675-139">**O recurso pertence à mesma unidade organizacional que a unidade de contratação do projeto**</span><span class="sxs-lookup"><span data-stu-id="74675-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="74675-140">Evento</span><span class="sxs-lookup"><span data-stu-id="74675-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="74675-141">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="74675-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="74675-142">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="74675-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="74675-143">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="74675-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="74675-144">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="74675-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="74675-145">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="74675-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="74675-146">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="74675-146">Actuals</span></span></th>
<th><span data-ttu-id="74675-147">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="74675-147">Transaction currency</span></span></th>
<th><span data-ttu-id="74675-148">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="74675-148">Fixed price</span></span></th>
<th><span data-ttu-id="74675-149">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="74675-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="74675-150">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="74675-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="74675-151">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="74675-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-152">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="74675-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="74675-153">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="74675-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="74675-154">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="74675-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="74675-155">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-155">Cost actual</span></span></td>
<td><span data-ttu-id="74675-156">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-157">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-158">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="74675-159">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-160">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-161">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="74675-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="74675-162">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="74675-163">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="74675-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="74675-164">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-164">Cost actual</span></span></td>
<td><span data-ttu-id="74675-165">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-166">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-167">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-168">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-169">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-170">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="74675-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="74675-171">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-172">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="74675-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="74675-173">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="74675-174">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="74675-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="74675-175">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="74675-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="74675-176">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-177">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="74675-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-178">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-179">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-180">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-181">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="74675-181">Billed sales</span></span></td>
<td><span data-ttu-id="74675-182">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="74675-183">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="74675-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="74675-184">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="74675-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="74675-185">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-187">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-188">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-189">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-190">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="74675-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="74675-191">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-192">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="74675-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="74675-193">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="74675-194">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="74675-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="74675-195">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="74675-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="74675-196">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="74675-197">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="74675-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="74675-198">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="74675-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="74675-199">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="74675-200">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="74675-201">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-202">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="74675-202">Billed sales</span></span></td>
<td><span data-ttu-id="74675-203">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="74675-204">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="74675-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="74675-205">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="74675-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="74675-206">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-207">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="74675-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="74675-208">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-209">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="74675-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="74675-210">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="74675-211">**O recurso pertence à uma unidade organizacional que é diferente da unidade de contratação do projeto**</span><span class="sxs-lookup"><span data-stu-id="74675-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="74675-212">Evento</span><span class="sxs-lookup"><span data-stu-id="74675-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="74675-213">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="74675-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="74675-214">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="74675-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="74675-215">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="74675-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="74675-216">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="74675-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="74675-217">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="74675-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="74675-218">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="74675-218">Actuals</span></span></th>
<th><span data-ttu-id="74675-219">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="74675-219">Transaction currency</span></span></th>
<th><span data-ttu-id="74675-220">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="74675-220">Fixed price</span></span></th>
<th><span data-ttu-id="74675-221">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="74675-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="74675-222">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="74675-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="74675-223">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="74675-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-224">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="74675-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="74675-225">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="74675-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="74675-226">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="74675-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="74675-227">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-227">Cost actual</span></span></td>
<td><span data-ttu-id="74675-228">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="74675-229">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="74675-230">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="74675-231">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="74675-232">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-233">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="74675-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="74675-234">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-235">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="74675-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="74675-236">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="74675-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-237">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="74675-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="74675-238">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="74675-239">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="74675-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="74675-240">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-240">Cost actual</span></span></td>
<td><span data-ttu-id="74675-241">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="74675-242">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="74675-243">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="74675-244">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="74675-245">Custo real</span><span class="sxs-lookup"><span data-stu-id="74675-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-246">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="74675-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="74675-247">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="74675-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-248">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="74675-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="74675-249">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="74675-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-250">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="74675-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="74675-251">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-252">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="74675-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="74675-253">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="74675-254">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="74675-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="74675-255">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="74675-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="74675-256">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-257">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="74675-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-258">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-259">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="74675-260">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-261">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="74675-261">Billed sales</span></span></td>
<td><span data-ttu-id="74675-262">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="74675-263">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="74675-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="74675-264">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="74675-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="74675-265">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-267">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-268">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="74675-269">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-270">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="74675-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="74675-271">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-272">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="74675-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="74675-273">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="74675-274">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="74675-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="74675-275">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="74675-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="74675-276">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="74675-277">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="74675-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="74675-278">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="74675-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="74675-279">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="74675-280">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="74675-281">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="74675-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-282">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="74675-282">Billed sales</span></span></td>
<td><span data-ttu-id="74675-283">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="74675-284">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="74675-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="74675-285">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="74675-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="74675-286">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-287">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="74675-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="74675-288">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="74675-289">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="74675-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="74675-290">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="74675-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]