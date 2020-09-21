---
title: Contratos de projeto
description: Este tópico fornece exemplos de contratos de projeto que você pode criar para vários tipos de projetos e fontes de financiamento, e como você pode gerenciar contratos e faturar clientes do projeto.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749105"
---
# <a name="project-contracts"></a><span data-ttu-id="4bfd0-103">Contratos de projeto</span><span class="sxs-lookup"><span data-stu-id="4bfd0-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bfd0-104">Este artigo fornece exemplos de contratos de projeto que você pode criar para vários tipos de projetos e fontes de financiamento, e como você pode gerenciar contratos e faturar clientes do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="4bfd0-105">O tipo de projeto que você cria para um contrato de projeto determina o método que é usado para faturar clientes do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="4bfd0-106">Você pode alterar um contrato de projeto e o projeto relacionado, mas não pode alterar o tipo de projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="4bfd0-107">Ao usar um contrato de projeto, você pode faturar um ou mais projetos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="4bfd0-108">O contrato de projeto também ajuda a garantir um procedimento de faturamento consistente para todos os subprojetos em uma estrutura de projetos.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="4bfd0-109">Cada projeto que será faturado deve estar associado a um contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="4bfd0-110">As configurações de um contrato de projeto se aplicam a todos os projetos e subprojetos associados a esse contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="4bfd0-111">Um contrato de projeto pode especificar uma ou mais fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="4bfd0-112">Portanto, você pode dividir a cobrança entre vários financiadores, definir limites de financiamento para que as fontes de financiamento não sejam cobradas mais do que um valor especificado e configurar regras de financiamento para cobrar despesas.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="4bfd0-113">Financiamento para contratos de projeto</span><span class="sxs-lookup"><span data-stu-id="4bfd0-113">Funding for project contracts</span></span>
<span data-ttu-id="4bfd0-114">Alguns contratos de projeto especificam que várias partes compartilham a responsabilidade pelo financiamento dos custos do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="4bfd0-115">Veja alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-115">Here are some examples:</span></span>

-   <span data-ttu-id="4bfd0-116">Um grande cliente que tem várias divisões solicita que o financiamento de um projeto seja quebrado por divisão.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="4bfd0-117">Sua empresa compartilha os custos de um grande projeto com uma organização externa.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="4bfd0-118">Um projeto rodoviário é cofinanciado por dois municípios.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="4bfd0-119">O projeto de uma ponte é financiado por uma concessão do governo e uma empresa privada.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="4bfd0-120">No Dynamics 365 Finance, você pode dividir a cobrança de uma única transação ou de um projeto inteiro entre vários clientes, concessões ou organizações.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="4bfd0-121">Em projetos que têm vários financiadores, todas as partes que contribuem para o financiamento de um projeto de financiamento avançado são chamadas de fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="4bfd0-122">Depois que um cliente, organização ou concessão é definido como uma fonte de financiamento, ele pode ser atribuído a uma ou mais regras de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="4bfd0-123">As regras de financiamento contêm os critérios que determinam como as cobranças são alocadas às várias fontes de financiamento de um projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="4bfd0-124">Já que itens em estoque, como aqueles que aparecem nas requisições e pedidos de compra, não podem ser divididos, o valor do custo não pode ser dividido entre várias fontes de financiamento no momento da distribuição.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="4bfd0-125">Portanto, o valor da fonte de financiamento permanece 0 (zero) até que a saída do estoque seja lançada.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="4bfd0-126">Quando a saída do estoque é lançada, o valor do custo é distribuído de acordo com as regras de distribuição de contas do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="4bfd0-127">Veja algumas etapas que você pode seguir para facilitar a divisão da cobrança entre várias fontes de financiamento:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="4bfd0-128">Especificar que todas as transações inseridas para um projeto usem a mesma moeda de venda que o contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="4bfd0-129">Estabelecer limites de financiamento, de modo que uma fonte de financiamento não fature mais do que um valor especificado para um projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="4bfd0-130">Configurar regras e limites de financiamento para cada funcionário, item, categoria, grupo de categoria e tipo de transação (ou para todos os tipos de transação).</span><span class="sxs-lookup"><span data-stu-id="4bfd0-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="4bfd0-131">Selecionar datas de início e de término opcionais para definir o período em que cada regra de financiamento é válida.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="4bfd0-132">Especificar a porcentagem pela qual cada fonte de financiamento é responsável.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="4bfd0-133">Especificar qual fonte de financiamento é responsável pelas diferenças de arredondamento causadas por cálculos de alocação de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="4bfd0-134">Configurar regras que determinem como os custos do projeto são faturados para clientes externos e cobrados de organizações internas.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="4bfd0-135">Registrar as transações em uma conta de financiamento retido até que um financiamento adicional possa ser obtido ou até que você decida arcar com os custos internamente.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="4bfd0-136">Para determinar qual grupo de impostos associar a uma transação, é feita uma pesquisa no projeto em busca de uma atribuição de grupo de impostos.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="4bfd0-137">Se nenhuma atribuição de grupo de imposto foi feita no nível do projeto, é feita uma pesquisa no contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="4bfd0-138">Exemplo: múltiplas fontes de financiamento (simples)</span><span class="sxs-lookup"><span data-stu-id="4bfd0-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="4bfd0-139">A tabela a seguir fornece cenários para gerenciar a alocação de financiamento entre várias fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="4bfd0-140">Esses cenários são baseados nas seguintes suposições:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="4bfd0-141">As configurações de prioridade são levadas em consideração na alocação de fundos antes que outros critérios de regra de financiamento sejam aplicados.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="4bfd0-142">Nenhum intervalo de datas foi especificado para definir o período quando a regra de financiamento é válida.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bfd0-143"><strong>Cenário</strong></span><span class="sxs-lookup"><span data-stu-id="4bfd0-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="4bfd0-144"><strong>Fonte de financiamento</strong></span><span class="sxs-lookup"><span data-stu-id="4bfd0-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="4bfd0-145"><strong>Porcentagem de alocação</strong></span><span class="sxs-lookup"><span data-stu-id="4bfd0-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="4bfd0-146"><strong>Prioridade de alocação</strong></span><span class="sxs-lookup"><span data-stu-id="4bfd0-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bfd0-147">Você deseja alocar os custos a uma fonte de financiamento até que seus fundos se esgotem, alocar os custos a uma segunda fonte de financiamento até que seus fundos se esgotem e, por fim, alocar os custos restantes a uma terceira fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4bfd0-148">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="4bfd0-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="4bfd0-149">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="4bfd0-150">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="4bfd0-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfd0-151">100%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-151">100%</span></span></li>
<li><span data-ttu-id="4bfd0-152">100%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-152">100%</span></span></li>
<li><span data-ttu-id="4bfd0-153">100%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfd0-154">0</span><span class="sxs-lookup"><span data-stu-id="4bfd0-154">1</span></span></li>
<li><span data-ttu-id="4bfd0-155">2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-155">2</span></span></li>
<li><span data-ttu-id="4bfd0-156">3</span><span class="sxs-lookup"><span data-stu-id="4bfd0-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bfd0-157">Você deseja alocar 75% dos custos para uma fonte de financiamento e 25% para uma segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="4bfd0-158">Quando os recursos dessas fontes de financiamento se esgotarem, você deseja pagar os custos restantes em uma terceira fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4bfd0-159">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="4bfd0-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="4bfd0-160">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="4bfd0-161">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="4bfd0-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfd0-162">75%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-162">75%</span></span></li>
<li><span data-ttu-id="4bfd0-163">25%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-163">25%</span></span></li>
<li><span data-ttu-id="4bfd0-164">100%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfd0-165">0</span><span class="sxs-lookup"><span data-stu-id="4bfd0-165">1</span></span></li>
<li><span data-ttu-id="4bfd0-166">0</span><span class="sxs-lookup"><span data-stu-id="4bfd0-166">1</span></span></li>
<li><span data-ttu-id="4bfd0-167">2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bfd0-168">Você deseja alocar 75% dos custos para uma fonte de financiamento e 25% para uma segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="4bfd0-169">Quando os recursos dessas fontes de financiamento se esgotarem, você deseja dividir custos restantes entre uma terceira e uma quarta fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4bfd0-170">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="4bfd0-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="4bfd0-171">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="4bfd0-172">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="4bfd0-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="4bfd0-173">Fonte de financiamento 4</span><span class="sxs-lookup"><span data-stu-id="4bfd0-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfd0-174">75%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-174">75%</span></span></li>
<li><span data-ttu-id="4bfd0-175">25%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-175">25%</span></span></li>
<li><span data-ttu-id="4bfd0-176">50%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-176">50%</span></span></li>
<li><span data-ttu-id="4bfd0-177">50%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfd0-178">0</span><span class="sxs-lookup"><span data-stu-id="4bfd0-178">1</span></span></li>
<li><span data-ttu-id="4bfd0-179">0</span><span class="sxs-lookup"><span data-stu-id="4bfd0-179">1</span></span></li>
<li><span data-ttu-id="4bfd0-180">2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-180">2</span></span></li>
<li><span data-ttu-id="4bfd0-181">2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bfd0-182">Você deseja alocar os primeiros 25% dos custos para uma fonte de financiamento e o restante para uma segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4bfd0-183">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="4bfd0-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="4bfd0-184">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfd0-185">25%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-185">25%</span></span></li>
<li><span data-ttu-id="4bfd0-186">100%</span><span class="sxs-lookup"><span data-stu-id="4bfd0-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfd0-187">0</span><span class="sxs-lookup"><span data-stu-id="4bfd0-187">1</span></span></li>
<li><span data-ttu-id="4bfd0-188">2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="4bfd0-189">Exemplo: múltiplas fontes de financiamento (complexo)</span><span class="sxs-lookup"><span data-stu-id="4bfd0-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="4bfd0-190">Você tem três fontes de financiamento que deseja usar na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="4bfd0-191">Usar as fontes de financiamento 2 e 3 igualmente até que a fonte de financiamento 2 se esgote.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="4bfd0-192">Continuar a usar a fonte de financiamento 3 até que ela se esgote.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="4bfd0-193">Usar a fonte de financiamento 1 depois que a fonte de financiamento 3 se esgotar.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="4bfd0-194">Para atingir essa meta, primeiro faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="4bfd0-195">Estabeleça limites de financiamento para as fontes de financiamento 2 e 3, para seus respectivos valores.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="4bfd0-196">Crie as seguintes regras de financiamento:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="4bfd0-197">Regra 1 (prioridade 1): alocar 50% das transações para a fonte de financiamento 2 e 50% para a fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="4bfd0-198">Regra 2 (prioridade 2): alocar 100% das transações para a fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="4bfd0-199">Regra 3 (prioridade 3): alocar 100% das transações para a fonte de financiamento 1.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="4bfd0-200">Essa configuração funciona porque as transações são verificadas em relação às regras e limites para determinar se alguma delas se aplica à transação.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="4bfd0-201">Se nenhuma regra ou limite específico se aplicar à transação, a regra Todas as transações se aplica.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="4bfd0-202">A regra Todas as transações corresponde a todas as transações.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="4bfd0-203">Se for encontrada uma regra que corresponda a uma transação, a porcentagem que foi alocada nessa regra será aplicada primeiro, mas somente depois que as correspondências forem verificadas em relação a quaisquer limites configurados.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="4bfd0-204">Se um limite foi atingido e os fundos de uma fonte de financiamento se esgotaram, a regra de financiamento associada ao limite de financiamento é desconsiderada e o programa verifica a próxima regra aplicável.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="4bfd0-205">Em alguns casos, apenas parte de uma transação pode ser alocada sob uma regra.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="4bfd0-206">Isso pode acontecer quando um limite é atingido ao alocar a transação.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="4bfd0-207">Nesse caso, apenas um determinado valor é alocado de acordo com essa regra, como 50% para cada fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="4bfd0-208">Esse é o caso da regra 1, descrita anteriormente nesta seção.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="4bfd0-209">O restante é alocado de acordo com a próxima regra na sequência.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="4bfd0-210">A tabela a seguir examina esse cenários em mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bfd0-211"><strong>Foco</strong></span><span class="sxs-lookup"><span data-stu-id="4bfd0-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="4bfd0-212"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="4bfd0-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bfd0-213">Regras de financiamento</span><span class="sxs-lookup"><span data-stu-id="4bfd0-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="4bfd0-214">Regra 1 (prioridade 1): todas as transações.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="4bfd0-215">Alocar a fonte de financiamento 2 em 50% e a fonte de financiamento 3 em 50%.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="4bfd0-216">Regra 2 (prioridade 2): todas as transações.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="4bfd0-217">Alocar a fonte de financiamento 3 em 100%.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="4bfd0-218">Regra 3 (prioridade 2): todas as transações.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="4bfd0-219">Alocar a fonte de financiamento 1 em 100%.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bfd0-220">Limites de financiamento</span><span class="sxs-lookup"><span data-stu-id="4bfd0-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="4bfd0-221">Limite da fonte de financiamento 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="4bfd0-222">Limite da fonte de financiamento 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="4bfd0-223">Limite da fonte de financiamento 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bfd0-224">Transação 1</span><span class="sxs-lookup"><span data-stu-id="4bfd0-224">Transaction 1</span></span></td>
<td><span data-ttu-id="4bfd0-225"><strong>Valor da transação:</strong> 100,00<strong>Financiamento:</strong> a transação é paga de acordo com a regra 1 apenas, porque a transação é totalmente paga após a aplicação da regra 1.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="4bfd0-226">A transação é financiada igualmente entre as fontes de financiamento 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="4bfd0-227">Fonte de financiamento 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="4bfd0-228">Fonte de financiamento 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bfd0-229">Transação 2</span><span class="sxs-lookup"><span data-stu-id="4bfd0-229">Transaction 2</span></span></td>
<td><span data-ttu-id="4bfd0-230"><strong>Valor da transação:</strong> 5.000,00<strong>Financiamento:</strong> a transação é paga de acordo com as três regras.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="4bfd0-231"><strong>Regra 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="4bfd0-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="4bfd0-232">Fonte de financiamento 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="4bfd0-233">Fonte de financiamento 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="4bfd0-234">
<strong>Regra 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="4bfd0-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="4bfd0-235">Fonte de financiamento 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="4bfd0-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="4bfd0-236">
<strong>Regra 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="4bfd0-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="4bfd0-237">Fonte de financiamento 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="4bfd0-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bfd0-238">Total de fundos que são distribuídos para cada fonte de financiamento</span><span class="sxs-lookup"><span data-stu-id="4bfd0-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="4bfd0-239">Fonte de financiamento 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="4bfd0-240">Fonte de financiamento 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="4bfd0-241">Fonte de financiamento 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="4bfd0-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="4bfd0-242">Regras de cobrança</span><span class="sxs-lookup"><span data-stu-id="4bfd0-242">Billing rules</span></span>
<span data-ttu-id="4bfd0-243">Ao negociar um contrato de projeto com um cliente, você define como e quando pode faturar o cliente pelo trabalho em um projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="4bfd0-244">Depois de configurar o contrato de projeto e o projeto, você pode configurar as regras de cobrança do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="4bfd0-245">As regras de cobrança são baseadas nos termos do projeto especificados no contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="4bfd0-246">As regras de cobrança que você pode criar dependem dos termos do contrato de projeto e do tipo de projeto (por exemplo, de tempo e material ou de preço fixo) que você associa à regra de cobrança.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="4bfd0-247">Você pode criar mais de uma regra de cobrança para um contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="4bfd0-248">Você também pode atribuir uma regra de cobrança a vários projetos que estão associados ao mesmo contrato de projeto e têm termos de cobrança semelhantes.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="4bfd0-249">Você pode configurar os seguintes tipos de regras de cobrança:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="4bfd0-250">**Unidade de entrega**: faturar um cliente ao concluir uma unidade de entrega.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="4bfd0-251">Você define as unidades de entrega no contrato.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="4bfd0-252">**Progresso**: faturar um cliente quando você concluir uma porcentagem especificada do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="4bfd0-253">Você pode configurar uma regra de cobrança para calcular automaticamente a porcentagem de trabalho concluído, ou pode calcular manualmente a porcentagem de trabalho concluído e o valor para faturar o cliente.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="4bfd0-254">**Etapa**: faturar um cliente pelo valor total de uma etapa do projeto quando ela for atingida.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="4bfd0-255">**Taxa**: faturar um cliente por seus serviços, mais uma taxa de administração, que normalmente é uma porcentagem do custo dos serviços.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="4bfd0-256">**Tempo e material**: faturar um cliente pelo valor do tempo e dos materiais usados em um projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="4bfd0-257">Para todos os tipos de regras de cobrança, você pode especificar uma porcentagem de retenção que é deduzida das faturas do cliente até que um projeto alcance um estágio combinado.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="4bfd0-258">A porcentagem de retenção de pagamento é especificada no contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="4bfd0-259">O valor é calculado com base no valor total das linhas em uma fatura do cliente e subtraído dele.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="4bfd0-260">Para regras de cobrança de **Tempo e material** e **Progresso**, você pode atribuir categorias cobráveis.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="4bfd0-261">As categorias cobráveis indicam as transações que devem ser incluídas nas faturas do cliente.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="4bfd0-262">Quando você está pronto para faturar o cliente, o valor da fatura para o projeto é calculado com base nas regras de cobrança, e uma proposta de fatura do projeto é gerada.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="4bfd0-263">As seções a seguir fornecem exemplos que mostram como configurar e gerenciar regras de cobrança para um projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="4bfd0-264">Exemplo: criar uma regra de cobrança baseada no número de unidades entregues</span><span class="sxs-lookup"><span data-stu-id="4bfd0-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="4bfd0-265">Sua organização firma um contrato para fornecer um total de cinco sessões de treinamento para os funcionários de um cliente a um custo de 10.000 por sessão de treinamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="4bfd0-266">Você fatura o cliente após cada sessão de treinamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="4bfd0-267">Ao configurar as regras de cobrança para o contrato, você usa os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="4bfd0-268">A unidade de entrega é uma sessão de treinamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="4bfd0-269">O preço unitário é 10.000 por sessão de treinamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="4bfd0-270">O número total de unidades é cinco sessões de treinamento.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="4bfd0-271">Quando tiver concluído uma sessão de treinamento, você poderá criar uma fatura de 10.000 para a primeira unidade que foi entregue, e enviar a fatura ao cliente.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="4bfd0-272">Exemplo: criar uma regra de cobrança com base em uma porcentagem especificada de conclusão do projeto (cálculo manual)</span><span class="sxs-lookup"><span data-stu-id="4bfd0-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="4bfd0-273">Sua organização, uma empresa de consultoria de software, celebra um contrato com um cliente para desenvolver parte de um produto que o cliente está desenvolvendo.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="4bfd0-274">Sua organização concorda em entregar o código do software em um período de seis meses.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="4bfd0-275">O cliente concorda em pagar à sua organização um total de 100.000 pelo trabalho.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="4bfd0-276">Você cria uma regra de cobrança para faturar o cliente com base na porcentagem de trabalho concluído no projeto, conforme especificado no contrato.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="4bfd0-277">No final do primeiro mês, você se encontra com o cliente para determinar a porcentagem do trabalho concluído.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="4bfd0-278">Depois que você e o cliente analisam o projeto, você decide que ele está 15% concluído.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="4bfd0-279">Você cria uma fatura de 15.000 (15% de 100.000) e a envia ao cliente.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="4bfd0-280">Exemplo: criar uma regra de cobrança com base em uma porcentagem especificada de conclusão do projeto (cálculo automático)</span><span class="sxs-lookup"><span data-stu-id="4bfd0-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="4bfd0-281">Sua organização, uma empresa de desenvolvimento de software, concorda em desenvolver um pacote de contabilidade da folha de pagamento para um cliente por 30.000.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="4bfd0-282">O cliente concorda em pagar à sua organização com base em uma porcentagem do trabalho concluído.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="4bfd0-283">Você estima que os custos do projeto são 20.000.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="4bfd0-284">O contrato do projeto especifica as categorias de trabalho que você usa no processo de cobrança.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="4bfd0-285">Você configura regras de cobrança que calculam automaticamente os valores da fatura para a porcentagem de trabalho concluído em cada categoria.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="4bfd0-286">Você configura um orçamento para cada categoria:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="4bfd0-287">**Desenvolvimento**: custo de 15.000 e receita de 20.000</span><span class="sxs-lookup"><span data-stu-id="4bfd0-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="4bfd0-288">**Instalação**: custo de 5.000 e receita de 10.000</span><span class="sxs-lookup"><span data-stu-id="4bfd0-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="4bfd0-289">Quando você cria uma fatura do cliente pela primeira vez, o valor dela é calculado automaticamente com base nas seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="4bfd0-290">Depois de um mês, o funcionário do projeto envia uma folha de ponto para o projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="4bfd0-291">O custo das horas do funcionário é de 5.000 para desenvolvimento e 1.000 para instalação.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="4bfd0-292">O trabalho de desenvolvimento está 33% concluído (custo real de 5.000/custo orçado de 15.000) e o trabalho de instalação está 20% concluído (custo real de 1.000/custo orçado de 5.000).</span><span class="sxs-lookup"><span data-stu-id="4bfd0-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="4bfd0-293">O valor da fatura de 8.667 é calculado automaticamente (33% de 20.000 + 20% de 10.000).</span><span class="sxs-lookup"><span data-stu-id="4bfd0-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="4bfd0-294">Você cria uma fatura de 8.667 e a envia ao cliente.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="4bfd0-295">Exemplo: criar uma regra de cobrança baseada em etapas acordadas</span><span class="sxs-lookup"><span data-stu-id="4bfd0-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="4bfd0-296">Sua organização, uma empresa de consultoria de gestão, concorda em conduzir pesquisas de mercado para um produto de consumo que o cliente planeja vender.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="4bfd0-297">O cliente concorda em usar seus serviços por um período de três meses, começando em março, e concorda em pagar 50.000 à sua organização.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="4bfd0-298">O projeto tem três etapas:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-298">The project has three milestones:</span></span>

-   <span data-ttu-id="4bfd0-299">Etapa 1: coletar dados de consumo – 31 de março</span><span class="sxs-lookup"><span data-stu-id="4bfd0-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="4bfd0-300">Etapa 2: analisar dados de consumo – 30 de abril</span><span class="sxs-lookup"><span data-stu-id="4bfd0-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="4bfd0-301">Etapa 3: apresentar uma proposta de viabilidade do produto – 31 de maio</span><span class="sxs-lookup"><span data-stu-id="4bfd0-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="4bfd0-302">O cliente concorda em pagar à sua organização 10.000 pela primeira etapa, 20.000 pela segunda e 20.000 pela terceira.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="4bfd0-303">Ao configurar o contrato de projeto, você concorda em cobrar o cliente com base na etapa que foi concluída.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="4bfd0-304">A configuração da regra de cobrança inclui os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="4bfd0-305">Definir as etapas do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-305">Define the project milestones.</span></span>
-   <span data-ttu-id="4bfd0-306">Definir o valor para faturar o cliente quando cada etapa for concluída.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="4bfd0-307">Quando a primeira etapa é concluída em 31 de março, você a marca como concluída e, em seguida, cria uma fatura de 10.000 e a envia ao cliente.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="4bfd0-308">Você não pode criar uma fatura para uma etapa até que tenha marcado essa etapa como concluída.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="4bfd0-309">Exemplo: criar uma regra de cobrança baseada em serviços mais uma taxa de administração</span><span class="sxs-lookup"><span data-stu-id="4bfd0-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="4bfd0-310">Sua organização, uma empresa de consultoria de gestão, concorda em conduzir pesquisas de mercado para avaliar a viabilidade de um produto que o cliente, uma empresa de varejo, está desenvolvendo.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="4bfd0-311">Os termos do contrato especificam que você fornecerá os serviços de seus três principais consultores de gestão, que conduzirão a pesquisa com base no tempo e nos materiais utilizados.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="4bfd0-312">O cliente concorda em pagar 100 por hora, mais uma taxa de administração de 10% pelas horas de consultoria cobradas do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="4bfd0-313">Ao configurar o contrato do projeto, crie uma regra de cobrança para adicionar uma taxa de administração de 10% às horas de consultoria que são cobradas do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="4bfd0-314">Quando você cria uma fatura para o cliente, ele é cobrado uma taxa de administração de 10% mais o custo das horas de consultoria.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="4bfd0-315">Por exemplo, se os três consultores trabalharam um total de 200 horas no projeto, uma fatura de 22.000 será criada com base no seguinte cálculo:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="4bfd0-316">200 horas a 100 por hora = 20.000</span><span class="sxs-lookup"><span data-stu-id="4bfd0-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="4bfd0-317">Taxa de administração de 10% = 2.000</span><span class="sxs-lookup"><span data-stu-id="4bfd0-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="4bfd0-318">Valor total da fatura = 22.000</span><span class="sxs-lookup"><span data-stu-id="4bfd0-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="4bfd0-319">Se as taxas forem tributáveis para um cliente e você selecionar um grupo de impostos sobre vendas no contrato de projeto, esse grupo será inserido automaticamente em uma regra de cobrança de taxas.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="4bfd0-320">Exemplo: criar uma regra de cobrança para o valor de tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="4bfd0-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="4bfd0-321">Sua organização, uma empresa de consultoria de software, concorda em fornecer cinco consultores técnicos para trabalhar em um projeto de desenvolvimento de software para um cliente nos próximos seis meses.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="4bfd0-322">O cliente concorda em pagar 150 por hora de consultoria, mais o custo do material de escritório.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="4bfd0-323">Sua organização envia uma fatura ao cliente no final de cada mês.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="4bfd0-324">Ao definir o contrato de projeto, você concorda em cobrar do cliente todo mês o tempo e os materiais do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="4bfd0-325">Você cria uma regra de cobrança que inclui as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="4bfd0-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="4bfd0-326">O período do contrato é de seis meses.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-326">The contract period is six months.</span></span>
-   <span data-ttu-id="4bfd0-327">O tempo de consultoria é calculado a uma taxa de 150 por hora.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="4bfd0-328">Os materiais de escritório são faturados pelo custo, e o custo total do projeto não deve exceder 10.000.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="4bfd0-329">Você cria uma fatura do cliente no final de cada mês durante o projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="4bfd0-330">No primeiro mês, são registradas 800 horas pelos consultores do projeto.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="4bfd0-331">O custo do material de escritório cobrado do projeto é de 2.000.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="4bfd0-332">Portanto, ao final do mês, você cria uma fatura de 122.000, que é calculada como 800 horas a 150 por hora, mais 2.000 para materiais de escritório.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



