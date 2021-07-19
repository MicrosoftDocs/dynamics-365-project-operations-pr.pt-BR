---
title: Visão geral de linhas de cotação de projeto
description: Este tópico fornece informações sobre como usar linhas de cotação de projeto para o trabalho do projeto.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: c585bbc55119e678a4f75f5dfe8966a436db1a34
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368057"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="6eced-103">Visão geral de linhas de cotação de projeto</span><span class="sxs-lookup"><span data-stu-id="6eced-103">Project quote lines overview</span></span>

<span data-ttu-id="6eced-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="6eced-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6eced-105">As linhas de cotação baseadas em projeto são projetadas para ajudar a estimar o trabalho do projeto em uma participação.</span><span class="sxs-lookup"><span data-stu-id="6eced-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6eced-106">A estrutura de uma linha de cotação baseada em projeto é estendida para estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="6eced-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6eced-107">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="6eced-107">Billing Method</span></span>
- <span data-ttu-id="6eced-108">Mapeamento de projeto</span><span class="sxs-lookup"><span data-stu-id="6eced-108">Project Mapping</span></span>
- <span data-ttu-id="6eced-109">Classes de transação incluídas</span><span class="sxs-lookup"><span data-stu-id="6eced-109">Included Transaction classes</span></span>
- <span data-ttu-id="6eced-110">Limite máximo</span><span class="sxs-lookup"><span data-stu-id="6eced-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6eced-111">Configuração dos encargos</span><span class="sxs-lookup"><span data-stu-id="6eced-111">Chargeability setup</span></span>
- <span data-ttu-id="6eced-112">Estimativa usando os detalhes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="6eced-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6eced-113">Clientes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="6eced-113">Quote line Customers</span></span>

<span data-ttu-id="6eced-114">A tabela a seguir fornece informações sobre os campos na guia **Geral** da linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="6eced-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6eced-115">Esses campos ajudam a estabelecer uma base para uma estimativa detalhada do trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="6eced-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6eced-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="6eced-116">**Field**</span></span> | <span data-ttu-id="6eced-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6eced-117">**Description**</span></span> | <span data-ttu-id="6eced-118">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="6eced-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6eced-119">Nome</span><span class="sxs-lookup"><span data-stu-id="6eced-119">Name</span></span> | <span data-ttu-id="6eced-120">O nome da linha de cotação que deve ajudar você a identificar o componente discreto da cotação que está sendo estimada.</span><span class="sxs-lookup"><span data-stu-id="6eced-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6eced-121">Copiado para a linha do contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-122">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="6eced-122">Billing Method</span></span> | <span data-ttu-id="6eced-123">Em uma cotação é criada a partir de uma oportunidade, este valor é copiado do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="6eced-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6eced-124">Este campo inclui os dois principais modelos de contratação compatíveis com o Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="6eced-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6eced-125">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6eced-125">- Fixed price</span></span></br><span data-ttu-id="6eced-126">- Hora e material.</span><span class="sxs-lookup"><span data-stu-id="6eced-126">- Time and material.</span></span>| <span data-ttu-id="6eced-127">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-128">Project</span><span class="sxs-lookup"><span data-stu-id="6eced-128">Project</span></span> | <span data-ttu-id="6eced-129">Use este campo opcional para identificar o projeto que será usado para entregar o trabalho nesta participação.</span><span class="sxs-lookup"><span data-stu-id="6eced-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6eced-130">Quando um projeto é mapeado para uma linha de cotação, isso ajuda a configurar tarefas cobráveis e também a gerar uma estimativa baseada em projeto para a linha de cotação como detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6eced-131">Quando um projeto não é mapeado para uma linha de cotação baseada em projeto, a estimativa deve ser criada manualmente criando cada detalhe da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6eced-132">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-133">Incluir Hora</span><span class="sxs-lookup"><span data-stu-id="6eced-133">Include Time</span></span> | <span data-ttu-id="6eced-134">Um sinalizador **Sim**/**Não** indica se as transações de tempo ou custo de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6eced-135">Um valor **Não** indica que as transações de tempo ou custo de mão de obra não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6eced-136">Um valor **Sim** indica que as transações de tempo ou custo de mão de obra serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6eced-137">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-138">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="6eced-138">Include Expense</span></span> | <span data-ttu-id="6eced-139">Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6eced-140">Um valor **Não** indica que as despesas de custo não serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6eced-141">Um valor **Sim** indica que as despesas de custo serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6eced-142">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-143">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="6eced-143">Include Fee</span></span> | <span data-ttu-id="6eced-144">Um sinalizador **Sim**/**Não** indica se os valores no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6eced-145">Um valor **Não** indica que os valores não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6eced-146">Um valor **Sim** indica que os valores serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6eced-147">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-148">Valor da Cotação</span><span class="sxs-lookup"><span data-stu-id="6eced-148">Quoted Amount</span></span> | <span data-ttu-id="6eced-149">Este é o valor que será cotado ao cliente para todo o trabalho previsto nesta linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="6eced-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6eced-150">Em uma cotação criada a partir de uma oportunidade, este valor é copiado do campo **Orçamento do cliente** na linha da oportunidade.</span><span class="sxs-lookup"><span data-stu-id="6eced-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6eced-151">Quando a linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6eced-152">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-153">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="6eced-153">Estimated Tax</span></span> | <span data-ttu-id="6eced-154">Este é um campo editável para o usuário adicionar o valor estimado do imposto na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6eced-155">Quando uma linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor do imposto nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6eced-156">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-157">Valor Cotado Após Imposto</span><span class="sxs-lookup"><span data-stu-id="6eced-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="6eced-158">Este campo é o valor da linha de cotação após o imposto e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6eced-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6eced-159">O valor neste campo é calculado como *Valor cotado + imposto*.</span><span class="sxs-lookup"><span data-stu-id="6eced-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6eced-160">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-161">Limite de NTE (limite máximo)</span><span class="sxs-lookup"><span data-stu-id="6eced-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="6eced-162">Este campo é editável e está disponível apenas em linhas de cotação baseadas em projeto que tenham o método de cobrança **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="6eced-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6eced-163">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6eced-164">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="6eced-164">Customer Budget</span></span> | <span data-ttu-id="6eced-165">Se a cotação tiver sido criada a partir de uma Oportunidade, este campo é editável e copiado a partir do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="6eced-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6eced-166">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6eced-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6eced-167">Regras de validação para os campos na guia Geral de linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="6eced-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6eced-168">**Regra 1** : uma determinada classe de transação no projeto selecionado só pode ser incluída em uma linha de cotação baseada em projeto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="6eced-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6eced-169">**Regra 2** : se uma oportunidade tiver várias cotações, pode haver linhas de cotação de cotações diferentes que façam referência ao mesmo projeto e incluam a mesma classe de transação.</span><span class="sxs-lookup"><span data-stu-id="6eced-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6eced-170">**Regra 3** : se as cotações não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transação.</span><span class="sxs-lookup"><span data-stu-id="6eced-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="6eced-171">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6eced-172">
                    <strong>Cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6eced-173">
                    <strong>Linha de cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6eced-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6eced-175">
                    <strong>Incluir hora</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6eced-176">
                    <strong>Incluir despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6eced-177">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6eced-178">
                    <strong>valor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="6eced-179">
                    <strong>Válido/ Não inválido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="6eced-180">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6eced-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-181">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-182">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-183">QL1</span><span class="sxs-lookup"><span data-stu-id="6eced-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-184">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-185">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-186">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-187">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-188">Não é válido</span><span class="sxs-lookup"><span data-stu-id="6eced-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-189">Violação da regra nº1.</span><span class="sxs-lookup"><span data-stu-id="6eced-189">Violation of Rule #1.</span></span> <span data-ttu-id="6eced-190">Tempo, despesa e valores no projeto P1 estão incluídos em ambas as linhas de cotação, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="6eced-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-191">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-192">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-193">QL2</span><span class="sxs-lookup"><span data-stu-id="6eced-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-194">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-195">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-196">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-197">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-198">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-199">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-200">QL1</span><span class="sxs-lookup"><span data-stu-id="6eced-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-201">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-202">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-203">No</span><span class="sxs-lookup"><span data-stu-id="6eced-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-204">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-205">Não é válido</span><span class="sxs-lookup"><span data-stu-id="6eced-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-206">Violação da regra nº1.</span><span class="sxs-lookup"><span data-stu-id="6eced-206">Violation of Rule #1.</span></span> <span data-ttu-id="6eced-207">Tempo e valores no projeto P1 estão incluídos em ambas as linhas de cotação, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="6eced-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-208">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-209">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-210">QL2</span><span class="sxs-lookup"><span data-stu-id="6eced-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-211">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-212">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-213">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-214">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-215">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-216">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-217">QL1</span><span class="sxs-lookup"><span data-stu-id="6eced-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-218">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-219">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-220">No</span><span class="sxs-lookup"><span data-stu-id="6eced-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-221">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-222">Válido</span><span class="sxs-lookup"><span data-stu-id="6eced-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="6eced-223">Tempo e valores do projeto P1 estão incluídos no QL1.</span><span class="sxs-lookup"><span data-stu-id="6eced-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="6eced-224">A despesa do projeto P1 está incluída no QL2.</span><span class="sxs-lookup"><span data-stu-id="6eced-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="6eced-225">Não há sobreposição no que está sendo incluído em cada linha de cotação, portanto, é válido.</span><span class="sxs-lookup"><span data-stu-id="6eced-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-226">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-227">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-228">QL2</span><span class="sxs-lookup"><span data-stu-id="6eced-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-229">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-230">No</span><span class="sxs-lookup"><span data-stu-id="6eced-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-231">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-232">No</span><span class="sxs-lookup"><span data-stu-id="6eced-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-233">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-234">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-235">QL1</span><span class="sxs-lookup"><span data-stu-id="6eced-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-236">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-237">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-238">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-239">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-240">Não é válido</span><span class="sxs-lookup"><span data-stu-id="6eced-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-241">Violação da regra nº1 acima</span><span class="sxs-lookup"><span data-stu-id="6eced-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="6eced-242">Q1 inclui Tempo, despesas e valores para todo o projeto P1.</span><span class="sxs-lookup"><span data-stu-id="6eced-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6eced-243">QL2 inclui Tempo, despesas e valores para todo o projeto P1 e se sobrepõe ao que está incluído em Q1.</span><span class="sxs-lookup"><span data-stu-id="6eced-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-244">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-245">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-246">QL2</span><span class="sxs-lookup"><span data-stu-id="6eced-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-247">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-248">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-249">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-250">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-251">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-252">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-253">QL1</span><span class="sxs-lookup"><span data-stu-id="6eced-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-254">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-255">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-256">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-257">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6eced-258">Válido</span><span class="sxs-lookup"><span data-stu-id="6eced-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-259">Com base na regra nº2, Q1 e Q2 são duas cotações na mesma oportunidade, então ambos podem estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="6eced-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-260">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-261">T2</span><span class="sxs-lookup"><span data-stu-id="6eced-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-262">QL1 em Q2</span><span class="sxs-lookup"><span data-stu-id="6eced-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-263">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-264">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-265">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-266">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-267">O1</span><span class="sxs-lookup"><span data-stu-id="6eced-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-268">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-269">QL1</span><span class="sxs-lookup"><span data-stu-id="6eced-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-270">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-271">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-272">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-273">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6eced-274">Válido</span><span class="sxs-lookup"><span data-stu-id="6eced-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6eced-275">Com base na regra nº3, Q1 e Q2 são duas cotações em oportunidades diferentes, então não podem estimar para os mesmos componentes do mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="6eced-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6eced-276">O2</span><span class="sxs-lookup"><span data-stu-id="6eced-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6eced-277">T1</span><span class="sxs-lookup"><span data-stu-id="6eced-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-278">QL1</span><span class="sxs-lookup"><span data-stu-id="6eced-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-279">P1</span><span class="sxs-lookup"><span data-stu-id="6eced-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-280">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6eced-281">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6eced-282">Sim</span><span class="sxs-lookup"><span data-stu-id="6eced-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6eced-283">Não é válido</span><span class="sxs-lookup"><span data-stu-id="6eced-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
