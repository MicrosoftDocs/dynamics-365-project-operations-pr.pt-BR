---
title: Gerenciando vários clientes em cotações de projeto
description: Este tópico fornece informações sobre como trabalhar em cotações com vários clientes que financiarão o projeto. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071328"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a><span data-ttu-id="2fe0d-104">Gerenciando vários clientes em cotações de projeto (Vendas)</span><span class="sxs-lookup"><span data-stu-id="2fe0d-104">Managing multiple customers on project quotes (Sales)</span></span>

<span data-ttu-id="2fe0d-105">_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="2fe0d-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2fe0d-106">As cotações de projeto viabilizam o cenário em que a proposta envolve vários clientes que financiarão o negócio.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-106">Project quotes support the scenario where the proposal involves multiple customers who will fund the deal.</span></span> <span data-ttu-id="2fe0d-107">A guia **Resumo** da cotação tem o campo **Cliente potencial** , que identifica o cliente principal da oferta.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-107">The **Summary** tab of the Quote has the **Potential customer** field that identifies the primary customer of the deal.</span></span> <span data-ttu-id="2fe0d-108">Outros clientes do negócio podem ser configurados na guia **Clientes** da cotação do projeto.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-108">Other customers for the deal can be set up on the **Customers** tab of the project quote.</span></span>

<span data-ttu-id="2fe0d-109">Todos os clientes de cotação na guia **Clientes** do padrão de cotação do projeto como clientes da linha de cotação em qualquer **nova** linha de cotação baseada em projeto criada para a cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-109">All quote customers on the **Customers** tab of the project quote default as quote line customers on any **new** project-based quote lines created for the quote.</span></span> <span data-ttu-id="2fe0d-110">Quaisquer linhas de cotação baseadas em projeto existentes não herdam novos registros de cliente de cotação criados depois delas.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-110">Any existing project-based quote lines will not inherit new quote customer records created after them.</span></span>

<span data-ttu-id="2fe0d-111">As linhas de cotação baseadas em produto são automaticamente associadas ao cliente principal, que também é o cliente no campo **Cliente potencial** na guia **Resumo**.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-111">Product-based quote lines are automatically associated to the primary customer who is also the customer in the **Potential Customer** field on the **Summary** tab of the quote.</span></span>

<span data-ttu-id="2fe0d-112">É possível adicionar, atualizar ou excluir clientes de cotação e clientes de linha de cotação a qualquer momento antes de a cotação ser ganha.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-112">Quote customers and quote line customers can be added, updated, or deleted at any time before the quote is won.</span></span>

## <a name="concept-of-a-primary-customer"></a><span data-ttu-id="2fe0d-113">Conceito de cliente principal</span><span class="sxs-lookup"><span data-stu-id="2fe0d-113">Concept of a primary customer</span></span>

<span data-ttu-id="2fe0d-114">O cliente que está na guia resumo da cotação de projeto como o cliente potencial é o cliente principal da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-114">The customer who is on the summary tab of the project quote as the potential customer is the primary customer of the quote.</span></span> <span data-ttu-id="2fe0d-115">Quando você tentar excluir o cliente principal da lista de clientes da cotação, verá um erro informando que um registro do cliente principal em uma cotação não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-115">When you try to delete the primary customer from customers list on quote, you will see an error that a primary customer record on a quote cannot be deleted.</span></span>

<span data-ttu-id="2fe0d-116">O cliente principal não deve ser atualizado a partir da lista de clientes na cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-116">The primary customer shouldn't be updated from the customer list on the quote.</span></span> <span data-ttu-id="2fe0d-117">No entanto, você pode influenciar o cliente principal alterando o cliente potencial na guia **Resumo** da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-117">However, you can influence the primary customer by changing the potential customer on the **Summary** tab of the quote.</span></span> <span data-ttu-id="2fe0d-118">Quando este campo é atualizado no **Resumo da Cotação** , o cliente potencial recém-selecionado é adicionado como um novo cliente da cotação com o sinalizador **Principal** definido.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-118">When this field is updated on the **Quote Summary** , the newly selected potential customer is added as a new quote customer with the **Primary** flag set.</span></span> <span data-ttu-id="2fe0d-119">O antigo cliente potencial ainda será um cliente na cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-119">The old potential customer will still be a customer on the quote.</span></span>

## <a name="create-update-or-delete-a-quote-customer-record"></a><span data-ttu-id="2fe0d-120">Criar, atualizar ou excluir um registro de cliente de linha de cotação</span><span class="sxs-lookup"><span data-stu-id="2fe0d-120">Create, Update, or Delete a quote customer record</span></span>

<span data-ttu-id="2fe0d-121">Um cliente de cotação pode ser criado, atualizado ou excluído na guia **Clientes da cotação** na página **Citar**.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-121">A quote customer can be created, updated, or deleted from the **Quote customers** tab on the **Quote** page.</span></span> <span data-ttu-id="2fe0d-122">Os campos listados na seguinte tabela estão no registro do cliente da cotação de uma cotação de projeto.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-122">The fields listed in the following table are on the quote customer record of a project quote.</span></span>

| <span data-ttu-id="2fe0d-123">**Campo**</span><span class="sxs-lookup"><span data-stu-id="2fe0d-123">**Field**</span></span> | <span data-ttu-id="2fe0d-124">**Local**</span><span class="sxs-lookup"><span data-stu-id="2fe0d-124">**Location**</span></span> | <span data-ttu-id="2fe0d-125">**Relevância, finalidade e orientação**</span><span class="sxs-lookup"><span data-stu-id="2fe0d-125">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="2fe0d-126">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="2fe0d-126">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="2fe0d-127">Conta</span><span class="sxs-lookup"><span data-stu-id="2fe0d-127">Account</span></span> | <span data-ttu-id="2fe0d-128">Grade editável na guia **Clientes de cotação** , o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-128">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="2fe0d-129">Lista todas as contas ativas.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-129">Lists all the active accounts.</span></span> <span data-ttu-id="2fe0d-130">Este campo será bloqueado após a criação do registro.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-130">This field is locked after the record is created.</span></span> <span data-ttu-id="2fe0d-131">Se você quiser atualizá-lo, exclua e recrie o registro.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-131">If you want to update it, delete the record, and re-create it.</span></span> <span data-ttu-id="2fe0d-132">Se você tiver registrado quaisquer dados reais, ou se o registro do cliente da cotação for um cliente principal, você terá permissão para excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-132">If you have recorded any actuals, or if the quote customer record is a primary customer, you will be allowed to delete the record.</span></span> | <span data-ttu-id="2fe0d-133">Quando uma linha de cotação é criada, os clientes da cotação são copiados para os clientes da linha de cotação do projeto.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-133">Quote customers are copied over as quote line customers when a quote line is created.</span></span> <span data-ttu-id="2fe0d-134">Quando uma cotação é ganha, os clientes da cotação são copiados para os clientes do contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-134">Quote customers are also copied over to the project contract customers when a quote is won.</span></span> |
| <span data-ttu-id="2fe0d-135">Percentual de cobrança dividida</span><span class="sxs-lookup"><span data-stu-id="2fe0d-135">Billing split percent</span></span> | <span data-ttu-id="2fe0d-136">Grade editável na guia **Clientes de cotação** , o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-136">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="2fe0d-137">Represente a porcentagem de cada transação de vendas não faturada que será atribuída a este cliente da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-137">Represent the percentage of each unbilled sales transaction that will be attributed to this quote customer.</span></span> | <span data-ttu-id="2fe0d-138">Copiado para novas linhas de cotação e para clientes de contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-138">Copied over to new quote lines and to project contract customers.</span></span> |
| <span data-ttu-id="2fe0d-139">Nome do Contato para Cobrança</span><span class="sxs-lookup"><span data-stu-id="2fe0d-139">Bill to Contact Name</span></span> | <span data-ttu-id="2fe0d-140">Grade editável na guia **Clientes de cotação** , o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-140">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="2fe0d-141">Este é um campo de texto e deve ser usado para identificar a pessoa de contato da fatura para este cliente.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-141">This is a text field and should be used to identify the Invoice contact person for this customer.</span></span> <span data-ttu-id="2fe0d-142">Eles são padronizados a partir do registro da conta relacionado</span><span class="sxs-lookup"><span data-stu-id="2fe0d-142">These are defaulted from the related account record</span></span> | <span data-ttu-id="2fe0d-143">Copiado para os clientes do contrato do projeto quando uma cotação é ganha e, por sua vez, para o campo nome Contrato para Cobrança na fatura que é gerada para este cliente.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-143">Copied over to project contract customers when a Quote is won and in turn to the Bill to Contract name field on the Invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="2fe0d-144">Nome para Cobrança</span><span class="sxs-lookup"><span data-stu-id="2fe0d-144">Bill to Name</span></span> | <span data-ttu-id="2fe0d-145">Grade editável na guia **Clientes de cotação** , o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-145">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="2fe0d-146">Este campo de texto deve ser usado para identificar a pessoa de contato da fatura para este cliente.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-146">This text field should be used to identify the invoice contact person for this customer.</span></span> | <span data-ttu-id="2fe0d-147">Copiado para os clientes do contrato do projeto quando uma cotação é ganha e, por sua vez, para o campo nome **Contrato para Cobrança** na fatura que é gerada para este cliente.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-147">Copied to the project contract customers when a quote is won and in turn to the **Bill to Contract Name** field on the invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="2fe0d-148">Condições de Pagamento</span><span class="sxs-lookup"><span data-stu-id="2fe0d-148">Payment Terms</span></span> | <span data-ttu-id="2fe0d-149">Grade editável na guia **Clientes de cotação** , o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-149">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="2fe0d-150">Este é um conjunto de opções com valores padrão do registro da conta relacionado.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-150">This is an option set with values that default from the related account record.</span></span> | <span data-ttu-id="2fe0d-151">Copiado para os clientes do contrato do projeto quando uma cotação é ganha e, por sua vez, para o campo nome **Contrato para Cobrança** na fatura que é gerada para este cliente,</span><span class="sxs-lookup"><span data-stu-id="2fe0d-151">Copied to the project contract customers when a quote is won and in turn, to the **Bill to Contract Name** field on the invoice that is generated for this customer,</span></span> |
| <span data-ttu-id="2fe0d-152">É Arredondamento</span><span class="sxs-lookup"><span data-stu-id="2fe0d-152">Is Rounding</span></span> | <span data-ttu-id="2fe0d-153">Grade editável na guia **Clientes de cotação** , o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-153">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="2fe0d-154">Indica se este cliente é um cliente de arredondamento padrão para esta oferta.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-154">Indicates if this customer is a default rounding customer for this deal.</span></span> | <span data-ttu-id="2fe0d-155">Copiado para os clientes do contrato do projeto quando uma cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-155">Copied to the project contract customers when a quote is won.</span></span> |
| <span data-ttu-id="2fe0d-156">Limite máximo</span><span class="sxs-lookup"><span data-stu-id="2fe0d-156">Not-to-exceed limit</span></span> | <span data-ttu-id="2fe0d-157">Grade editável na guia **Clientes de cotação** , o formulário **Principal** e os formulários de **Criação rápida** para um cliente da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-157">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="2fe0d-158">Indica se há um limite negociado para o valor total que será faturado a este cliente para este contrato</span><span class="sxs-lookup"><span data-stu-id="2fe0d-158">Indicates if there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for this engagement</span></span> | <span data-ttu-id="2fe0d-159">Copiado para os clientes do contrato do projeto quando uma cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-159">Copied to the project contract customers when a quote is won.</span></span> |

## <a name="editing-billing-split-percentages"></a><span data-ttu-id="2fe0d-160">Editar porcentagens de divisão de cobrança</span><span class="sxs-lookup"><span data-stu-id="2fe0d-160">Editing billing split percentages</span></span>

<span data-ttu-id="2fe0d-161">Você pode editar as porcentagens de divisão de cobrança usando a experiência de edição de grade em linha.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-161">You can edit the billing split percentages by using the in-line grid edit experience.</span></span> <span data-ttu-id="2fe0d-162">Quando as porcentagens de divisão do cobrança não totalizam 100%, ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-162">When the billing split percentages don't total 100%, an error will occur.</span></span> <span data-ttu-id="2fe0d-163">Depois de atualizar as porcentagens de divisão de cobrança, atualize a página para remover o erro.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-163">After you update the billing split percentages, refresh the page to remove the error.</span></span>

<span data-ttu-id="2fe0d-164">Você também pode tentar selecionar **Distribuir uniformemente** na subgrade dos clientes da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-164">You can also try selecting **Evenly Distribute** on the quote customers' sub-grid.</span></span> <span data-ttu-id="2fe0d-165">Esta ação aloca divisões de cobrança para todos os clientes da cotação.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-165">This action allocates billing splits to all quote customers.</span></span> <span data-ttu-id="2fe0d-166">Se houver qualquer fator de arredondamento, ele será adicionado ao cliente de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-166">If there is any rounding factor, that will be added to the rounding customer.</span></span> <span data-ttu-id="2fe0d-167">Um dos clientes da cotação é sempre marcado como o cliente de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-167">One of the quote customers is always tagged as the rounding customer.</span></span> <span data-ttu-id="2fe0d-168">Isso significa que o registro do cliente da cotação tem o sinalizador **Arredondamento** definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-168">this means that the quote customer record has the **Rounding** flag set to **Yes**.</span></span> <span data-ttu-id="2fe0d-169">Normalmente, este é o cliente principal da cotação, mas isso pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="2fe0d-169">Typically this is the primary customer of the quote, but that can be changed.</span></span>