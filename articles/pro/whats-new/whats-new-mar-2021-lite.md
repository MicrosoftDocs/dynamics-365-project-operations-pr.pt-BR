---
title: Novidades em março de 2021 – implantação lite do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de março de 2021 da implantação lite do Project Operations.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499974"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="fd799-103">Novidades em março de 2021 – implantação lite do Project Operations</span><span class="sxs-lookup"><span data-stu-id="fd799-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="fd799-104">_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="fd799-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fd799-105">Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="fd799-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="fd799-106">Project Operations no ambiente do Dataverse versão 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="fd799-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="fd799-107">Atualizações de qualidade</span><span class="sxs-lookup"><span data-stu-id="fd799-107">Quality updates</span></span>

| <span data-ttu-id="fd799-108">**Área do recurso**</span><span class="sxs-lookup"><span data-stu-id="fd799-108">**Feature area**</span></span> | <span data-ttu-id="fd799-109">**Número de referência**</span><span class="sxs-lookup"><span data-stu-id="fd799-109">**Reference number**</span></span> | <span data-ttu-id="fd799-110">**Atualização de qualidade**</span><span class="sxs-lookup"><span data-stu-id="fd799-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fd799-111">Cobrança e preço</span><span class="sxs-lookup"><span data-stu-id="fd799-111">Billing and pricing</span></span> | <span data-ttu-id="fd799-112">2133873</span><span class="sxs-lookup"><span data-stu-id="fd799-112">2133873</span></span> | <span data-ttu-id="fd799-113">Corrigida a exibição do símbolo da moeda **Preço Unitário de Venda** na grade **Estimativas de Despesas**.</span><span class="sxs-lookup"><span data-stu-id="fd799-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="fd799-114">Cobrança e preço</span><span class="sxs-lookup"><span data-stu-id="fd799-114">Billing and pricing</span></span> | <span data-ttu-id="fd799-115">2174616</span><span class="sxs-lookup"><span data-stu-id="fd799-115">2174616</span></span> | <span data-ttu-id="fd799-116">Ao ganhar uma cotação, a lista de preços personalizada do contrato é referenciada nos detalhes da linha de contrato que são copiados da cotação.</span><span class="sxs-lookup"><span data-stu-id="fd799-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="fd799-117">Gerenciamento de Oportunidades</span><span class="sxs-lookup"><span data-stu-id="fd799-117">Opportunity Management</span></span> | <span data-ttu-id="fd799-118">2167475</span><span class="sxs-lookup"><span data-stu-id="fd799-118">2167475</span></span> | <span data-ttu-id="fd799-119">Valor de imposto fixo na fatura de correção que originou uma entrada real não faturada.</span><span class="sxs-lookup"><span data-stu-id="fd799-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="fd799-120">Gerenciamento de Oportunidades</span><span class="sxs-lookup"><span data-stu-id="fd799-120">Opportunity Management</span></span> | <span data-ttu-id="fd799-121">2176285</span><span class="sxs-lookup"><span data-stu-id="fd799-121">2176285</span></span> | <span data-ttu-id="fd799-122">O valor do imposto não deve ser copiado dos detalhes da linha do contrato de venda/cotação para os detalhes da linha do contrato de custo/cotação.</span><span class="sxs-lookup"><span data-stu-id="fd799-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="fd799-123">Gerenciamento de Oportunidades</span><span class="sxs-lookup"><span data-stu-id="fd799-123">Opportunity Management</span></span> | <span data-ttu-id="fd799-124">2188079</span><span class="sxs-lookup"><span data-stu-id="fd799-124">2188079</span></span> | <span data-ttu-id="fd799-125">A regra de divisão de cobrança não deve ser criada para contratos que não sejam baseados no trabalho.</span><span class="sxs-lookup"><span data-stu-id="fd799-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="fd799-126">Planejamento e acompanhamento</span><span class="sxs-lookup"><span data-stu-id="fd799-126">Planning and Tracking</span></span> | <span data-ttu-id="fd799-127">2138853</span><span class="sxs-lookup"><span data-stu-id="fd799-127">2138853</span></span> | <span data-ttu-id="fd799-128">Função de cópia do projeto atualizada para garantir que as linhas de estimativa de despesa que fazem referência às tarefas sejam copiadas para o projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="fd799-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="fd799-129">Planejamento e acompanhamento</span><span class="sxs-lookup"><span data-stu-id="fd799-129">Planning and Tracking</span></span> | <span data-ttu-id="fd799-130">2173259</span><span class="sxs-lookup"><span data-stu-id="fd799-130">2173259</span></span> | <span data-ttu-id="fd799-131">Função de cópia do projeto atualizada para garantir que ela não exiba a mensagem de erro **Copiando WBS** em determinados cenários.</span><span class="sxs-lookup"><span data-stu-id="fd799-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="fd799-132">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="fd799-132">Time and Expense</span></span> | <span data-ttu-id="fd799-133">2148910</span><span class="sxs-lookup"><span data-stu-id="fd799-133">2148910</span></span> | <span data-ttu-id="fd799-134">Corrigido o problema de exibição com a página **Editar Entrada** na grade **Entrada de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="fd799-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="fd799-135">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="fd799-135">Time and Expense</span></span> | <span data-ttu-id="fd799-136">2159798</span><span class="sxs-lookup"><span data-stu-id="fd799-136">2159798</span></span> | <span data-ttu-id="fd799-137">Controles mais rígidos para garantir que as entradas de despesas aprovadas não possam ser editadas.</span><span class="sxs-lookup"><span data-stu-id="fd799-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |

