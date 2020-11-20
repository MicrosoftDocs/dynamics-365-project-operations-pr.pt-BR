---
title: Visão geral de aprovações
description: Este tópico fornece informações sobre como trabalhar com aprovações em Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 14c6914cf9b5fb52e7554e51604e79f0920064df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123814"
---
# <a name="approvals-overview"></a><span data-ttu-id="5ee0d-103">Visão geral de aprovações</span><span class="sxs-lookup"><span data-stu-id="5ee0d-103">Approvals overview</span></span>

<span data-ttu-id="5ee0d-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="5ee0d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5ee0d-105">Os envios de Tempo e Despesa passam por um fluxo de trabalho de aprovação.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="5ee0d-106">Depois que as entradas forem aprovadas, as transações serão registradas em dados reais ou as horas serão reservadas na agenda.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="5ee0d-107">Fluxo de trabalho de aprovações</span><span class="sxs-lookup"><span data-stu-id="5ee0d-107">Approvals workflow</span></span>
<span data-ttu-id="5ee0d-108">Ao criar e enviar uma entrada de hora ou de despesa, é criada uma entrada de aprovação.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="5ee0d-109">O Aprovador do projeto ou o gerente revisa e aprova a entrada.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="5ee0d-110">Se a entrada estiver relacionada a um projeto, após a aprovação, os dados reais serão criados.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="5ee0d-111">Isso permite que o custo e a cobrança sejam rastreados.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="5ee0d-112">Aprovar uma entrada</span><span class="sxs-lookup"><span data-stu-id="5ee0d-112">Approve an entry</span></span>
<span data-ttu-id="5ee0d-113">O formulário **Aprovações** permite alternar entre diferentes exibições para que você possa exibir os diferentes tipos de aprovações.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="5ee0d-114">Vá para o formulário **Aprovações** e selecione **Despesas**, **Hora** ou **Recuperações**.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="5ee0d-115">Revise cada aprovação e selecione aquelas que deseja aprovar.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="5ee0d-116">Selecione **Aprovar** para aprovar as entradas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="5ee0d-117">O sistema processará essas entradas e criará dados reais ou uma reserva.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="5ee0d-118">Rejeitar uma entrada</span><span class="sxs-lookup"><span data-stu-id="5ee0d-118">Reject an entry</span></span>
<span data-ttu-id="5ee0d-119">Como Aprovador do projeto, talvez seja necessário enviar uma entrada de volta para um usuário para correção.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="5ee0d-120">Vá para o formulário **Aprovações** e selecione a entrada que deseja rejeitar.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="5ee0d-121">Selecione **Rejeitar**.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-121">Select **Reject**.</span></span>
3. <span data-ttu-id="5ee0d-122">Opcional – Adicione um comentário na caixa de diálogo **Rejeitar Comentários** para informar o usuário o motivo pelo qual a entrada está sendo rejeitada.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="5ee0d-123">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-123">Select **OK**.</span></span> <span data-ttu-id="5ee0d-124">A entrada será devolvida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="5ee0d-125">Recuperar entradas</span><span class="sxs-lookup"><span data-stu-id="5ee0d-125">Recall entries</span></span>
<span data-ttu-id="5ee0d-126">Em algum momento, talvez seja necessário recuperar uma entrada enviada.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="5ee0d-127">Se a entrada não tiver sido aprovada, ela será devolvida imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="5ee0d-128">No entanto, uma entrada aprovada poderá ter um impacto material.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="5ee0d-129">O Aprovador do projeto deve aprovar a recuperação para reverter a transação em Dados reais.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="5ee0d-130">Especificar Aprovadores de projeto</span><span class="sxs-lookup"><span data-stu-id="5ee0d-130">Specify Project approvers</span></span>
<span data-ttu-id="5ee0d-131">Cada projeto tem vários membros da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-131">Each project has a number of project team members.</span></span> <span data-ttu-id="5ee0d-132">Você pode especificar quais membros da equipe também são Aprovadores de projeto.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="5ee0d-133">Vá para o formulário **Projetos** e abra o projeto da lista.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="5ee0d-134">Na guia **Equipe**, selecione o membro da equipe que será um Aprovador do projeto e selecione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="5ee0d-135">Defina o campo **Aprovador do projeto** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="5ee0d-136">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-136">Select **Save**.</span></span>
5. <span data-ttu-id="5ee0d-137">Repita as etapas 2 e 4 para adicionar Aprovadores de projeto.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="5ee0d-138">Configurar o gerente do usuário</span><span class="sxs-lookup"><span data-stu-id="5ee0d-138">Configure the user's manager</span></span>

1. <span data-ttu-id="5ee0d-139">Vá para **Configurações** > **Segurança** > **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="5ee0d-140">Selecione o usuário ao qual você está atribuindo um gerente e, na área **Informações da Organização**, selecione o gerente na lista.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="5ee0d-141">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="5ee0d-141">Select **Save**.</span></span>


