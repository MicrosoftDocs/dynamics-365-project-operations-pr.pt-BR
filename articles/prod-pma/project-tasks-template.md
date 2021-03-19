---
title: Sincronizar tarefas de projetos diretamente do Project Service Automation para o Finance and Operations
description: Este tópico descreve o modelo e a tarefa subjacente usada para sincronizar tarefas de projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288905"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="35243-103">Sincronizar tarefas de projetos diretamente do Project Service Automation para o Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="35243-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="35243-104">Este tópico descreve o modelo e a tarefa subjacente usada para sincronizar tarefas de projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="35243-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="35243-105">A integração de tarefas de projeto, as categorias de transação de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.</span><span class="sxs-lookup"><span data-stu-id="35243-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="35243-106">Se você estiver usando a Enterprise Edition 7.3.0, após instalar o KB 4132657 e o KB 4132660, será possível usar os modelos para integrar as tarefas de projeto, as categorias de transação, as estimativas de horas, as estimativas de despesas e os dados reais, além de configurar o bloqueio de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="35243-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="35243-107">Se você precisar redefinir as distribuições de contabilidade, recomendamos que você também instale o KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="35243-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="35243-108">A integração dos valores reais está disponível na versão 8.0.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="35243-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="35243-109">Fluxo de dados do Project Service Automation para o Finance</span><span class="sxs-lookup"><span data-stu-id="35243-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="35243-110">A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Project Service Automation e do Finance.</span><span class="sxs-lookup"><span data-stu-id="35243-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="35243-111">O modelo de integração disponível com o recurso de integração de dados permite transferir dados sobre tarefas de projeto do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="35243-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="35243-112">A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="35243-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="35243-113">[![Fluxo de dados para a integração do Project Service Automation ao Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="35243-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="35243-114">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="35243-114">Template and task</span></span>

<span data-ttu-id="35243-115">Para acessar o modelo, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="35243-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="35243-116">O seguinte modelo e as tarefa subjacente são usados para sincronizar tarefas do projeto do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="35243-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="35243-117">**Nome do modelo na integração de dados:** Tarefas do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="35243-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="35243-118">**Nome da tarefa no projeto:** Tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="35243-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="35243-119">Antes de que as tarefas de projeto possam ser realizadas, você deve sincronizar contratos de projeto e projetos.</span><span class="sxs-lookup"><span data-stu-id="35243-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="35243-120">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="35243-120">Entity set</span></span>

| <span data-ttu-id="35243-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="35243-121">Project Service Automation</span></span> | <span data-ttu-id="35243-122">Financeiro</span><span class="sxs-lookup"><span data-stu-id="35243-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="35243-123">Tarefas do Projeto</span><span class="sxs-lookup"><span data-stu-id="35243-123">Project Tasks</span></span>              | <span data-ttu-id="35243-124">Entidade de integração para tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="35243-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="35243-125">Fluxo da entidade</span><span class="sxs-lookup"><span data-stu-id="35243-125">Entity flow</span></span>

<span data-ttu-id="35243-126">As tarefas de projeto são gerenciadas no Project Service Automation e são sincronizadas com o Finance como atividades de projeto.</span><span class="sxs-lookup"><span data-stu-id="35243-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="35243-127">Pré-requisitos e configuração de mapeamento</span><span class="sxs-lookup"><span data-stu-id="35243-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="35243-128">Antes de que as tarefas de projeto possam ser realizadas, você deve sincronizar contratos de projeto e projetos.</span><span class="sxs-lookup"><span data-stu-id="35243-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="35243-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="35243-129">Power Query</span></span>

<span data-ttu-id="35243-130">Você deverá usar o Microsoft Power Query para Excel para filtrar dados se essa condição for atendida:</span><span class="sxs-lookup"><span data-stu-id="35243-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="35243-131">Você tem registros específicos de recursos em uma tarefa de projeto.</span><span class="sxs-lookup"><span data-stu-id="35243-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="35243-132">Se você precisar usar o Power Query, siga esta diretriz:</span><span class="sxs-lookup"><span data-stu-id="35243-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="35243-133">O modelo de tarefas do projeto (PSA para Fin e Ops) tem um filtro padrão que exclui registros específicos de recursos de uma tarefa do projeto, definindo o filtro em **IsLineTask** como **Falso**.</span><span class="sxs-lookup"><span data-stu-id="35243-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="35243-134">Se você criar seu próprio modelo, deverá adicionar esse filtro.</span><span class="sxs-lookup"><span data-stu-id="35243-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="35243-135">Mapeamento de modelos na integração de dados</span><span class="sxs-lookup"><span data-stu-id="35243-135">Template mapping in Data integration</span></span>

<span data-ttu-id="35243-136">A ilustração a seguir mostra um exemplo de mapeamentos de tarefas do modelo na integração de dados.</span><span class="sxs-lookup"><span data-stu-id="35243-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="35243-137">O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="35243-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="35243-138">[![Mapeamento de modelo](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="35243-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]