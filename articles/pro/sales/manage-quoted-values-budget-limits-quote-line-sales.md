---
title: Visão geral de linhas de cotação baseadas em projeto
description: Este tópico fornece informações sobre como usar linhas de cotação baseadas no projeto para o trabalho do projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369857"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="076c3-103">Visão geral de linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="076c3-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="076c3-104">_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma, Project Operations para cenários com base em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="076c3-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="076c3-105">As linhas de cotação baseadas em projeto são projetadas para ajudar a estimar o trabalho do projeto em uma participação.</span><span class="sxs-lookup"><span data-stu-id="076c3-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="076c3-106">A estrutura de uma linha de cotação baseada em projeto é estendida para estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="076c3-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="076c3-107">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="076c3-107">Billing Method</span></span>
- <span data-ttu-id="076c3-108">Mapeamento de projeto e tarefa</span><span class="sxs-lookup"><span data-stu-id="076c3-108">Project and Task Mapping</span></span>
- <span data-ttu-id="076c3-109">Classes de transação incluídas</span><span class="sxs-lookup"><span data-stu-id="076c3-109">Included Transaction classes</span></span>
- <span data-ttu-id="076c3-110">Limite máximo</span><span class="sxs-lookup"><span data-stu-id="076c3-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="076c3-111">Configuração dos encargos</span><span class="sxs-lookup"><span data-stu-id="076c3-111">Chargeability setup</span></span>
- <span data-ttu-id="076c3-112">Estimativa usando os detalhes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="076c3-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="076c3-113">Clientes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="076c3-113">Quote line Customers</span></span>

<span data-ttu-id="076c3-114">A tabela a seguir fornece informações sobre os campos na guia **Geral** da linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="076c3-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="076c3-115">Esses campos ajudam a estabelecer uma base para uma estimativa detalhada do trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="076c3-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="076c3-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="076c3-116">**Field**</span></span> | <span data-ttu-id="076c3-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="076c3-117">**Description**</span></span> | <span data-ttu-id="076c3-118">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="076c3-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="076c3-119">Nome</span><span class="sxs-lookup"><span data-stu-id="076c3-119">Name</span></span> | <span data-ttu-id="076c3-120">O nome da linha de cotação que ajuda a identificar o componente discreto da cotação que está sendo estimada.</span><span class="sxs-lookup"><span data-stu-id="076c3-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="076c3-121">Copiado para a linha do contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="076c3-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-122">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="076c3-122">Billing Method</span></span> | <span data-ttu-id="076c3-123">Em uma cotação é criada a partir de uma oportunidade, este valor é copiado do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="076c3-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="076c3-124">Este campo inclui os dois principais modelos de contratação compatíveis com o Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="076c3-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="076c3-125">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="076c3-125">- Fixed price</span></span></br><span data-ttu-id="076c3-126">- Hora e material.</span><span class="sxs-lookup"><span data-stu-id="076c3-126">- Time and material.</span></span>| <span data-ttu-id="076c3-127">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-128">Project</span><span class="sxs-lookup"><span data-stu-id="076c3-128">Project</span></span> | <span data-ttu-id="076c3-129">Use este campo opcional para identificar o projeto que será usado para entregar o trabalho nesta participação.</span><span class="sxs-lookup"><span data-stu-id="076c3-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="076c3-130">Quando um projeto é mapeado para uma linha de cotação, isso ajuda a configurar tarefas cobráveis e também a gerar uma estimativa baseada em projeto para a linha de cotação como detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="076c3-131">Quando um projeto não é mapeado para uma linha de cotação baseada em projeto, a estimativa deve ser criada manualmente criando cada detalhe da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="076c3-132">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="076c3-133">Tarefas Incluídas</span><span class="sxs-lookup"><span data-stu-id="076c3-133">Included Tasks</span></span> | <span data-ttu-id="076c3-134">Indica se esta linha de cotação é usada para todas ou algumas das tarefas do projeto para o projeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="076c3-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="076c3-135">Este campo possui os valores possíveis a seguir:</span><span class="sxs-lookup"><span data-stu-id="076c3-135">This field has the following possible values:</span></span></br><span data-ttu-id="076c3-136">- Todas as tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="076c3-136">- All project tasks</span></span></br><span data-ttu-id="076c3-137">- Somente tarefas do projeto selecionadas</span><span class="sxs-lookup"><span data-stu-id="076c3-137">- Selected project tasks only</span></span></br><span data-ttu-id="076c3-138">Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**.</span><span class="sxs-lookup"><span data-stu-id="076c3-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="076c3-139">Quando **Somente tarefas do projeto selecionadas** é selecionado na página do projeto, a guia **Configuração de cobrança da tarefa** permite selecionar tarefas específicas para associá-las a esta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="076c3-140">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-141">Incluir Hora</span><span class="sxs-lookup"><span data-stu-id="076c3-141">Include Time</span></span> | <span data-ttu-id="076c3-142">Um valor **Sim**/**Não** indica se as transações de tempo ou custos de mão de obra no projeto selecionado serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="076c3-143">Um valor **Não** indica que as transações de tempo ou custo de mão de obra não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="076c3-144">Um valor **Sim** indica que as transações de tempo ou custo de mão de obra serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="076c3-145">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-146">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="076c3-146">Include Expense</span></span> | <span data-ttu-id="076c3-147">Um valor **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="076c3-148">Um valor **Não** indica que as despesas de custo não serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="076c3-149">Um valor **Sim** indica que as despesas de custo serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="076c3-150">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-151">Material Incluso</span><span class="sxs-lookup"><span data-stu-id="076c3-151">Include Material</span></span> | <span data-ttu-id="076c3-152">Um valor **Sim**/**Não** indica se os custos de material no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="076c3-153">Um valor **Não** indica que os custos de material não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="076c3-154">Um valor **Sim** indica que os custos de material serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="076c3-155">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-156">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="076c3-156">Include Fee</span></span> | <span data-ttu-id="076c3-157">Um valor **Sim**/**Não** indica se valores no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="076c3-158">Um valor **Não** indica que os valores não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="076c3-159">Um valor **Sim** indica que os valores serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="076c3-160">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-161">Valor da Cotação</span><span class="sxs-lookup"><span data-stu-id="076c3-161">Quoted Amount</span></span> | <span data-ttu-id="076c3-162">Este é o valor que será cotado ao cliente para todo o trabalho previsto nesta linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="076c3-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="076c3-163">Em uma cotação criada a partir de uma oportunidade, este valor é copiado do campo **Orçamento do cliente** na linha da oportunidade.</span><span class="sxs-lookup"><span data-stu-id="076c3-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="076c3-164">Quando a linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="076c3-165">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-166">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="076c3-166">Estimated Tax</span></span> | <span data-ttu-id="076c3-167">Este é um campo editável para o usuário adicionar o valor estimado do imposto na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="076c3-168">Quando uma linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor do imposto nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="076c3-169">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-170">Valor Cotado Após Imposto</span><span class="sxs-lookup"><span data-stu-id="076c3-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="076c3-171">Este campo é o valor da linha de cotação após o imposto e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="076c3-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="076c3-172">O valor neste campo é calculado como *Valor cotado + imposto*.</span><span class="sxs-lookup"><span data-stu-id="076c3-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="076c3-173">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-174">Limite de NTE (limite máximo)</span><span class="sxs-lookup"><span data-stu-id="076c3-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="076c3-175">Este campo é editável e está disponível apenas em linhas de cotação baseadas em projeto que tenham o método de cobrança **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="076c3-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="076c3-176">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="076c3-177">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="076c3-177">Customer Budget</span></span> | <span data-ttu-id="076c3-178">Se a cotação tiver sido criada a partir de uma Oportunidade, este campo é editável e copiado a partir do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="076c3-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="076c3-179">Este valor é copiado para a linha do contrato do projeto criada a partir desta linha de cotação quando a cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="076c3-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="076c3-180">Regras de validação para os campos na guia Geral de linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="076c3-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="076c3-181">**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto será incluído na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="076c3-182">**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em uma única linha de cotação baseada em projeto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="076c3-183">**Regra 3**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Somente determinadas tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em várias linhas de cotação baseada em projeto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="076c3-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="076c3-184">**Regra 4** : se uma oportunidade tiver várias cotações, pode haver linhas de cotação de cotações diferentes que façam referência ao mesmo projeto e incluam a mesma classe de transação.</span><span class="sxs-lookup"><span data-stu-id="076c3-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="076c3-185">**Regra 5**: se as cotações não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transação.</span><span class="sxs-lookup"><span data-stu-id="076c3-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="076c3-186">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="076c3-187">
                    <strong>Cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="076c3-188">
                    <strong>Linha de cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="076c3-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="076c3-190">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="076c3-191">
                    <strong>Incluir Hora</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="076c3-192">
                    <strong>Incluir Despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="076c3-193">
                    <strong>Material Incluso</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="076c3-194">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="076c3-195">
                    <strong>Taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="076c3-196">
                    <strong>Válido/ Não inválido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="076c3-197">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="076c3-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-198">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-199">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-200">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-201">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-202">Em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-203">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-204">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-205">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-206">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-207">Não é válido</span><span class="sxs-lookup"><span data-stu-id="076c3-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-208">Violação da regra Nº 2.</span><span class="sxs-lookup"><span data-stu-id="076c3-208">Violation of Rule #2.</span></span> <span data-ttu-id="076c3-209">Tempo, Despesa e Valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="076c3-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-210">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-211">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-212">QL2</span><span class="sxs-lookup"><span data-stu-id="076c3-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-213">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-214">Em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-215">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-216">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-217">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-218">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-219">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-220">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-221">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-222">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-223">Em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-224">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-225">No</span><span class="sxs-lookup"><span data-stu-id="076c3-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-226">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-227">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-228">Não é válido</span><span class="sxs-lookup"><span data-stu-id="076c3-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-229">Violação da regra Nº 2.</span><span class="sxs-lookup"><span data-stu-id="076c3-229">Violation of Rule #2.</span></span> <span data-ttu-id="076c3-230">Tempo, Material e Valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="076c3-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-231">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-232">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-233">QL2</span><span class="sxs-lookup"><span data-stu-id="076c3-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-234">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-235">Em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-236">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-237">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-238">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-239">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-240">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-241">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-242">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-243">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-244">Em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-245">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-246">No</span><span class="sxs-lookup"><span data-stu-id="076c3-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-247">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-248">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-249">Válido</span><span class="sxs-lookup"><span data-stu-id="076c3-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-250">Tempo, Material e Valores no projeto P1 estão incluídos em QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="076c3-251">A despesa do projeto P1 está incluída em QL2</span><span class="sxs-lookup"><span data-stu-id="076c3-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="076c3-252">Nenhuma sobreposição no que está sendo incluído em cada linha da cotação e, portanto, ela é válida.</span><span class="sxs-lookup"><span data-stu-id="076c3-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-253">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-254">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-255">QL2</span><span class="sxs-lookup"><span data-stu-id="076c3-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-256">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-257">Em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-258">No</span><span class="sxs-lookup"><span data-stu-id="076c3-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-259">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-260">No</span><span class="sxs-lookup"><span data-stu-id="076c3-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-261">No</span><span class="sxs-lookup"><span data-stu-id="076c3-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-262">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-263">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-264">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-265">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-266">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="076c3-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-267">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-268">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-269">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-270">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-271">Não é válido</span><span class="sxs-lookup"><span data-stu-id="076c3-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-272">Violação da regra Nº 2</span><span class="sxs-lookup"><span data-stu-id="076c3-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="076c3-273">Q1 inclui Tempo, Material, Despesas e Valores em um subconjunto de tarefas no projeto P1</span><span class="sxs-lookup"><span data-stu-id="076c3-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="076c3-274">QL2 inclui Tempo, Despesas e Valores para todo o projeto P1 e, portanto, se sobrepõe ao que está incluído em Q1.</span><span class="sxs-lookup"><span data-stu-id="076c3-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-275">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-276">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-277">QL2</span><span class="sxs-lookup"><span data-stu-id="076c3-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-278">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-279">Em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-280">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-281">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-282">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-283">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-284">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-285">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-286">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-287">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-288">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="076c3-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-289">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-290">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-291">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-292">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-293">Válido</span><span class="sxs-lookup"><span data-stu-id="076c3-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-294">Por regra nº 3,</span><span class="sxs-lookup"><span data-stu-id="076c3-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="076c3-295">Q1 inclui Tempo, Material, Despesas e Valores em um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="076c3-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="076c3-296">QL2 inclui Tempo, Material, Despesas e Valores para um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="076c3-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="076c3-297">A única validação adicional é o subconjunto de tarefas no QL1 que difere do subconjunto de tarefas no QL2 para garantir que não haja sobreposições.</span><span class="sxs-lookup"><span data-stu-id="076c3-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="076c3-298">Isso é feito pelo sistema quando as tarefas são associadas.</span><span class="sxs-lookup"><span data-stu-id="076c3-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-299">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-300">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-301">QL2</span><span class="sxs-lookup"><span data-stu-id="076c3-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-302">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-303">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="076c3-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-304">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-305">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-306">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-307">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-308">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-309">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-310">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-311">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-312">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-313">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-314">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-315">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-316">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-317">Válido</span><span class="sxs-lookup"><span data-stu-id="076c3-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-318">De acordo com a regra nº 5, Q1 e Q2 são duas cotações na mesma oportunidade; portanto, ambos podem estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="076c3-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-319">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-320">T2</span><span class="sxs-lookup"><span data-stu-id="076c3-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-321">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-322">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-323">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-324">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-325">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-326">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-327">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-328">O1</span><span class="sxs-lookup"><span data-stu-id="076c3-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-329">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-330">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-331">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-332">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-333">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-334">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-335">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-336">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-337">Não é válido</span><span class="sxs-lookup"><span data-stu-id="076c3-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="076c3-338">De acordo com a regra nº 4, Q1 e Q2 são duas cotações em oportunidades diferentes; portanto, eles não podem fazer estimativa para os mesmos componentes do mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="076c3-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="076c3-339">O2</span><span class="sxs-lookup"><span data-stu-id="076c3-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="076c3-340">T1</span><span class="sxs-lookup"><span data-stu-id="076c3-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="076c3-341">QL1</span><span class="sxs-lookup"><span data-stu-id="076c3-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-342">P1</span><span class="sxs-lookup"><span data-stu-id="076c3-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="076c3-343">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="076c3-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="076c3-344">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="076c3-345">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="076c3-346">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="076c3-347">Sim</span><span class="sxs-lookup"><span data-stu-id="076c3-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
