---
title: Fluxo de trabalho de gerenciamento de despesas
description: Este tópico explica como você pode usar o sistema de fluxo de trabalho no Microsoft Dynamics 365 Finance para configurar um processo de revisão para relatórios de despesas no gerenciamento de despesas.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005192"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="4eaf0-103">Fluxo de trabalho de gerenciamento de despesas</span><span class="sxs-lookup"><span data-stu-id="4eaf0-103">Expense management workflow</span></span>

<span data-ttu-id="4eaf0-104">Você pode usar o sistema de fluxo de trabalho para configurar um processo de revisão para relatórios de despesas no gerenciamento de despesas.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="4eaf0-105">Você pode configurar um fluxo de trabalho que usa os seguintes critérios para determinar quem aprova os relatórios de despesas:</span><span class="sxs-lookup"><span data-stu-id="4eaf0-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="4eaf0-106">A hierarquia de relatórios de funcionários e limites de aprovação predefinidos</span><span class="sxs-lookup"><span data-stu-id="4eaf0-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="4eaf0-107">Aprovação em vários níveis que dá suporte a aprovadores provisórios e um aprovador final</span><span class="sxs-lookup"><span data-stu-id="4eaf0-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="4eaf0-108">Dimensões financeiras e responsabilidade do projeto</span><span class="sxs-lookup"><span data-stu-id="4eaf0-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="4eaf0-109">Atribuição a usuários ou grupos de usuários específicos</span><span class="sxs-lookup"><span data-stu-id="4eaf0-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="4eaf0-110">As aprovações de fluxo de trabalho podem ser criadas para relatórios de despesas, requisições de viagem, adiantamentos de dinheiro e recuperação de imposto de valor agregado (IVA).</span><span class="sxs-lookup"><span data-stu-id="4eaf0-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="4eaf0-111">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="4eaf0-111">**Example**</span></span>

<span data-ttu-id="4eaf0-112">O processo a seguir é um exemplo do fluxo de trabalho de gerenciamento de despesas para um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="4eaf0-113">Um funcionário cria e salva um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="4eaf0-114">O funcionário envia o relatório de despesas para aprovação.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="4eaf0-115">O aprovador é identificado com base nas regras definidas quando o fluxo de trabalho foi configurado.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="4eaf0-116">O aprovador recebe uma notificação de que um relatório de despesas está pronto para aprovação.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="4eaf0-117">O aprovador analisa o relatório de despesas e verifica se as seguintes condições foram atendidas:</span><span class="sxs-lookup"><span data-stu-id="4eaf0-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="4eaf0-118">As despesas não violam políticas de despesas.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="4eaf0-119">Se uma despesa violar uma política, o aprovador verificará se o relatório de despesas inclui uma justificativa comercial válida.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="4eaf0-120">Os recibos eletrônicos são anexados ao relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="4eaf0-121">O aprovador aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="4eaf0-122">O relatório de despesas é atribuído ao coordenador de contas a pagar para postagem.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="4eaf0-123">Uma das seguintes etapas ocorre, dependendo se a postagem automática está configurada:</span><span class="sxs-lookup"><span data-stu-id="4eaf0-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="4eaf0-124">Se a postagem automática estiver configurado, o relatório de despesas será processado para pagamento e o status do relatório de despesas será atualizado.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="4eaf0-125">Se a postagem automática não estiver configurada, o coordenador de contas a pagar verificará se todos os recibos originais foram enviados e se os recibos estão alinhados com as despesas no relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="4eaf0-126">Todos os códigos de imposto inseridos no relatório de despesas também devem ser verificados como corretos.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="4eaf0-127">Após a verificação desses requisitos, o relatório de despesas é postado.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="4eaf0-128">Depois que o relatório de despesas é postado, o pagamento é autorizado para o relatório de despesas e o funcionário é reembolsado.</span><span class="sxs-lookup"><span data-stu-id="4eaf0-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]