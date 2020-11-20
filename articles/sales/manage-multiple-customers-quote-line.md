---
title: Gerenciar vários clientes em linhas de cotação baseadas em projeto
description: Este tópico fornece informações sobre como gerenciar vários clientes em linhas de cotação baseadas em projeto.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48336af0ad522e9d6aa68fa82ffa7921f09662d4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118549"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a><span data-ttu-id="ba114-103">Gerenciar vários clientes em linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="ba114-103">Manage multiple customers on project-based quote lines</span></span>

<span data-ttu-id="ba114-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="ba114-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ba114-105">As linhas de cotação baseadas em projeto suportam cenários em que cada linha de cotação tem uma lista de clientes que estão pagando por ela.</span><span class="sxs-lookup"><span data-stu-id="ba114-105">Project-based quote lines support scenarios where each quote line has a list of customers that are paying for it.</span></span> <span data-ttu-id="ba114-106">Esta lista de clientes na linha de cotação baseada em projeto pode ser igual à lista de clientes na cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-106">This list of customers on the project-based quote line can be same as the list of customers on the quote.</span></span> <span data-ttu-id="ba114-107">Você também pode alterar a lista de clientes para ser diferente.</span><span class="sxs-lookup"><span data-stu-id="ba114-107">You can also change the list of customers to be different.</span></span> <span data-ttu-id="ba114-108">Quando uma cotação de projeto é ganha, a lista de clientes na linha de cotação baseada em projeto é copiada para a linha de contrato baseada em projeto correspondente para criar o contrato de projeto eventual.</span><span class="sxs-lookup"><span data-stu-id="ba114-108">To create the eventual project contract when a project quote is won, the customer list on project-based quote line is copied to the corresponding project–based contract line.</span></span> <span data-ttu-id="ba114-109">Os clientes na cotação baseada em projeto são copiados para o contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="ba114-109">Customers on the project-based quote are copied to the project contract.</span></span>

<span data-ttu-id="ba114-110">Quando você fatura o eventual contrato do projeto, a lista de clientes na linha do contrato com base no projeto tem prioridade sobre a lista no contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="ba114-110">When you invoice the eventual project contract, the customer list on the project-based contract line takes priority over the list on the project contract.</span></span> <span data-ttu-id="ba114-111">A lista de clientes no contrato de projeto é usada apenas para padrões em novas linhas de contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="ba114-111">The customer list on the project contract is only used to default new project contract lines.</span></span>

<span data-ttu-id="ba114-112">Todos os clientes de cotação na guia **Clientes** do padrão de cotação do projeto como clientes da linha de cotação em qualquer nova linha de cotação baseada em projeto criada para a cotação do projeto.</span><span class="sxs-lookup"><span data-stu-id="ba114-112">All quote customers on the **Customers** tab of the project quote default as quote line customers on any new project-based quote lines created for the project quote.</span></span> <span data-ttu-id="ba114-113">Quaisquer linhas de cotação baseadas em projeto existentes não herdam novos registros de cliente de cotação criados depois delas.</span><span class="sxs-lookup"><span data-stu-id="ba114-113">Any existing project-based quote lines don't inherit new quote customer records created after them.</span></span>

## <a name="create-update-or-delete-a-quote-line-customer-record"></a><span data-ttu-id="ba114-114">Criar, atualizar ou excluir um registro de cliente de linha de cotação</span><span class="sxs-lookup"><span data-stu-id="ba114-114">Create, update, or delete a quote line customer record</span></span>

<span data-ttu-id="ba114-115">Você pode criar, atualizar ou excluir um cliente de linha de cotação na guia **Clientes da linha de cotação** na página **Linha de cotação baseada em projeto**.</span><span class="sxs-lookup"><span data-stu-id="ba114-115">You can create, update, or delete a quote line customer on the **Quote line customers** tab on the **Project-based quote line** page.</span></span> <span data-ttu-id="ba114-116">Quando você adiciona um novo cliente na linha de cotação baseada em projeto, o cliente também é adicionado à cotação geral como um cliente de cotação, com uma porcentagem de divisão de faturamento padrão na cotação geral de 0%.</span><span class="sxs-lookup"><span data-stu-id="ba114-116">When you add a new customer on the project-based quote line, the customer is also added to the overall quote as a quote customer, with a default billing split percentage on the overall quote of 0%.</span></span> <span data-ttu-id="ba114-117">O percentual de divisão do faturamento na cotação geral é copiado para novas linhas de cotação e para o contrato de projeto eventual.</span><span class="sxs-lookup"><span data-stu-id="ba114-117">The billing split percentage on the overall quote is copied to new quote lines and to the eventual project contract.</span></span> <span data-ttu-id="ba114-118">No entanto, ao faturar do contrato, a porcentagem de divisão do faturamento no nível da linha de cotação é usada, não a porcentagem de divisão do faturamento no nível geral do contrato.</span><span class="sxs-lookup"><span data-stu-id="ba114-118">However, when you invoice from the contract, the billing split percentage at the quote line level is used, not the billing split percentage at the overall contract level.</span></span> 

<span data-ttu-id="ba114-119">A tabela a seguir mostra os campos no registro do cliente da linha de cotação de uma linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="ba114-119">The following table shows the fields on the quote line customer record of a project-based quote line.</span></span>

| <span data-ttu-id="ba114-120">Campo</span><span class="sxs-lookup"><span data-stu-id="ba114-120">Field</span></span> | <span data-ttu-id="ba114-121">Localização</span><span class="sxs-lookup"><span data-stu-id="ba114-121">Location</span></span> | <span data-ttu-id="ba114-122">Descrição e orientação</span><span class="sxs-lookup"><span data-stu-id="ba114-122">Description and guidance</span></span> | <span data-ttu-id="ba114-123">Impacto a jusante</span><span class="sxs-lookup"><span data-stu-id="ba114-123">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="ba114-124">**Conta**</span><span class="sxs-lookup"><span data-stu-id="ba114-124">**Account**</span></span> | <span data-ttu-id="ba114-125">Uma grade editável na guia **Clientes da linha de cotação**, o formulário principal e o formulário de criação rápida para um cliente com linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-125">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer.</span></span> | <span data-ttu-id="ba114-126">Lista todas as contas ativas.</span><span class="sxs-lookup"><span data-stu-id="ba114-126">Lists all active accounts.</span></span> <span data-ttu-id="ba114-127">Este campo será bloqueado após a criação do registro.</span><span class="sxs-lookup"><span data-stu-id="ba114-127">This field is locked after the record is created.</span></span> <span data-ttu-id="ba114-128">Se você precisar atualizar o campo, exclua e recrie o registro.</span><span class="sxs-lookup"><span data-stu-id="ba114-128">If you need to update the field, delete and recreate the record.</span></span> <span data-ttu-id="ba114-129">Se você gravou algum real, não pode deletar o registro.</span><span class="sxs-lookup"><span data-stu-id="ba114-129">If you recorded any actuals, you can't delete the record.</span></span> | <span data-ttu-id="ba114-130">Quando você escolhe uma conta da lista mestre de contas para adicionar, o cliente da linha de cotação também é adicionado como um cliente de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-130">When you pick an account from the master list of accounts to add, the Quote line customer is also added as a Quote customer.</span></span> <span data-ttu-id="ba114-131">Quando uma cotação é ganha, os clientes da linha de cotação são copiados para os clientes da linha de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="ba114-131">Quote line customers are copied to the project contract line customers when a quote is won.</span></span> |
| <span data-ttu-id="ba114-132">**Percentual de cobrança dividida**</span><span class="sxs-lookup"><span data-stu-id="ba114-132">**Billing split percent**</span></span> | <span data-ttu-id="ba114-133">Uma grade editável na guia **Clientes da linha de cotação**, o formulário principal e o formulário de criação rápida para um cliente com linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-133">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer.</span></span> | <span data-ttu-id="ba114-134">Representa a porcentagem de cada transação de vendas não faturada que será atribuída a este cliente de linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-134">Represents the percentage of each unbilled sales transaction that will be attributed to this quote line customer.</span></span> | <span data-ttu-id="ba114-135">Copiado para clientes de linha de contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="ba114-135">Copied over to project contract line customers.</span></span> |
| <span data-ttu-id="ba114-136">**Limite máximo**</span><span class="sxs-lookup"><span data-stu-id="ba114-136">**Not-to-exceed limit**</span></span> | <span data-ttu-id="ba114-137">Uma grade editável na guia **Clientes da linha de cotação**, o formulário principal e o formulário de criação rápida para um cliente com linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-137">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer.</span></span> | <span data-ttu-id="ba114-138">Indica se há um limite negociado para o valor total que será faturado a este cliente para esta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-138">Indicates whether there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for this quoted line.</span></span> | <span data-ttu-id="ba114-139">Copiado para os clientes da linha de contrato do projeto quando uma cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="ba114-139">Copied over to project contract line customers when a quote is won.</span></span> |
| <span data-ttu-id="ba114-140">**Empresa proprietária**</span><span class="sxs-lookup"><span data-stu-id="ba114-140">**Owning company**</span></span> | <span data-ttu-id="ba114-141">Uma grade editável na guia **Clientes da linha de cotação**, o formulário principal e o formulário de criação rápida para um cliente com linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-141">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer,</span></span> | <span data-ttu-id="ba114-142">A pessoa jurídica para a qual este cliente está configurado no módulo **Gestão e contabilidade de projetos**.</span><span class="sxs-lookup"><span data-stu-id="ba114-142">The legal entity in which this customer is set up in the **Project management and accounting** module.</span></span> <span data-ttu-id="ba114-143">Este campo é somente leitura e é definido para a empresa proprietária da própria cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-143">This field is read-only and is set to the owning company of the quote itself.</span></span> <span data-ttu-id="ba114-144">A lista de clientes para adicionar no campo **Conta** já está filtrada para a lista da empresa proprietária no módulo **Gestão e contabilidade de projetos** de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ba114-144">The list of customers to add in the **Account** field is already filtered to the list from the owning company in the **Project management and accounting** module of Project Operations.</span></span> | <span data-ttu-id="ba114-145">A empresa proprietária equivale ao conceito de pessoa jurídica.</span><span class="sxs-lookup"><span data-stu-id="ba114-145">The owning company equates to the concept of legal entity.</span></span> <span data-ttu-id="ba114-146">Todos os custos e receitas provenientes deste projeto são contabilizados na contabilidade da empresa proprietária.</span><span class="sxs-lookup"><span data-stu-id="ba114-146">All costs and revenue that accrue from this project are accounted in the General ledger of the owning company.</span></span> |
| <span data-ttu-id="ba114-147">**É arredondado**</span><span class="sxs-lookup"><span data-stu-id="ba114-147">**Is rounding**</span></span> | <span data-ttu-id="ba114-148">Uma grade editável na guia **Clientes da linha de cotação**, o formulário principal e o formulário de criação rápida para um cliente com linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-148">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer.</span></span> | <span data-ttu-id="ba114-149">Indica se este cliente é um cliente de arredondamento padrão para esta linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="ba114-149">Indicates whether this customer is a default rounding customer for this project-based quote line.</span></span> | <span data-ttu-id="ba114-150">Copiado para os clientes do contrato do projeto quando uma cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="ba114-150">Copied over to project contract customers when a quote is won.</span></span> |

## <a name="edit-billing-split-percentages"></a><span data-ttu-id="ba114-151">Editar porcentagens de divisão de cobrança</span><span class="sxs-lookup"><span data-stu-id="ba114-151">Edit billing split percentages</span></span>

<span data-ttu-id="ba114-152">Você pode editar as porcentagens de divisão do faturamento in-line.</span><span class="sxs-lookup"><span data-stu-id="ba114-152">You can edit billing split percentages in-line.</span></span> <span data-ttu-id="ba114-153">Quando as porcentagens de divisão do faturamento não totalizam 100%, ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="ba114-153">When the billing split percentages don't total 100%, an error occurs.</span></span> <span data-ttu-id="ba114-154">Depois de editar as porcentagens de divisão do faturamento, atualize a página da linha de cotação para remover o erro.</span><span class="sxs-lookup"><span data-stu-id="ba114-154">After you edit the billing split percentages, refresh the quote line page to remove the error.</span></span>

<span data-ttu-id="ba114-155">Use a ação distribuir uniformemente na subgrade dos clientes da linha de cotação para alocar divisões de faturamento para todos os clientes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ba114-155">Use the evenly distribute action on the quote line customers subgrid to allocate billing splits to all quote line customers.</span></span> <span data-ttu-id="ba114-156">Se houver um fator de arredondamento, ele será adicionado ao cliente de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="ba114-156">If there's a rounding factor, that will be added to the rounding customer.</span></span> <span data-ttu-id="ba114-157">Um dos clientes da linha de cotação é sempre marcado como o cliente de arredondamento, o que significa que o registro do cliente da linha de cotação tem o sinalizador de arredondamento definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="ba114-157">One of the quote line customers is always tagged as the rounding customer, which means that quote line customer record has the rounding flag set to **Yes**.</span></span> 