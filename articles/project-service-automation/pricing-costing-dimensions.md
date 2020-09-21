---
title: Home page de dimensões de preço e custo
description: Este tópico fornece uma visão geral das dimensões de preço.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749056"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="68e23-103">Home page de dimensões de preço e custo</span><span class="sxs-lookup"><span data-stu-id="68e23-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="68e23-104">As dimensões que são usadas em recursos humanos para configurar preço e custos são divididas em duas categorias:</span><span class="sxs-lookup"><span data-stu-id="68e23-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="68e23-105">Pessoas</span><span class="sxs-lookup"><span data-stu-id="68e23-105">People</span></span>
- <span data-ttu-id="68e23-106">Trabalho planejado</span><span class="sxs-lookup"><span data-stu-id="68e23-106">Planned work</span></span>

<span data-ttu-id="68e23-107">Por isso, há dois tipos de valor de dimensão de preço disponíveis no PSA (Project Service Automation):</span><span class="sxs-lookup"><span data-stu-id="68e23-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="68e23-108">**Conjuntos de opções**– dimensões que são enumerações fixas para um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="68e23-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="68e23-109">**Valores baseados em entidade** – dimensões que podem ser um variado conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="68e23-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="68e23-110">Dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="68e23-110">Pricing dimensions</span></span>

<span data-ttu-id="68e23-111">O PSA apresenta um conjunto padrão de dimensões de preço.</span><span class="sxs-lookup"><span data-stu-id="68e23-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="68e23-112">É possível exibi-las acessando **Project Service** > **Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="68e23-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="68e23-113">No registro do parâmetro, na guia **Dimensões de preço baseadas em valor**, verifique se a função **msdyn_resourcecategory** e a unidade organizacional de recursos **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="68e23-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="68e23-114">Isso permitirá configurar o preço e o custo para cada combinação de função e unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="68e23-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captura de tela dos parâmetros do Project Service com "Aplicável às Vendas" em destaque](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="68e23-116">Se você vem usando os campos prontos para uso da função e da unidade organizacional como dimensões de preço antes da versão 3 do PSA, não haverá qualquer mudança significativa.</span><span class="sxs-lookup"><span data-stu-id="68e23-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="68e23-117">Você pode continuar usando o Project Service normalmente.</span><span class="sxs-lookup"><span data-stu-id="68e23-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="68e23-118">Se precisar precificar ou colocar custo para seus recursos usando atributos adicionais, você poderá criar campos, entidades e dimensões personalizados.</span><span class="sxs-lookup"><span data-stu-id="68e23-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="68e23-119">Para obter mais informações, consulte os tópicos a seguir. No entanto, observe que você deve concluir os procedimento na ordem lista abaixo:</span><span class="sxs-lookup"><span data-stu-id="68e23-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="68e23-120">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="68e23-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="68e23-121">Adicionar campos personalizados a entidades transacionais e de configuração de preço</span><span class="sxs-lookup"><span data-stu-id="68e23-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="68e23-122">Configurar campos personalizados como dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="68e23-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="68e23-123">Atualizar os atributos de plug-in para incluir novas dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="68e23-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="68e23-124">Precificação do tempo do recurso humano</span><span class="sxs-lookup"><span data-stu-id="68e23-124">Pricing human resource time</span></span>
<span data-ttu-id="68e23-125">Como uma organização precifica o tempo do recurso humano, às vezes, é uma consideração estratégica importante que afeta diretamente a lucratividade da organização.</span><span class="sxs-lookup"><span data-stu-id="68e23-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="68e23-126">Trabalhe com as equipes e líderes financeiros quando sua organização estiver pronta para identificar como ela quer configurar tarifas de cobrança e custo para tempo do recurso humano.</span><span class="sxs-lookup"><span data-stu-id="68e23-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="68e23-127">Outras considerações para preço incluem considerar a reutilização de campos ou entidades que atualmente não são dimensões de preço, mas são aplicados como uma dimensão de preço para sua organização.</span><span class="sxs-lookup"><span data-stu-id="68e23-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="68e23-128">Campos como **Categoria de Transação** (**msdyn_transactioncategory**) e **Recurso Reservável** (**bookableresource**) são exemplos de dimensões candidatas.</span><span class="sxs-lookup"><span data-stu-id="68e23-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="68e23-129">Você também deve considerar se sua dimensão de preço deve ser uma tabela ou um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="68e23-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="68e23-130">Se houver previsão de alterações nos valores de uma dimensão que excedam 10 ou 12, e forem necessários atributos adicionais nesses valores, você poderá criar uma entidade em vez de um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="68e23-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="68e23-131">Manter um conjunto de opções, como adição ou remoção de valores, exige um administrador ou desenvolvedor, enquanto a adição de novas linhas a uma tabela pode ser feita por qualquer usuário.</span><span class="sxs-lookup"><span data-stu-id="68e23-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="68e23-132">O exemplo a seguir mostra taxas de cobrança que são configuradas com base na função e na unidade organizacional de recursos à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="68e23-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="68e23-133">As taxas de custo geralmente se baseiam na faixa salarial do funcionário e na unidade organizacional a que ele pertence.</span><span class="sxs-lookup"><span data-stu-id="68e23-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="68e23-134">Nesse exemplo, as tabelas de taxa de cobrança e taxa de custo serão parecidas com as que se seguem.</span><span class="sxs-lookup"><span data-stu-id="68e23-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="68e23-135">**Taxas de cobrança de exemplo**</span><span class="sxs-lookup"><span data-stu-id="68e23-135">**Sample bill rates**</span></span>

| <span data-ttu-id="68e23-136">Função</span><span class="sxs-lookup"><span data-stu-id="68e23-136">Role</span></span>        | <span data-ttu-id="68e23-137">Unidades Organizacionais</span><span class="sxs-lookup"><span data-stu-id="68e23-137">Org Unit</span></span>    |<span data-ttu-id="68e23-138">Unidade</span><span class="sxs-lookup"><span data-stu-id="68e23-138">Unit</span></span>      |<span data-ttu-id="68e23-139">Preço</span><span class="sxs-lookup"><span data-stu-id="68e23-139">Price</span></span>      |<span data-ttu-id="68e23-140">Moeda</span><span class="sxs-lookup"><span data-stu-id="68e23-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="68e23-141">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="68e23-141">Developer</span></span>   | <span data-ttu-id="68e23-142">Cabral EUA</span><span class="sxs-lookup"><span data-stu-id="68e23-142">Contoso US</span></span>  |<span data-ttu-id="68e23-143">Hour</span><span class="sxs-lookup"><span data-stu-id="68e23-143">Hour</span></span> | <span data-ttu-id="68e23-144">200</span><span class="sxs-lookup"><span data-stu-id="68e23-144">200</span></span>|<span data-ttu-id="68e23-145">USD</span><span class="sxs-lookup"><span data-stu-id="68e23-145">USD</span></span>     |
| <span data-ttu-id="68e23-146">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="68e23-146">Developer</span></span>   | <span data-ttu-id="68e23-147">Cabral India</span><span class="sxs-lookup"><span data-stu-id="68e23-147">Contoso India</span></span> |<span data-ttu-id="68e23-148">Hour</span><span class="sxs-lookup"><span data-stu-id="68e23-148">Hour</span></span>|   <span data-ttu-id="68e23-149">112</span><span class="sxs-lookup"><span data-stu-id="68e23-149">112</span></span>|<span data-ttu-id="68e23-150">USD</span><span class="sxs-lookup"><span data-stu-id="68e23-150">USD</span></span>     |


<span data-ttu-id="68e23-151">**Taxas de custo de exemplo**</span><span class="sxs-lookup"><span data-stu-id="68e23-151">**Sample cost rates**</span></span>

| <span data-ttu-id="68e23-152">Faixa Salarial</span><span class="sxs-lookup"><span data-stu-id="68e23-152">Salary Band</span></span>     | <span data-ttu-id="68e23-153">Unidades Organizacionais</span><span class="sxs-lookup"><span data-stu-id="68e23-153">Org Unit</span></span>    |<span data-ttu-id="68e23-154">Unidade</span><span class="sxs-lookup"><span data-stu-id="68e23-154">Unit</span></span>      |<span data-ttu-id="68e23-155">Preço</span><span class="sxs-lookup"><span data-stu-id="68e23-155">Price</span></span>      |<span data-ttu-id="68e23-156">Moeda</span><span class="sxs-lookup"><span data-stu-id="68e23-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="68e23-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="68e23-157">My company_Band1</span></span> | <span data-ttu-id="68e23-158">Cabral EUA</span><span class="sxs-lookup"><span data-stu-id="68e23-158">Contoso US</span></span>  |<span data-ttu-id="68e23-159">Hour</span><span class="sxs-lookup"><span data-stu-id="68e23-159">Hour</span></span> | <span data-ttu-id="68e23-160">145</span><span class="sxs-lookup"><span data-stu-id="68e23-160">145</span></span>|<span data-ttu-id="68e23-161">USD</span><span class="sxs-lookup"><span data-stu-id="68e23-161">USD</span></span>     |
| <span data-ttu-id="68e23-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="68e23-162">My company_Band2</span></span> | <span data-ttu-id="68e23-163">Cabral India</span><span class="sxs-lookup"><span data-stu-id="68e23-163">Contoso India</span></span> |<span data-ttu-id="68e23-164">Hour</span><span class="sxs-lookup"><span data-stu-id="68e23-164">Hour</span></span>|   <span data-ttu-id="68e23-165">67</span><span class="sxs-lookup"><span data-stu-id="68e23-165">67</span></span>|<span data-ttu-id="68e23-166">USD</span><span class="sxs-lookup"><span data-stu-id="68e23-166">USD</span></span>     |
