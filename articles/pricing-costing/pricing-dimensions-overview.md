---
title: Visão geral das dimensões de preço
description: Este tópico fornece informações sobre as dimensões de preço no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898202"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="7a43a-103">Visão geral das dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="7a43a-103">Pricing dimensions overview</span></span>

<span data-ttu-id="7a43a-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="7a43a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7a43a-105">As dimensões que são usadas em recursos humanos para configurar preço e custos são divididas em duas categorias:</span><span class="sxs-lookup"><span data-stu-id="7a43a-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="7a43a-106">Pessoas</span><span class="sxs-lookup"><span data-stu-id="7a43a-106">People</span></span>
- <span data-ttu-id="7a43a-107">Trabalho planejado</span><span class="sxs-lookup"><span data-stu-id="7a43a-107">Planned work</span></span>

<span data-ttu-id="7a43a-108">Por isso, há dois tipos de valor de dimensão de preço disponíveis:</span><span class="sxs-lookup"><span data-stu-id="7a43a-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="7a43a-109">**Conjuntos de opções**: dimensões que são enumerações fixas para um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="7a43a-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="7a43a-110">**Valores baseados em entidade**: dimensões que podem ser um conjunto variado de valores.</span><span class="sxs-lookup"><span data-stu-id="7a43a-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="7a43a-111">Dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="7a43a-111">Pricing dimensions</span></span>

<span data-ttu-id="7a43a-112">O Dynamics 365 Project Operations é fornecido com um conjunto padrão de dimensões de preços.</span><span class="sxs-lookup"><span data-stu-id="7a43a-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="7a43a-113">É possível exibir essas dimensões de preços acessando **Project Operations** > **Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="7a43a-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="7a43a-114">No registro do parâmetro, na guia **Dimensões de preço baseadas em valor**, verifique se a função **msdyn_resourcecategory** e a unidade organizacional de recursos **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="7a43a-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="7a43a-115">Com esses campos habilitados, você pode configurar o preço e o custo para cada combinação de função e unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="7a43a-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="7a43a-116">Se precisar precificar ou colocar custo para seus recursos usando atributos adicionais, você poderá criar campos, entidades e dimensões personalizados.</span><span class="sxs-lookup"><span data-stu-id="7a43a-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="7a43a-117">Precificação do tempo do recurso humano</span><span class="sxs-lookup"><span data-stu-id="7a43a-117">Pricing human resource time</span></span>
<span data-ttu-id="7a43a-118">Como uma organização precifica o tempo do recurso humano, às vezes, é uma consideração estratégica importante que afeta diretamente a lucratividade da organização.</span><span class="sxs-lookup"><span data-stu-id="7a43a-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="7a43a-119">Trabalhe com as equipes e líderes financeiros quando sua organização estiver pronta para identificar como ela quer configurar tarifas de cobrança e custo para tempo do recurso humano.</span><span class="sxs-lookup"><span data-stu-id="7a43a-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="7a43a-120">Outras considerações para preço incluem considerar a reutilização de campos ou entidades que atualmente não são dimensões de preço, mas são aplicados como uma dimensão de preço para sua organização.</span><span class="sxs-lookup"><span data-stu-id="7a43a-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="7a43a-121">Campos como **Categoria de Transação** (**msdyn_transactioncategory**) e **Recurso Reservável** (**bookableresource**) são exemplos de dimensões candidatas.</span><span class="sxs-lookup"><span data-stu-id="7a43a-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="7a43a-122">Considere se sua dimensão de preço deve ser uma tabela ou um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="7a43a-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="7a43a-123">Se houver previsão de alterações nos valores de uma dimensão que excedam 10 ou 12, e forem necessários atributos adicionais nesses valores, você poderá criar uma entidade em vez de um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="7a43a-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="7a43a-124">Manter um conjunto de opções, como adição ou remoção de valores, exige um administrador ou desenvolvedor, enquanto a adição de novas linhas a uma tabela pode ser feita por qualquer usuário.</span><span class="sxs-lookup"><span data-stu-id="7a43a-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="7a43a-125">O exemplo a seguir mostra taxas de cobrança que são configuradas com base na função e na unidade organizacional de recursos à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="7a43a-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="7a43a-126">As taxas de custo geralmente se baseiam na faixa salarial do funcionário e na unidade organizacional a que ele pertence.</span><span class="sxs-lookup"><span data-stu-id="7a43a-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="7a43a-127">Nesse exemplo, as tabelas de taxa de cobrança e taxa de custo serão parecidas com as que se seguem.</span><span class="sxs-lookup"><span data-stu-id="7a43a-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="7a43a-128">**Taxas de cobrança de exemplo**</span><span class="sxs-lookup"><span data-stu-id="7a43a-128">**Sample bill rates**</span></span>

| <span data-ttu-id="7a43a-129">Função</span><span class="sxs-lookup"><span data-stu-id="7a43a-129">Role</span></span>        | <span data-ttu-id="7a43a-130">Unidades Organizacionais</span><span class="sxs-lookup"><span data-stu-id="7a43a-130">Org Unit</span></span>    |<span data-ttu-id="7a43a-131">Unidade</span><span class="sxs-lookup"><span data-stu-id="7a43a-131">Unit</span></span>      |<span data-ttu-id="7a43a-132">Preço</span><span class="sxs-lookup"><span data-stu-id="7a43a-132">Price</span></span>      |<span data-ttu-id="7a43a-133">Moeda</span><span class="sxs-lookup"><span data-stu-id="7a43a-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="7a43a-134">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="7a43a-134">Developer</span></span>   | <span data-ttu-id="7a43a-135">Cabral EUA</span><span class="sxs-lookup"><span data-stu-id="7a43a-135">Contoso US</span></span>  |<span data-ttu-id="7a43a-136">Hour</span><span class="sxs-lookup"><span data-stu-id="7a43a-136">Hour</span></span> | <span data-ttu-id="7a43a-137">200</span><span class="sxs-lookup"><span data-stu-id="7a43a-137">200</span></span>|<span data-ttu-id="7a43a-138">USD</span><span class="sxs-lookup"><span data-stu-id="7a43a-138">USD</span></span>     |
| <span data-ttu-id="7a43a-139">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="7a43a-139">Developer</span></span>   | <span data-ttu-id="7a43a-140">Cabral India</span><span class="sxs-lookup"><span data-stu-id="7a43a-140">Contoso India</span></span> |<span data-ttu-id="7a43a-141">Hour</span><span class="sxs-lookup"><span data-stu-id="7a43a-141">Hour</span></span>|   <span data-ttu-id="7a43a-142">112</span><span class="sxs-lookup"><span data-stu-id="7a43a-142">112</span></span>|<span data-ttu-id="7a43a-143">USD</span><span class="sxs-lookup"><span data-stu-id="7a43a-143">USD</span></span>     |


<span data-ttu-id="7a43a-144">**Taxas de custo de exemplo**</span><span class="sxs-lookup"><span data-stu-id="7a43a-144">**Sample cost rates**</span></span>

| <span data-ttu-id="7a43a-145">Faixa Salarial</span><span class="sxs-lookup"><span data-stu-id="7a43a-145">Salary Band</span></span>     | <span data-ttu-id="7a43a-146">Unidades Organizacionais</span><span class="sxs-lookup"><span data-stu-id="7a43a-146">Org Unit</span></span>    |<span data-ttu-id="7a43a-147">Unidade</span><span class="sxs-lookup"><span data-stu-id="7a43a-147">Unit</span></span>      |<span data-ttu-id="7a43a-148">Preço</span><span class="sxs-lookup"><span data-stu-id="7a43a-148">Price</span></span>      |<span data-ttu-id="7a43a-149">Moeda</span><span class="sxs-lookup"><span data-stu-id="7a43a-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="7a43a-150">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="7a43a-150">My company_Band1</span></span> | <span data-ttu-id="7a43a-151">Cabral EUA</span><span class="sxs-lookup"><span data-stu-id="7a43a-151">Contoso US</span></span>  |<span data-ttu-id="7a43a-152">Hour</span><span class="sxs-lookup"><span data-stu-id="7a43a-152">Hour</span></span> | <span data-ttu-id="7a43a-153">145</span><span class="sxs-lookup"><span data-stu-id="7a43a-153">145</span></span>|<span data-ttu-id="7a43a-154">USD</span><span class="sxs-lookup"><span data-stu-id="7a43a-154">USD</span></span>     |
| <span data-ttu-id="7a43a-155">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="7a43a-155">My company_Band2</span></span> | <span data-ttu-id="7a43a-156">Cabral India</span><span class="sxs-lookup"><span data-stu-id="7a43a-156">Contoso India</span></span> |<span data-ttu-id="7a43a-157">Hour</span><span class="sxs-lookup"><span data-stu-id="7a43a-157">Hour</span></span>|   <span data-ttu-id="7a43a-158">67</span><span class="sxs-lookup"><span data-stu-id="7a43a-158">67</span></span>|<span data-ttu-id="7a43a-159">USD</span><span class="sxs-lookup"><span data-stu-id="7a43a-159">USD</span></span>     |
