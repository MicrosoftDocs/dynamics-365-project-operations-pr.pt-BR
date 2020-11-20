---
title: Visão geral de linhas de cotação baseadas em projeto - lite
description: Este tópico fornece informações sobre como usar linhas de cotação baseadas no projeto para o trabalho do projeto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181078"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="fbbb0-104">Visão geral de linhas de cotação baseadas em projeto - lite</span><span class="sxs-lookup"><span data-stu-id="fbbb0-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="fbbb0-105">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="fbbb0-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fbbb0-106">As linhas de cotação baseadas em projeto são projetadas para ajudar a estimar o trabalho do projeto em uma participação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="fbbb0-107">A estrutura de uma linha de cotação baseada em projeto é estendida para estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="fbbb0-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="fbbb0-108">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="fbbb0-108">Billing Method</span></span>
- <span data-ttu-id="fbbb0-109">Mapeamento de projeto e tarefa</span><span class="sxs-lookup"><span data-stu-id="fbbb0-109">Project and Task Mapping</span></span>
- <span data-ttu-id="fbbb0-110">Classes de transação incluídas</span><span class="sxs-lookup"><span data-stu-id="fbbb0-110">Included Transaction classes</span></span>
- <span data-ttu-id="fbbb0-111">Limite máximo</span><span class="sxs-lookup"><span data-stu-id="fbbb0-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="fbbb0-112">Configuração dos encargos</span><span class="sxs-lookup"><span data-stu-id="fbbb0-112">Chargeability setup</span></span>
- <span data-ttu-id="fbbb0-113">Estimativa usando os detalhes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="fbbb0-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="fbbb0-114">Clientes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="fbbb0-114">Quote line Customers</span></span>

<span data-ttu-id="fbbb0-115">A tabela a seguir fornece informações sobre os campos na guia **Geral** da linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="fbbb0-116">Esses campos ajudam a estabelecer uma base para uma estimativa detalhada do trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="fbbb0-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="fbbb0-117">**Field**</span></span> | <span data-ttu-id="fbbb0-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbbb0-118">**Description**</span></span> | <span data-ttu-id="fbbb0-119">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="fbbb0-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fbbb0-120">Nome</span><span class="sxs-lookup"><span data-stu-id="fbbb0-120">Name</span></span> | <span data-ttu-id="fbbb0-121">O nome da linha de cotação que deve ajudar você a identificar o componente discreto da cotação que está sendo estimada.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="fbbb0-122">Copiado para a linha do contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-123">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="fbbb0-123">Billing Method</span></span> | <span data-ttu-id="fbbb0-124">Em uma cotação é criada a partir de uma oportunidade, este valor é copiado do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="fbbb0-125">Este campo inclui os dois modelos de contratação principais compatíveis com o Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="fbbb0-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="fbbb0-126">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="fbbb0-126">- Fixed price</span></span></br><span data-ttu-id="fbbb0-127">- Hora e material.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-127">- Time and material.</span></span>| <span data-ttu-id="fbbb0-128">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-129">Project</span><span class="sxs-lookup"><span data-stu-id="fbbb0-129">Project</span></span> | <span data-ttu-id="fbbb0-130">Use este campo opcional para identificar o projeto que será usado para entregar o trabalho nesta participação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="fbbb0-131">Quando um projeto é mapeado para uma linha de cotação, isso ajuda a configurar tarefas cobráveis e também a gerar uma estimativa baseada em projeto para a linha de cotação como detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="fbbb0-132">Quando um projeto não é mapeado para uma linha de cotação baseada em projeto, a estimativa deve ser criada manualmente criando cada detalhe da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="fbbb0-133">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="fbbb0-134">Tarefas Incluídas</span><span class="sxs-lookup"><span data-stu-id="fbbb0-134">Included Tasks</span></span> | <span data-ttu-id="fbbb0-135">Indica se esta linha de cotação é usada para todas ou algumas das tarefas do projeto para o projeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="fbbb0-136">Este campo possui os valores possíveis a seguir:</span><span class="sxs-lookup"><span data-stu-id="fbbb0-136">This field has the following possible values:</span></span></br><span data-ttu-id="fbbb0-137">- Todas as tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="fbbb0-137">- All project tasks</span></span></br><span data-ttu-id="fbbb0-138">- Somente tarefas do projeto selecionadas</span><span class="sxs-lookup"><span data-stu-id="fbbb0-138">- Selected project tasks only</span></span></br><span data-ttu-id="fbbb0-139">Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="fbbb0-140">Quando **Somente tarefas selecionadas do projeto** é selecionado, na página do projeto, a guia **Configuração de cobrança de tarefas** a guia permite que você selecione tarefas específicas para associá-las a esta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="fbbb0-141">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-142">Incluir Hora</span><span class="sxs-lookup"><span data-stu-id="fbbb0-142">Include Time</span></span> | <span data-ttu-id="fbbb0-143">Um sinalizador **Sim**/**Não** indica se as transações de tempo ou custo de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fbbb0-144">Um valor **Não** indica que as transações de tempo ou custo de mão de obra não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fbbb0-145">Um valor **Sim** indica que as transações de tempo ou custo de mão de obra serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fbbb0-146">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-147">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="fbbb0-147">Include Expense</span></span> | <span data-ttu-id="fbbb0-148">Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fbbb0-149">Um valor **Não** indica que as despesas de custo não serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fbbb0-150">Um valor **Sim** indica que as despesas de custo serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fbbb0-151">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-152">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="fbbb0-152">Include Fee</span></span> | <span data-ttu-id="fbbb0-153">Um sinalizador **Sim**/**Não** indica se os valores no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fbbb0-154">Um valor **Não** indica que os valores não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fbbb0-155">Um valor **Sim** indica que os valores serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fbbb0-156">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-157">Valor da Cotação</span><span class="sxs-lookup"><span data-stu-id="fbbb0-157">Quoted Amount</span></span> | <span data-ttu-id="fbbb0-158">Este é o valor que será cotado ao cliente para todo o trabalho previsto nesta linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="fbbb0-159">Em uma cotação criada a partir de uma oportunidade, este valor é copiado do campo **Orçamento do cliente** na linha da oportunidade.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="fbbb0-160">Quando a linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="fbbb0-161">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-162">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="fbbb0-162">Estimated Tax</span></span> | <span data-ttu-id="fbbb0-163">Este é um campo editável para o usuário adicionar o valor estimado do imposto na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="fbbb0-164">Quando uma linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor do imposto nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="fbbb0-165">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-166">Valor Cotado Após Imposto</span><span class="sxs-lookup"><span data-stu-id="fbbb0-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="fbbb0-167">Este campo é o valor da linha de cotação após o imposto e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="fbbb0-168">O valor neste campo é calculado como *Valor cotado + imposto*.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="fbbb0-169">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-170">Limite de NTE (limite máximo)</span><span class="sxs-lookup"><span data-stu-id="fbbb0-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="fbbb0-171">Este campo é editável e está disponível apenas em linhas de cotação baseadas em projeto que tenham o método de cobrança **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="fbbb0-172">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fbbb0-173">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="fbbb0-173">Customer Budget</span></span> | <span data-ttu-id="fbbb0-174">Se a cotação tiver sido criada a partir de uma Oportunidade, este campo é editável e copiado a partir do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="fbbb0-175">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="fbbb0-176">Regras de validação para os campos na guia Geral de linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="fbbb0-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="fbbb0-177">**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto será incluído na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="fbbb0-178">**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em uma única linha de cotação baseada em projeto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="fbbb0-179">**Regra 3**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Somente determinadas tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em várias linhas de cotação baseada em projeto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="fbbb0-180">**Regra 4** : se uma oportunidade tiver várias cotações, pode haver linhas de cotação de cotações diferentes que façam referência ao mesmo projeto e incluam a mesma classe de transação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="fbbb0-181">**Regra 5**: se as cotações não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transação.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="fbbb0-182">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="fbbb0-183">
                    <strong>Cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fbbb0-184">
                    <strong>Linha de cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fbbb0-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="fbbb0-186">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fbbb0-187">
                    <strong>Incluir Hora</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fbbb0-188">
                    <strong>Incluir Despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fbbb0-189">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="fbbb0-190">
                    <strong>Taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="fbbb0-191">
                    <strong>Válido/ Não inválido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="fbbb0-192">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fbbb0-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-193">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-194">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-195">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-196">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-197">Em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-198">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-199">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-200">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-201">Não é válido</span><span class="sxs-lookup"><span data-stu-id="fbbb0-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-202">Violação da regra nº2.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-202">Violation of Rule #2.</span></span> <span data-ttu-id="fbbb0-203">Tempo, despesa e valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-204">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-205">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-206">QL2</span><span class="sxs-lookup"><span data-stu-id="fbbb0-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-207">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-208">Em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-209">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-210">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-211">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="fbbb0-212">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-213">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-214">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-215">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-216">Em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-217">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-218">No</span><span class="sxs-lookup"><span data-stu-id="fbbb0-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-219">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-220">Não é válido</span><span class="sxs-lookup"><span data-stu-id="fbbb0-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-221">Violação da regra nº2.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-221">Violation of Rule #2.</span></span> <span data-ttu-id="fbbb0-222">Tempo e valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-223">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-224">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-225">QL2</span><span class="sxs-lookup"><span data-stu-id="fbbb0-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-226">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-227">Em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-228">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-229">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-230">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-231">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-232">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-233">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-234">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-235">Em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-236">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-237">No</span><span class="sxs-lookup"><span data-stu-id="fbbb0-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-238">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-239">Válido</span><span class="sxs-lookup"><span data-stu-id="fbbb0-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="fbbb0-240">Tempo e valores do projeto P1 estão incluídos no QL1.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="fbbb0-241">A despesa do projeto P1 está incluída no QL2.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="fbbb0-242">Não há sobreposição no que está sendo incluído em cada linha de cotação e é válido.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-243">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-244">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-245">QL2</span><span class="sxs-lookup"><span data-stu-id="fbbb0-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-246">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-247">Em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-248">No</span><span class="sxs-lookup"><span data-stu-id="fbbb0-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-249">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-250">No</span><span class="sxs-lookup"><span data-stu-id="fbbb0-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="fbbb0-251">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-252">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-253">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-254">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-255">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="fbbb0-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-256">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-257">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-258">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-259">Não é válido</span><span class="sxs-lookup"><span data-stu-id="fbbb0-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-260">Violação da regra nº2 acima</span><span class="sxs-lookup"><span data-stu-id="fbbb0-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="fbbb0-261">Q1 inclui Tempo, despesas e valores em um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fbbb0-262">QL2 inclui Tempo, despesas e valores para todo o projeto P1 e se sobrepõe ao que está incluído em Q1.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-263">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-264">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-265">QL2</span><span class="sxs-lookup"><span data-stu-id="fbbb0-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-266">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-267">Em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-268">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-269">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-270">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-271">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-272">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-273">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-274">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-275">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="fbbb0-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-276">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-277">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-278">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-279">Válido</span><span class="sxs-lookup"><span data-stu-id="fbbb0-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-280">De acordo com a regra nº 3 acima,</span><span class="sxs-lookup"><span data-stu-id="fbbb0-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="fbbb0-281">Q1 inclui Tempo, despesas e valores em um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fbbb0-282">QL2 inclui Tempo, despesas e valores de um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fbbb0-283">A única validação adicional é em torno do subconjunto de tarefas em QL1, que é diferente do subconjunto de tarefas em QL2.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="fbbb0-284">Isso garante que não haja sobreposições.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="fbbb0-285">Isso é feito pelo sistema quando as tarefas são associadas.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-286">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-287">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-288">QL2</span><span class="sxs-lookup"><span data-stu-id="fbbb0-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-289">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-290">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="fbbb0-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-291">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-292">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-293">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="fbbb0-294">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-295">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-296">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-297">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-298">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-299">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-300">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-301">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fbbb0-302">Válido</span><span class="sxs-lookup"><span data-stu-id="fbbb0-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-303">Com base na regra nº5, Q1 e Q2 são duas cotações na mesma oportunidade, então ambas podem estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-304">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-305">T2</span><span class="sxs-lookup"><span data-stu-id="fbbb0-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-306">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-307">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-308">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-309">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-310">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-311">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="fbbb0-312">O1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-313">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-314">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-315">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-316">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-317">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-318">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-319">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fbbb0-320">Válido</span><span class="sxs-lookup"><span data-stu-id="fbbb0-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fbbb0-321">Com base na regra nº4, Q1 e Q2 são duas cotações em oportunidades diferentes, então não podem estimar para os mesmos componentes do mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="fbbb0-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fbbb0-322">O2</span><span class="sxs-lookup"><span data-stu-id="fbbb0-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fbbb0-323">T1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-324">QL1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-325">P1</span><span class="sxs-lookup"><span data-stu-id="fbbb0-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fbbb0-326">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="fbbb0-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-327">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fbbb0-328">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fbbb0-329">Sim</span><span class="sxs-lookup"><span data-stu-id="fbbb0-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fbbb0-330">Não é válido</span><span class="sxs-lookup"><span data-stu-id="fbbb0-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

