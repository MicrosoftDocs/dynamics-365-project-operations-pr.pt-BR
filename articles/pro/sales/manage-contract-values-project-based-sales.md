---
title: Visão geral de linhas de contrato baseadas em projeto
description: Este tópico fornece informações sobre como trabalhar com linhas de contrato baseadas em projeto.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858144"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="942a3-103">Visão geral de linhas de contrato baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="942a3-103">Project-based contract lines overview</span></span>

<span data-ttu-id="942a3-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="942a3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="942a3-105">Linhas de contrato baseadas em projeto no Dynamics 365 Project Operations são projetadas para conter a estimativa e os contratos de cobrança para componentes específicos do trabalho do projeto em uma participação.</span><span class="sxs-lookup"><span data-stu-id="942a3-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="942a3-106">A estrutura de uma linha de contrato baseada em projeto é estendida para estimativas de projeto e cenários de cobrança com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="942a3-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="942a3-107">Método de cobrança</span><span class="sxs-lookup"><span data-stu-id="942a3-107">Billing method</span></span>
- <span data-ttu-id="942a3-108">Mapeamento de projeto e tarefa</span><span class="sxs-lookup"><span data-stu-id="942a3-108">Project and task mapping</span></span>
- <span data-ttu-id="942a3-109">Classes de transação incluídas</span><span class="sxs-lookup"><span data-stu-id="942a3-109">Included transaction classes</span></span>
- <span data-ttu-id="942a3-110">Limite máximo</span><span class="sxs-lookup"><span data-stu-id="942a3-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="942a3-111">Configuração dos encargos</span><span class="sxs-lookup"><span data-stu-id="942a3-111">Chargeability setup</span></span>
- <span data-ttu-id="942a3-112">Estimativas usando detalhes da linha de contrato</span><span class="sxs-lookup"><span data-stu-id="942a3-112">Estimates using contract line details</span></span>
- <span data-ttu-id="942a3-113">Clientes da linha de contrato</span><span class="sxs-lookup"><span data-stu-id="942a3-113">Contract line customers</span></span>

<span data-ttu-id="942a3-114">A tabela a seguir inclui os campos na guia **Geral** de linhas de contrato baseadas em projeto que ajudam a configurar a base para uma estimativa detalhada básica e disposições de cobrança para o trabalho baseado em projeto.</span><span class="sxs-lookup"><span data-stu-id="942a3-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="942a3-115">Campo</span><span class="sxs-lookup"><span data-stu-id="942a3-115">Field</span></span> | <span data-ttu-id="942a3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="942a3-116">Description</span></span> | <span data-ttu-id="942a3-117">Impacto a jusante</span><span class="sxs-lookup"><span data-stu-id="942a3-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="942a3-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="942a3-118">**Name**</span></span> | <span data-ttu-id="942a3-119">Nome da linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-119">Name of the contract line.</span></span> <span data-ttu-id="942a3-120">Isso identifica o componente discreto do contrato que está sendo estimado.</span><span class="sxs-lookup"><span data-stu-id="942a3-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="942a3-121">Para um contrato de projeto criado a partir de uma cotação, este valor é copiado de um valor correspondente da linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="942a3-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="942a3-122">O nome copiado na linha da fatura do projeto que é criada a partir dessa linha do contrato quando a fatura é criada.</span><span class="sxs-lookup"><span data-stu-id="942a3-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="942a3-123">**Método de Cobrança**</span><span class="sxs-lookup"><span data-stu-id="942a3-123">**Billing Method**</span></span> | <span data-ttu-id="942a3-124">Em um contrato de projeto criado a partir de uma cotação, este valor é copiado do campo correspondente na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="942a3-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="942a3-125">Este é um conjunto de opções que representa os dois principais modelos de contratação com suporte do Project Operations:</span><span class="sxs-lookup"><span data-stu-id="942a3-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="942a3-126">- **Preço Fixo**</span><span class="sxs-lookup"><span data-stu-id="942a3-126">- **Fixed Price**</span></span></br><span data-ttu-id="942a3-127">- **Hora e Material**</span><span class="sxs-lookup"><span data-stu-id="942a3-127">- **Time and Material**</span></span> | <span data-ttu-id="942a3-128">Com base no método de cobrança da linha de contrato referenciada, a transação real será processada.</span><span class="sxs-lookup"><span data-stu-id="942a3-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="942a3-129">Se a linha do contrato referenciada pelo dado real tiver um método de cobrança por hora e material, serão criados registros de custos e dado real de vendas não cobradas.</span><span class="sxs-lookup"><span data-stu-id="942a3-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="942a3-130">Se a linha do contrato referenciada pelo real tiver um método de cobrança de preço fixo, apenas um dado real de custo será criado.</span><span class="sxs-lookup"><span data-stu-id="942a3-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="942a3-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="942a3-131">**Project**</span></span> | <span data-ttu-id="942a3-132">Use este campo para identificar o projeto que será usado para entregar o trabalho nesta participação.</span><span class="sxs-lookup"><span data-stu-id="942a3-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="942a3-133">Este valor será usado junto com **Tarefas Incluídas** e **Classes de Transação Incluídas** para resolver a referência da linha do contrato em um registro de linha real ou estimado.</span><span class="sxs-lookup"><span data-stu-id="942a3-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="942a3-134">**Tarefas Incluídas**</span><span class="sxs-lookup"><span data-stu-id="942a3-134">**Included Tasks**</span></span> | <span data-ttu-id="942a3-135">Indica se esta linha de contrato inclui todas as tarefas do projeto para o projeto selecionado ou apenas um subconjunto das tarefas.</span><span class="sxs-lookup"><span data-stu-id="942a3-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="942a3-136">Este é um conjunto de opções que tem os seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="942a3-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="942a3-137">- **Todas as Tarefas do Projeto**</span><span class="sxs-lookup"><span data-stu-id="942a3-137">- **All Project Tasks**</span></span></br><span data-ttu-id="942a3-138">- **Tarefas do Projeto Selecionadas Somente**.</span><span class="sxs-lookup"><span data-stu-id="942a3-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="942a3-139">Um valor em branco neste campo equivale a selecionar **Todas as Tarefas do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="942a3-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="942a3-140">Se **Tarefas Selecionadas Somente** for selecionado, você poderá selecionar tarefas específicas e associá-las a esta linha de contrato na guia **Configuração de Cobrança da Tarefa** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="942a3-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="942a3-141">O valor será usado em conjunto com as classes **Projeto** e **Transação Incluída** para resolver a referência da linha do contrato em um dado real ou em um registro de linha de estimativa.</span><span class="sxs-lookup"><span data-stu-id="942a3-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="942a3-142">**Incluir Hora**</span><span class="sxs-lookup"><span data-stu-id="942a3-142">**Include Time**</span></span> | <span data-ttu-id="942a3-143">Um valor **Sim**/**Não** indica se as transações de tempo ou custos de mão de obra no projeto selecionado serão incluídas nesta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="942a3-144">Um valor **Não** indica que as transações de hora ou custo de mão de obra não serão incluídas nesta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="942a3-145">Um valor **Sim** indica que serão incluídas.</span><span class="sxs-lookup"><span data-stu-id="942a3-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="942a3-146">Este valor é usado junto com o projeto para resolver a referência da linha do contrato em um registro real ou de linha de estimativa.</span><span class="sxs-lookup"><span data-stu-id="942a3-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="942a3-147">**Incluir Despesa**</span><span class="sxs-lookup"><span data-stu-id="942a3-147">**Include Expense**</span></span> | <span data-ttu-id="942a3-148">Um valor **Sim**/**Não** indica se custos de despesa no projeto selecionado serão incluídos nesta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="942a3-149">Um valor **Não** indica que o custo de despesas não será incluído nesta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="942a3-150">Um valor **Sim** indica que ele será incluído.</span><span class="sxs-lookup"><span data-stu-id="942a3-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="942a3-151">Este valor é usado junto com o projeto para resolver a referência da linha do contrato em um registro real ou de linha de estimativa.</span><span class="sxs-lookup"><span data-stu-id="942a3-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="942a3-152">**Incluir Materiais**</span><span class="sxs-lookup"><span data-stu-id="942a3-152">**Include Materials**</span></span> | <span data-ttu-id="942a3-153">Um valor **Sim**/**Não** indica se custos de material no projeto selecionado serão incluídos nesta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="942a3-154">Um valor **Não** indica se os custos de material não serão incluídos nesta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="942a3-155">Um valor **Sim** indica que ele será incluído.</span><span class="sxs-lookup"><span data-stu-id="942a3-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="942a3-156">Este valor é usado junto com o projeto para resolver a referência da linha do contrato em um registro real ou de linha de estimativa.</span><span class="sxs-lookup"><span data-stu-id="942a3-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="942a3-157">**Incluir Taxa**</span><span class="sxs-lookup"><span data-stu-id="942a3-157">**Include Fee**</span></span> | <span data-ttu-id="942a3-158">Um valor **Sim**/**Não** indica se valores no projeto selecionado serão incluídos nesta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="942a3-159">Um valor **Não** indica que os valores não serão incluídos nesta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="942a3-160">Um valor **Sim** indica que serão incluídas.</span><span class="sxs-lookup"><span data-stu-id="942a3-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="942a3-161">Este valor é usado junto com o projeto para resolver a referência da linha do contrato em um registro real ou de linha de estimativa.</span><span class="sxs-lookup"><span data-stu-id="942a3-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="942a3-162">**Valor Contratado**</span><span class="sxs-lookup"><span data-stu-id="942a3-162">**Contracted Amount**</span></span> | <span data-ttu-id="942a3-163">Em uma linha de contrato de preço fixo, este é o valor acordado que será faturado ao cliente para todos os componentes de trabalho associados a esta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="942a3-164">Em uma linha de contrato de horas e materiais, este é um valor estimado do que será faturado ao cliente para todos os componentes de trabalho associados a esta linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="942a3-165">Em um contrato de projeto que é criado a partir de uma cotação, este valor é copiado do campo correspondente na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="942a3-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="942a3-166">Quando uma linha de contrato baseada em projeto tem detalhes de linha, este campo é bloqueado para edição e é resumido a partir do valor nos detalhes da linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="942a3-167">Quando a linha do contrato tem detalhes da linha, este valor pode ser modificado alterando os valores nos detalhes da linha.</span><span class="sxs-lookup"><span data-stu-id="942a3-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="942a3-168">Em uma linha de contrato de preço fixo, esse valor é usado para gerar o valor antes do imposto em etapas de cobrança periódica.</span><span class="sxs-lookup"><span data-stu-id="942a3-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="942a3-169">**Imposto Estimado**</span><span class="sxs-lookup"><span data-stu-id="942a3-169">**Estimated Tax**</span></span> | <span data-ttu-id="942a3-170">O usuário pode editar este campo para inserir o valor estimado do imposto na linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="942a3-171">Quando uma linha de contrato baseada em projeto tem detalhes de linha, este campo é bloqueado para edição e é resumido a partir do valor do imposto nos detalhes da linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="942a3-172">Quando a linha do contrato tem detalhes da linha, este valor pode ser modificado alterando os valores do imposto nos detalhes da linha.</span><span class="sxs-lookup"><span data-stu-id="942a3-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="942a3-173">Em uma linha de contrato de preço fixo, esse valor é usado para gerar os impostos sobre etapas de cobrança periódica.</span><span class="sxs-lookup"><span data-stu-id="942a3-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="942a3-174">**Valor Contratado após Imposto**</span><span class="sxs-lookup"><span data-stu-id="942a3-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="942a3-175">O valor da linha do contrato após Imposto.</span><span class="sxs-lookup"><span data-stu-id="942a3-175">The contract line amount after tax.</span></span> <span data-ttu-id="942a3-176">Este campo é somente leitura e é calculado como **Valor Contratado + Imposto**.</span><span class="sxs-lookup"><span data-stu-id="942a3-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="942a3-177">Em uma linha de contrato de preço fixo, esse valor é usado para gerar etapas de cobrança periódica.</span><span class="sxs-lookup"><span data-stu-id="942a3-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="942a3-178">**Limite de NTE (limite máximo)**</span><span class="sxs-lookup"><span data-stu-id="942a3-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="942a3-179">O usuário pode editar este campo e ele está disponível apenas em linhas de contrato baseadas em projeto que têm um método de cobrança definido como horas e materiais.</span><span class="sxs-lookup"><span data-stu-id="942a3-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="942a3-180">O usuário pode editar este campo.</span><span class="sxs-lookup"><span data-stu-id="942a3-180">The user can edit this field.</span></span> <span data-ttu-id="942a3-181">Quando um dado real de horas e materiais referencia esta linha do contrato para horas e materiais, o valor no dado real é avaliado em relação ao limite máximo na linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="942a3-182">Essa avaliação é concluída após a contabilização dos valores já gastos e comprometidos.</span><span class="sxs-lookup"><span data-stu-id="942a3-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="942a3-183">**Orçamento do Cliente**</span><span class="sxs-lookup"><span data-stu-id="942a3-183">**Customer Budget**</span></span> | <span data-ttu-id="942a3-184">Este campo é editável e será copiado do campo correspondente na linha de cotação se o contrato tiver sido criado a partir de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="942a3-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="942a3-185">Este campo é usado apenas para informações e não tem significado posterior.</span><span class="sxs-lookup"><span data-stu-id="942a3-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="942a3-186">Regras de validação para as opções na guia Geral de linhas de contrato baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="942a3-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="942a3-187">Regra 1: se o campo **Tarefas Incluídas** estiver em branco ou definido como **Todas as Tarefas do Projeto**, todas as tarefas do projeto serão incluídas na linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="942a3-188">Regra 2: quando o campo **Tarefas Incluídas** estiver em branco ou explicitamente definido como **Todas as Tarefas do Projeto**, um projeto e uma certa classe de transação só poderão ser incluídos em uma linha de contrato baseada em projeto de um contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="942a3-189">Regra 3: quando o campo **Tarefas Incluídas** estiver definido como **Tarefas do Projeto Selecionadas Somente**, um projeto e uma certa classe de transação poderão ser incluídos em várias linhas de contrato baseadas em projeto de um contrato.</span><span class="sxs-lookup"><span data-stu-id="942a3-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="942a3-190">
                    <strong>Contrato</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="942a3-191">
                    <strong>Linha de contrato</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="942a3-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="942a3-193">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="942a3-194">
                    <strong>Incluir Hora</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="942a3-195">
                    <strong>Incluir Despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="942a3-196">
                    <strong>Incluir Materiais</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="942a3-197">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="942a3-198">
                    <strong>Taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="942a3-199">
                    <strong>Válido/ Não inválido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="942a3-200">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="942a3-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-201">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-202">CL1</span><span class="sxs-lookup"><span data-stu-id="942a3-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-203">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-204">Em branco</span><span class="sxs-lookup"><span data-stu-id="942a3-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-205">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-206">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-207">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-208">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-209">Não é válido</span><span class="sxs-lookup"><span data-stu-id="942a3-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-210">Violação da regra Nº 2.</span><span class="sxs-lookup"><span data-stu-id="942a3-210">Violation of Rule #2.</span></span> <span data-ttu-id="942a3-211">Tempo, Despesas, Materiais e Valores no projeto P1 estão incluídos nas linhas de contrato CL1 e CL2.</span><span class="sxs-lookup"><span data-stu-id="942a3-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-212">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-213">CL2</span><span class="sxs-lookup"><span data-stu-id="942a3-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-214">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-215">Em branco</span><span class="sxs-lookup"><span data-stu-id="942a3-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-216">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-217">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-218">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-219">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-220">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-221">CL1</span><span class="sxs-lookup"><span data-stu-id="942a3-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-222">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-223">Em branco</span><span class="sxs-lookup"><span data-stu-id="942a3-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-224">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-225">No</span><span class="sxs-lookup"><span data-stu-id="942a3-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-226">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-227">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-228">Não é válido</span><span class="sxs-lookup"><span data-stu-id="942a3-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-229">Violação da regra Nº 2.</span><span class="sxs-lookup"><span data-stu-id="942a3-229">Violation of Rule #2.</span></span> <span data-ttu-id="942a3-230">Tempo, Materiais e Valores no projeto P1 estão incluídos nas linhas de contrato CL1 e CL2.</span><span class="sxs-lookup"><span data-stu-id="942a3-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-231">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-232">CL2</span><span class="sxs-lookup"><span data-stu-id="942a3-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-233">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-234">Em branco</span><span class="sxs-lookup"><span data-stu-id="942a3-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-235">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-236">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-237">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-238">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-239">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-240">CL1</span><span class="sxs-lookup"><span data-stu-id="942a3-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-241">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-242">Em branco</span><span class="sxs-lookup"><span data-stu-id="942a3-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-243">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-244">No</span><span class="sxs-lookup"><span data-stu-id="942a3-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-245">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-246">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-247">Válido</span><span class="sxs-lookup"><span data-stu-id="942a3-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-248">Tempo, Materiais e Valores no projeto P1 estão incluídos no CL1.</span><span class="sxs-lookup"><span data-stu-id="942a3-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="942a3-249">A despesa do projeto P1 está incluída no CL2.</span><span class="sxs-lookup"><span data-stu-id="942a3-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="942a3-250">Nenhuma sobreposição no que está sendo incluído em cada linha do contrato e, portanto, ele é válido.</span><span class="sxs-lookup"><span data-stu-id="942a3-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-251">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-252">CL2</span><span class="sxs-lookup"><span data-stu-id="942a3-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-253">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-254">Em branco</span><span class="sxs-lookup"><span data-stu-id="942a3-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-255">No</span><span class="sxs-lookup"><span data-stu-id="942a3-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-256">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-257">No</span><span class="sxs-lookup"><span data-stu-id="942a3-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-258">No</span><span class="sxs-lookup"><span data-stu-id="942a3-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-259">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-260">CL1</span><span class="sxs-lookup"><span data-stu-id="942a3-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-261">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-262">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="942a3-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-263">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-264">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-265">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-266">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-267">Não é válido</span><span class="sxs-lookup"><span data-stu-id="942a3-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-268">Violação da regra Nº 2</span><span class="sxs-lookup"><span data-stu-id="942a3-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="942a3-269">C1 inclui Tempo, Materiais, Despesas e Valores em um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="942a3-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="942a3-270">CL2 inclui Tempo, Materiais, Despesas e Valores para todo o projeto P1 e, portanto, se sobrepõe ao que está incluído em C1.</span><span class="sxs-lookup"><span data-stu-id="942a3-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-271">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-272">CL2</span><span class="sxs-lookup"><span data-stu-id="942a3-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-273">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-274">Em branco</span><span class="sxs-lookup"><span data-stu-id="942a3-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-275">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-276">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-277">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-278">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-279">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-280">CL1</span><span class="sxs-lookup"><span data-stu-id="942a3-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-281">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-282">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="942a3-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-283">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-284">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-285">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-286">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-287">Válido</span><span class="sxs-lookup"><span data-stu-id="942a3-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="942a3-288">Por regra nº 3</span><span class="sxs-lookup"><span data-stu-id="942a3-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="942a3-289">C1 inclui Tempo, Despesas, Materiais e Valores em um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="942a3-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="942a3-290">CL2 inclui Tempo, Despesas, Materiais e Valores para um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="942a3-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="942a3-291">A única validação adicional é que o subconjunto de tarefas no CL1 é diferente do subconjunto de tarefas no CL2 para garantir que não haja sobreposições.</span><span class="sxs-lookup"><span data-stu-id="942a3-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="942a3-292">Isso é feito pelo sistema quando as tarefas são associadas.</span><span class="sxs-lookup"><span data-stu-id="942a3-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="942a3-293">C1</span><span class="sxs-lookup"><span data-stu-id="942a3-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="942a3-294">CL2</span><span class="sxs-lookup"><span data-stu-id="942a3-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-295">P1</span><span class="sxs-lookup"><span data-stu-id="942a3-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="942a3-296">Somente tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="942a3-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-297">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="942a3-298">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-299">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="942a3-300">Sim</span><span class="sxs-lookup"><span data-stu-id="942a3-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
