---
title: Confirmar uma fatura pro forma do projeto
description: Este tópico fornece informações sobre como confirmar faturas de projeto pro forma no Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867072"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="026bf-103">Confirmar uma fatura pro forma do projeto</span><span class="sxs-lookup"><span data-stu-id="026bf-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="026bf-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="026bf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="026bf-105">Depois que uma fatura pro forma é confirmada, o status da fatura do projeto é atualizado para **Confirmada**.</span><span class="sxs-lookup"><span data-stu-id="026bf-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="026bf-106">Quando uma fatura é confirmada, ela se torna somente leitura.</span><span class="sxs-lookup"><span data-stu-id="026bf-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="026bf-107">A partir deste momento, a fatura só poderá ser corrigida se houver correções ou créditos iniciados pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="026bf-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="026bf-108">A tabela a seguir lista os reais criados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="026bf-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="026bf-109">Esses reais são criados quando certas operações são executadas no rascunho da fatora de projeto antes de ser confirmada.</span><span class="sxs-lookup"><span data-stu-id="026bf-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="026bf-110">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="026bf-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="026bf-111">
                    <strong>Reais criados na confirmação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="026bf-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-112">Faturamento antecipado ou honorários</span><span class="sxs-lookup"><span data-stu-id="026bf-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-113">Uma venda cobrada real do tipo <strong>Honorários</strong> é criada para o valor do adiantamento ou honorários.</span><span class="sxs-lookup"><span data-stu-id="026bf-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-114">Uma venda não cobrada real de um valor negativo dos honorários ou adiantamento a serem usados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="026bf-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-115">Depois de reconciliar totalmente honorários ou adiantamento em uma fatura.</span><span class="sxs-lookup"><span data-stu-id="026bf-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-116">Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="026bf-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="026bf-117">Este valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="026bf-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-118">Uma venda cobrada real para o valor desta fatura.</span><span class="sxs-lookup"><span data-stu-id="026bf-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="026bf-119">Depois de reconciliar parcialmente honorários ou adiantamento em uma fatura.</span><span class="sxs-lookup"><span data-stu-id="026bf-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-120">Um estorno de venda não cobrada dos honorários ou adiantamento criados para reconciliação.</span><span class="sxs-lookup"><span data-stu-id="026bf-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="026bf-121">Este valor é positivo porque se destina a anular o valor negativo gerado no momento da faturação dos honorários ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="026bf-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-122">Uma venda cobrada real para o valor desta fatura.</span><span class="sxs-lookup"><span data-stu-id="026bf-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-123">Uma venda não cobrada real negativa do valor restante dos honorários ou adiantamento a ser usado para reconciliação em faturas futuras.</span><span class="sxs-lookup"><span data-stu-id="026bf-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-124">Faturamento de uma transação única sem nenhuma edição no rascunho da fatura.</span><span class="sxs-lookup"><span data-stu-id="026bf-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-125">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="026bf-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-126">Uma renda cobrada real para as horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="026bf-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="026bf-127">Faturamento de uma transação de tempo que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="026bf-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-128">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="026bf-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-129">Uma nova venda não cobrada real que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-130">Uma nova venda não cobrada real que não é cobrada pelas horas restantes e o valor após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-131">Faturamento de uma transação de tempo que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="026bf-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-132">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="026bf-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-133">Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-134">Faturamento de uma transação de despesas sem nenhuma edição no rascunho da fatura.</span><span class="sxs-lookup"><span data-stu-id="026bf-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-135">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="026bf-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-136">Uma venda cobrada real para a quantidade e o valor na aprovação de despesas original</span><span class="sxs-lookup"><span data-stu-id="026bf-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="026bf-137">Faturamento de uma transação de despesas que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="026bf-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-138">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="026bf-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-139">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-140">Uma nova venda não cobrada real que não é cobrada pela quantidade e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-141">Faturamento de uma transação de despesas que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="026bf-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-142">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="026bf-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-143">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-144">Faturar uma transação de material sem quaisquer edições na fatura de rascunho.</span><span class="sxs-lookup"><span data-stu-id="026bf-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-145">Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de uso de material original.</span><span class="sxs-lookup"><span data-stu-id="026bf-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-146">As vendas reais faturadas para a quantidade e o valor na aprovação de uso de material original.</span><span class="sxs-lookup"><span data-stu-id="026bf-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="026bf-147">Faturar uma transação de material editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="026bf-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-148">Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de tempo.</span><span class="sxs-lookup"><span data-stu-id="026bf-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-149">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-150">Uma nova venda não cobrada real que não é cobrada pela quantidade e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-151">Faturar uma transação de material editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="026bf-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-152">Um retorno de vendas não faturadas para a quantidade e o valor na aprovação de uso de material original.</span><span class="sxs-lookup"><span data-stu-id="026bf-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-153">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="026bf-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="026bf-154">Faturamento de um valor.</span><span class="sxs-lookup"><span data-stu-id="026bf-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-155">Um estorno de venda não cobrada pelo valor na linha do diário original.</span><span class="sxs-lookup"><span data-stu-id="026bf-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-156">Uma venda cobrada real para a quantidade e o valor na linha do diário de valor original.</span><span class="sxs-lookup"><span data-stu-id="026bf-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="026bf-157">Faturamento de um marco.</span><span class="sxs-lookup"><span data-stu-id="026bf-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-158">Uma venda cobrada real para o valor do marco original na linha de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="026bf-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="026bf-159">Faturamento de uma linha de contrato baseada em produto.</span><span class="sxs-lookup"><span data-stu-id="026bf-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="026bf-160">Uma venda cobrada real para a linha de produto com a quantidade e o valor provenientes da linha de contrato baseada em produto.</span><span class="sxs-lookup"><span data-stu-id="026bf-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
