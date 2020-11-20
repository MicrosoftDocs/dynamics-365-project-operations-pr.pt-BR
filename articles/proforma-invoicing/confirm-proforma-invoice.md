---
title: Confirmar uma fatura pro forma
description: Este tópico fornece informações sobre como confirmar uma fatura pro forma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128089"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="7e962-103">Confirmar uma fatura pro forma</span><span class="sxs-lookup"><span data-stu-id="7e962-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="7e962-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="7e962-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7e962-105">Depois que uma fatura pro forma é confirmada, o status da fatura do projeto é atualizado para **Confirmada**.</span><span class="sxs-lookup"><span data-stu-id="7e962-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="7e962-106">Quando uma fatura é confirmada, ela se torna somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7e962-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="7e962-107">A partir de agora, a fatura só poderá ser corrigida se houver correções ou créditos iniciados pelo cliente ou quando for marcada como paga.</span><span class="sxs-lookup"><span data-stu-id="7e962-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="7e962-108">A tabela a seguir lista os reais criados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="7e962-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="7e962-109">Esses reais são criados quando certas operações são executadas no rascunho da fatora de projeto antes de ser confirmada.</span><span class="sxs-lookup"><span data-stu-id="7e962-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="7e962-110">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e962-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="7e962-111">
                    <strong>Reais criados na confirmação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e962-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e962-112">Faturamento de uma transação única sem nenhuma edição no rascunho da fatura.</span><span class="sxs-lookup"><span data-stu-id="7e962-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-113">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7e962-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-114">Uma renda cobrada real para as horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7e962-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7e962-115">Faturamento de uma transação de tempo que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7e962-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-116">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7e962-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-117">Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="7e962-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-118">Uma nova venda real não faturada que não é cobrada pelas horas e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda real não faturada e uma venda real faturada equivalente.</span><span class="sxs-lookup"><span data-stu-id="7e962-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e962-119">Faturamento de uma transação de tempo que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7e962-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-120">Um estorno de venda não cobrada pelas horas e o valor na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7e962-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-121">Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="7e962-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e962-122">Faturamento de uma transação de despesas sem nenhuma edição no rascunho da fatura.</span><span class="sxs-lookup"><span data-stu-id="7e962-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-123">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="7e962-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-124">Uma venda cobrada real para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="7e962-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7e962-125">Faturamento de uma transação de despesas que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7e962-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-126">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="7e962-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-127">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="7e962-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-128">Uma nova venda não cobrada real que não é cobrada pela quantidade e o valor restantes após a dedução dos números corrigidos no detalhe da linha da fatura editada, um estorno da venda não cobrada real e um equivalente da venda cobrada real.</span><span class="sxs-lookup"><span data-stu-id="7e962-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e962-129">Faturamento de uma transação de despesas que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7e962-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-130">Um estorno de venda não cobrada para a quantidade e o valor na aprovação de despesas original.</span><span class="sxs-lookup"><span data-stu-id="7e962-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-131">Uma nova venda não cobrada real que é cobrada pela quantidade e o valor no detalhe da linha da fatura editada, um estorno da venda não cobrada real e uma venda cobrada real equivalente.</span><span class="sxs-lookup"><span data-stu-id="7e962-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e962-132">Faturamento de um valor.</span><span class="sxs-lookup"><span data-stu-id="7e962-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-133">Um estorno de venda não cobrada pelo valor na linha do diário original.</span><span class="sxs-lookup"><span data-stu-id="7e962-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-134">Uma venda cobrada real para a quantidade e o valor na linha do diário de valor original.</span><span class="sxs-lookup"><span data-stu-id="7e962-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7e962-135">Faturamento de um marco.</span><span class="sxs-lookup"><span data-stu-id="7e962-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7e962-136">Uma venda cobrada real para o valor do marco original na linha de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="7e962-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
