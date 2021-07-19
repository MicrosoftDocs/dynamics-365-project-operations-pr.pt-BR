---
title: Dados reais
description: Este tópico oferece informações sobre como trabalhar com dados reais no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368597"
---
# <a name="actuals"></a><span data-ttu-id="676d6-103">Dados Reais</span><span class="sxs-lookup"><span data-stu-id="676d6-103">Actuals</span></span> 

<span data-ttu-id="676d6-104">_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="676d6-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="676d6-105">Os dados reais representam o progresso financeiro revisado e aprovado e da agenda em um projeto.</span><span class="sxs-lookup"><span data-stu-id="676d6-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="676d6-106">Eles são criados como resultado de aprovação de tempo, despesas, entradas de uso de material e entradas de diário e faturas.</span><span class="sxs-lookup"><span data-stu-id="676d6-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="676d6-107">Linhas do diário e envio de horas</span><span class="sxs-lookup"><span data-stu-id="676d6-107">Journal lines and time submission</span></span>

<span data-ttu-id="676d6-108">Para obter mais informações sobre a entrada de hora, consulte [Visão geral de entrada de hora](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="676d6-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="676d6-109">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="676d6-109">Time and materials</span></span>

<span data-ttu-id="676d6-110">Quando uma entrada de hora enviada está vinculada a um projeto mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas de diário, uma para custo e a outra para vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="676d6-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="676d6-111">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="676d6-111">Fixed price</span></span>

<span data-ttu-id="676d6-112">Quando uma entrada enviada está vinculada a um projeto que está mapeado para uma linha de contrato de preço fixo, o sistema cria uma linha de diário para custo.</span><span class="sxs-lookup"><span data-stu-id="676d6-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="676d6-113">Preço padrão</span><span class="sxs-lookup"><span data-stu-id="676d6-113">Default pricing</span></span>

<span data-ttu-id="676d6-114">A lógica para criar preços padrão reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="676d6-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="676d6-115">Os valores de campo da entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="676d6-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="676d6-116">Esses valores incluem a data da transação, a linha de contrato para a qual o projeto está mapeado e o resultado da moeda na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="676d6-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="676d6-117">Os campos que afetam preços padrão, como **Função** e **Unidade de Recursos**, são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="676d6-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="676d6-118">Você pode adicionar um campo personalizado à entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="676d6-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="676d6-119">Se quiser que o valor do campo seja propagado para reais, crie o campo nas tabelas **Dados Reais** e **Linha do Diário**.</span><span class="sxs-lookup"><span data-stu-id="676d6-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="676d6-120">Use o código personalizado para propagar o valor do campo selecionado de Entrada de Hora para Dados Reais pela linha de diário usando origens de transação.</span><span class="sxs-lookup"><span data-stu-id="676d6-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="676d6-121">Para obter mais informações sobre origens de transação e conexões, consulte [Vinculando Dados Reais a registros originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="676d6-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="676d6-122">Linhas de diário e envio de despesas básicas</span><span class="sxs-lookup"><span data-stu-id="676d6-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="676d6-123">Para obter mais informações sobre a entrada de despesa, consulte [Visão geral de despesas](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="676d6-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="676d6-124">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="676d6-124">Time and materials</span></span>

<span data-ttu-id="676d6-125">Quando uma entrada de despesa básica enviada está vinculada a um projeto mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas de diário, uma para custo e a outra para vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="676d6-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="676d6-126">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="676d6-126">Fixed price</span></span>

<span data-ttu-id="676d6-127">Quando uma entrada de despesa básica enviada é vinculada a um projeto que está mapeado para uma linha de contrato de preço fixo, o sistema cria uma linha do diário para custo.</span><span class="sxs-lookup"><span data-stu-id="676d6-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="676d6-128">Preço padrão</span><span class="sxs-lookup"><span data-stu-id="676d6-128">Default pricing</span></span>

<span data-ttu-id="676d6-129">A lógica para inserir preços padrão para despesas é baseada na categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="676d6-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="676d6-130">A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada.</span><span class="sxs-lookup"><span data-stu-id="676d6-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="676d6-131">Os campos que afetam preços padrão, como **Categoria da Transação** e **Unidade**, são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="676d6-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="676d6-132">No entanto, isso funciona somente quando o método de precificação na lista de preços for **Preço por unidade**.</span><span class="sxs-lookup"><span data-stu-id="676d6-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="676d6-133">Se o método de precificação for **A preço de custo** ou **Markup sobre custo**, o preço inserido quando a entrada de despesa é criada é usado para o custo e o preço na linha de diário de vendas é calculado com base no método de precificação.</span><span class="sxs-lookup"><span data-stu-id="676d6-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="676d6-134">Você pode adicionar um campo personalizado na entrada de despesa.</span><span class="sxs-lookup"><span data-stu-id="676d6-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="676d6-135">Se quiser que o valor do campo seja propagado para reais, crie o campo nas tabelas **Dados Reais** e **Linha do Diário**.</span><span class="sxs-lookup"><span data-stu-id="676d6-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="676d6-136">Use o código personalizado para propagar o valor do campo selecionado de Entrada de Hora para Dados Reais pela linha de diário usando origens de transação.</span><span class="sxs-lookup"><span data-stu-id="676d6-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="676d6-137">Para obter mais informações sobre origens de transação e conexões, consulte [Vinculando Dados Reais a registros originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="676d6-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="676d6-138">Linhas de diário e envio de log de uso de material</span><span class="sxs-lookup"><span data-stu-id="676d6-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="676d6-139">Para obter mais informações sobre entrada de despesa, consulte [Log de Uso de Material](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="676d6-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="676d6-140">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="676d6-140">Time and materials</span></span>

<span data-ttu-id="676d6-141">Quando uma entrada de log de uso de material enviada for vinculada a um projeto mapeado para uma linha de contrato de tempo e material, o sistema criará duas linhas de diário, uma para custo e outra para vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="676d6-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="676d6-142">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="676d6-142">Fixed price</span></span>

<span data-ttu-id="676d6-143">Quando uma entrada de uso de material enviada é vinculada a um projeto que está mapeado para uma linha de contrato de preço fixo, o sistema cria uma linha do diário para custo.</span><span class="sxs-lookup"><span data-stu-id="676d6-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="676d6-144">Preço padrão</span><span class="sxs-lookup"><span data-stu-id="676d6-144">Default pricing</span></span>

<span data-ttu-id="676d6-145">A lógica para inserir preços padrão para material é baseada na combinação de produto e unidade.</span><span class="sxs-lookup"><span data-stu-id="676d6-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="676d6-146">A data da transação, a linha de contrato para a qual o projeto é mapeado e a moeda são usados para determinar a lista de preços adequada.</span><span class="sxs-lookup"><span data-stu-id="676d6-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="676d6-147">Os campos que afetam preços padrão, como **ID do Produto** e **Unidade**, são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="676d6-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="676d6-148">No entanto, isso funciona apenas para produtos do catálogo.</span><span class="sxs-lookup"><span data-stu-id="676d6-148">However, this only works for catalog products.</span></span> <span data-ttu-id="676d6-149">Para produtos fora do catálogo, o preço inserido quando a entrada de log de uso de material é criada é usado para o custo e o preço de vendas nas linhas do diário.</span><span class="sxs-lookup"><span data-stu-id="676d6-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="676d6-150">Você pode adicionar um campo personalizado na entrada **Log de Uso de Material**.</span><span class="sxs-lookup"><span data-stu-id="676d6-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="676d6-151">Se quiser que o valor do campo seja propagado para reais, crie o campo nas tabelas **Dados Reais** e **Linha do Diário**.</span><span class="sxs-lookup"><span data-stu-id="676d6-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="676d6-152">Use o código personalizado para propagar o valor do campo selecionado de Entrada de Hora para Dados Reais pela linha de diário usando origens de transação.</span><span class="sxs-lookup"><span data-stu-id="676d6-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="676d6-153">Para obter mais informações sobre origens de transação e conexões, consulte [Vinculando Dados Reais a registros originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="676d6-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="676d6-154">Usar diários de entrada para registrar custos</span><span class="sxs-lookup"><span data-stu-id="676d6-154">Use entry journals to record costs</span></span>

<span data-ttu-id="676d6-155">Você pode usar diários de entrada para registrar o custo ou receita nas classes de material, valor, hora, despesa ou transação de imposto.</span><span class="sxs-lookup"><span data-stu-id="676d6-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="676d6-156">Os diários podem ser usados para as seguintes finalidades:</span><span class="sxs-lookup"><span data-stu-id="676d6-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="676d6-157">Mova os dados reais de transações de outro sistema para o Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="676d6-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="676d6-158">Registre os custos que ocorreram em outro sistema.</span><span class="sxs-lookup"><span data-stu-id="676d6-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="676d6-159">Esses custos podem incluir custos de aquisição ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="676d6-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="676d6-160">O aplicativo não valida o tipo de linha do diário ou o preço relacionado inserido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="676d6-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="676d6-161">Portanto, somente um usuário que está totalmente ciente do impacto contábil que os dados reais têm no projeto devem usar diários de entrada para criar os dados reais.</span><span class="sxs-lookup"><span data-stu-id="676d6-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="676d6-162">Devido ao impacto deste tipo de diário, é necessário escolher cuidadosamente quem tem acesso para criar diários de entrada.</span><span class="sxs-lookup"><span data-stu-id="676d6-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="676d6-163">Registrar dados reais baseados em eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-163">Record actuals based on project events</span></span>

<span data-ttu-id="676d6-164">O Project Operations registra as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="676d6-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="676d6-165">Essas transações são registradas como dados reais.</span><span class="sxs-lookup"><span data-stu-id="676d6-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="676d6-166">As tabelas a seguir mostram os diferentes tipos de dados reais que são criados de acordo com o tipo de projeto; se é de preço fixo ou de tempo e materiais, se está no estágio da venda ou se está em um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="676d6-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="676d6-167">O recurso pertence à mesma unidade organizacional que a unidade de contratação do projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="676d6-168">Evento</span><span class="sxs-lookup"><span data-stu-id="676d6-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="676d6-169">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="676d6-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="676d6-170">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="676d6-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="676d6-171">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="676d6-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="676d6-172">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="676d6-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="676d6-173">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="676d6-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="676d6-174">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="676d6-174">Actuals</span></span></th>
<th><span data-ttu-id="676d6-175">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="676d6-175">Transaction currency</span></span></th>
<th><span data-ttu-id="676d6-176">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="676d6-176">Fixed price</span></span></th>
<th><span data-ttu-id="676d6-177">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="676d6-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="676d6-178">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="676d6-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="676d6-179">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="676d6-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-180">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="676d6-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="676d6-181">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="676d6-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="676d6-182">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="676d6-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="676d6-183">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-183">Cost actual</span></span></td>
<td><span data-ttu-id="676d6-184">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-185">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-186">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="676d6-187">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-188">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-189">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="676d6-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="676d6-190">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="676d6-191">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="676d6-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="676d6-192">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-192">Cost actual</span></span></td>
<td><span data-ttu-id="676d6-193">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-194">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-195">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-196">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-197">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-198">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="676d6-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="676d6-199">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-200">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="676d6-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="676d6-201">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="676d6-202">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="676d6-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="676d6-203">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="676d6-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="676d6-204">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-205">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="676d6-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-206">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-207">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-208">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-209">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="676d6-209">Billed sales</span></span></td>
<td><span data-ttu-id="676d6-210">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="676d6-211">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="676d6-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="676d6-212">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="676d6-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="676d6-213">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-214">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-215">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-216">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-217">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-218">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="676d6-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="676d6-219">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-220">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="676d6-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="676d6-221">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="676d6-222">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="676d6-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="676d6-223">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="676d6-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="676d6-224">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="676d6-225">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="676d6-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="676d6-226">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="676d6-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="676d6-227">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="676d6-228">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="676d6-229">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-230">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="676d6-230">Billed sales</span></span></td>
<td><span data-ttu-id="676d6-231">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="676d6-232">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="676d6-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="676d6-233">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="676d6-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="676d6-234">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-235">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="676d6-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="676d6-236">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-237">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="676d6-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="676d6-238">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="676d6-239">O recurso pertence à uma unidade organizacional que é diferente da unidade de contratação do projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="676d6-240">Evento</span><span class="sxs-lookup"><span data-stu-id="676d6-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="676d6-241">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="676d6-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="676d6-242">Projeto no estágio de pré-venda</span><span class="sxs-lookup"><span data-stu-id="676d6-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="676d6-243">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="676d6-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="676d6-244">Tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="676d6-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="676d6-245">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="676d6-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="676d6-246">Dados Efetivos</span><span class="sxs-lookup"><span data-stu-id="676d6-246">Actuals</span></span></th>
<th><span data-ttu-id="676d6-247">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="676d6-247">Transaction currency</span></span></th>
<th><span data-ttu-id="676d6-248">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="676d6-248">Fixed price</span></span></th>
<th><span data-ttu-id="676d6-249">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="676d6-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="676d6-250">Uma entrada de hora é criada.</span><span class="sxs-lookup"><span data-stu-id="676d6-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="676d6-251">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="676d6-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-252">Uma entrada de hora é enviada.</span><span class="sxs-lookup"><span data-stu-id="676d6-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="676d6-253">Nenhuma atividade na entidade Dados Reais</span><span class="sxs-lookup"><span data-stu-id="676d6-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="676d6-254">A hora é aprovada, e não ocorre qualquer alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="676d6-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="676d6-255">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-255">Cost actual</span></span></td>
<td><span data-ttu-id="676d6-256">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="676d6-257">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="676d6-258">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="676d6-259">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="676d6-260">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-261">Vendas reais não cobradas – passível de cobrança</span><span class="sxs-lookup"><span data-stu-id="676d6-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="676d6-262">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-263">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="676d6-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="676d6-264">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="676d6-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-265">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="676d6-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="676d6-266">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="676d6-267">A hora é aprovada e ocorre uma redução nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="676d6-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="676d6-268">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-268">Cost actual</span></span></td>
<td><span data-ttu-id="676d6-269">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="676d6-270">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="676d6-271">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="676d6-272">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="676d6-273">Custo real</span><span class="sxs-lookup"><span data-stu-id="676d6-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-274">Custo da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="676d6-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="676d6-275">Moeda da unidade de recursos</span><span class="sxs-lookup"><span data-stu-id="676d6-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-276">Vendas entre organizações</span><span class="sxs-lookup"><span data-stu-id="676d6-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="676d6-277">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="676d6-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-278">Vendas reais não cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="676d6-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="676d6-279">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-280">Vendas reais não cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="676d6-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="676d6-281">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="676d6-282">Uma fatura é confirmada e não ocorrem alterações nem aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="676d6-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="676d6-283">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="676d6-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="676d6-284">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-285">Vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="676d6-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-286">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-287">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="676d6-288">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-289">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="676d6-289">Billed sales</span></span></td>
<td><span data-ttu-id="676d6-290">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="676d6-291">Uma fatura é confirmada e ocorre uma redução nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="676d6-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="676d6-292">Reversão de vendas não cobradas</span><span class="sxs-lookup"><span data-stu-id="676d6-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="676d6-293">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-294">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-295">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-296">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="676d6-297">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-298">Vendas cobradas – passível de cobrança para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="676d6-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="676d6-299">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-300">Vendas cobradas – não passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="676d6-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="676d6-301">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="676d6-302">Uma fatura é corrigida para aumento da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="676d6-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="676d6-303">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="676d6-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="676d6-304">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="676d6-305">Estorno de vendas cobradas por etapa</span><span class="sxs-lookup"><span data-stu-id="676d6-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="676d6-306">Alteração no status da etapa, de <strong>Faturado</strong> para <strong>Pronto para fatura</strong></span><span class="sxs-lookup"><span data-stu-id="676d6-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="676d6-307">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="676d6-308">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="676d6-309">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="676d6-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-310">Vendas cobradas</span><span class="sxs-lookup"><span data-stu-id="676d6-310">Billed sales</span></span></td>
<td><span data-ttu-id="676d6-311">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="676d6-312">Uma fatura é corrigida para redução da quantidade passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="676d6-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="676d6-313">Vendas cobradas – estorno</span><span class="sxs-lookup"><span data-stu-id="676d6-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="676d6-314">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-315">Vendas cobradas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="676d6-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="676d6-316">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="676d6-317">Vendas não cobradas – passível de cobrança para a diferença</span><span class="sxs-lookup"><span data-stu-id="676d6-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="676d6-318">Moeda de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="676d6-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
