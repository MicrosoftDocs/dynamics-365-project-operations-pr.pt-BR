---
title: Entrada de despesa (lite)
description: Este tópico fornece informações sobre como trabalhar com entrada de despesa em uma implantação lite.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965723"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="ab327-103">Entrada de despesa (lite)</span><span class="sxs-lookup"><span data-stu-id="ab327-103">Expense entry (lite)</span></span>

<span data-ttu-id="ab327-104">_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="ab327-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ab327-105">Básico ou lite, o gerenciamento de despesas é o recurso usado para registrar despesas simples.</span><span class="sxs-lookup"><span data-stu-id="ab327-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="ab327-106">Você pode registrar despesas em um projeto e, em seguida, o aprovador do projeto revisará e aprovará essas despesas.</span><span class="sxs-lookup"><span data-stu-id="ab327-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="ab327-107">Para obter mais informações sobre os recursos de despesas no Dynamics 365 Project Operations, consulte [Visão geral de despesas](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ab327-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="ab327-108">Capturar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="ab327-108">Capture a basic expense</span></span>

<span data-ttu-id="ab327-109">Você pode capturar as despesas para que você possa enviá-las para o aprovador.</span><span class="sxs-lookup"><span data-stu-id="ab327-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="ab327-110">Vá para **Despesas** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ab327-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="ab327-111">Na página **Nova Despesa**, insira as informações de despesas obrigatórias e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ab327-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="ab327-112">Enviar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="ab327-112">Submit a basic expense</span></span>

<span data-ttu-id="ab327-113">Quando tiver capturado todas as suas despesas e estiver pronto para aprová-las, você deve enviá-las.</span><span class="sxs-lookup"><span data-stu-id="ab327-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="ab327-114">Vá para **Despesas** e selecione uma despesa.</span><span class="sxs-lookup"><span data-stu-id="ab327-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="ab327-115">Ou, selecione todas as despesas usando a caixa de seleção no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ab327-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="ab327-116">Selecione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="ab327-116">Select **Submit**.</span></span> <span data-ttu-id="ab327-117">O sistema processa as entradas selecionadas e depois cria solicitações de aprovação de despesas.</span><span class="sxs-lookup"><span data-stu-id="ab327-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="ab327-118">Recuperar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="ab327-118">Recall a basic expense</span></span>

<span data-ttu-id="ab327-119">Ao enviar uma despesa por engano, é possível recuperá-la.</span><span class="sxs-lookup"><span data-stu-id="ab327-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="ab327-120">O tempo necessário para recuperar uma entrada de despesa depende do estágio de aprovação.</span><span class="sxs-lookup"><span data-stu-id="ab327-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="ab327-121">Se o aprovador ainda não tiver aprovado a entrada, a recuperação poderá ser executada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ab327-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="ab327-122">No entanto, se a entrada já tiver sido aprovada, o aprovador receberá uma solicitação para aprovar a recuperação e reverter as transações.</span><span class="sxs-lookup"><span data-stu-id="ab327-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="ab327-123">Vá para **Despesas** e, na lista de despesas, selecione a despesa que deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="ab327-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="ab327-124">Selecione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="ab327-124">Select **Recall**.</span></span> <span data-ttu-id="ab327-125">Se a entrada de despesa não tiver sido aprovada, o sistema a recuperará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ab327-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="ab327-126">Se a entrada de despesa já tiver sido aprovada, uma solicitação de recuperação será criada para notificar o aprovador que você deseja reverter a despesa.</span><span class="sxs-lookup"><span data-stu-id="ab327-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="ab327-127">O aprovador confirmará se a reversão poderá ser feita e a entrada será retornada.</span><span class="sxs-lookup"><span data-stu-id="ab327-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="ab327-128">Excluir uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="ab327-128">Delete a basic expense</span></span>

<span data-ttu-id="ab327-129">As despesas que ainda não foram enviadas podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="ab327-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="ab327-130">Para excluir uma despesa que já foi enviada, é necessário antes recuperá-la.</span><span class="sxs-lookup"><span data-stu-id="ab327-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab327-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ab327-131">See also</span></span>

- [<span data-ttu-id="ab327-132">Visão geral de aprovações</span><span class="sxs-lookup"><span data-stu-id="ab327-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
