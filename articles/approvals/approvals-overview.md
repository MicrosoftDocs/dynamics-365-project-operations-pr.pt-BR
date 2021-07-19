---
title: Visão geral de aprovações
description: Este tópico fornece informações sobre como trabalhar com aprovações em Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368642"
---
# <a name="approvals-overview"></a><span data-ttu-id="863eb-103">Visão geral de aprovações</span><span class="sxs-lookup"><span data-stu-id="863eb-103">Approvals overview</span></span>

<span data-ttu-id="863eb-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="863eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="863eb-105">Tempo, despesas e uso de material são enviados por um fluxo de trabalho de aprovação.</span><span class="sxs-lookup"><span data-stu-id="863eb-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="863eb-106">Depois que as entradas forem aprovadas, as transações serão registradas em dados reais ou as horas serão reservadas na agenda.</span><span class="sxs-lookup"><span data-stu-id="863eb-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="863eb-107">Fluxo de trabalho de aprovações</span><span class="sxs-lookup"><span data-stu-id="863eb-107">Approvals workflow</span></span>
<span data-ttu-id="863eb-108">Ao criar e enviar uma entrada de tempo, despesa ou uso de material, é criado um registro de aprovação.</span><span class="sxs-lookup"><span data-stu-id="863eb-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="863eb-109">O aprovador ou gerente do projeto avalia e aprova a entrada.</span><span class="sxs-lookup"><span data-stu-id="863eb-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="863eb-110">Se a entrada estiver relacionada a um projeto, os dados reais serão criados quando ele for aprovado.</span><span class="sxs-lookup"><span data-stu-id="863eb-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="863eb-111">Isso permite que o custo e a cobrança sejam rastreados.</span><span class="sxs-lookup"><span data-stu-id="863eb-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="863eb-112">Aprovar uma entrada</span><span class="sxs-lookup"><span data-stu-id="863eb-112">Approve an entry</span></span>
<span data-ttu-id="863eb-113">A página **Aprovações** permite alternar entre exibições diferentes para permitir a exibição de diferentes tipos de aprovações.</span><span class="sxs-lookup"><span data-stu-id="863eb-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="863eb-114">Acesse a página **Aprovações** e selecione **Despesas**, **Hora**, **Uso de Material** ou **Recalls**.</span><span class="sxs-lookup"><span data-stu-id="863eb-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="863eb-115">Revise cada aprovação e selecione aquelas que deseja aprovar.</span><span class="sxs-lookup"><span data-stu-id="863eb-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="863eb-116">Selecione **Aprovar** para aprovar as entradas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="863eb-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="863eb-117">O sistema processa essas entradas e cria dados reais.</span><span class="sxs-lookup"><span data-stu-id="863eb-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="863eb-118">Rejeitar uma entrada</span><span class="sxs-lookup"><span data-stu-id="863eb-118">Reject an entry</span></span>
<span data-ttu-id="863eb-119">Como Aprovador do projeto, talvez seja necessário enviar uma entrada de volta para um usuário para correção.</span><span class="sxs-lookup"><span data-stu-id="863eb-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="863eb-120">Acesse a página **Aprovações** e selecione a entrada a ser rejeitada.</span><span class="sxs-lookup"><span data-stu-id="863eb-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="863eb-121">Selecione **Rejeitar**.</span><span class="sxs-lookup"><span data-stu-id="863eb-121">Select **Reject**.</span></span>
3. <span data-ttu-id="863eb-122">Opcional, adicione um comentário na caixa de diálogo **Comentários de Rejeição** para informar ao usuário de que a entrada está sendo rejeitada.</span><span class="sxs-lookup"><span data-stu-id="863eb-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="863eb-123">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="863eb-123">Select **OK**.</span></span> <span data-ttu-id="863eb-124">A entrada será devolvida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="863eb-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="863eb-125">Cancelar aprovação</span><span class="sxs-lookup"><span data-stu-id="863eb-125">Cancel approval</span></span>
<span data-ttu-id="863eb-126">Em alguns casos, pode ser necessário cancelar uma entrada aprovada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="863eb-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="863eb-127">O cancelamento de uma entrada aprovada anteriormente terá um impacto financeiro.</span><span class="sxs-lookup"><span data-stu-id="863eb-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="863eb-128">Aprovar solicitações de recuperação</span><span class="sxs-lookup"><span data-stu-id="863eb-128">Approving recall requests</span></span>
<span data-ttu-id="863eb-129">Em alguns casos, um consultor pode precisar recuperar uma entrada aprovada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="863eb-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="863eb-130">O cancelamento de uma entrada aprovada anteriormente terá um impacto financeiro.</span><span class="sxs-lookup"><span data-stu-id="863eb-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="863eb-131">O aprovador do projeto deve aprovar a recuperação para reverter a transação em Dados reais.</span><span class="sxs-lookup"><span data-stu-id="863eb-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="863eb-132">Especificar Aprovadores de projeto</span><span class="sxs-lookup"><span data-stu-id="863eb-132">Specify Project approvers</span></span>
<span data-ttu-id="863eb-133">Cada projeto tem vários membros da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="863eb-133">Each project has a number of project team members.</span></span> <span data-ttu-id="863eb-134">Você pode especificar quais membros da equipe também são Aprovadores de projeto.</span><span class="sxs-lookup"><span data-stu-id="863eb-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="863eb-135">Acesse a página **Projetos** e abra o projeto da lista.</span><span class="sxs-lookup"><span data-stu-id="863eb-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="863eb-136">Na guia **Equipe**, selecione o membro da equipe que será um Aprovador do projeto e selecione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="863eb-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="863eb-137">Defina o campo **Aprovador do projeto** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="863eb-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="863eb-138">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="863eb-138">Select **Save**.</span></span>
5. <span data-ttu-id="863eb-139">Repita as etapas 2 e 4 para adicionar Aprovadores de projeto.</span><span class="sxs-lookup"><span data-stu-id="863eb-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="863eb-140">Configurar o gerente do usuário</span><span class="sxs-lookup"><span data-stu-id="863eb-140">Configure the user's manager</span></span>

1. <span data-ttu-id="863eb-141">Vá para **Configurações** > **Segurança** > **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="863eb-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="863eb-142">Selecione o usuário ao qual você está atribuindo um gerente e, na área **Informações da Organização**, selecione o gerente na lista.</span><span class="sxs-lookup"><span data-stu-id="863eb-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="863eb-143">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="863eb-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
