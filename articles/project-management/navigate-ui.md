---
title: Navegando pela interface do usuário
description: Este tópico fornece informações sobre o gerenciamento de projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961815"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="54a3f-103">Navegando pela interface do usuário</span><span class="sxs-lookup"><span data-stu-id="54a3f-103">Navigating the user interface</span></span>

<span data-ttu-id="54a3f-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="54a3f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="54a3f-105">Visão Geral</span><span class="sxs-lookup"><span data-stu-id="54a3f-105">Overview</span></span>

<span data-ttu-id="54a3f-106">O formulário principal do projeto é separado em várias guias.</span><span class="sxs-lookup"><span data-stu-id="54a3f-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="54a3f-107">Cada guia representa um nível diferente de detalhe dentro do projeto.</span><span class="sxs-lookup"><span data-stu-id="54a3f-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="54a3f-108">**Resumo** : fornece uma descrição do projeto e agrega o desempenho planejado e real do projeto.</span><span class="sxs-lookup"><span data-stu-id="54a3f-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Guia Resumo e seus campos](media/navigation7.png)

- <span data-ttu-id="54a3f-110">**Tarefas** : fornece os detalhes sobre a estrutura de detalhamento de trabalho representada por uma visualização em grade, visualização em painel e um gantt.</span><span class="sxs-lookup"><span data-stu-id="54a3f-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Guia Tarefa e seus campos](media/navigation8.png)

- <span data-ttu-id="54a3f-112">**Equipe**: fornece detalhes sobre os participantes do projeto.</span><span class="sxs-lookup"><span data-stu-id="54a3f-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="54a3f-113">O esforço atribuído a cada membro da equipe também é resumido nesta visualização.</span><span class="sxs-lookup"><span data-stu-id="54a3f-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Guia Equipe e seus campos](media/navigation9.png)

- <span data-ttu-id="54a3f-115">**Atribuições de recursos**: fornece uma visão baseada em tempo do esforço para cada recurso em um projeto.</span><span class="sxs-lookup"><span data-stu-id="54a3f-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Guia Atribuições de recursos e seus campos](media/navigation10.png)

- <span data-ttu-id="54a3f-117">**Reconciliação de recursos** : fornece uma visão baseada no tempo das diferenças entre as atribuições de cada recurso nomeado e suas reservas.</span><span class="sxs-lookup"><span data-stu-id="54a3f-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Guia Reconciliação de recursos e seus campos](media/navigation11.png)

- <span data-ttu-id="54a3f-119">**Estimativas** : fornece uma visão baseada no tempo das estimativas de custo e vendas de um projeto.</span><span class="sxs-lookup"><span data-stu-id="54a3f-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Guia Estimativas e seus campos](media/navigation12.png)

- <span data-ttu-id="54a3f-121">**Rastreamento** : fornece uma visualização que mostra o progresso das tarefas na estrutura analítica do trabalho em relação a esforço, custo e vendas.</span><span class="sxs-lookup"><span data-stu-id="54a3f-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Guia Rastreamento e seus campos](media/navigation13.png)

- <span data-ttu-id="54a3f-123">**Vendas** : fornece links diretos para cotações e contratos associados ao projeto.</span><span class="sxs-lookup"><span data-stu-id="54a3f-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="54a3f-124">**Estimativas de despesas**: fornece uma grade que define as despesas do projeto com base nas categorias de despesas organizacionais.</span><span class="sxs-lookup"><span data-stu-id="54a3f-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Guia Estimativas de despesas e seus campos](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="54a3f-126">Controles de grade</span><span class="sxs-lookup"><span data-stu-id="54a3f-126">Grid controls</span></span>

<span data-ttu-id="54a3f-127">A seguir, veja uma visão geral dos controles comuns encontrados nas várias guias de planejamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="54a3f-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="54a3f-128">Atualizar</span><span class="sxs-lookup"><span data-stu-id="54a3f-128">Refresh</span></span>

<span data-ttu-id="54a3f-129">**Atualizar**: recupera os dados mais recentes do servidor se ocorrer alguma alteração após o carregamento da grade.</span><span class="sxs-lookup"><span data-stu-id="54a3f-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Botão Atualizar](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="54a3f-131">Agrupar por</span><span class="sxs-lookup"><span data-stu-id="54a3f-131">Group by</span></span>

<span data-ttu-id="54a3f-132">**Agrupar por**: atualiza o agrupamento das linhas na grade para indicar recursos, funções ou categorias com base nas necessidades do usuário.</span><span class="sxs-lookup"><span data-stu-id="54a3f-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Botão Agrupar por](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="54a3f-134">Anterior/Próximo</span><span class="sxs-lookup"><span data-stu-id="54a3f-134">Previous/Next</span></span>

<span data-ttu-id="54a3f-135">**Anterior**/**Próximo**: atualiza os períodos de tempo visíveis nas grades baseadas no tempo.</span><span class="sxs-lookup"><span data-stu-id="54a3f-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Botões Anterior e Próximo](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="54a3f-137">Escala de tempo</span><span class="sxs-lookup"><span data-stu-id="54a3f-137">Timescale</span></span>

<span data-ttu-id="54a3f-138">**Escala de tempo**: altere a agregação dos dados baseados no tempo entre dias, semanas, meses e anos.</span><span class="sxs-lookup"><span data-stu-id="54a3f-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Botão Escala de tempo](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="54a3f-140">Expandir</span><span class="sxs-lookup"><span data-stu-id="54a3f-140">Expand</span></span>

<span data-ttu-id="54a3f-141">**Expandir**: renderiza a grade visível em tela inteira, facilitando a visualização de funções adicionais.</span><span class="sxs-lookup"><span data-stu-id="54a3f-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Botão Expandir](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="54a3f-143">Tempo baseado em</span><span class="sxs-lookup"><span data-stu-id="54a3f-143">Time-phase by</span></span>

<span data-ttu-id="54a3f-144">**Tempo baseado em**: atualize o agrupamento das linhas na grade para refletir as estimativas de custo para estimativas de vendas.</span><span class="sxs-lookup"><span data-stu-id="54a3f-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="54a3f-145">Esse controle também aplica-se ao script de estimativa e à grade de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="54a3f-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Botão Tempo baseado em](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="54a3f-147">Adicionar coluna</span><span class="sxs-lookup"><span data-stu-id="54a3f-147">Add column</span></span>

<span data-ttu-id="54a3f-148">**Adicionar coluna**: permite ao usuário definir as colunas visíveis na grade.</span><span class="sxs-lookup"><span data-stu-id="54a3f-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="54a3f-149">Somente colunas de funcionalidade predefinida podem ser adicionadas às grades no formulário **Planejamento de projeto**.</span><span class="sxs-lookup"><span data-stu-id="54a3f-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Botão Adicionar coluna](media/navigation5.png)
