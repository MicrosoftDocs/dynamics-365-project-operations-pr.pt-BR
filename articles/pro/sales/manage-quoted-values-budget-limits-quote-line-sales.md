---
title: Linhas de cotação baseadas em projeto (Pro)
description: Este tópico fornece informações sobre como usar linhas de cotação baseadas no projeto para o trabalho do projeto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907859"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="cc90b-104">Linhas de cotação baseadas em projeto (Pro)</span><span class="sxs-lookup"><span data-stu-id="cc90b-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="cc90b-105">_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="cc90b-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc90b-106">As linhas de cotação baseadas em projeto são projetadas para ajudar a estimar o trabalho do projeto em uma participação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="cc90b-107">A estrutura de uma linha de cotação baseada em projeto é estendida para estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="cc90b-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="cc90b-108">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="cc90b-108">Billing Method</span></span>
- <span data-ttu-id="cc90b-109">Mapeamento de projeto e tarefa</span><span class="sxs-lookup"><span data-stu-id="cc90b-109">Project and Task Mapping</span></span>
- <span data-ttu-id="cc90b-110">Classes de transação incluídas</span><span class="sxs-lookup"><span data-stu-id="cc90b-110">Included Transaction classes</span></span>
- <span data-ttu-id="cc90b-111">Limite máximo</span><span class="sxs-lookup"><span data-stu-id="cc90b-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="cc90b-112">Configuração dos encargos</span><span class="sxs-lookup"><span data-stu-id="cc90b-112">Chargeability setup</span></span>
- <span data-ttu-id="cc90b-113">Estimativa usando os detalhes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="cc90b-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="cc90b-114">Clientes da linha de cotação</span><span class="sxs-lookup"><span data-stu-id="cc90b-114">Quote line Customers</span></span>

<span data-ttu-id="cc90b-115">A tabela a seguir fornece informações sobre os campos na guia **Geral** da linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="cc90b-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="cc90b-116">Esses campos ajudam a estabelecer uma base para uma estimativa detalhada do trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="cc90b-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="cc90b-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="cc90b-117">**Field**</span></span> | <span data-ttu-id="cc90b-118">**Relevância, finalidade e orientação**</span><span class="sxs-lookup"><span data-stu-id="cc90b-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="cc90b-119">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="cc90b-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cc90b-120">Nome</span><span class="sxs-lookup"><span data-stu-id="cc90b-120">Name</span></span> | <span data-ttu-id="cc90b-121">O nome da linha de cotação que deve ajudar você a identificar o componente discreto da cotação que está sendo estimada.</span><span class="sxs-lookup"><span data-stu-id="cc90b-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="cc90b-122">Copiado para a linha do contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-123">Método de Cobrança</span><span class="sxs-lookup"><span data-stu-id="cc90b-123">Billing Method</span></span> | <span data-ttu-id="cc90b-124">Em uma cotação é criada a partir de uma oportunidade, este valor é copiado do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="cc90b-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="cc90b-125">Este campo inclui os dois modelos de contratação principais compatíveis com o Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="cc90b-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="cc90b-126">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="cc90b-126">- Fixed price</span></span></br><span data-ttu-id="cc90b-127">- Hora e material.</span><span class="sxs-lookup"><span data-stu-id="cc90b-127">- Time and material.</span></span>| <span data-ttu-id="cc90b-128">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-129">Project</span><span class="sxs-lookup"><span data-stu-id="cc90b-129">Project</span></span> | <span data-ttu-id="cc90b-130">Use este campo opcional para identificar o projeto que será usado para entregar o trabalho nesta participação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="cc90b-131">Quando um projeto é mapeado para uma linha de cotação, isso ajuda a configurar tarefas cobráveis e também a gerar uma estimativa baseada em projeto para a linha de cotação como detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="cc90b-132">Quando um projeto não é mapeado para uma linha de cotação baseada em projeto, a estimativa deve ser criada manualmente criando cada detalhe da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="cc90b-133">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="cc90b-134">Tarefas Incluídas</span><span class="sxs-lookup"><span data-stu-id="cc90b-134">Included Tasks</span></span> | <span data-ttu-id="cc90b-135">Indica se esta linha de cotação é usada para todas ou algumas das tarefas do projeto para o projeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="cc90b-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="cc90b-136">Este campo possui os valores possíveis a seguir:</span><span class="sxs-lookup"><span data-stu-id="cc90b-136">This field has the following possible values:</span></span></br><span data-ttu-id="cc90b-137">- Todas as tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="cc90b-137">- All project tasks</span></span></br><span data-ttu-id="cc90b-138">- Somente tarefas do projeto selecionadas</span><span class="sxs-lookup"><span data-stu-id="cc90b-138">- Selected project tasks only</span></span></br><span data-ttu-id="cc90b-139">Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**.</span><span class="sxs-lookup"><span data-stu-id="cc90b-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="cc90b-140">Quando **Somente tarefas selecionadas do projeto** é selecionado, na página do projeto, a guia **Configuração de cobrança de tarefas** a guia permite que você selecione tarefas específicas para associá-las a esta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="cc90b-141">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-142">Incluir Hora</span><span class="sxs-lookup"><span data-stu-id="cc90b-142">Include Time</span></span> | <span data-ttu-id="cc90b-143">Um sinalizador **Sim**/**Não** indica se as transações de tempo ou custo de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="cc90b-144">Um valor **Não** indica que as transações de tempo ou custo de mão de obra não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="cc90b-145">Um valor **Sim** indica que as transações de tempo ou custo de mão de obra serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="cc90b-146">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-147">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="cc90b-147">Include Expense</span></span> | <span data-ttu-id="cc90b-148">Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="cc90b-149">Um valor **Não** indica que as despesas de custo não serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="cc90b-150">Um valor **Sim** indica que as despesas de custo serão incluídas na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="cc90b-151">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-152">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="cc90b-152">Include Fee</span></span> | <span data-ttu-id="cc90b-153">Um sinalizador **Sim**/**Não** indica se os valores no projeto selecionado serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="cc90b-154">Um valor **Não** indica que os valores não serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="cc90b-155">Um valor **Sim** indica que os valores serão incluídos na estimativa nesta linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="cc90b-156">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-157">Valor da Cotação</span><span class="sxs-lookup"><span data-stu-id="cc90b-157">Quoted Amount</span></span> | <span data-ttu-id="cc90b-158">Este é o valor que será cotado ao cliente para todo o trabalho previsto nesta linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="cc90b-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="cc90b-159">Em uma cotação criada a partir de uma oportunidade, este valor é copiado do campo **Orçamento do cliente** na linha da oportunidade.</span><span class="sxs-lookup"><span data-stu-id="cc90b-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="cc90b-160">Quando a linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="cc90b-161">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-162">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="cc90b-162">Estimated Tax</span></span> | <span data-ttu-id="cc90b-163">Este é um campo editável para o usuário adicionar o valor estimado do imposto na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="cc90b-164">Quando uma linha de cotação baseada em projeto tiver detalhes de linha, este campo será bloqueado para edição resumido com base no valor do imposto nos detalhes da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="cc90b-165">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-166">Valor Cotado Após Imposto</span><span class="sxs-lookup"><span data-stu-id="cc90b-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="cc90b-167">Este campo é o valor da linha de cotação após o imposto e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cc90b-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="cc90b-168">O valor neste campo é calculado como *Valor cotado + imposto*.</span><span class="sxs-lookup"><span data-stu-id="cc90b-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="cc90b-169">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-170">Limite de NTE (limite máximo)</span><span class="sxs-lookup"><span data-stu-id="cc90b-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="cc90b-171">Este campo é editável e está disponível apenas em linhas de cotação baseadas em projeto que tenham o método de cobrança **Tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="cc90b-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="cc90b-172">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cc90b-173">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="cc90b-173">Customer Budget</span></span> | <span data-ttu-id="cc90b-174">Se a cotação tiver sido criada a partir de uma Oportunidade, este campo é editável e copiado a partir do campo correspondente na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="cc90b-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="cc90b-175">O valor deste campo é copiado para a linha de contrato do projeto que é criada a partir desta linha de cotação quando uma cotação é vencida.</span><span class="sxs-lookup"><span data-stu-id="cc90b-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="cc90b-176">Regras de validação para os campos na guia Geral de linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="cc90b-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="cc90b-177">**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto será incluído na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="cc90b-178">**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em uma única linha de cotação baseada em projeto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="cc90b-179">**Regra 3**: se o campo **Tarefas Incluídas** estiver em branco ou se definido como **Somente determinadas tarefas do projeto**, um projeto e uma determinada classe de transação só poderão ser incluídos em várias linhas de cotação baseada em projeto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="cc90b-180">**Regra 4** : se uma oportunidade tiver várias cotações, pode haver linhas de cotação de cotações diferentes que façam referência ao mesmo projeto e incluam a mesma classe de transação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="cc90b-181">**Regra 5**: se as cotações não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transação.</span><span class="sxs-lookup"><span data-stu-id="cc90b-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="cc90b-182">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="cc90b-183">
                    <strong>Cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="cc90b-184">
                    <strong>Linha de cotação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="cc90b-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="cc90b-186">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="cc90b-187">
                    <strong>Incluir Hora</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="cc90b-188">
                    <strong>Incluir Despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="cc90b-189">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="cc90b-190">
                    <strong>Taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="cc90b-191">
                    <strong>Válido/ Não inválido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="cc90b-192">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cc90b-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cc90b-193">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-194">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-195">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-196">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-197">Em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-198">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-199">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-200">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-201">Não é válido</span><span class="sxs-lookup"><span data-stu-id="cc90b-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-202">Violação da regra nº2.</span><span class="sxs-lookup"><span data-stu-id="cc90b-202">Violation of Rule #2.</span></span> <span data-ttu-id="cc90b-203">Tempo, despesa e valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="cc90b-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cc90b-204">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-205">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-206">QL2</span><span class="sxs-lookup"><span data-stu-id="cc90b-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-207">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-208">Em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-209">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-210">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-211">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-211">Yes</span></span> </p>
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
<span data-ttu-id="cc90b-212">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-213">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-214">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-215">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-216">Em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-217">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-218">No</span><span class="sxs-lookup"><span data-stu-id="cc90b-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-219">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-220">Não é válido</span><span class="sxs-lookup"><span data-stu-id="cc90b-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-221">Violação da regra nº2.</span><span class="sxs-lookup"><span data-stu-id="cc90b-221">Violation of Rule #2.</span></span> <span data-ttu-id="cc90b-222">Tempo e valores no projeto P1 estão incluídos nas linhas de cotação QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="cc90b-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cc90b-223">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-224">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-225">QL2</span><span class="sxs-lookup"><span data-stu-id="cc90b-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-226">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-227">Em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-228">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-229">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-230">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-230">Yes</span></span> </p>
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
<span data-ttu-id="cc90b-231">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-232">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-233">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-234">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-235">Em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-236">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-237">No</span><span class="sxs-lookup"><span data-stu-id="cc90b-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-238">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-239">Válido</span><span class="sxs-lookup"><span data-stu-id="cc90b-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="cc90b-240">Tempo e valores do projeto P1 estão incluídos no QL1.</span><span class="sxs-lookup"><span data-stu-id="cc90b-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="cc90b-241">A despesa do projeto P1 está incluída no QL2.</span><span class="sxs-lookup"><span data-stu-id="cc90b-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="cc90b-242">Não há sobreposição no que está sendo incluído em cada linha de cotação e é válido.</span><span class="sxs-lookup"><span data-stu-id="cc90b-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cc90b-243">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-244">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-245">QL2</span><span class="sxs-lookup"><span data-stu-id="cc90b-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-246">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-247">Em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-248">No</span><span class="sxs-lookup"><span data-stu-id="cc90b-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-249">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-250">No</span><span class="sxs-lookup"><span data-stu-id="cc90b-250">No</span></span> </p>
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
<span data-ttu-id="cc90b-251">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-252">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-253">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-254">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-255">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="cc90b-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-256">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-257">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-258">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-259">Não é válido</span><span class="sxs-lookup"><span data-stu-id="cc90b-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-260">Violação da regra nº2 acima</span><span class="sxs-lookup"><span data-stu-id="cc90b-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="cc90b-261">Q1 inclui Tempo, despesas e valores em um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="cc90b-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="cc90b-262">QL2 inclui Tempo, despesas e valores para todo o projeto P1 e se sobrepõe ao que está incluído em Q1.</span><span class="sxs-lookup"><span data-stu-id="cc90b-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cc90b-263">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-264">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-265">QL2</span><span class="sxs-lookup"><span data-stu-id="cc90b-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-266">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-267">Em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-268">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-269">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-270">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-270">Yes</span></span> </p>
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
<span data-ttu-id="cc90b-271">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-272">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-273">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-274">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-275">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="cc90b-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-276">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-277">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-278">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-279">Válido</span><span class="sxs-lookup"><span data-stu-id="cc90b-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-280">De acordo com a regra nº 3 acima,</span><span class="sxs-lookup"><span data-stu-id="cc90b-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="cc90b-281">Q1 inclui Tempo, despesas e valores em um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="cc90b-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="cc90b-282">QL2 inclui Tempo, despesas e valores de um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="cc90b-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="cc90b-283">A única validação adicional é em torno do subconjunto de tarefas em QL1, que é diferente do subconjunto de tarefas em QL2.</span><span class="sxs-lookup"><span data-stu-id="cc90b-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="cc90b-284">Isso garante que não haja sobreposições.</span><span class="sxs-lookup"><span data-stu-id="cc90b-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="cc90b-285">Isso é feito pelo sistema quando as tarefas são associadas.</span><span class="sxs-lookup"><span data-stu-id="cc90b-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cc90b-286">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-287">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-288">QL2</span><span class="sxs-lookup"><span data-stu-id="cc90b-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-289">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-290">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="cc90b-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-291">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-292">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-293">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-293">Yes</span></span> </p>
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
<span data-ttu-id="cc90b-294">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-295">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-296">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-297">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-298">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-299">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-300">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-301">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="cc90b-302">Válido</span><span class="sxs-lookup"><span data-stu-id="cc90b-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-303">Com base na regra nº5, Q1 e Q2 são duas cotações na mesma oportunidade, então ambas podem estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="cc90b-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cc90b-304">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-305">T2</span><span class="sxs-lookup"><span data-stu-id="cc90b-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-306">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-307">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-308">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-309">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-310">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-311">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-311">Yes</span></span> </p>
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
<span data-ttu-id="cc90b-312">O1</span><span class="sxs-lookup"><span data-stu-id="cc90b-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-313">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-314">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-315">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-316">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-317">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-318">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-319">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="cc90b-320">Válido</span><span class="sxs-lookup"><span data-stu-id="cc90b-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cc90b-321">Com base na regra nº4, Q1 e Q2 são duas cotações em oportunidades diferentes, então não podem estimar para os mesmos componentes do mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="cc90b-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cc90b-322">O2</span><span class="sxs-lookup"><span data-stu-id="cc90b-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cc90b-323">T1</span><span class="sxs-lookup"><span data-stu-id="cc90b-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-324">QL1</span><span class="sxs-lookup"><span data-stu-id="cc90b-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-325">P1</span><span class="sxs-lookup"><span data-stu-id="cc90b-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cc90b-326">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="cc90b-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-327">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cc90b-328">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cc90b-329">Sim</span><span class="sxs-lookup"><span data-stu-id="cc90b-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="cc90b-330">Não é válido</span><span class="sxs-lookup"><span data-stu-id="cc90b-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

