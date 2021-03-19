---
title: Recuperar entradas de hora ou despesa aprovadas
description: Este tópico fornece informações sobre como recuperar uma transação de hora ou despesa aprovada anteriormente.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1a199985099745b2e62b844ef748ea2031054458
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283444"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="4122d-103">Recuperar entradas de hora ou despesa aprovadas</span><span class="sxs-lookup"><span data-stu-id="4122d-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4122d-104">Um membro da equipe do projeto ou outra pessoa que enviar uma entrada de hora ou despesa pode recuperar essa entrada após sua aprovação.</span><span class="sxs-lookup"><span data-stu-id="4122d-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="4122d-105">O processo de recuperação de uma entrada de hora ou despesa aprovada tem duas etapas:</span><span class="sxs-lookup"><span data-stu-id="4122d-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="4122d-106">Um remetente solicita uma recuperação.</span><span class="sxs-lookup"><span data-stu-id="4122d-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="4122d-107">Um aprovador aprova a recuperação.</span><span class="sxs-lookup"><span data-stu-id="4122d-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="4122d-108">Solicitar uma recuperação</span><span class="sxs-lookup"><span data-stu-id="4122d-108">Request a recall</span></span>

<span data-ttu-id="4122d-109">Siga estas etapas para solicitar a recuperação de uma entrada de hora ou despesa aprovada.</span><span class="sxs-lookup"><span data-stu-id="4122d-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="4122d-110">Para entradas de hora, acesse **Projetos** \> **Minhas Atividades** \> **Entrada de Hora**.</span><span class="sxs-lookup"><span data-stu-id="4122d-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="4122d-111">–ou–</span><span class="sxs-lookup"><span data-stu-id="4122d-111">–or–</span></span>

    <span data-ttu-id="4122d-112">Para entradas de despesa, acesse **Projetos** \> **Minhas Atividades** \> **Despesas**.</span><span class="sxs-lookup"><span data-stu-id="4122d-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="4122d-113">Para entradas de hora, selecione todas as entradas de hora para uma combinação específica de um projeto e uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="4122d-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="4122d-114">Como alternativa, na grade, selecione as células individuais de hora em uma data específica para um projeto específico.</span><span class="sxs-lookup"><span data-stu-id="4122d-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="4122d-115">–ou–</span><span class="sxs-lookup"><span data-stu-id="4122d-115">–or–</span></span>

    <span data-ttu-id="4122d-116">Para entradas de despesa, selecione a linha para a entrada de despesa recuperar.</span><span class="sxs-lookup"><span data-stu-id="4122d-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="4122d-117">Selecione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="4122d-117">Select **Recall**.</span></span> <span data-ttu-id="4122d-118">Uma caixa de diálogo de confirmação é exibida.</span><span class="sxs-lookup"><span data-stu-id="4122d-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="4122d-119">Se as entradas de hora e despesa selecionadas já tiverem sido aprovadas, você será solicitado a inserir um motivo para a recuperação.</span><span class="sxs-lookup"><span data-stu-id="4122d-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="4122d-120">Insira um motivo para a recuperação e, em seguida, selecione **OK** para confirmar a operação.</span><span class="sxs-lookup"><span data-stu-id="4122d-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="4122d-121">O sistema enviará para a pessoa que aprovou as entradas uma solicitação para aprovar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="4122d-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="4122d-122">Embora as entradas de hora e despesa aprovadas possam ser recuperadas, se uma hora ou despesa aprovada já tiver sido faturada para o cliente, uma solicitação de recuperação não poderá ser criada.</span><span class="sxs-lookup"><span data-stu-id="4122d-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="4122d-123">O usuário que tentar criar uma solicitação de recuperação receberá uma mensagem informando que a hora ou despesa não pode ser recuperada, pois já foi faturada.</span><span class="sxs-lookup"><span data-stu-id="4122d-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="4122d-124">Aprovar ou rejeitar uma solicitação de recuperação</span><span class="sxs-lookup"><span data-stu-id="4122d-124">Approve or reject a recall request</span></span>

<span data-ttu-id="4122d-125">Siga estas etapas para aprovar ou rejeitar uma solicitação de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4122d-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="4122d-126">Vá para **Projetos** \> **Meu Trabalho** \> **Aprovações**.</span><span class="sxs-lookup"><span data-stu-id="4122d-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="4122d-127">Na página da lista **Aprovações**, altere a exibição para **Solicitações de recuperação para aprovação**.</span><span class="sxs-lookup"><span data-stu-id="4122d-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="4122d-128">Uma lista das solicitações de recuperação enviadas é exibida.</span><span class="sxs-lookup"><span data-stu-id="4122d-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="4122d-129">Selecione uma ou mais entradas e, em seguida, selecione **Aprovar** ou **Rejeitar**.</span><span class="sxs-lookup"><span data-stu-id="4122d-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="4122d-130">Se você selecionou **Aprovar**, receberá uma mensagem de aviso que explica o impacto da aprovação.</span><span class="sxs-lookup"><span data-stu-id="4122d-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="4122d-131">Selecione **OK** para confirmar a operação.</span><span class="sxs-lookup"><span data-stu-id="4122d-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="4122d-132">A solicitação de recuperação foi aprovada.</span><span class="sxs-lookup"><span data-stu-id="4122d-132">The recall request is approved.</span></span>

    <span data-ttu-id="4122d-133">–ou–</span><span class="sxs-lookup"><span data-stu-id="4122d-133">–or–</span></span>

    <span data-ttu-id="4122d-134">Se você selecionou **Rejeitar**, a solicitação de recuperação foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="4122d-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="4122d-135">Assim como ocorre na solicitação de recuperação, quando uma recuperação é aprovada, o sistema verifica se há atividade de faturamento nas entradas de hora ou despesa.</span><span class="sxs-lookup"><span data-stu-id="4122d-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="4122d-136">Se uma entrada já tiver sido faturada ou se estiver em uma fatura de rascunho, o aprovador receberá uma mensagem de erro informando que a hora ou despesa não pode ser aprovada para recuperação, pois já foi faturada.</span><span class="sxs-lookup"><span data-stu-id="4122d-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="4122d-137">Impacto de uma solicitação de recuperação</span><span class="sxs-lookup"><span data-stu-id="4122d-137">Impact of a recall request</span></span>

<span data-ttu-id="4122d-138">Quando uma aprovação é recuperada, há impactos operacionais e financeiros.</span><span class="sxs-lookup"><span data-stu-id="4122d-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="4122d-139">Impacto operacional</span><span class="sxs-lookup"><span data-stu-id="4122d-139">Operational impact</span></span>

<span data-ttu-id="4122d-140">Se uma solicitação de recuperação for aprovada, o registro de aprovação será marcado como **Rejeitado**.</span><span class="sxs-lookup"><span data-stu-id="4122d-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="4122d-141">O status da entrada será alterado para **Devolvido** ou **Rejeitado**, dependendo da entrada ser de hora ou despesa.</span><span class="sxs-lookup"><span data-stu-id="4122d-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="4122d-142">O membro da equipe do projeto pode visualizar entradas, editá-las e reenviá-las ou excluí-las totalmente.</span><span class="sxs-lookup"><span data-stu-id="4122d-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="4122d-143">Se uma solicitação de recuperação for rejeitada, o status da entrada permanecerá **Aprovado** e ela não poderá ser editada pelo membro da equipe ou o aprovador do projeto.</span><span class="sxs-lookup"><span data-stu-id="4122d-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="4122d-144">Impacto financeiro</span><span class="sxs-lookup"><span data-stu-id="4122d-144">Financial impact</span></span>

<span data-ttu-id="4122d-145">Se uma solicitação de recuperação for aprovada, os dados efetivos correspondentes de custo e vendas serão atualizados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4122d-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="4122d-146">O campo **Status do Ajuste** será atualizado para **Ajustado**.</span><span class="sxs-lookup"><span data-stu-id="4122d-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="4122d-147">O campo **Status de Cobrança** será atualizado para **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="4122d-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="4122d-148">Em seguida, as entradas reversas são criadas na tabela Dados reais.</span><span class="sxs-lookup"><span data-stu-id="4122d-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="4122d-149">Para criar entradas de reversão, o sistema dados reais originais nos valores de campo.</span><span class="sxs-lookup"><span data-stu-id="4122d-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="4122d-150">Os únicos valores que não são copiados são os valores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="4122d-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="4122d-151">Esses valores são revertidos.</span><span class="sxs-lookup"><span data-stu-id="4122d-151">These values are reversed instead.</span></span> <span data-ttu-id="4122d-152">Os dados reais revertidos são criados para dados reais de **Custo** e **Vendas Não Cobradas**.</span><span class="sxs-lookup"><span data-stu-id="4122d-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="4122d-153">O campo **Status do Ajuste** nos dados efetivos revertidos será definido como **Não Ajustável**, e o campo **Status de Cobrança** será definido como **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="4122d-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="4122d-154">Devido a essas alterações, o gasto registrado e a lista de pendências de receita no projeto não vão mais considerar os valores que esses dados efetivos representam.</span><span class="sxs-lookup"><span data-stu-id="4122d-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="4122d-155">Se uma solicitação de recuperação for rejeitada, não haverá impacto financeiro no projeto.</span><span class="sxs-lookup"><span data-stu-id="4122d-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="4122d-156">Alterações em registros de entradas de hora</span><span class="sxs-lookup"><span data-stu-id="4122d-156">Changes to time entry records</span></span>

<span data-ttu-id="4122d-157">A ilustração a seguir mostra as alterações que ocorrem em entradas de hora aprovadas quando elas são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="4122d-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Transições de estado de Entradas de Hora](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="4122d-159">Alterações em registros de entradas de despesa</span><span class="sxs-lookup"><span data-stu-id="4122d-159">Changes to expense entry records</span></span>

<span data-ttu-id="4122d-160">A ilustração a seguir mostra as alterações que ocorrem em entradas de despesa aprovadas quando elas são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="4122d-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Transições de estado de Entradas de Despesa](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]