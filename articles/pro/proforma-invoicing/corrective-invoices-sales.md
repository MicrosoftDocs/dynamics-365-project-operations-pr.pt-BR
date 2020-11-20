---
title: Créditos e faturas corrigidas
description: Este tópico fornece informações sobre faturas corrigidas no Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071539"
---
# <a name="credits-and-corrected-invoices"></a><span data-ttu-id="630b1-103">Créditos e faturas corrigidas</span><span class="sxs-lookup"><span data-stu-id="630b1-103">Credits and corrected invoices</span></span>

<span data-ttu-id="630b1-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="630b1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="630b1-105">Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos negociados com o cliente e o gerente de projeto.</span><span class="sxs-lookup"><span data-stu-id="630b1-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="630b1-106">Para fazer edições em uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**.</span><span class="sxs-lookup"><span data-stu-id="630b1-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="630b1-107">Esta seleção não estará disponível a menos que uma fatura do projeto seja confirmada.</span><span class="sxs-lookup"><span data-stu-id="630b1-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="630b1-108">Um novo esboço de fatura é criado da fatura confirmada.</span><span class="sxs-lookup"><span data-stu-id="630b1-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="630b1-109">Todos os detalhes da linha da fatura confirmada anteriormente são copiados para o novo rascunho.</span><span class="sxs-lookup"><span data-stu-id="630b1-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="630b1-110">A seguir estão alguns dos pontos-chave para entender sobre os detalhes da linha na nova fatura corrigida:</span><span class="sxs-lookup"><span data-stu-id="630b1-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="630b1-111">Todas as quantidades são atualizadas para zero.</span><span class="sxs-lookup"><span data-stu-id="630b1-111">All quantities are updated to zero.</span></span> <span data-ttu-id="630b1-112">O aplicativo assume que todos os itens faturados estejam totalmente creditados.</span><span class="sxs-lookup"><span data-stu-id="630b1-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="630b1-113">Se necessário, você pode atualizar manualmente essas quantidades para refletir a quantidade que está sendo faturada, e não a quantidade que está sendo creditada.</span><span class="sxs-lookup"><span data-stu-id="630b1-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="630b1-114">Com base na quantidade inserida, o aplicativo calcula a quantidade creditada.</span><span class="sxs-lookup"><span data-stu-id="630b1-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="630b1-115">Esse valor é refletido nos valores reais criados quando a fatura corrigida é confirmada.</span><span class="sxs-lookup"><span data-stu-id="630b1-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="630b1-116">Se você estiver fazendo alterações no valor do imposto, deverá inserir o valor correto do imposto e não o valor do imposto que está sendo creditado.</span><span class="sxs-lookup"><span data-stu-id="630b1-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="630b1-117">Linhas de contrato baseadas em produto previamente confirmadas não são copiadas.</span><span class="sxs-lookup"><span data-stu-id="630b1-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="630b1-118">O processamento de correções em uma fatura de projeto com base no produto não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="630b1-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="630b1-119">As correções de marcos são sempre processadas como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="630b1-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="630b1-120">Os valores retidos ou adiantados poderão ser corrigidos se o cliente tiver sido faturado com um valor incorreto.</span><span class="sxs-lookup"><span data-stu-id="630b1-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="630b1-121">As reconciliações de retenções e adiantamentos podem ser corrigidas se um valor incorreto tiver sido usado para reconciliar com os encargos em uma fatura previamente confirmada.</span><span class="sxs-lookup"><span data-stu-id="630b1-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="630b1-122">Os detalhes da linha da fatura que são correções para outras despesas já faturadas têm o campo **Correção** definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="630b1-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="630b1-123">As faturas com os detalhes da linha da fatura corrigidos têm um campo chamado **Tem correções** , que também está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="630b1-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="630b1-124">Reais criados na Confirmação de uma fatura corretiva:</span><span class="sxs-lookup"><span data-stu-id="630b1-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="630b1-125">Abaixo estão os dados reais criados pelo aplicativo na confirmação de um corretivo com base nas operações realizadas no projeto de fatura corretiva antes da confirmação.</span><span class="sxs-lookup"><span data-stu-id="630b1-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="630b1-126">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="630b1-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="630b1-127">
                    <strong>Reais criados na confirmação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="630b1-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="630b1-128">Confirme a correção de um adiantamento ou honorário faturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="630b1-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-129">Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="630b1-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="630b1-130">Esse valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="630b1-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-131">Um estorno real de vendas faturadas é criado para o valor nos honorários ou adiantamento para estornar as vendas faturadas originais.</span><span class="sxs-lookup"><span data-stu-id="630b1-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-132">Uma nova venda cobrada real é criada para o valor corrigido na linha de fatura corrigida com base em honorários ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="630b1-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-133">Uma venda não cobrada real de um valor negativo da linha de fatura corrigida com base em honorários ou adiantamento, que será usada para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="630b1-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="630b1-134">Uma confirmação da correção de honorários ou adiantamento previamente reconciliados.</span><span class="sxs-lookup"><span data-stu-id="630b1-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-135">Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="630b1-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="630b1-136">Esse valor é positivo e se destina a anular o valor negativo gerado no momento em que a reconciliação anterior ocorreu.</span><span class="sxs-lookup"><span data-stu-id="630b1-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-137">Um estorno de venda cobrada real para o valor na fatura anterior.</span><span class="sxs-lookup"><span data-stu-id="630b1-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-138">Uma nova venda cobrada real para o valor de honorários corrigido que é aplicado na fatura corrigida.</span><span class="sxs-lookup"><span data-stu-id="630b1-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-139">Uma venda não cobrada real com um valor negativo dos honorários ou adiantamento restantes corrigidos, que será usado para reconciliação em faturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="630b1-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="630b1-140">Faturamento do crédito total de uma transação de tempo faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="630b1-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-141">Um estorno de venda cobrada pelas horas e o valor no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="630b1-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-142">Uma nova venda não cobrada real pelas horas e o valor no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="630b1-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="630b1-143">Faturamento do crédito parcial em uma transação de tempo.</span><span class="sxs-lookup"><span data-stu-id="630b1-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-144">Um estorno de venda cobrada pelas horas e o valor faturado no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="630b1-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-145">Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="630b1-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-146">Uma nova venda não cobrada real que é passível de cobrança pelas horas e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.</span><span class="sxs-lookup"><span data-stu-id="630b1-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="630b1-147">Faturamento do crédito total de uma transação de despesa faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="630b1-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-148">Um estorno de venda cobrada pela quantidade e o valor no detalhe da linha de fatura original para a despesa.</span><span class="sxs-lookup"><span data-stu-id="630b1-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-149">Uma nova venda não cobrada real pela quantidade e o valor no detalhe da linha de fatura original para a despesa.</span><span class="sxs-lookup"><span data-stu-id="630b1-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="630b1-150">Faturamento do crédito parcial de uma transação de despesa faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="630b1-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-151">Um estorno de venda cobrada pela quantidade e o valor faturados no detalhe da linha de fatura original para uma despesa.</span><span class="sxs-lookup"><span data-stu-id="630b1-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-152">Uma nova venda real não faturada que é passível de cobrança pela quantidade e o valor no detalhe da linha da fatura corrigida, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="630b1-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-153">Uma nova venda não cobrada real que é passível de cobrança pela quantidade e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.</span><span class="sxs-lookup"><span data-stu-id="630b1-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="630b1-154">Faturamento do crédito total de uma transação de valor faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="630b1-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-155">Um estorno de venda cobrada pela quantidade e o valor no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="630b1-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-156">Uma nova venda não cobrada real pela quantidade e o valor no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="630b1-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="630b1-157">Faturamento do crédito parcial de uma transação de valor faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="630b1-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-158">Um estorno de venda cobrada pela quantidade e o valor faturados no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="630b1-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-159">Uma nova venda não cobrada real que é passível de cobrança pela quantidade e o valor no detalhe da linha da fatura corretiva editada, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="630b1-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="630b1-160">Faturamento do crédito total de um marco faturado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="630b1-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-161">Um estorno de venda cobrada pelas horas e o valor no detalhe da linha de fatura original para o marco.</span><span class="sxs-lookup"><span data-stu-id="630b1-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="630b1-162">A fatura do marco ou o status do cobrança na linha de contrato do projeto é atualizada para **Pronta para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="630b1-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="630b1-163">Faturamento do crédito parcial de um marco faturado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="630b1-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-164">Com suporte</span><span class="sxs-lookup"><span data-stu-id="630b1-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="630b1-165">Créditos e correções de uma linha de contrato com base em produto previamente faturado.</span><span class="sxs-lookup"><span data-stu-id="630b1-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="630b1-166">Com suporte</span><span class="sxs-lookup"><span data-stu-id="630b1-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>