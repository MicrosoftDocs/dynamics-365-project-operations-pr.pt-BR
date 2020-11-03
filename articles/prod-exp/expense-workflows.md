---
title: Configurar fluxos de trabalho para gerenciamento de despesas
description: Você pode configurar um processo de fluxo de trabalho para analisar e aprovar documentos de viagens e despesas.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071582"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="c3282-103">Configurar fluxos de trabalho para gerenciamento de despesas</span><span class="sxs-lookup"><span data-stu-id="c3282-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3282-104">Você pode configurar um processo de fluxo de trabalho que é usado para analisar e aprovar documentos de viagens e despesas.</span><span class="sxs-lookup"><span data-stu-id="c3282-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="c3282-105">Os documentos para os quais fluxos de trabalho podem ser definidos incluem relatórios de despesas, requisições de viagem e solicitações de adiantamento em dinheiro.</span><span class="sxs-lookup"><span data-stu-id="c3282-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="c3282-106">Um fluxo de trabalho representa um processo empresarial.</span><span class="sxs-lookup"><span data-stu-id="c3282-106">A workflow represents a business process.</span></span> <span data-ttu-id="c3282-107">Ele define como um documento flui pelo sistema e indica quem deve concluir uma tarefa ou aprovar um documento.</span><span class="sxs-lookup"><span data-stu-id="c3282-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="c3282-108">Há vários benefícios em usar o sistema de fluxo de trabalho na sua organização:</span><span class="sxs-lookup"><span data-stu-id="c3282-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="c3282-109">**Processos consistentes** — você pode definir o processo de aprovação para documentos específicos, como requisições de compra e relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="c3282-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="c3282-110">O uso do sistema de fluxo de trabalho ajuda a garantir que documentos sejam processados e aprovados de maneira consistente e eficiente.</span><span class="sxs-lookup"><span data-stu-id="c3282-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="c3282-111">Visibilidade de processos — você pode rastrear o status, o histórico e as métricas de desempenho de uma instância de fluxo de trabalho específica.</span><span class="sxs-lookup"><span data-stu-id="c3282-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="c3282-112">Isso ajuda a determinar se é necessário fazer alterações no fluxo de trabalho para melhorar a eficiência.</span><span class="sxs-lookup"><span data-stu-id="c3282-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="c3282-113">Lista de trabalho centralizada — os usuários podem exibir uma lista de trabalho centralizada para exibir as tarefas e aprovações do fluxo de trabalho atribuídas a eles.</span><span class="sxs-lookup"><span data-stu-id="c3282-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="c3282-114">**Os tipos de fluxos de trabalho que você pode criar**</span><span class="sxs-lookup"><span data-stu-id="c3282-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="c3282-115">A tabela a seguir lista os tipos de fluxos de trabalho que podem ser criados em **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="c3282-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="c3282-116"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="c3282-117"><strong>Use este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="c3282-118"><strong>Relatório de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="c3282-119">Criar fluxos de trabalho de aprovação para relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="c3282-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="c3282-120"><strong>Lançamento automático de relatórios de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="c3282-121">Criar fluxos de trabalho de lançamento automático para relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="c3282-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="c3282-122"><strong>Item de linha de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="c3282-123">Criar fluxos de trabalho de aprovação para itens de linha em relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="c3282-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="c3282-124"><strong>Lançamento automático de item de linha de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="c3282-125">Criar fluxos de trabalho de lançamento automático para itens de linha em relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="c3282-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="c3282-126"><strong>Requisição de viagem</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="c3282-127">Criar fluxos de trabalho de aprovação para requisições de viagem.</span><span class="sxs-lookup"><span data-stu-id="c3282-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="c3282-128"><strong>Solicitação de adiantamento em dinheiro</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="c3282-129">Criar fluxos de trabalho de aprovação para solicitações de adiantamento em dinheiro.</span><span class="sxs-lookup"><span data-stu-id="c3282-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="c3282-130"><strong>Recuperação do imposto IVA</strong></span><span class="sxs-lookup"><span data-stu-id="c3282-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="c3282-131">Criar fluxos de trabalho de aprovação para a recuperação do imposto sobre valor agregado (IVA).</span><span class="sxs-lookup"><span data-stu-id="c3282-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

