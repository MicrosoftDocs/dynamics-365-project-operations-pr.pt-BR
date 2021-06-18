---
title: Faturas corretivas baseadas em projeto
description: Este tópico fornece informações sobre como criar e confirmar faturas corretivas baseadas em projeto no Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012257"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="96188-103">Faturas corretivas baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="96188-103">Corrective project-based invoices</span></span>

<span data-ttu-id="96188-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="96188-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="96188-105">Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos negociados com o cliente e o gerente de projeto.</span><span class="sxs-lookup"><span data-stu-id="96188-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="96188-106">Para fazer edições em uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**.</span><span class="sxs-lookup"><span data-stu-id="96188-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="96188-107">Esta seleção não está disponível a menos que uma fatura do projeto seja confirmada ou a fatura baseada no projeto tenha adiantamentos ou honorários ou reconciliações de adiantamentos ou honorários.</span><span class="sxs-lookup"><span data-stu-id="96188-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="96188-108">Um novo esboço de fatura é criado da fatura confirmada.</span><span class="sxs-lookup"><span data-stu-id="96188-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="96188-109">Todos os detalhes da linha da fatura confirmada anteriormente são copiados para o novo rascunho.</span><span class="sxs-lookup"><span data-stu-id="96188-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="96188-110">A seguir estão alguns dos pontos-chave para entender sobre os detalhes da linha na nova fatura corrigida:</span><span class="sxs-lookup"><span data-stu-id="96188-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="96188-111">Todas as quantidades são atualizadas para zero.</span><span class="sxs-lookup"><span data-stu-id="96188-111">All quantities are updated to zero.</span></span> <span data-ttu-id="96188-112">O Dynamics 365 Project Operations assume que todos os itens faturados são totalmente creditados.</span><span class="sxs-lookup"><span data-stu-id="96188-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="96188-113">Se necessário, você pode atualizar manualmente essas quantidades para refletir a quantidade que está sendo faturada, e não a quantidade que está sendo creditada.</span><span class="sxs-lookup"><span data-stu-id="96188-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="96188-114">Com base na quantidade inserida, o aplicativo calcula a quantidade creditada.</span><span class="sxs-lookup"><span data-stu-id="96188-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="96188-115">Esse valor é refletido nos valores reais criados quando a fatura corrigida é confirmada.</span><span class="sxs-lookup"><span data-stu-id="96188-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="96188-116">Se você estiver fazendo alterações no valor do imposto, deverá inserir o valor correto do imposto e não o valor do imposto que está sendo creditado.</span><span class="sxs-lookup"><span data-stu-id="96188-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="96188-117">As correções de marcos são sempre processadas como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="96188-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="96188-118">Para detalhes de linha de fatura que são correções para outros encargos já faturados, o campo **Correção** está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="96188-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="96188-119">Para faturas que têm detalhes da linha da fatura corrigidos, o campo **Tem correções** é definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="96188-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="96188-120">Os valores reais quando uma fatura corretiva é confirmada</span><span class="sxs-lookup"><span data-stu-id="96188-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="96188-121">A tabela a seguir lista os valores reais criados quando uma fatura corretiva é confirmada.</span><span class="sxs-lookup"><span data-stu-id="96188-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="96188-122">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96188-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="96188-123">
                    <strong>Reais criados na confirmação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96188-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96188-124">Faturamento do crédito total de uma transação de tempo faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96188-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-125">Um estorno de venda cobrada pelas horas e o valor no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="96188-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-126">Uma nova venda não cobrada real pelas horas e o valor no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="96188-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="96188-127">Faturamento do crédito parcial em uma transação de tempo.</span><span class="sxs-lookup"><span data-stu-id="96188-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-128">Um estorno de venda cobrada pelas horas e o valor faturado no detalhe da linha de fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="96188-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-129">Uma nova venda real não faturada que é cobrada pelas horas e o valor no detalhe da linha da fatura editada, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="96188-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-130">Uma nova venda não cobrada real que é passível de cobrança pelas horas e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.</span><span class="sxs-lookup"><span data-stu-id="96188-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96188-131">Faturamento do crédito total de uma transação de despesa faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96188-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-132">Um estorno de venda cobrada pela quantidade e o valor no detalhe da linha de fatura original para a despesa.</span><span class="sxs-lookup"><span data-stu-id="96188-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-133">Uma nova venda não cobrada real pela quantidade e o valor no detalhe da linha de fatura original para a despesa.</span><span class="sxs-lookup"><span data-stu-id="96188-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="96188-134">Faturamento do crédito parcial de uma transação de despesa faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96188-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-135">Um estorno de venda cobrada pela quantidade e o valor faturados no detalhe da linha de fatura original para uma despesa.</span><span class="sxs-lookup"><span data-stu-id="96188-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-136">Uma nova venda real não faturada que é passível de cobrança pela quantidade e o valor no detalhe da linha da fatura corrigida, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="96188-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-137">Uma nova venda não cobrada real que é passível de cobrança pela quantidade e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.</span><span class="sxs-lookup"><span data-stu-id="96188-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96188-138">Faturar o crédito total de uma transação de material faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96188-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-139">Um estorno de vendas faturadas para a quantidade e o valor no detalhe da linha da fatura original do material.</span><span class="sxs-lookup"><span data-stu-id="96188-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-140">Um novo valor de vendas não faturado para a quantidade e o valor no detalhe da linha da fatura original do material.</span><span class="sxs-lookup"><span data-stu-id="96188-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="96188-141">Faturamento do crédito parcial em uma transação de material.</span><span class="sxs-lookup"><span data-stu-id="96188-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-142">Um estorno de vendas faturadas para a quantidade e o valor faturado no detalhe da linha da fatura original do material.</span><span class="sxs-lookup"><span data-stu-id="96188-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-143">Um novo valor real de vendas não faturadas que é cobrado pela quantidade e valor no detalhe da linha da fatura editada, um estorno disso e um valor real de vendas faturadas equivalente.</span><span class="sxs-lookup"><span data-stu-id="96188-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-144">Uma nova venda não cobrada real que é passível de cobrança pela quantidade e valores restantes após a dedução dos números corrigidos no detalhe da linha da fatura.</span><span class="sxs-lookup"><span data-stu-id="96188-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96188-145">Faturamento do crédito total de uma transação de valor faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96188-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-146">Um estorno de venda cobrada pela quantidade e o valor no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="96188-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-147">Uma nova venda não cobrada real pela quantidade e o valor no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="96188-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96188-148">Faturamento do crédito parcial de uma transação de valor faturada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96188-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-149">Um estorno de venda cobrada pela quantidade e o valor faturados no detalhe da linha de fatura original para o valor.</span><span class="sxs-lookup"><span data-stu-id="96188-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-150">Uma nova venda não cobrada real que é passível de cobrança pela quantidade e o valor no detalhe da linha da fatura corretiva editada, um estorno disso e um valor real das vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="96188-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="96188-151">Faturamento do crédito total de um marco faturado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96188-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-152">Um estorno de venda cobrada pelas horas e o valor no detalhe da linha de fatura original para o marco.</span><span class="sxs-lookup"><span data-stu-id="96188-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="96188-153">O status da fatura no marco é atualizado de <b>Fatura do Cliente Lançada</b> para <b>Pronto para Faturamento</b>.</span><span class="sxs-lookup"><span data-stu-id="96188-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="96188-154">Faturamento do crédito parcial de um marco faturado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96188-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="96188-155">Este não é suportado.</span><span class="sxs-lookup"><span data-stu-id="96188-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
