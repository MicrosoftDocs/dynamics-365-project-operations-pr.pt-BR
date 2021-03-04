---
title: Cancelar entradas de tempo e despesa aprovadas anteriormente
description: Este tópico fornece informações sobre como cancelar uma transação aprovada de tempo e despesa do projeto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150564"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="1751f-103">Cancelar entradas de tempo ou despesa aprovadas anteriormente</span><span class="sxs-lookup"><span data-stu-id="1751f-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1751f-104">Na versão mais recente do Dynamics 365 Project Service Automation, os aprovadores podem cancelar entradas de tempo ou despesa que eles aprovaram anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1751f-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="1751f-105">Cancelar uma entrada de tempo ou despesa aprovadas anteriormente</span><span class="sxs-lookup"><span data-stu-id="1751f-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="1751f-106">Siga estas etapas para cancelar uma entrada de tempo ou despesa que foi aprovada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1751f-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="1751f-107">Vá para **Projetos** \> **Meu Trabalho** \> **Aprovações**.</span><span class="sxs-lookup"><span data-stu-id="1751f-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="1751f-108">Na página de lista **Aprovações**, altere a exibição para **Minhas aprovações anteriores**.</span><span class="sxs-lookup"><span data-stu-id="1751f-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="1751f-109">Uma lista das entradas de tempo e despesa que você aprovou anteriormente é mostrada.</span><span class="sxs-lookup"><span data-stu-id="1751f-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="1751f-110">Selecione uma ou mais entradas e selecione **Cancelar aprovação**.</span><span class="sxs-lookup"><span data-stu-id="1751f-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="1751f-111">Você recebe uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="1751f-111">You receive a warning message.</span></span>
4. <span data-ttu-id="1751f-112">Selecione **OK** para cancelar a aprovação.</span><span class="sxs-lookup"><span data-stu-id="1751f-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="1751f-113">Compreenda o impacto de cancelar uma aprovação de entrada de tempo ou despesa</span><span class="sxs-lookup"><span data-stu-id="1751f-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="1751f-114">Quando uma aprovação é cancelada, há impactos operacionais e financeiros.</span><span class="sxs-lookup"><span data-stu-id="1751f-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="1751f-115">Impacto operacional</span><span class="sxs-lookup"><span data-stu-id="1751f-115">Operational impact</span></span>

<span data-ttu-id="1751f-116">No lado das operações, quando uma aprovação é cancelada, o status do registro é redefinido para **Rascunho** e a aprovação não aparece mais na exibição **Minhas aprovações anteriores**.</span><span class="sxs-lookup"><span data-stu-id="1751f-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="1751f-117">Em vez disso, a aprovação cancelada aparece na exibição **Entradas de tempo para aprovação** ou **Entradas de despesa para aprovação** se era uma entrada de tempo ou uma entrada de despesa, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1751f-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="1751f-118">Além disso, o status da entrada de tempo ou despesa relacionada é alterado para **Enviado**, de modo que a entrada relacionada é consistente com as aprovações que tem um status de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="1751f-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="1751f-119">Como aprovador, você pode editar alguns dos campos de uma provação que tem um status de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="1751f-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="1751f-120">Esses campos incluem **Tipo de Cobrança** e **Horas Faturáveis para Entradas de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="1751f-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="1751f-121">Depois de fazer as alterações, é possível aprovar o registro novamente.</span><span class="sxs-lookup"><span data-stu-id="1751f-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="1751f-122">Se desejar, você pode rejeitar a entrada.</span><span class="sxs-lookup"><span data-stu-id="1751f-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="1751f-123">Se você rejeitar a aprovação de uma entrada de tempo, o status da entrada será alterado para **Devolvida**.</span><span class="sxs-lookup"><span data-stu-id="1751f-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="1751f-124">Se você rejeitar a aprovação de uma entrada de despesa, o status será alterado para **Rejeitada**.</span><span class="sxs-lookup"><span data-stu-id="1751f-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="1751f-125">De modo prático, as entradas devolvidas e rejeitadas se comportam igualmente a uma entrada com o status de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="1751f-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="1751f-126">Um membro da equipe do projeto pode fazer qualquer mudança necessária na entrada e reenviá-la para aprovação, ou excluir completamente a entrada.</span><span class="sxs-lookup"><span data-stu-id="1751f-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="1751f-127">Impacto financeiro</span><span class="sxs-lookup"><span data-stu-id="1751f-127">Financial impact</span></span>

<span data-ttu-id="1751f-128">Um projeto também é afetado financeiramente quando uma aprovação é cancelada.</span><span class="sxs-lookup"><span data-stu-id="1751f-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="1751f-129">Primeiramente, os dados reais correspondentes de custo e vendas são atualizados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1751f-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="1751f-130">O status de ajuste é definido como **Ajustado**.</span><span class="sxs-lookup"><span data-stu-id="1751f-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="1751f-131">O status da cobrança é definido como **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="1751f-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="1751f-132">Em seguida, as entradas reversas são criadas na tabela Dados reais.</span><span class="sxs-lookup"><span data-stu-id="1751f-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="1751f-133">Para criar entradas de reversão, o sistema dados reais originais nos valores de campo.</span><span class="sxs-lookup"><span data-stu-id="1751f-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="1751f-134">Os únicos valores que não são copiados são os valores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="1751f-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="1751f-135">Esses valores são revertidos.</span><span class="sxs-lookup"><span data-stu-id="1751f-135">These values are reversed instead.</span></span> <span data-ttu-id="1751f-136">Os dados reais revertidos são criados para dados reais de **Custo** e **Vendas Não Cobradas**.</span><span class="sxs-lookup"><span data-stu-id="1751f-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="1751f-137">O campo **Status do Ajuste** nos dados reais revertidos é definido como **Não Ajustável** e o status de cobrança é definido como **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="1751f-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="1751f-138">Depois que as alterações forem feitas, o valor que é registrado como gasto no projeto e na lista de pendências de receita no projeto não será mais contado para os valores representados por esses dados reais.</span><span class="sxs-lookup"><span data-stu-id="1751f-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
