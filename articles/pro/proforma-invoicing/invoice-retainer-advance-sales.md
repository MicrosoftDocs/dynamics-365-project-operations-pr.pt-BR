---
title: Faturar um honorário ou adiantamento - lite
description: Este tópico fornece informações sobre como faturar um honorário ou adiantamento no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9013529b615026eab92177c9fd9fb84c50d66f4f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180538"
---
# <a name="invoice-a-retainer-or-an-advance---lite"></a><span data-ttu-id="dfa71-103">Faturar um honorário ou adiantamento - lite</span><span class="sxs-lookup"><span data-stu-id="dfa71-103">Invoice a retainer or an advance - lite</span></span>

<span data-ttu-id="dfa71-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="dfa71-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dfa71-105">O Dynamics 365 Project Operations dá suporte a contratos baseados em honorários e adiantamentos únicos.</span><span class="sxs-lookup"><span data-stu-id="dfa71-105">Dynamics 365 Project Operations supports retainer-based contracts and one-time advances.</span></span> <span data-ttu-id="dfa71-106">Em um contrato de projeto, você pode registrar uma agenda de honorários ou um adiantamento único.</span><span class="sxs-lookup"><span data-stu-id="dfa71-106">On a project contract, you can record a schedule of retainers or a one-time advance.</span></span> <span data-ttu-id="dfa71-107">No entanto, o registro em nível de contrato do projeto não disponibiliza imediatamente um honorário ou adiantamento para uso.</span><span class="sxs-lookup"><span data-stu-id="dfa71-107">However, recording at the project contract level doesn't immediately make a retainer or advance available for use.</span></span> <span data-ttu-id="dfa71-108">Para usar um honorário ou adiantamento em uma fatura que realmente cobre do cliente, o honorário ou adiantamento deve ser faturado primeiro.</span><span class="sxs-lookup"><span data-stu-id="dfa71-108">To use a retainer or advance on an invoice that actually charges the customer, the retainer or advance must be invoiced first.</span></span>

<span data-ttu-id="dfa71-109">Conclua as etapas a seguir para faturar um honorário ou um adiantamento.</span><span class="sxs-lookup"><span data-stu-id="dfa71-109">Complete the following steps to invoice a retainer or an advance.</span></span>

1. <span data-ttu-id="dfa71-110">Selecione **Vendas** > **Cobrança** > **Honorários e Adiantamentos**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-110">Select **Sales** > **Billing** > **Retainers and Advances**.</span></span> 
2. <span data-ttu-id="dfa71-111">Na página **Adiantamentos e Honorários**, use o filtro para selecionar o honorário ou adiantamento específico para faturamento e marque-o como **Pronto para Faturamento**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-111">On the **Advances and Retainers** page, use the filter to select the specific retainer or advance to invoice and mark it as **Ready to Invoice**.</span></span>
3. <span data-ttu-id="dfa71-112">Crie uma fatura manualmente a partir da lista **Contrato do Projeto** ou página de detalhes.</span><span class="sxs-lookup"><span data-stu-id="dfa71-112">Create an invoice either manually from the **Project Contract** list or detail page.</span></span> <span data-ttu-id="dfa71-113">O honorário ou adiantamento é mostrado na fatura de rascunho na seção **Adiantamentos e Honorários** na página **Fatura**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-113">The retainer or advance is shown on the draft invoice in the **Advances and Retainers** section on the **Invoice** page.</span></span>
4. <span data-ttu-id="dfa71-114">Confirme a fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-114">Confirm the invoice.</span></span> <span data-ttu-id="dfa71-115">Isso disponibilizará o honorário ou adiantamento para uso.</span><span class="sxs-lookup"><span data-stu-id="dfa71-115">This will make the retainer or advance available for use.</span></span> <span data-ttu-id="dfa71-116">Você pode verificar a fatura na página de listagem **Honorários e Adiantamentos**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-116">You can verify the invoice on the **Retainers and Advances** list page.</span></span> <span data-ttu-id="dfa71-117">Para um Adiantamento ou Honorário faturado, o valor disponível é mostrado na grade.</span><span class="sxs-lookup"><span data-stu-id="dfa71-117">For an invoiced Advance or Retainer, the available amount is shown in the grid.</span></span>

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a><span data-ttu-id="dfa71-118">Criar um honorário ou adiantamento na grade de fatura</span><span class="sxs-lookup"><span data-stu-id="dfa71-118">Create a retainer or advance from the Invoice grid</span></span>

<span data-ttu-id="dfa71-119">Você pode criar um honorário ou um adiantamento diretamente em uma fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-119">You can create a retainer or an advance directly on an invoice.</span></span>

1. <span data-ttu-id="dfa71-120">Em uma fatura de rascunho, na subgrade **Adiantamentos e Honorários**, selecione **Novo** para criar um novo honorário ou adiantamento.</span><span class="sxs-lookup"><span data-stu-id="dfa71-120">On a draft invoice, on the **Advances and Retainers** subgrid, select **New** to create a new retainer or advance.</span></span> 
2. <span data-ttu-id="dfa71-121">Na página **Criação Rápida**, adicione as informações necessárias e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-121">On the **Quick Create** page, add the necessary information, and then select **Save**.</span></span> <span data-ttu-id="dfa71-122">O honorário ou adiantamento é criado no contrato do projeto relacionado à fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-122">The retainer or advance is created on the project contract related to the invoice.</span></span> <span data-ttu-id="dfa71-123">O honorário ou adiantamento é marcado automaticamente como **Pronto para Faturamento** e, depois, adicionado à subgrade **Adiantamentos e Honorários** na página **Fatura**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-123">The retainer or advance is automatically marked as **Ready to Invoice** and then added to the **Advances and Retainers** subgrid on the **Invoice** page.</span></span>

## <a name="reconcile-an-invoiced-retainer-or-advance"></a><span data-ttu-id="dfa71-124">Reconciliar um honorário ou adiantamento faturado</span><span class="sxs-lookup"><span data-stu-id="dfa71-124">Reconcile an invoiced retainer or advance</span></span>

<span data-ttu-id="dfa71-125">Depois que um honorário ou adiantamento é faturado, eles podem ser usados ou reconciliados em uma fatura com hora, despesas, etapas ou outros encargos baseados no projeto.</span><span class="sxs-lookup"><span data-stu-id="dfa71-125">After a retainer or advance is invoiced, they can be used or reconciled on an invoice with time, expenses, milestones, or other project-based charges.</span></span> <span data-ttu-id="dfa71-126">O cliente verá o valor da fatura reduzido pelo valor de honorário ou adiantamento usado nesta fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-126">The customer will see their invoice amount reduced by the retainer or advance amount used on this invoice.</span></span>

<span data-ttu-id="dfa71-127">Em cada fatura gerada para um contrato de projeto que faturou honorários ou adiantamentos, o Project Operation aplica automaticamente o honorário ou adiantamento à fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-127">On every invoice that is generated for a project contract that has invoiced retainers or advances, Project Operation automatically applies the retainer or advance to the invoice.</span></span>

<span data-ttu-id="dfa71-128">Isso pode ser visto na grade **Honorários e Adiantamentos Aplicados** na página **Fatura**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-128">This can be seen in the **Applied Retainers and Advances** grid on the **Invoice** page.</span></span> <span data-ttu-id="dfa71-129">A tabela a seguir fornece informações sobre os campos na grade **Honorários e Adiantamentos Aplicados** da página **Fatura do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-129">The following table provides information about the fields on the **Applied Retainers and Advances** grid of the **Project Invoice** page.</span></span>

| <span data-ttu-id="dfa71-130">Campo</span><span class="sxs-lookup"><span data-stu-id="dfa71-130">Field</span></span> | <span data-ttu-id="dfa71-131">Localização</span><span class="sxs-lookup"><span data-stu-id="dfa71-131">Location</span></span> | <span data-ttu-id="dfa71-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfa71-132">Description</span></span> | <span data-ttu-id="dfa71-133">Impacto a jusante</span><span class="sxs-lookup"><span data-stu-id="dfa71-133">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="dfa71-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfa71-134">Description</span></span> | <span data-ttu-id="dfa71-135">Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**</span><span class="sxs-lookup"><span data-stu-id="dfa71-135">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span> |<span data-ttu-id="dfa71-136">Este campo somente leitura fornece uma descrição do honorário ou adiantamento usado nesta fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-136">This read-only field provides a description of the retainer or advance used on this invoice.</span></span> <span data-ttu-id="dfa71-137">Este valor não pode ser alterado na fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-137">This value can't be changed on the invoice.</span></span> <span data-ttu-id="dfa71-138">Este valor pode ser atualizado na subgrade na página **Contrato de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-138">This value can be updated on the subgrid on the **Project Contract** page.</span></span> | <span data-ttu-id="dfa71-139">Este campo pode ser exibido para o cliente na fatura impressa para indicar qual honorário ou adiantamento é aplicado na fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-139">This field can be displayed to the customer on the printed invoice to indicate which retainer or advance is applied on the invoice.</span></span> |
| <span data-ttu-id="dfa71-140">Data da Entrega</span><span class="sxs-lookup"><span data-stu-id="dfa71-140">Delivered On</span></span> | <span data-ttu-id="dfa71-141">Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**</span><span class="sxs-lookup"><span data-stu-id="dfa71-141">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="dfa71-142">Este campo somente leitura fornece a data da fatura do honorário ou adiantamento usado nesta fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-142">This read-only field provides the invoice date of the retainer or advance used on this invoice.</span></span> <span data-ttu-id="dfa71-143">Este valor não pode ser alterado na fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-143">This value can't be changed on the invoice.</span></span> <span data-ttu-id="dfa71-144">Este valor pode ser atualizado na subgrade na página **Contrato de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-144">This value can be updated on the subgrid on the **Project Contract** page.</span></span> | <span data-ttu-id="dfa71-145">Este campo pode ser exibido para o cliente na fatura impressa para indicar a data em que o honorário ou adiantamento foi faturado pela primeira vez para o cliente.</span><span class="sxs-lookup"><span data-stu-id="dfa71-145">This field can be displayed to the customer on the printed invoice to indicate the date when the retainer or advance was first invoiced to the customer.</span></span> |
| <span data-ttu-id="dfa71-146">Valor</span><span class="sxs-lookup"><span data-stu-id="dfa71-146">Amount</span></span> | <span data-ttu-id="dfa71-147">Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**</span><span class="sxs-lookup"><span data-stu-id="dfa71-147">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="dfa71-148">Este campo somente leitura fornece o valor do honorário ou adiantamento usado nesta fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-148">This read-only field provides the amount of the retainer or advance used on this invoice.</span></span> <span data-ttu-id="dfa71-149">Este valor não pode ser alterado na fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-149">This value can't be changed on the invoice.</span></span> <span data-ttu-id="dfa71-150">Este valor pode ser atualizado na subgrade na página **Contrato de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="dfa71-150">This value can be updated on the subgrid on the **Project Contract** page.</span></span> | <span data-ttu-id="dfa71-151">Este campo pode ser exibido para o cliente na fatura impressa para indicar o valor original do honorário ou adiantamento que foi pago pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="dfa71-151">This field can be displayed to the customer on the printed invoice to indicate the original amount of retainer or advance that was paid by the customer.</span></span> |
| <span data-ttu-id="dfa71-152">Valor Usado</span><span class="sxs-lookup"><span data-stu-id="dfa71-152">Used Amount</span></span> | <span data-ttu-id="dfa71-153">Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**</span><span class="sxs-lookup"><span data-stu-id="dfa71-153">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="dfa71-154">Este campo somente leitura fornece o valor calculado que resume quanto do honorário ou adiantamento foi usado.</span><span class="sxs-lookup"><span data-stu-id="dfa71-154">This read-only field provides the calculated value that summarizes how much of the retainer or advance has been used.</span></span> | <span data-ttu-id="dfa71-155">Este campo pode ser exibido para o cliente na fatura impressa para indicar o valor deste honorário ou adiantamento que já foi usado.</span><span class="sxs-lookup"><span data-stu-id="dfa71-155">This field can be displayed to the customer on the printed invoice to indicate the amount from this retainer or advance that was already used.</span></span> |
| <span data-ttu-id="dfa71-156">Valor Ampliado</span><span class="sxs-lookup"><span data-stu-id="dfa71-156">Extended Amount</span></span> | <span data-ttu-id="dfa71-157">Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**</span><span class="sxs-lookup"><span data-stu-id="dfa71-157">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="dfa71-158">Este campo editável fornece o valor do honorário ou adiantamento que está sendo usado nesta fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="dfa71-158">This editable field provides the amount of the retainer or advance that is being used on this project invoice.</span></span> <span data-ttu-id="dfa71-159">Este valor não pode ser superior ao que está disponível no adiantamento.</span><span class="sxs-lookup"><span data-stu-id="dfa71-159">This amount can't be more that what is available on the advance.</span></span> <span data-ttu-id="dfa71-160">O sistema calcula automaticamente isso como a diferença entre os campos **Valor** e **Quantidade Usada** na grade.</span><span class="sxs-lookup"><span data-stu-id="dfa71-160">The system automatically calculates this as the difference between the **Amount** and **Used Amount** fields on the grid.</span></span> <span data-ttu-id="dfa71-161">Você pode diminuir esse valor para usar menos do que o disponível, mas não pode aumentar o valor para usar mais do que está disponível.</span><span class="sxs-lookup"><span data-stu-id="dfa71-161">You can decrease this amount to use less than what is available but you can't increase the amount to use more than what is available.</span></span> | <span data-ttu-id="dfa71-162">Este campo pode ser exibido para o cliente na fatura impressa para indicar o valor deste honorário ou adiantamento que está sendo usado na fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-162">This field can be displayed to the customer on the printed invoice to indicate the amount from this retainer or advance that being used on the invoice.</span></span> |
| <span data-ttu-id="dfa71-163">Valor do Saldo dos Honorários.</span><span class="sxs-lookup"><span data-stu-id="dfa71-163">Balance Retainer Amount.</span></span> | <span data-ttu-id="dfa71-164">Grade **Honorários e Adiantamentos Aplicados** na página **Fatura do Projeto**</span><span class="sxs-lookup"><span data-stu-id="dfa71-164">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="dfa71-165">Este campo somente leitura fornece o valor de quanto restará do honorário ou adiantamento após a confirmação da fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-165">This read-only field provides the value of how much of the retainer or advance will be left after the invoice is confirmed.</span></span> | <span data-ttu-id="dfa71-166">Este campo pode ser exibido para o cliente na fatura impressa para indicar o valor que restará deste honorário ou adiantamento após a confirmação ou o pagamento da fatura.</span><span class="sxs-lookup"><span data-stu-id="dfa71-166">This field can be displayed to the customer on the printed invoice to indicate the amount that will be left from this retainer or advance after the invoice is confirmed and paid.</span></span> |