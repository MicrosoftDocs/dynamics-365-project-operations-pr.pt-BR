---
title: Reservar para um projeto
description: Este tópico fornece informações sobre como reservar um recurso em um projeto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071280"
---
# <a name="book-to-a-project"></a><span data-ttu-id="3d00e-103">Reservar para um projeto</span><span class="sxs-lookup"><span data-stu-id="3d00e-103">Book to a project</span></span>

<span data-ttu-id="3d00e-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="3d00e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3d00e-105">Há momentos em que um Gerente de projeto ou Gerente de recursos precisará alocar um recurso a um projeto sem um requisito específico definido por um membro genérico da equipe.</span><span class="sxs-lookup"><span data-stu-id="3d00e-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="3d00e-106">Isso pode ser realizado de três formas.</span><span class="sxs-lookup"><span data-stu-id="3d00e-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="3d00e-107">Reservar da grade de membros da equipe</span><span class="sxs-lookup"><span data-stu-id="3d00e-107">Book from the team member grid</span></span>
- <span data-ttu-id="3d00e-108">Reservar no painel de agendamento</span><span class="sxs-lookup"><span data-stu-id="3d00e-108">Book from the schedule board</span></span>
- <span data-ttu-id="3d00e-109">Reservar no formulário **Projeto**</span><span class="sxs-lookup"><span data-stu-id="3d00e-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="3d00e-110">Reservar da grade de membros da equipe</span><span class="sxs-lookup"><span data-stu-id="3d00e-110">Book from the team member grid</span></span>

<span data-ttu-id="3d00e-111">Se a sua organização estiver operando no modo de Alocação de recursos híbrido, o Gerente de projeto pode reservar um recurso diretamente para o projeto ao concluir as seguintes etapas.</span><span class="sxs-lookup"><span data-stu-id="3d00e-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="3d00e-112">No projeto, vá para a grade de membros da equipe e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="3d00e-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="3d00e-113">Defina o nome da posição e a função do recurso.</span><span class="sxs-lookup"><span data-stu-id="3d00e-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="3d00e-114">Selecione o recurso reservável da pesquisa disponível.</span><span class="sxs-lookup"><span data-stu-id="3d00e-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="3d00e-115">Depois de selecionar o recurso, defina as seguintes informações de campo para reservar o recurso:</span><span class="sxs-lookup"><span data-stu-id="3d00e-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="3d00e-116">Data de Início</span><span class="sxs-lookup"><span data-stu-id="3d00e-116">Start date</span></span>
    - <span data-ttu-id="3d00e-117">Data de término</span><span class="sxs-lookup"><span data-stu-id="3d00e-117">Finish date</span></span>
    - <span data-ttu-id="3d00e-118">Método de alocação</span><span class="sxs-lookup"><span data-stu-id="3d00e-118">Allocation method</span></span>
    - <span data-ttu-id="3d00e-119">Horas, se aplicável</span><span class="sxs-lookup"><span data-stu-id="3d00e-119">Hours, if applicable</span></span>
    - <span data-ttu-id="3d00e-120">Aprovador do projeto</span><span class="sxs-lookup"><span data-stu-id="3d00e-120">Project approver</span></span>

6. <span data-ttu-id="3d00e-121">Selecione **Salvar e Fechar**</span><span class="sxs-lookup"><span data-stu-id="3d00e-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="3d00e-122">Reservar no painel de agendamento</span><span class="sxs-lookup"><span data-stu-id="3d00e-122">Book from the schedule board</span></span>

<span data-ttu-id="3d00e-123">Quando um Gerente de recursos precisa reservar um recurso diretamente para um projeto, é possível usar o quadro de agendamento e os requisitos do projeto.</span><span class="sxs-lookup"><span data-stu-id="3d00e-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="3d00e-124">Os requisitos do projeto é um requisito de recurso que está sempre disponível para reserva.</span><span class="sxs-lookup"><span data-stu-id="3d00e-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="3d00e-125">Para reservar diretamente em um projeto do quadro de agendamento, execute as seguintes etapas.</span><span class="sxs-lookup"><span data-stu-id="3d00e-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="3d00e-126">Navegue até o quadro de agendamento e na página à esquerda, filtre os recursos que está considerando para o requisito.</span><span class="sxs-lookup"><span data-stu-id="3d00e-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="3d00e-127">No painel inferior, selecione a guia **Projeto** para exibir uma lista de requisitos do projeto.</span><span class="sxs-lookup"><span data-stu-id="3d00e-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="3d00e-128">Arraste o requisito até um recurso e defina as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="3d00e-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="3d00e-129">Data de Início</span><span class="sxs-lookup"><span data-stu-id="3d00e-129">Start date</span></span>
    - <span data-ttu-id="3d00e-130">Data de término</span><span class="sxs-lookup"><span data-stu-id="3d00e-130">Finish date</span></span>
    - <span data-ttu-id="3d00e-131">Status da reserva</span><span class="sxs-lookup"><span data-stu-id="3d00e-131">Booking status</span></span>
    - <span data-ttu-id="3d00e-132">Método de reserva</span><span class="sxs-lookup"><span data-stu-id="3d00e-132">Booking method</span></span>
    - <span data-ttu-id="3d00e-133">Duração</span><span class="sxs-lookup"><span data-stu-id="3d00e-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="3d00e-134">Reservar no formulário Projeto</span><span class="sxs-lookup"><span data-stu-id="3d00e-134">Book from the Project form</span></span>

<span data-ttu-id="3d00e-135">Como Gerente de projeto, talvez seja necessário reservar um recurso para um projeto, mas conhecer apenas os critérios em vez do nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3d00e-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="3d00e-136">Execute as seguintes etapas para usar o assistente de agendamento para encontrar um recurso baseado em quaisquer atributos disponíveis do recurso.</span><span class="sxs-lookup"><span data-stu-id="3d00e-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="3d00e-137">Navegue até o projeto e selecione **Reservar** para abrir o Assistente de Agendamento.</span><span class="sxs-lookup"><span data-stu-id="3d00e-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="3d00e-138">Usando os filtros do lado esquerdo do Assistente de Agendamento, restrinja os critérios e selecione **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="3d00e-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="3d00e-139">Com base nos recursos retornados nos resultados, é possível reservar um recurso.</span><span class="sxs-lookup"><span data-stu-id="3d00e-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="3d00e-140">Esse método não cria reservas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="3d00e-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="3d00e-141">Em vez disso, adiciona o recurso à equipe.</span><span class="sxs-lookup"><span data-stu-id="3d00e-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="3d00e-142">Depois que o membro da equipe tiver sido adicionado ao projeto, o gerente do projeto poderá manter reservas ou estender reservas para adicionar as reservas necessárias ao recurso.</span><span class="sxs-lookup"><span data-stu-id="3d00e-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
