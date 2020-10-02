---
title: Configurar fluxos de trabalho para gerenciamento de despesas
description: Você pode configurar um processo de fluxo de trabalho que é usado para analisar e aprovar documentos de viagens e despesas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896537"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="246d4-103">Configurar fluxos de trabalho para gerenciamento de despesas</span><span class="sxs-lookup"><span data-stu-id="246d4-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="246d4-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="246d4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="246d4-105">Você pode configurar um processo de fluxo de trabalho para analisar e aprovar documentos de viagens e despesas.</span><span class="sxs-lookup"><span data-stu-id="246d4-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="246d4-106">É possível definir fluxos de trabalho para relatórios de despesas, requisições de viagem e solicitações de adiantamento em dinheiro.</span><span class="sxs-lookup"><span data-stu-id="246d4-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="246d4-107">Um fluxo de trabalho representa um processo empresarial e define como um documento flui pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="246d4-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="246d4-108">O fluxo de trabalho também indica quem deve concluir uma tarefa ou aprovar um documento.</span><span class="sxs-lookup"><span data-stu-id="246d4-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="246d4-109">Há vários benefícios em usar o sistema de fluxo de trabalho na sua organização:</span><span class="sxs-lookup"><span data-stu-id="246d4-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="246d4-110">**Processos consistentes**: você pode definir o processo de aprovação para documentos específicos, como requisições de compra e relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="246d4-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="246d4-111">O uso do sistema de fluxo de trabalho ajuda a garantir que os documentos sejam processados e aprovados de maneira consistente e eficiente.</span><span class="sxs-lookup"><span data-stu-id="246d4-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="246d4-112">**Visibilidade de processos**: você pode rastrear o status, o histórico e as métricas de desempenho de uma instância de fluxo de trabalho específica.</span><span class="sxs-lookup"><span data-stu-id="246d4-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="246d4-113">Isso ajuda a determinar se é necessário fazer alterações no fluxo de trabalho para melhorar a eficiência.</span><span class="sxs-lookup"><span data-stu-id="246d4-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="246d4-114">**Lista de trabalho centralizada**: os usuários podem exibir uma lista de trabalho centralizada para visualizar as tarefas e aprovações do fluxo de trabalho atribuídas a eles.</span><span class="sxs-lookup"><span data-stu-id="246d4-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="246d4-115">Tipos de fluxo de trabalho</span><span class="sxs-lookup"><span data-stu-id="246d4-115">Workflow types</span></span>

<span data-ttu-id="246d4-116">A tabela a seguir lista os tipos de fluxo de trabalho que podem ser criados em **Gerenciamento de Despesas**.</span><span class="sxs-lookup"><span data-stu-id="246d4-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="246d4-117"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="246d4-118"><strong>Use este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="246d4-119"><strong>Aprovação automática de relatórios de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="246d4-120">Criar fluxos de trabalho de aprovação para relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="246d4-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="246d4-121"><strong>Lançamento automático de relatórios de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="246d4-122">Criar fluxos de trabalho de lançamento automático para relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="246d4-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="246d4-123"><strong>Item de linha de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="246d4-124">Criar fluxos de trabalho de aprovação para itens de linha em relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="246d4-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="246d4-125"><strong>Lançamento automático de item de linha de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="246d4-126">Criar fluxos de trabalho de lançamento automático para itens de linha em relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="246d4-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="246d4-127"><strong>Requisição de viagem</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="246d4-128">Criar fluxos de trabalho de aprovação para requisições de viagem.</span><span class="sxs-lookup"><span data-stu-id="246d4-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="246d4-129"><strong>Solicitação de adiantamento em dinheiro</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="246d4-130">Criar fluxos de trabalho de aprovação para solicitações de adiantamento em dinheiro.</span><span class="sxs-lookup"><span data-stu-id="246d4-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="246d4-131"><strong>Recuperação do imposto IVA</strong></span><span class="sxs-lookup"><span data-stu-id="246d4-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="246d4-132">Criar fluxos de trabalho de aprovação para a recuperação do imposto sobre valor agregado (IVA).</span><span class="sxs-lookup"><span data-stu-id="246d4-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
