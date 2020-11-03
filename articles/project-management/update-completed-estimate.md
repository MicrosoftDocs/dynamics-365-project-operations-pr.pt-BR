---
title: Atualizar estimativa ao término
description: Este tópico fornece informações sobre como atualizar a projeção de esforço em um projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071611"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="f25bc-103">Atualizar estimativa ao término</span><span class="sxs-lookup"><span data-stu-id="f25bc-103">Update estimate at completion</span></span>

<span data-ttu-id="f25bc-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="f25bc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f25bc-105">É comum que um gerente de projetos revise as estimativas originais em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="f25bc-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="f25bc-106">As reprojeções de projetos são a percepção de um gerente de projetos sobre as estimativas, considerando o estado atual de um projeto.</span><span class="sxs-lookup"><span data-stu-id="f25bc-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="f25bc-107">No entanto, não é recomendável que os gerentes de projetos alterem os números da linha de base, pois a linha de base do projeto representa a fonte de referência estabelecida para a estimativa de custo e de agenda dele e todos os participantes do projeto concordaram com ela.</span><span class="sxs-lookup"><span data-stu-id="f25bc-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="f25bc-108">Um gerente de projetos pode reprojetar o esforço em tarefas de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="f25bc-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="f25bc-109">Substituindo a estimativa até a conclusão (ETC) padrão por uma nova estimativa do esforço restante real na tarefa.</span><span class="sxs-lookup"><span data-stu-id="f25bc-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="f25bc-110">Substituindo a porcentagem de progresso padrão por uma nova estimativa do verdadeiro progresso na tarefa.</span><span class="sxs-lookup"><span data-stu-id="f25bc-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="f25bc-111">Cada uma dessas abordagens causa o recálculo de ETC, estimativa ao término (EAT), porcentagem de progresso e variação de esforço projetada da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f25bc-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="f25bc-112">A EAT, a ETC e a porcentagem de progresso nas tarefas de resumo são recalculadas e produzem uma nova projeção da variação de esforço.</span><span class="sxs-lookup"><span data-stu-id="f25bc-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
