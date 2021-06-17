---
title: Relatórios de despesas e vários aprovadores
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação de mais de uma pessoa.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002042"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="d03a6-103">Relatórios de despesas e vários aprovadores</span><span class="sxs-lookup"><span data-stu-id="d03a6-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="d03a6-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="d03a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d03a6-105">Dependendo das políticas de aprovação de despesas da organização, talvez seja necessária a aprovação por mais de uma pessoa de um relatório de despesas enviado.</span><span class="sxs-lookup"><span data-stu-id="d03a6-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="d03a6-106">Ao configurar o processo de fluxo de trabalho para aprovação de relatório de despesas, você pode adicionar elementos de fluxo de trabalho que incluem tarefas ou etapas para um ou mais aprovadores de relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d03a6-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d03a6-107">Por exemplo, você pode exigir que todos os relatórios de despesas sejam aprovados por duas pessoas diferentes, o gerente do funcionário que enviou o relatório e o coordenador de contas a pagar.</span><span class="sxs-lookup"><span data-stu-id="d03a6-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="d03a6-108">Se você decidir exigir vários aprovadores de relatórios de despesas, poderá adicionar os elementos do fluxo de trabalho de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="d03a6-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d03a6-109">Adicione um elemento de aprovação com uma etapa.</span><span class="sxs-lookup"><span data-stu-id="d03a6-109">Add one approval element that has one step.</span></span> <span data-ttu-id="d03a6-110">Por exemplo, a etapa pode exigir que um relatório de despesas seja atribuído a um grupo de usuários e que seja aprovado por 50% dos membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="d03a6-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d03a6-111">Adicione um elemento de aprovação com várias etapas.</span><span class="sxs-lookup"><span data-stu-id="d03a6-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d03a6-112">Por exemplo, o elemento de aprovação pode ter as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d03a6-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d03a6-113">O gerente do funcionário que enviou o relatório de despesas o aprova.</span><span class="sxs-lookup"><span data-stu-id="d03a6-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d03a6-114">O administrador de contas a pagar verifica os recibos e os itens do relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d03a6-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d03a6-115">O proprietário do orçamento aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d03a6-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d03a6-116">Adicione vários elementos de aprovação, cada um com uma etapa.</span><span class="sxs-lookup"><span data-stu-id="d03a6-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d03a6-117">Por exemplo, você pode adicionar um elemento de aprovação separado para cada uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d03a6-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d03a6-118">O gerente do funcionário aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d03a6-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d03a6-119">O proprietário do orçamento aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d03a6-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]