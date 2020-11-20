---
title: Criar agendas de faturas em uma linha de contrato baseada em projeto
description: Este tópico fornece informações sobre a criação de agendas de faturas e etapas em linhas de contrato.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2183b915dd2f67e03964246cb0689003e48363f7
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4071662"
---
# <a name="creating-invoice-schedules-on-a-project-based-contract-line"></a><span data-ttu-id="70632-103">Criar agendas de faturas em uma linha de contrato baseada em projeto</span><span class="sxs-lookup"><span data-stu-id="70632-103">Creating invoice schedules on a project-based contract line</span></span>

<span data-ttu-id="70632-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="70632-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="70632-105">Você pode criar uma agenda de faturas para uma linha de contrato baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="70632-105">You can an invoice schedule to a  project-based contract line.</span></span> <span data-ttu-id="70632-106">O faturamento só será permitido depois que o contrato for ganho e você estiver criando um contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="70632-106">Invoicing is only allowed after the contract is won to and you are creating a project contract.</span></span> <span data-ttu-id="70632-107">Uma agenda de faturas permite que faturas de rascunho para uma linha de contrato baseada em projeto sejam criadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="70632-107">An invoice schedule allows draft invoices for a project-based contract line to be automatically created.</span></span> <span data-ttu-id="70632-108">No entanto, se você só criar faturas manualmente, poderá ignorar a criação de agendas de faturas em linhas do contrato.</span><span class="sxs-lookup"><span data-stu-id="70632-108">If however, you only manually create invoices, you can skip creating invoice schedules on contract lines.</span></span>

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a><span data-ttu-id="70632-109">Criar uma agenda de fatura de hora e material para uma linha de contrato</span><span class="sxs-lookup"><span data-stu-id="70632-109">Create a time and material invoice schedule for a contract line</span></span>

<span data-ttu-id="70632-110">Quando uma linha de contrato baseada em projeto tem um método de cobrança de hora e material, você pode criar uma agenda de faturas baseada em data.</span><span class="sxs-lookup"><span data-stu-id="70632-110">When a project-based contract line has a time and material billing method, you can create a date-based invoice schedule.</span></span> <span data-ttu-id="70632-111">Para gerar automaticamente uma programação de fatura com base em data, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="70632-111">To automatically generate a date-based invoice schedule, complete the following steps.</span></span>

1. <span data-ttu-id="70632-112">Vá para **Configurações** > **Frequências de fatura** e configure uma frequência de fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-112">Go to **Settings** > **Invoice frequencies** and set up an invoice frequence.</span></span>
2. <span data-ttu-id="70632-113">Vá para o registro do contrato do projeto e na guia **Resumo** , no campo **Data de Entrega Solicitada** , selecione uma data.</span><span class="sxs-lookup"><span data-stu-id="70632-113">Go to the project contract record, and on the **Summary** tab, in the **Requested Delivery Date** field, select a date.</span></span>
3. <span data-ttu-id="70632-114">Abra a linha de contrato **Hora e Material** para a qual você está criando a agenda de faturas baseada em data.</span><span class="sxs-lookup"><span data-stu-id="70632-114">Open the **Time and Material** contract line that you are making the date-based invoice schedule for.</span></span> 
4. <span data-ttu-id="70632-115">Na guia **Agenda de Faturas** , selecione a data inicial de cobrança e a frequência de fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-115">On the **Invoice Schedule** tab, select the billing start date and the invoice frequency.</span></span>
5. <span data-ttu-id="70632-116">Na subgrade, selecione **Gerar Agenda de Faturas**.</span><span class="sxs-lookup"><span data-stu-id="70632-116">On the subgrid, select **Generate Invoice Schedule**.</span></span> <span data-ttu-id="70632-117">A agenda de faturas é gerada com os campos **Data de Execução da Fatura** , **Data de Corte da Transação** e **Status de Execução** definidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="70632-117">The invoice schedule is generated with the **Invoice Run Date** , **Transaction Cutoff Date** and **Run Status** fields set as follows:</span></span>

    - <span data-ttu-id="70632-118">**Data de Execução da Fatura** : esta data é ditada pela frequência da fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-118">**Invoice Run Date** : This date is dictated by the invoice frequency.</span></span>
    - <span data-ttu-id="70632-119">**Data de Corte da Transação** : o dia anterior à data de execução da fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-119">**Transaction Cutoff Date** : The day before the invoice run date.</span></span>
    - <span data-ttu-id="70632-120">**Status de Execução** : automaticamente definido como **Não Executado**.</span><span class="sxs-lookup"><span data-stu-id="70632-120">**Run Status** : Automatically set to **Not Run**.</span></span> <span data-ttu-id="70632-121">Quando o trabalho de criação de fatura automática for executado para determinada data de execução da fatura, este campo será atualizado para **Execução Bem-sucedida** ou **Falha na Execução**.</span><span class="sxs-lookup"><span data-stu-id="70632-121">When the automatic invoice creation job runs for a certain invoice run date, this field is updated to **Run Successful** or **Run Failed**.</span></span>


## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a><span data-ttu-id="70632-122">Crie uma agenda de faturas de preço fixo para uma linha de contrato</span><span class="sxs-lookup"><span data-stu-id="70632-122">Create a fixed price invoice schedule for a contract line</span></span>

<span data-ttu-id="70632-123">Quando a linha de contrato tem um método de cobrança fixa, você pode criar uma agenda de faturas baseada em etapas.</span><span class="sxs-lookup"><span data-stu-id="70632-123">When the contract line has a fixed billing method, you can create a milestone-based invoice schedule.</span></span> <span data-ttu-id="70632-124">Conclua as etapas a seguir para gerar uma agenda de faturas baseada em etapas para um conjunto fixo de etapas igualmente distribuídas para o período do calendário.</span><span class="sxs-lookup"><span data-stu-id="70632-124">Complete the following steps to generate a milestone-based invoice schedule for a fixed set of equally distributed milestones for the calendar period.</span></span>

1. <span data-ttu-id="70632-125">Vá para **Configurações** > **Frequências de fatura** e configure uma frequência de fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-125">Go to **Settings** > **Invoice frequencies** and set up an invoice frequence.</span></span>
2. <span data-ttu-id="70632-126">Vá para o registro do contrato do projeto e na guia **Resumo** , no campo **Data de Entrega Solicitada** , selecione uma data.</span><span class="sxs-lookup"><span data-stu-id="70632-126">Go to the project contract record, and on the **Summary** tab, in the **Requested Delivery Date** field, select a date.</span></span>
3. <span data-ttu-id="70632-127">Abra a linha de contrato **Preço Fixo** para a qual você está criando a agenda de etapas.</span><span class="sxs-lookup"><span data-stu-id="70632-127">Open the **Fixed Price** contract line that you are creating the milestone schedule for.</span></span> <span data-ttu-id="70632-128">Na guia **Etapas de Cobrança** , selecione a data inicial de cobrança e a frequência de fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-128">On the **Billing Milestones** tab, select the billing start date and the invoice frequency.</span></span> 
4. <span data-ttu-id="70632-129">Na subgrade, selecione **Gerar Etapas Periódicas**.</span><span class="sxs-lookup"><span data-stu-id="70632-129">On the subgrid, select **Generate Periodic Milestones**.</span></span> <span data-ttu-id="70632-130">A agenda de faturas é gerada com os campos **Nome da Etapa** , **Data da Etapa** e **Valor da Etapa** definidos da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="70632-130">The  invoice schedule is generated with the **Milestone Name** , **Milestone Date** , and **Milestone Amount** fields set as follows:</span></span>

    - <span data-ttu-id="70632-131">**Nome da Etapa** : esta data é ditada pela frequência da fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-131">**Milestone Name** : This date is dictated by the invoice frequency.</span></span>
    - <span data-ttu-id="70632-132">**Data da Etapa** : esta data é ditada pela frequência da fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-132">**Milestone Date** : This date is dictated by the invoice frequency.</span></span>
    - <span data-ttu-id="70632-133">**Valor da Etapa** : este valor é calculado dividindo o valor do contrato na linha do contrato pelo número de etapas, conforme determinado pela frequência, início da cobrança e datas de entrega solicitadas.</span><span class="sxs-lookup"><span data-stu-id="70632-133">**Milestone Amount** : This amount is calculated by dividing the contract amount on the contract line by the number of milestones as dictated by the frequency, billing start, and requested delivery dates.</span></span>

    <span data-ttu-id="70632-134">Se a linha do contrato tiver um valor no campo **Valor estimado do imposto** , esse campo também será distribuído para cada etapa igualmente ao gerar etapas periódicas.</span><span class="sxs-lookup"><span data-stu-id="70632-134">If the contract line has a value in the **Estimated Tax amount** field, then this field is also apportioned to each milestone equally when generating periodic milestones.</span></span>

<span data-ttu-id="70632-135">As etapas de cobrança devem ser iguais ao valor contratado da linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="70632-135">Billing milestones should equal the contracted value of the contract line.</span></span> <span data-ttu-id="70632-136">Caso contrário, você receberá um erro na página **Linha do Contrato**.</span><span class="sxs-lookup"><span data-stu-id="70632-136">If they don't, you will receive an  error on the **Contract Line** page.</span></span> <span data-ttu-id="70632-137">Você pode corrigir o erro verificando se as etapas de cobrança totalizam o valor contratado da linha, criando, editando ou excluindo etapas.</span><span class="sxs-lookup"><span data-stu-id="70632-137">You can fix the error by verifying that the billing milestones total the contracted value of the line by creating, editing, or deleting milestones.</span></span> <span data-ttu-id="70632-138">Depois que as alterações forem feitas, atualize a página para remover o erro.</span><span class="sxs-lookup"><span data-stu-id="70632-138">After the changes are made, refresh the page to remove the error.</span></span>

### <a name="manually-create-milestones"></a><span data-ttu-id="70632-139">Criar etapas manualmente</span><span class="sxs-lookup"><span data-stu-id="70632-139">Manually create milestones</span></span>

<span data-ttu-id="70632-140">Você pode gerar manualmente etapas de preço fixo quando elas não são divididas periodicamente.</span><span class="sxs-lookup"><span data-stu-id="70632-140">You can generate fixed price milestones manually when they are not periodically split.</span></span> <span data-ttu-id="70632-141">Conclua as etapas a seguir para criar manualmente uma etapa.</span><span class="sxs-lookup"><span data-stu-id="70632-141">Complete the following steps to manually create a milestone.</span></span>

1. <span data-ttu-id="70632-142">Abra a linha de contrato de preço fixo para a qual você está criando uma etapa. Na guia **Agenda de Faturas** , na subgrade, selecione **+ Criar nova etapa da linha de contrato**.</span><span class="sxs-lookup"><span data-stu-id="70632-142">Open the fixed price contract line that you are creating a milestone for, and on the **Invoice Schedule** tab, on the subgrid, select **+ Create new Contract line milestone**.</span></span> 
2. <span data-ttu-id="70632-143">Na página **Criação de Etapa** , insira as informações necessárias com base na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="70632-143">On the **Milestone Creation** page, enter the required information based on the following table.</span></span>

| <span data-ttu-id="70632-144">Campo</span><span class="sxs-lookup"><span data-stu-id="70632-144">Field</span></span> | <span data-ttu-id="70632-145">Localização</span><span class="sxs-lookup"><span data-stu-id="70632-145">Location</span></span> | <span data-ttu-id="70632-146">Relevância, finalidade e orientação</span><span class="sxs-lookup"><span data-stu-id="70632-146">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="70632-147">Impacto a jusante</span><span class="sxs-lookup"><span data-stu-id="70632-147">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="70632-148">Nome da Etapa</span><span class="sxs-lookup"><span data-stu-id="70632-148">Milestone Name</span></span> | <span data-ttu-id="70632-149">Criação Rápida</span><span class="sxs-lookup"><span data-stu-id="70632-149">Quick Create</span></span> | <span data-ttu-id="70632-150">Campo de texto para o nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="70632-150">Text field for the name of the milestone.</span></span> | <span data-ttu-id="70632-151">Isso é transferido para a etapa de linha do contrato do projeto e a fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-151">This is carried over to the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="70632-152">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="70632-152">Project Task</span></span> | <span data-ttu-id="70632-153">Criação Rápida</span><span class="sxs-lookup"><span data-stu-id="70632-153">Quick Create</span></span> | <span data-ttu-id="70632-154">Se a etapa estiver vinculada à tarefa do projeto, use esta referência para adicionar lógica personalizada para definir o status da etapa com base no status da tarefa.</span><span class="sxs-lookup"><span data-stu-id="70632-154">If the milestone is tied to project task, use this reference to add custom logic to set the milestone status based on the task status.</span></span> | <span data-ttu-id="70632-155">O aplicativo não tem impacto downstream dessa referência a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="70632-155">The application, doesn't have any downstream impact of this reference to a task.</span></span> |
| <span data-ttu-id="70632-156">Data da Etapa</span><span class="sxs-lookup"><span data-stu-id="70632-156">Milestone Date</span></span> | <span data-ttu-id="70632-157">Criação Rápida</span><span class="sxs-lookup"><span data-stu-id="70632-157">Quick Create</span></span> | <span data-ttu-id="70632-158">Defina a data em que o processo de criação automática de nota fiscal deve procurar o status deste marco para considerá-lo para o faturamento.</span><span class="sxs-lookup"><span data-stu-id="70632-158">Set the date on which the automatic invoice creation process should look for the status of this milestone to consider it for invoicing.</span></span> | <span data-ttu-id="70632-159">Isso é transferido para a etapa de linha do contrato do projeto e a fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-159">This is carried over to the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="70632-160">Status da Fatura</span><span class="sxs-lookup"><span data-stu-id="70632-160">Invoice Status</span></span> | <span data-ttu-id="70632-161">Criação Rápida</span><span class="sxs-lookup"><span data-stu-id="70632-161">Quick Create</span></span> | <span data-ttu-id="70632-162">Quando uma etapa é criada, este status é sempre definido como **Não Pronto para Faturamento** ou **Não Iniciado**.</span><span class="sxs-lookup"><span data-stu-id="70632-162">When a milestone is created, this status is always set to **Not Ready for Invoicing** or **Not Started**.</span></span> | <span data-ttu-id="70632-163">Isso é transferido para a etapa de linha do contrato do projeto e a fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-163">This is carried over to the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="70632-164">Valor da Linha</span><span class="sxs-lookup"><span data-stu-id="70632-164">Line Amount</span></span> | <span data-ttu-id="70632-165">Criação Rápida</span><span class="sxs-lookup"><span data-stu-id="70632-165">Quick Create</span></span> | <span data-ttu-id="70632-166">Quantidade ou valor da etapa que será faturada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="70632-166">Amount or value of the milestone that will be invoiced to the customer.</span></span> | <span data-ttu-id="70632-167">Isso é transferido para a etapa de linha do contrato do projeto e a fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-167">This is carried over to the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="70632-168">Imposto</span><span class="sxs-lookup"><span data-stu-id="70632-168">Tax</span></span> | <span data-ttu-id="70632-169">Criação Rápida</span><span class="sxs-lookup"><span data-stu-id="70632-169">Quick Create</span></span> | <span data-ttu-id="70632-170">O valor do imposto aplicado na etapa.</span><span class="sxs-lookup"><span data-stu-id="70632-170">The tax amount applied on the milestone.</span></span> | <span data-ttu-id="70632-171">Isso é transferido para a etapa de linha do contrato do projeto e a fatura.</span><span class="sxs-lookup"><span data-stu-id="70632-171">This is carried over to the project contract line milestone and the invoice.</span></span> |

3. <span data-ttu-id="70632-172">Selecione **Salvar e Fechar**.</span><span class="sxs-lookup"><span data-stu-id="70632-172">Select **Save and Close**.</span></span>
<span data-ttu-id="70632-173">| Quantidade da linha | Criação rápida | Quantia ou valor da etapa que será faturada ao cliente | Isso é propagado para a linha de contrato do projeto Etapa e para a Fatura | | Imposto | Criação rápida | Valor do imposto que será aplicado na Etapa | Isso é propagado para a linha de contrato do projeto Etapa e para a Fatura |</span><span class="sxs-lookup"><span data-stu-id="70632-173">| Line Amount | Quick create | Amount or Value of the Milestone that will be invoiced to the customer | This is propagated to the Project contract line Milestone and to the Invoice | | Tax | Quick create | Tax amount that will be applied on the Milestone | This is propagated to the Project contract line Milestone and to the Invoice |</span></span>