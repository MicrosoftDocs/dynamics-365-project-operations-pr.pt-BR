---
title: Modos de agendamento
description: Este tópico fornece informações sobre os modos de agendamento.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116693"
---
# <a name="scheduling-modes"></a><span data-ttu-id="a5cf6-103">Modos de agendamento</span><span class="sxs-lookup"><span data-stu-id="a5cf6-103">Scheduling modes</span></span>

<span data-ttu-id="a5cf6-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="a5cf6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a5cf6-105">O Dynamics 365 Project Operations oferece às organizações a possibilidade de definir como elas gerenciam mudanças nas principais variáveis em tarefas dentro da estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="a5cf6-106">Com base nas necessidades específicas da organização, os gerentes de projeto podem fazer alterações no modo de agendamento quando um projeto é criado.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="a5cf6-107">Existem três modos de agendamento disponíveis no Project Operations:</span><span class="sxs-lookup"><span data-stu-id="a5cf6-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="a5cf6-108">Duração fixa (este é o modo padrão)</span><span class="sxs-lookup"><span data-stu-id="a5cf6-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="a5cf6-109">Esforço fixo (*Trabalho*)</span><span class="sxs-lookup"><span data-stu-id="a5cf6-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="a5cf6-110">Unidades fixas</span><span class="sxs-lookup"><span data-stu-id="a5cf6-110">Fixed units</span></span>

<span data-ttu-id="a5cf6-111">Os valores afetados pela definição de um modo de agendamento específico são determinados pela seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="a5cf6-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="a5cf6-112">Esforço = Duração x Unidades</span><span class="sxs-lookup"><span data-stu-id="a5cf6-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="a5cf6-113">Ao definir o modo de agendamento de um projeto, você está definindo um desses valores, que não poderá ser alterado.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="a5cf6-114">Manter esse valor como uma constante coloca uma prioridade sobre esse valor, o que notifica o sistema para não alterá-lo quando os outros dois valores mudarem.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="a5cf6-115">A tabela a seguir fornece informações sobre os impactos da seleção de um modo específico.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="a5cf6-116">**Nesta tarefa**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-116">**In this task**</span></span>             | <span data-ttu-id="a5cf6-117">**Se você revisar as unidades**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-117">**If you revise units**</span></span>   | <span data-ttu-id="a5cf6-118">**Se você revisar a duração**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-118">**If you revise duration**</span></span> | <span data-ttu-id="a5cf6-119">**Se você revisar o esforço**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="a5cf6-120">Tarefa de unidades fixas</span><span class="sxs-lookup"><span data-stu-id="a5cf6-120">Fixed units task</span></span>     | <span data-ttu-id="a5cf6-121">A duração é recalculada.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-121">Duration is recalculated.</span></span> | <span data-ttu-id="a5cf6-122">O esforço é recalculado.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-122">Effort is recalculated.</span></span>    | <span data-ttu-id="a5cf6-123">A duração é recalculada.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="a5cf6-124">Tarefa de esforço fixo</span><span class="sxs-lookup"><span data-stu-id="a5cf6-124">Fixed effort task</span></span>    | <span data-ttu-id="a5cf6-125">A duração é recalculada.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-125">Duration is recalculated.</span></span> | <span data-ttu-id="a5cf6-126">As unidades são recalculadas.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-126">Units are recalculated.</span></span>    | <span data-ttu-id="a5cf6-127">A duração é recalculada.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="a5cf6-128">Tarefa de duração fixa</span><span class="sxs-lookup"><span data-stu-id="a5cf6-128">Fixed duration task</span></span>  | <span data-ttu-id="a5cf6-129">O esforço é recalculado.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-129">Effort is recalculated.</span></span>   | <span data-ttu-id="a5cf6-130">O esforço é recalculado.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-130">Effort is recalculated.</span></span>    | <span data-ttu-id="a5cf6-131">As unidades são recalculadas.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-131">Units are recalculated.</span></span>   |

<span data-ttu-id="a5cf6-132">Para obter mais informações sobre as implicações de um determinado modo, consulte [Alterar o tipo de tarefa para um agendamento mais preciso](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="a5cf6-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="a5cf6-133">No tópico, o termo **Trabalho** é usado em vez de **Esforço**.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="a5cf6-134">Alterar o modo de agendamento da organização</span><span class="sxs-lookup"><span data-stu-id="a5cf6-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="a5cf6-135">Conclua as etapas a seguir para definir o modo de agendamento de uma organização.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="a5cf6-136">Acesse **Configurações** \> **Geral** \> **Parâmetros** e, a seguir, selecione o parâmetro do projeto.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="a5cf6-137">Na página **Parâmetros do Projeto**, selecione o modo de agendamento padrão para a organização e defina a capacidade do gerente de projeto de substituir a configuração ao criar um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="a5cf6-138">Alterar a configuração do modo de agendamento em um projeto</span><span class="sxs-lookup"><span data-stu-id="a5cf6-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="a5cf6-139">Se uma organização permitir que o gerente de projeto substitua o modo de agendamento padrão, o gerente de projeto poderá fazer essa alteração ao criar um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="a5cf6-140">No entanto, depois que o projeto for salvo, o modo de agendamento não poderá ser alterado.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="a5cf6-141">Projetos copiados</span><span class="sxs-lookup"><span data-stu-id="a5cf6-141">Copied projects</span></span>

<span data-ttu-id="a5cf6-142">Como um projeto é criado quando a ação de cópia do projeto é executada, o gerente de projeto não pode definir o modo de agendamento.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="a5cf6-143">O projeto de destino sempre será padronizado para o modo definido no nível organizacional.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="a5cf6-144">Tarefas copiadas</span><span class="sxs-lookup"><span data-stu-id="a5cf6-144">Copied tasks</span></span>

<span data-ttu-id="a5cf6-145">Quando uma tarefa é copiada de um projeto para outro, a tarefa herda o modo de agendamento do projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
