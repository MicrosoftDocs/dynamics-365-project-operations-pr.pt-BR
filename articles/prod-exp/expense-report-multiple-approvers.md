---
title: Vários aprovadores em um relatório de despesas
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação de várias pessoas.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071584"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="ddd7d-103">Vários aprovadores em um relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="ddd7d-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddd7d-104">Dependendo das políticas de aprovação de despesas da organização, talvez seja necessária a aprovação por mais de uma pessoa de um relatório de despesas enviado por um funcionário.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="ddd7d-105">Ao configurar o processo de fluxo de trabalho para aprovação de relatório de despesas, você pode adicionar elementos de fluxo de trabalho que incluem tarefas ou etapas para um ou mais aprovadores de relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="ddd7d-106">Por exemplo, você pode exigir que todos os relatórios de despesas sejam aprovados primeiro pelo gerente do funcionário que enviou o relatório e, depois, pelo coordenador de contas a pagar.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="ddd7d-107">Se você decidir exigir vários aprovadores de relatórios de despesas, poderá adicionar os elementos do fluxo de trabalho de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="ddd7d-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="ddd7d-108">Adicione um elemento de aprovação com uma etapa.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-108">Add one approval element that has one step.</span></span> <span data-ttu-id="ddd7d-109">Por exemplo, a etapa pode exigir que um relatório de despesas seja atribuído a um grupo de usuários e que seja aprovado por 50% dos membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="ddd7d-110">Adicione um elemento de aprovação com várias etapas.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="ddd7d-111">Por exemplo, o elemento de aprovação pode ter as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ddd7d-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="ddd7d-112">O gerente do funcionário que enviou o relatório de despesas o aprova.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="ddd7d-113">O administrador de contas a pagar verifica os recibos e os itens do relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="ddd7d-114">O proprietário do orçamento aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="ddd7d-115">Adicione vários elementos de aprovação, cada um com uma etapa.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="ddd7d-116">Por exemplo, você pode adicionar um elemento de aprovação separado para cada uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ddd7d-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="ddd7d-117">O gerente do funcionário aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="ddd7d-118">O proprietário do orçamento aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-118">The budget owner approves the expense report.</span></span>
