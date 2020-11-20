---
title: Visão geral de linhas de cotação baseadas em projeto
description: Este tópico fornece informações sobre como usar linhas de cotação baseadas no projeto para o trabalho do projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181843"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="6b526-103">Visão geral de linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="6b526-103">Project-based quote lines overview</span></span>

<span data-ttu-id="6b526-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="6b526-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6b526-105">As linhas de cotação baseadas em projeto são projetadas para ajudar a estimar o trabalho do projeto em uma participação.</span><span class="sxs-lookup"><span data-stu-id="6b526-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6b526-106">A estrutura de uma linha de cotação baseada em projeto é estendida para estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="6b526-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6b526-107">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="6b526-107">Billing Method</span></span>
- <span data-ttu-id="6b526-108">Mapeamento de projeto</span><span class="sxs-lookup"><span data-stu-id="6b526-108">Project Mapping</span></span>
- <span data-ttu-id="6b526-109">Classes de transação incluídas</span><span class="sxs-lookup"><span data-stu-id="6b526-109">Included Transaction classes</span></span>
- <span data-ttu-id="6b526-110">Limite máximo</span><span class="sxs-lookup"><span data-stu-id="6b526-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6b526-111">Configuração dos encargos</span><span class="sxs-lookup"><span data-stu-id="6b526-111">Chargeability setup</span></span>
- <span data-ttu-id="6b526-112">Estimativa usando os detalhes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="6b526-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6b526-113">Clientes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="6b526-113">Quote line Customers</span></span>

<span data-ttu-id="6b526-114">A tabela a seguir fornece informações sobre os campos na guia **Geral** da linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="6b526-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6b526-115">Esses campos ajudam a estabelecer uma base para uma estimativa detalhada do trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="6b526-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6b526-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="6b526-116">**Field**</span></span> | <span data-ttu-id="6b526-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6b526-117">**Description**</span></span> | <span data-ttu-id="6b526-118">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="6b526-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6b526-119">Nome</span><span class="sxs-lookup"><span data-stu-id="6b526-119">Name</span></span> | <span data-ttu-id="6b526-120">O nome da linha de cotação que deve ajudar você a identificar o componente discreto da cotação que está sendo estimada.</span><span class="sxs-lookup"><span data-stu-id="6b526-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6b526-121">Copiado para a linha do contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-122">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="6b526-122">Billing Method</span></span> | <span data-ttu-id="6b526-123">Em uma cotação é criada a partir de uma oportunidade, este valor é copiado do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="6b526-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6b526-124">Este campo inclui os dois modelos de contratação principais compatíveis com o Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="6b526-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6b526-125">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6b526-125">- Fixed price</span></span></br><span data-ttu-id="6b526-126">- Hora e material.</span><span class="sxs-lookup"><span data-stu-id="6b526-126">- Time and material.</span></span>| <span data-ttu-id="6b526-127">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-128">Project</span><span class="sxs-lookup"><span data-stu-id="6b526-128">Project</span></span> | <span data-ttu-id="6b526-129">Use este campo opcional para identificar o projeto que será usado para entregar o trabalho nesta participação.</span><span class="sxs-lookup"><span data-stu-id="6b526-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6b526-130">Quando um projeto é mapeado para uma linha de cotação, isso ajuda a configurar tarefas cobráveis e também a gerar uma estimativa baseada em projeto para a linha de cotação como detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6b526-131">Quando um projeto não é mapeado para uma linha de cotação baseada em projeto, a estimativa deve ser criada manualmente criando cada detalhe da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6b526-132">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-133">Incluir Hora</span><span class="sxs-lookup"><span data-stu-id="6b526-133">Include Time</span></span> | <span data-ttu-id="6b526-134">Um sinalizador **Sim**/**Não** indica se as transações de tempo ou custo de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b526-135">Um valor **Não** indica que as transações de tempo ou custo de mão de obra não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b526-136">Um valor **Sim** indica que as transações de tempo ou custo de mão de obra serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6b526-137">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-138">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="6b526-138">Include Expense</span></span> | <span data-ttu-id="6b526-139">Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b526-140">Um valor **Não** indica que as despesas de custo não serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b526-141">Um valor **Sim** indica que as despesas de custo serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6b526-142">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-143">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="6b526-143">Include Fee</span></span> | <span data-ttu-id="6b526-144">Um sinalizador **Sim**/**Não** indica se os valores no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b526-145">Um valor **Não** indica que os valores não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b526-146">Um valor **Sim** indica que os valores serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6b526-147">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-148">Valor da Cotação</span><span class="sxs-lookup"><span data-stu-id="6b526-148">Quoted Amount</span></span> | <span data-ttu-id="6b526-149">Este é o valor que será cotado ao cliente para todo o trabalho previsto nesta linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="6b526-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6b526-150">Em uma cotação criada a partir de uma oportunidade, este valor é copiado do campo **Orçamento do cliente** na linha da oportunidade.</span><span class="sxs-lookup"><span data-stu-id="6b526-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6b526-151">Quando a linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6b526-152">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-153">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="6b526-153">Estimated Tax</span></span> | <span data-ttu-id="6b526-154">Este é um campo editável para o usuário adicionar o valor estimado do imposto na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6b526-155">Quando uma linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor do imposto nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6b526-156">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-157">Valor Cotado Após Imposto</span><span class="sxs-lookup"><span data-stu-id="6b526-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="6b526-158">Este campo é o valor da linha de cotação após o imposto e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6b526-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6b526-159">O valor neste campo é calculado como *Valor cotado + imposto*.</span><span class="sxs-lookup"><span data-stu-id="6b526-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6b526-160">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-161">Limite de NTE (limite máximo)</span><span class="sxs-lookup"><span data-stu-id="6b526-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="6b526-162">Este campo é editável e está disponível apenas em linhas de cotação baseadas em projeto que tenham o método de cobrança **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="6b526-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6b526-163">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b526-164">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="6b526-164">Customer Budget</span></span> | <span data-ttu-id="6b526-165">Se a cotação tiver sido criada a partir de uma Oportunidade, este campo é editável e copiado a partir do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="6b526-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6b526-166">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="6b526-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6b526-167">Regras de validação para os campos na guia Geral de linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="6b526-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6b526-168">**Regra 1** : uma determinada classe de transação no projeto selecionado só pode ser incluída em uma linha de cotação baseada em projeto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="6b526-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6b526-169">**Regra 2** : se uma oportunidade tiver várias cotações, pode haver linhas de cotação de cotações diferentes que façam referência ao mesmo projeto e incluam a mesma classe de transação.</span><span class="sxs-lookup"><span data-stu-id="6b526-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6b526-170">**Regra 3** : se as cotações não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transação.</span><span class="sxs-lookup"><span data-stu-id="6b526-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="6b526-171">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6b526-172">
                    <strong>Cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6b526-173">
                    <strong>Linha de cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6b526-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6b526-175">
                    <strong>Incluir hora</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6b526-176">
                    <strong>Incluir despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6b526-177">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6b526-178">
                    <strong>valor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="6b526-179">
                    <strong>Válido/ Não inválido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="6b526-180">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b526-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b526-181">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-182">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-183">QL1</span><span class="sxs-lookup"><span data-stu-id="6b526-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-184">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-185">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-186">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-187">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-188">Não é válido</span><span class="sxs-lookup"><span data-stu-id="6b526-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-189">Violação da regra nº1.</span><span class="sxs-lookup"><span data-stu-id="6b526-189">Violation of Rule #1.</span></span> <span data-ttu-id="6b526-190">Tempo, despesa e valores no projeto P1 estão incluídos em ambas as linhas de cotação, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="6b526-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b526-191">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-192">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-193">QL2</span><span class="sxs-lookup"><span data-stu-id="6b526-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-194">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-195">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-196">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-197">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-197">Yes</span></span> </p>
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
<span data-ttu-id="6b526-198">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-199">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-200">QL1</span><span class="sxs-lookup"><span data-stu-id="6b526-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-201">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-202">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-203">No</span><span class="sxs-lookup"><span data-stu-id="6b526-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-204">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-205">Não é válido</span><span class="sxs-lookup"><span data-stu-id="6b526-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-206">Violação da regra nº1.</span><span class="sxs-lookup"><span data-stu-id="6b526-206">Violation of Rule #1.</span></span> <span data-ttu-id="6b526-207">Tempo e valores no projeto P1 estão incluídos em ambas as linhas de cotação, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="6b526-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b526-208">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-209">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-210">QL2</span><span class="sxs-lookup"><span data-stu-id="6b526-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-211">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-212">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-213">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-214">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-214">Yes</span></span> </p>
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
<span data-ttu-id="6b526-215">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-216">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-217">QL1</span><span class="sxs-lookup"><span data-stu-id="6b526-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-218">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-219">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-220">No</span><span class="sxs-lookup"><span data-stu-id="6b526-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-221">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-222">Válido</span><span class="sxs-lookup"><span data-stu-id="6b526-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="6b526-223">Tempo e valores do projeto P1 estão incluídos no QL1.</span><span class="sxs-lookup"><span data-stu-id="6b526-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="6b526-224">A despesa do projeto P1 está incluída no QL2.</span><span class="sxs-lookup"><span data-stu-id="6b526-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="6b526-225">Não há sobreposição no que está sendo incluído em cada linha de cotação, portanto, é válido.</span><span class="sxs-lookup"><span data-stu-id="6b526-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b526-226">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-227">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-228">QL2</span><span class="sxs-lookup"><span data-stu-id="6b526-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-229">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-230">No</span><span class="sxs-lookup"><span data-stu-id="6b526-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-231">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-232">No</span><span class="sxs-lookup"><span data-stu-id="6b526-232">No</span></span> </p>
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
<span data-ttu-id="6b526-233">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-234">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-235">QL1</span><span class="sxs-lookup"><span data-stu-id="6b526-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-236">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-237">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-238">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-239">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-240">Não é válido</span><span class="sxs-lookup"><span data-stu-id="6b526-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-241">Violação da regra nº1 acima</span><span class="sxs-lookup"><span data-stu-id="6b526-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="6b526-242">Q1 inclui Tempo, despesas e valores para todo o projeto P1.</span><span class="sxs-lookup"><span data-stu-id="6b526-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6b526-243">QL2 inclui Tempo, despesas e valores para todo o projeto P1 e se sobrepõe ao que está incluído em Q1.</span><span class="sxs-lookup"><span data-stu-id="6b526-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b526-244">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-245">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-246">QL2</span><span class="sxs-lookup"><span data-stu-id="6b526-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-247">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-248">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-249">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-250">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-250">Yes</span></span> </p>
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
<span data-ttu-id="6b526-251">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-252">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-253">QL1</span><span class="sxs-lookup"><span data-stu-id="6b526-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-254">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-255">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-256">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-257">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6b526-258">Válido</span><span class="sxs-lookup"><span data-stu-id="6b526-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-259">Com base na regra nº2, Q1 e Q2 são duas cotações na mesma oportunidade, então ambos podem estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="6b526-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b526-260">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-261">T2</span><span class="sxs-lookup"><span data-stu-id="6b526-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-262">QL1 em Q2</span><span class="sxs-lookup"><span data-stu-id="6b526-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-263">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-264">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-265">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-266">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-266">Yes</span></span> </p>
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
<span data-ttu-id="6b526-267">O1</span><span class="sxs-lookup"><span data-stu-id="6b526-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-268">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-269">QL1</span><span class="sxs-lookup"><span data-stu-id="6b526-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-270">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-271">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-272">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-273">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6b526-274">Válido</span><span class="sxs-lookup"><span data-stu-id="6b526-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b526-275">Com base na regra nº3, Q1 e Q2 são duas cotações em oportunidades diferentes, então não podem estimar para os mesmos componentes do mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="6b526-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b526-276">O2</span><span class="sxs-lookup"><span data-stu-id="6b526-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b526-277">T1</span><span class="sxs-lookup"><span data-stu-id="6b526-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-278">QL1</span><span class="sxs-lookup"><span data-stu-id="6b526-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-279">P1</span><span class="sxs-lookup"><span data-stu-id="6b526-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-280">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b526-281">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b526-282">Sim</span><span class="sxs-lookup"><span data-stu-id="6b526-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6b526-283">Não é válido</span><span class="sxs-lookup"><span data-stu-id="6b526-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

