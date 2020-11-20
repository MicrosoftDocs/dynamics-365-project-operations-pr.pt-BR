---
title: Definir políticas de despesas
description: Você pode definir políticas de despesas que seus funcionários devem seguir ao inserir e enviar relatórios de despesas e requisições de viagem.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128404"
---
# <a name="define-expense-policies"></a><span data-ttu-id="4d257-103">Definir políticas de despesas</span><span class="sxs-lookup"><span data-stu-id="4d257-103">Define expense policies</span></span>

<span data-ttu-id="4d257-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="4d257-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d257-105">Você pode definir políticas que seus funcionários devem seguir ao inserir e enviar relatórios de despesas e requisições de viagem.</span><span class="sxs-lookup"><span data-stu-id="4d257-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="4d257-106">A implementação de políticas de despesas pode ajudá-lo a gerenciar as despesas de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="4d257-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="4d257-107">Por exemplo, você pode definir uma política para despesas com hotel na cidade de Nova York, informando que a despesa por noite não pode exceder USD 250.</span><span class="sxs-lookup"><span data-stu-id="4d257-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="4d257-108">Se um funcionário enviar um relatório de despesas ou uma requisição de viagem em que a taxa de hospedagem exceda esse valor, o sistema notificará o</span><span class="sxs-lookup"><span data-stu-id="4d257-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="4d257-109">funcionário de que o valor da política para a despesa foi excedido.</span><span class="sxs-lookup"><span data-stu-id="4d257-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="4d257-110">Você pode configurar a mensagem que o funcionário receberá quando</span><span class="sxs-lookup"><span data-stu-id="4d257-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="4d257-111">definir a política.</span><span class="sxs-lookup"><span data-stu-id="4d257-111">define the policy.</span></span>      
        
<span data-ttu-id="4d257-112">É possível definir três tipos de políticas:</span><span class="sxs-lookup"><span data-stu-id="4d257-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="4d257-113">**Aviso**: permite que o funcionário envie um relatório de despesas ou uma requisição de viagem, mas a despesa será marcada para todos os aprovadores e</span><span class="sxs-lookup"><span data-stu-id="4d257-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="4d257-114">para relatórios posteriores.</span><span class="sxs-lookup"><span data-stu-id="4d257-114">for later reporting.</span></span>        

- <span data-ttu-id="4d257-115">**Erro**: exige que o funcionário revise as despesas para estar em conformidade com a política antes de enviar o relatório de despesas ou a requisição de viagem.</span><span class="sxs-lookup"><span data-stu-id="4d257-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="4d257-116">**Justificativa**: exige que o funcionário ou um gerente insira uma justificativa por exceder o valor da política antes de enviar o relatório de despesas ou a requisição de viagem.</span><span class="sxs-lookup"><span data-stu-id="4d257-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="4d257-117">Dicas de políticas</span><span class="sxs-lookup"><span data-stu-id="4d257-117">Policy tips</span></span>
<span data-ttu-id="4d257-118">Veja a seguir algumas sugestões que podem ajudá-lo na criação de novas políticas para o gerenciamento de despesas:</span><span class="sxs-lookup"><span data-stu-id="4d257-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="4d257-119">As políticas têm data de efetivação, o que significa que uma política não entrará em vigor se for criada com uma data posterior à data em que a despesa ocorreu.</span><span class="sxs-lookup"><span data-stu-id="4d257-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="4d257-120">Por exemplo, você cria uma nova política hoje para impor uma despesa máxima com refeição de USD 50.</span><span class="sxs-lookup"><span data-stu-id="4d257-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="4d257-121">Quaisquer despesas existentes inseridas até ontem não serão verificadas em relação a essa política.</span><span class="sxs-lookup"><span data-stu-id="4d257-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="4d257-122">Ao criar uma política para uma categoria de despesas que pode ser discriminada, considere adicionar uma condição para o tipo de linha de despesas.</span><span class="sxs-lookup"><span data-stu-id="4d257-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="4d257-123">Algumas políticas, como exigir um recibo, podem não fazer sentido para linhas discriminadas.</span><span class="sxs-lookup"><span data-stu-id="4d257-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="4d257-124">Nessa situação, a política é aplicada apenas à linha de cabeçalho ou a uma linha não discriminada.</span><span class="sxs-lookup"><span data-stu-id="4d257-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="4d257-125">As políticas de gerenciamento de despesas são avaliadas em relação à entidade de origem por padrão.</span><span class="sxs-lookup"><span data-stu-id="4d257-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="4d257-126">Para cenários intercompanhia, você pode definir a política a ser avaliada em relação à entidade de destino (entidade que toma o empréstimo).</span><span class="sxs-lookup"><span data-stu-id="4d257-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="4d257-127">Para executar as políticas em relação à entidade de destino, ative o recurso **Avaliar a Política de despesa em relação à entidade legal que toma o empréstimo** no espaço de trabalho **Gerenciamento de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="4d257-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="4d257-128">Quando avaliar as políticas</span><span class="sxs-lookup"><span data-stu-id="4d257-128">When to evaluate policies</span></span>

<span data-ttu-id="4d257-129">Nos parâmetros de gerenciamento de despesas, você pode escolher avaliar as políticas de gerenciamento de despesas quando uma linha for salva ou quando um relatório de despesas for enviado.</span><span class="sxs-lookup"><span data-stu-id="4d257-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="4d257-130">Se você optar por avaliar quando uma linha for salva, os usuários terão uma visibilidade antecipada do que precisam fazer para preencher o relatório de despesas de uma vez.</span><span class="sxs-lookup"><span data-stu-id="4d257-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="4d257-131">Caso contrário, você pode atrasar a avaliação da política e economizar tempo validando no final, durante o envio para o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d257-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
