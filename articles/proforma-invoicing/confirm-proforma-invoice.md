---
title: Confirmar uma fatura pro forma baseada no projeto
description: Este tópico fornece informações sobre como confirmar uma fatura de projeto pro forma.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867113"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="be542-103">Confirmar uma fatura pro forma baseada no projeto</span><span class="sxs-lookup"><span data-stu-id="be542-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="be542-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="be542-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="be542-105">Depois que uma fatura pro forma é confirmada, o status da fatura do projeto é atualizado para **Confirmada**.</span><span class="sxs-lookup"><span data-stu-id="be542-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="be542-106">Quando uma fatura é confirmada, ela se torna somente leitura.</span><span class="sxs-lookup"><span data-stu-id="be542-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="be542-107">A partir deste momento, a fatura só poderá ser corrigida se houver correções ou créditos iniciados pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="be542-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="be542-108">A tabela a seguir lista os reais criados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="be542-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="be542-109">Esses reais são criados quando certas operações são executadas no rascunho da fatora de projeto antes de ser confirmada.</span><span class="sxs-lookup"><span data-stu-id="be542-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="be542-110">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be542-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="be542-111">
                    <strong>Reais criados na confirmação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be542-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-112">Faturamento antecipado ou honorários</span><span class="sxs-lookup"><span data-stu-id="be542-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-113">Uma venda cobrada real do tipo <strong>Honorários</strong> é criada para o valor do adiantamento ou honorários.</span><span class="sxs-lookup"><span data-stu-id="be542-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-114">As vendas reais não faturadas com um valor negativo de retenção ou adiantamento a ser usado para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="be542-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-115">Depois de reconciliar totalmente honorários ou adiantamento em uma fatura.</span><span class="sxs-lookup"><span data-stu-id="be542-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-116">Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="be542-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="be542-117">Este valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="be542-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-118">Uma venda cobrada real para o valor desta fatura.</span><span class="sxs-lookup"><span data-stu-id="be542-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be542-119">Depois de reconciliar parcialmente honorários ou adiantamento em uma fatura.</span><span class="sxs-lookup"><span data-stu-id="be542-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-120">Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="be542-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="be542-121">Este valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="be542-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-122">Uma venda cobrada real para o valor desta fatura.</span><span class="sxs-lookup"><span data-stu-id="be542-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-123">Uma venda não cobrada real negativa do valor restante dos honorários ou adiantamento a ser usado para reconciliação em faturas futuras.</span><span class="sxs-lookup"><span data-stu-id="be542-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-124">Faturamento de uma transação única sem nenhuma edição no rascunho da fatura.</span><span class="sxs-lookup"><span data-stu-id="be542-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-125">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="be542-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-126">Uma renda cobrada real para as horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="be542-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be542-127">Faturamento de uma transação de tempo que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="be542-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-128">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="be542-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-129">Uma nova venda não cobrada real que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="be542-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-130">Uma nova venda real não faturada que não pode ser cobrada pelas horas e valores restantes após a dedução dos números corrigidos no detalhe da linha de fatura editada, uma reversão dos dados reais da venda e dados reais das vendas faturadas equivalentes.</span><span class="sxs-lookup"><span data-stu-id="be542-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-131">Faturamento de uma transação de tempo que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="be542-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-132">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="be542-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-133">Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="be542-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-134">Faturamento de uma transação de despesas sem nenhuma edição no rascunho da fatura.</span><span class="sxs-lookup"><span data-stu-id="be542-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-135">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="be542-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-136">Uma venda cobrada real para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="be542-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be542-137">Faturamento de uma transação de despesas que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="be542-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-138">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="be542-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-139">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="be542-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-140">Uma nova venda não cobrada real que não é cobrada pela quantidade e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="be542-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-141">Faturamento de uma transação de despesas que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="be542-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-142">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="be542-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-143">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="be542-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-144">Faturar uma transação de material sem quaisquer edições na fatura de rascunho.</span><span class="sxs-lookup"><span data-stu-id="be542-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-145">Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de uso de material original.</span><span class="sxs-lookup"><span data-stu-id="be542-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-146">As vendas reais faturadas para a quantidade e o valor na aprovação de uso de material original.</span><span class="sxs-lookup"><span data-stu-id="be542-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be542-147">Faturar uma transação de material editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="be542-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-148">Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de tempo.</span><span class="sxs-lookup"><span data-stu-id="be542-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-149">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="be542-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-150">Uma nova venda não cobrada real que não é cobrada pela quantidade e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="be542-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-151">Faturar uma transação de material editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="be542-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-152">Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de uso de material original.</span><span class="sxs-lookup"><span data-stu-id="be542-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-153">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="be542-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be542-154">Faturamento de um valor.</span><span class="sxs-lookup"><span data-stu-id="be542-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-155">Um estorno de venda não cobrada pelo valor na linha do diário original.</span><span class="sxs-lookup"><span data-stu-id="be542-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-156">Uma venda cobrada real para a quantidade e o valor na linha do diário de valor original.</span><span class="sxs-lookup"><span data-stu-id="be542-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="be542-157">Faturamento de um marco.</span><span class="sxs-lookup"><span data-stu-id="be542-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be542-158">Uma venda cobrada real para o valor do marco original na linha de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="be542-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
