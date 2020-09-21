---
title: Visão geral do Project Service Automation
description: Este tópico fornece informações sobre o Dynamics 365 Project Service Automation para a solução de integração do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749097"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="f79a9-103">Visão geral do Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f79a9-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f79a9-104">A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Dynamics 365 Finance e do Dynamics 365 Project Service Automation por meio do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f79a9-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="f79a9-105">Os modelos de integração disponíveis com o recurso de integração de dados permitem transferir fluxo de projeto, contratos de projetos, linhas de contrato de projetos, etapas da linha de contrato de projeto, tarefas de projeto, categorias de transação de despesas, estimativa de horas e estimativa de despesas do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="f79a9-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="f79a9-106">Se estiver usando a versão 7.3.0, você precisará instalar o KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="f79a9-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="f79a9-107">Você poderá então integrar projetos de preço fixo.</span><span class="sxs-lookup"><span data-stu-id="f79a9-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="f79a9-108">Se você estiver usando a versão 7.3.0 e estiver transferindo as transações de taxa do Project Service Automation, instale o KB 4345320 para incluir essas taxas na fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="f79a9-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="f79a9-109">Se você estiver usando a versão 8.0, você será capaz de usar a integração de tarefas de projeto, as categorias de transação de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="f79a9-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="f79a9-110">Se estiver usando a versão 8.0.1 ou posterior, você poderá sincronizar dados reais.</span><span class="sxs-lookup"><span data-stu-id="f79a9-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="f79a9-111">Antes de poder integrar o Project Service Automation Finance, você deve configurar os parâmetros de integração do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f79a9-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="f79a9-112">Para obter mais informações, consulte [Parâmetros de integração do Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f79a9-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="f79a9-113">Esta solução de integração permite a sincronização direta nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="f79a9-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="f79a9-114">Manter contratos de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.</span><span class="sxs-lookup"><span data-stu-id="f79a9-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f79a9-115">Criar projetos no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.</span><span class="sxs-lookup"><span data-stu-id="f79a9-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f79a9-116">Manter linhas de contrato de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.</span><span class="sxs-lookup"><span data-stu-id="f79a9-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f79a9-117">Manter etapas de linhas de contrato de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.</span><span class="sxs-lookup"><span data-stu-id="f79a9-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f79a9-118">Manter tarefas de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.</span><span class="sxs-lookup"><span data-stu-id="f79a9-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f79a9-119">Manter categorias de transação de despesas no Finance e sincronizá-los diretamente do Finance para o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f79a9-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="f79a9-120">Criar estimativas de hora de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.</span><span class="sxs-lookup"><span data-stu-id="f79a9-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f79a9-121">Criar estimativas de despesas de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.</span><span class="sxs-lookup"><span data-stu-id="f79a9-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f79a9-122">Criar horas do projeto, despesas e taxas efetivas no Project Service Automation e criar transações do projeto no diário de integração do Project Service Automation para que possam ser postadas em Finance.</span><span class="sxs-lookup"><span data-stu-id="f79a9-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="f79a9-123">Sincronização de dados</span><span class="sxs-lookup"><span data-stu-id="f79a9-123">Data synchronization</span></span>

<span data-ttu-id="f79a9-124">A ilustração a seguir mostra como os dados são sincronizados como parte da integração entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="f79a9-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="f79a9-125">Nem todos os modelos estão disponíveis atualmente.</span><span class="sxs-lookup"><span data-stu-id="f79a9-125">Not all templates are currently available.</span></span> <span data-ttu-id="f79a9-126">Os modelos serão lançados assim que forem concluídos.</span><span class="sxs-lookup"><span data-stu-id="f79a9-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="f79a9-127">[![Integração do Project Service Automation ao Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="f79a9-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="f79a9-128">Requisitos de sistema para finanças</span><span class="sxs-lookup"><span data-stu-id="f79a9-128">System requirements for Finance</span></span>

<span data-ttu-id="f79a9-129">Para usar a solução de integração Project Service Automation to Finance, você deve instalar Enterprise Edition 7.3 com atualização 12 da plataforma ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f79a9-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="f79a9-130">Requisitos do sistema para Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f79a9-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="f79a9-131">Para usar a solução de integração Project Service Automation to Finance, você deve instalar os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="f79a9-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="f79a9-132">Dynamics 365 Project Service Automation versão 9.0.0.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f79a9-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="f79a9-133">Solução de perspectiva de caixa para o Dynamics 365 Sales, versão 1.14.0.0 (v14) ou posterior</span><span class="sxs-lookup"><span data-stu-id="f79a9-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="f79a9-134">Automação de serviços de projeto para solução de finanças para Dynamics 365 Project Service Automation versão 1.0.0.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f79a9-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="f79a9-135">Instale a solução de integração do Project Service Automation para o Finance em sua instância do Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f79a9-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="f79a9-136">Baixe a solução de integração de Project Service Automation to Finance em [Centro de Download da Microsoft ](https://www.microsoft.com/download/details.aspx?id=57016) e siga as instruções que acompanham a solução.</span><span class="sxs-lookup"><span data-stu-id="f79a9-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
