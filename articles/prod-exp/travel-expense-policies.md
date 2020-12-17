---
title: Configurar políticas de despesas
description: Você pode configurar políticas de despesas que seus funcionários devem seguir ao inserir e enviar relatórios de despesas e requisições de viagem no Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650080"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="7383f-103">Configurar políticas de despesas</span><span class="sxs-lookup"><span data-stu-id="7383f-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7383f-104">Você pode definir políticas que seus funcionários devem seguir ao inserir e enviar relatórios de despesas e requisições de viagem.</span><span class="sxs-lookup"><span data-stu-id="7383f-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="7383f-105">A implementação de políticas de despesas pode ajudá-lo a gerenciar as despesas de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="7383f-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="7383f-106">Por exemplo, você pode definir uma política para despesas com hotel na cidade de Nova York, informando que a despesa por noite não pode exceder USD 250.</span><span class="sxs-lookup"><span data-stu-id="7383f-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="7383f-107">Se um funcionário enviar um relatório de despesas ou uma requisição de viagem em que a taxa de hospedagem exceda esse valor, o sistema notificará o</span><span class="sxs-lookup"><span data-stu-id="7383f-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="7383f-108">funcionário de que o valor da política para a despesa foi excedido.</span><span class="sxs-lookup"><span data-stu-id="7383f-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="7383f-109">Você pode configurar a mensagem que o funcionário receberá quando</span><span class="sxs-lookup"><span data-stu-id="7383f-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="7383f-110">definir a política.</span><span class="sxs-lookup"><span data-stu-id="7383f-110">define the policy.</span></span>      
        
<span data-ttu-id="7383f-111">É possível definir três tipos de políticas:</span><span class="sxs-lookup"><span data-stu-id="7383f-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="7383f-112">Aviso: permite que o funcionário envie um relatório de despesas ou uma requisição de viagem, mas a despesa será marcada para todos os aprovadores e</span><span class="sxs-lookup"><span data-stu-id="7383f-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="7383f-113">para relatórios posteriores.</span><span class="sxs-lookup"><span data-stu-id="7383f-113">for later reporting.</span></span>        

- <span data-ttu-id="7383f-114">Erro: exige que o funcionário revise as despesas para estar em conformidade com a política antes de enviar o relatório de despesas ou a requisição de viagem.</span><span class="sxs-lookup"><span data-stu-id="7383f-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="7383f-115">Justificativa: exige que o funcionário ou um gerente insira uma justificativa por exceder o valor da política antes de enviar o relatório de despesas ou a requisição de viagem.</span><span class="sxs-lookup"><span data-stu-id="7383f-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="7383f-116">Dicas de políticas</span><span class="sxs-lookup"><span data-stu-id="7383f-116">Policy tips</span></span>
<span data-ttu-id="7383f-117">Veja a seguir algumas sugestões que podem ajudá-lo na criação de novas políticas para o gerenciamento de despesas.</span><span class="sxs-lookup"><span data-stu-id="7383f-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="7383f-118">As políticas entram em vigor e não terão efeito se a política for criada com uma data posterior à data em que a despesa ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7383f-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="7383f-119">Por exemplo, se você estiver criando uma nova política hoje para impor uma despesa máxima de refeição de US$ 50, quaisquer despesas existentes inseridas até ontem não serão verificadas em relação a esta política.</span><span class="sxs-lookup"><span data-stu-id="7383f-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="7383f-120">Ao criar uma política para uma categoria de despesas que pode ser discriminada, considere adicionar uma condição para o tipo de linha de despesas.</span><span class="sxs-lookup"><span data-stu-id="7383f-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="7383f-121">Algumas políticas, como exigir um recibo, podem não fazer sentido para linhas discriminadas e devem ser aplicadas apenas à linha de cabeçalho ou a uma linha não detalhada.</span><span class="sxs-lookup"><span data-stu-id="7383f-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="7383f-122">As políticas de gerenciamento de despesas são avaliadas em relação à entidade de origem por padrão.</span><span class="sxs-lookup"><span data-stu-id="7383f-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="7383f-123">Para cenários intercompanhia, você pode definir a política a ser avaliada em relação à entidade de destino (entidade que toma o empréstimo).</span><span class="sxs-lookup"><span data-stu-id="7383f-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="7383f-124">Para executar as políticas em relação à entidade de destino, ative o recurso "Avaliar a Política de despesa em relação à entidade legal que toma o empréstimo" no espaço de trabalho **Gerenciamento de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="7383f-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="7383f-125">Quando avaliar as políticas</span><span class="sxs-lookup"><span data-stu-id="7383f-125">When to evaluate policies</span></span>

<span data-ttu-id="7383f-126">Nos parâmetros de gerenciamento de despesas, você pode escolher avaliar as políticas de gerenciamento de despesas quando uma linha for salva ou quando um relatório de despesas for enviado.</span><span class="sxs-lookup"><span data-stu-id="7383f-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="7383f-127">Se você optar por avaliar quando uma linha for salva, isso garante que os usuários terão uma visibilidade antecipada do que precisam fazer para preencher o relatório de despesas de uma vez.</span><span class="sxs-lookup"><span data-stu-id="7383f-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="7383f-128">Caso contrário, você pode atrasar a avaliação da política e economizar tempo validando no final, durante o envio para o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7383f-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
