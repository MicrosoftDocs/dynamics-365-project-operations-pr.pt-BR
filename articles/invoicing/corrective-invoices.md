---
title: Criar faturas baseadas em projeto
description: Este tópico fornece informações sobre faturas corretivas no Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001593"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="52413-103">Criar faturas baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="52413-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="52413-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="52413-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="52413-105">Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos negociados com o cliente e o gerente de projeto.</span><span class="sxs-lookup"><span data-stu-id="52413-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="52413-106">Para fazer edições em uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**.</span><span class="sxs-lookup"><span data-stu-id="52413-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="52413-107">Esta seleção não estará disponível a menos que uma fatura do projeto seja confirmada.</span><span class="sxs-lookup"><span data-stu-id="52413-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="52413-108">Um novo esboço de fatura é criado da fatura confirmada.</span><span class="sxs-lookup"><span data-stu-id="52413-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="52413-109">Todos os detalhes da linha da fatura confirmada anteriormente são copiados para o novo rascunho.</span><span class="sxs-lookup"><span data-stu-id="52413-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="52413-110">A seguir estão alguns pontos-chave para ajudá-lo a entender mais sobre os detalhes da linha na nova fatura corrigida:</span><span class="sxs-lookup"><span data-stu-id="52413-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="52413-111">Todas as quantidades são atualizadas para zero.</span><span class="sxs-lookup"><span data-stu-id="52413-111">All quantities are updated to zero.</span></span> <span data-ttu-id="52413-112">Isso presumo que todos os itens faturados são totalmente creditados.</span><span class="sxs-lookup"><span data-stu-id="52413-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="52413-113">Se necessário, você pode atualizar manualmente essas quantidades para refletir a quantidade que está sendo faturada, e não a quantidade que está sendo creditada.</span><span class="sxs-lookup"><span data-stu-id="52413-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="52413-114">Com base na quantidade inserida, o aplicativo calcula a quantidade creditada.</span><span class="sxs-lookup"><span data-stu-id="52413-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="52413-115">Esse valor é refletido nos valores reais criados quando a fatura corrigida é confirmada.</span><span class="sxs-lookup"><span data-stu-id="52413-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="52413-116">Se você estiver fazendo alterações no valor do imposto, deverá inserir o valor correto do imposto e não o valor do imposto que está sendo creditado.</span><span class="sxs-lookup"><span data-stu-id="52413-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="52413-117">As correções de marcos são sempre processadas como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="52413-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="52413-118">Os valores retidos ou adiantados poderão ser corrigidos se o cliente tiver sido faturado com um valor incorreto.</span><span class="sxs-lookup"><span data-stu-id="52413-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="52413-119">As reconciliações de retenções e adiantamentos podem ser corrigidas se um valor incorreto tiver sido usado para reconciliar com os encargos em uma fatura previamente confirmada.</span><span class="sxs-lookup"><span data-stu-id="52413-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52413-120">Os detalhes de linha de fatura que são correções para outros encargos já faturados têm o campo **Correção** definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="52413-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="52413-121">As faturas com os detalhes da linha da fatura corrigidos têm um campo chamado **Tem correções**, que também está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="52413-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="52413-122">Os valores reais criados na confirmação de uma fatura corretiva</span><span class="sxs-lookup"><span data-stu-id="52413-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="52413-123">A tabela a seguir lista os valores reais criados quando uma fatura corretiva é confirmada.</span><span class="sxs-lookup"><span data-stu-id="52413-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="52413-124">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="52413-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="52413-125">
                    <strong>Reais criados na confirmação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="52413-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="52413-126">Confirme a correção de um adiantamento ou honorário faturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="52413-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-127">Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="52413-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="52413-128">Esse valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="52413-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-129">Um estorno real de vendas faturadas é criado para o valor nos honorários ou adiantamento para estornar as vendas faturadas originais.</span><span class="sxs-lookup"><span data-stu-id="52413-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-130">Uma nova venda cobrada real é criada para o valor corrigido na linha de fatura corrigida com base em honorários ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="52413-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-131">Uma venda não cobrada real de um valor negativo da linha de fatura corrigida com base em honorários ou adiantamento, que será usada para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="52413-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="52413-132">Uma confirmação da correção de honorários ou adiantamento previamente reconciliados.</span><span class="sxs-lookup"><span data-stu-id="52413-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-133">Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="52413-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="52413-134">Esse valor é positivo e se destina a anular o valor negativo gerado no momento em que a reconciliação anterior ocorreu.</span><span class="sxs-lookup"><span data-stu-id="52413-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-135">Um estorno de venda cobrada real para o valor na fatura anterior.</span><span class="sxs-lookup"><span data-stu-id="52413-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-136">Uma nova venda cobrada real para o valor de honorários corrigido que é aplicado na fatura corrigida.</span><span class="sxs-lookup"><span data-stu-id="52413-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-137">Uma venda não cobrada real com um valor negativo dos honorários ou adiantamento restantes corrigidos, que será usado para reconciliação em faturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="52413-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52413-138">Faturamento do crédito total de uma transação de tempo faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52413-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-139">Um estorno de venda cobrada pelas horas e o valor no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="52413-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-140">Uma nova venda não cobrada real pelas horas e o valor no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="52413-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="52413-141">Faturamento do crédito parcial em uma transação de tempo.</span><span class="sxs-lookup"><span data-stu-id="52413-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-142">Um estorno de venda cobrada pelas horas e o valor faturado no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="52413-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-143">Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="52413-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-144">Uma nova venda não cobrada real que é passível de cobrança pelas horas e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.</span><span class="sxs-lookup"><span data-stu-id="52413-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52413-145">Faturamento do crédito total de uma transação de despesa faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52413-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-146">Um estorno de venda cobrada pela quantidade e o valor no detalhe da linha de fatura original para a despesa.</span><span class="sxs-lookup"><span data-stu-id="52413-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-147">Uma nova venda não cobrada real pela quantidade e o valor no detalhe da linha de fatura original para a despesa.</span><span class="sxs-lookup"><span data-stu-id="52413-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="52413-148">Faturamento do crédito parcial de uma transação de despesa faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52413-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-149">Um estorno de venda cobrada pela quantidade e o valor faturados no detalhe da linha de fatura original para uma despesa.</span><span class="sxs-lookup"><span data-stu-id="52413-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-150">Uma nova venda real não faturada que é passível de cobrança pela quantidade e o valor no detalhe da linha da fatura corrigida, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="52413-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-151">Uma nova venda não cobrada real que é passível de cobrança pela quantidade e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.</span><span class="sxs-lookup"><span data-stu-id="52413-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52413-152">Faturamento do crédito total de uma transação de valor faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52413-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-153">Um estorno de venda cobrada pela quantidade e o valor no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="52413-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-154">Uma nova venda não cobrada real pela quantidade e o valor no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="52413-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52413-155">Faturamento do crédito parcial de uma transação de valor faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52413-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-156">Um estorno de venda cobrada pela quantidade e o valor faturados no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="52413-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-157">Uma nova venda não cobrada real que é passível de cobrança pela quantidade e o valor no detalhe da linha da fatura corretiva editada, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="52413-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="52413-158">Faturamento do crédito total de um marco faturado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52413-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-159">Um estorno de venda cobrada pelas horas e o valor no detalhe da linha de fatura original para o marco.</span><span class="sxs-lookup"><span data-stu-id="52413-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="52413-160">O status da fatura no marco é atualizado de <b>Fatura do cliente lançada</b> para <b>Pronto para Faturar</b>.</span><span class="sxs-lookup"><span data-stu-id="52413-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="52413-161">Faturamento do crédito parcial de um marco faturado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52413-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52413-162">Com suporte</span><span class="sxs-lookup"><span data-stu-id="52413-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
