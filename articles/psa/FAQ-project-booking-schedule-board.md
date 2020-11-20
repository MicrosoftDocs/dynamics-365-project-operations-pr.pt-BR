---
title: Criar uma reserva de projeto no Quadro de Agendamento
description: Este tópico fornece informações sobre como criar uma reserva de projeto no quadro de agendamento.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122284"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="fc0df-103">Criar uma reserva de projeto no Quadro de Agendamento</span><span class="sxs-lookup"><span data-stu-id="fc0df-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="fc0df-104">É possível reservar um recurso em um projeto diretamente na guia **Equipe** do projeto ou gerando um requisito de recurso em uma atribuição de membro da equipe genérico e, em seguida, atendendo ao requisito com um membro da equipe de projeto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="fc0df-105">Você também pode reservar um recurso em um projeto diretamente no Quadro de Agendamento.</span><span class="sxs-lookup"><span data-stu-id="fc0df-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="fc0df-106">Isso pode ser feito de três maneiras:</span><span class="sxs-lookup"><span data-stu-id="fc0df-106">There are three ways to do this:</span></span>

- <span data-ttu-id="fc0df-107">**Fazer uma reserva em um requisito de recurso gerado:** você pode gerar um requisito de recurso depois de criar um recurso genérico e atribuir tarefas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="fc0df-108">**Fazer reserva no requisito principal:** os requisitos principais são mostrados no Quadro de agendamento da guia **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="fc0df-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="fc0df-109">**Fazer reserva em um novo requisito de recurso:** você pode criar um requisito de recurso do zero e associá-lo a um projeto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="fc0df-110">No Quadro de Agendamento, o requisito de recurso é exibido na guia **Requisitos em Aberto**.</span><span class="sxs-lookup"><span data-stu-id="fc0df-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="fc0df-111">Fazer uma reserva em um requisito de recurso gerado</span><span class="sxs-lookup"><span data-stu-id="fc0df-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="fc0df-112">É possível criar um recurso genérico e atribuí-lo a uma ou várias tarefas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="fc0df-113">Em seguida, você pode gerar um requisito de recurso de um membro da equipe genérico.</span><span class="sxs-lookup"><span data-stu-id="fc0df-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="fc0df-114">No Quadro de Agendamento, esse recurso será exibido na guia **Requisitos em Aberto** . Talvez seja necessário usar filtros de coluna na grade se você tiver muitos requisitos em aberto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="fc0df-115">![Guia Abrir Requisitos no painel Agendar](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de tela da tabela de reservas e atribuições")</span><span class="sxs-lookup"><span data-stu-id="fc0df-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="fc0df-116">Selecione o requisito.</span><span class="sxs-lookup"><span data-stu-id="fc0df-116">Select the requirement.</span></span> <span data-ttu-id="fc0df-117">A guia **Localizar Disponibilidade** aparecerá na parte superior da linha selecionada.</span><span class="sxs-lookup"><span data-stu-id="fc0df-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="fc0df-118">Quando você seleciona a guia, o modo Assistente de Agendamento do Quadro de Agendamento é aberto e filtra os recursos disponíveis que atendem ao requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="fc0df-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="fc0df-119">Depois disso, você pode reservar um recurso.</span><span class="sxs-lookup"><span data-stu-id="fc0df-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="fc0df-120">Você também pode arrastar e soltar a linha selecionada da parte inferior do Quadro de Agendamento até uma célula do recurso na grade acima.</span><span class="sxs-lookup"><span data-stu-id="fc0df-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="fc0df-121">Quando você soltá-lo, o painel **Criar reserva de recursos** abrirá à direita.</span><span class="sxs-lookup"><span data-stu-id="fc0df-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="fc0df-122">A seleção de **Reservar** reserva o recurso na equipe de projeto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-122">Selecting **Book** books the resource onto the project team.</span></span>

![Painel Criar Reserva de Recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="fc0df-124">Fazer reserva no Requisito principal</span><span class="sxs-lookup"><span data-stu-id="fc0df-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="fc0df-125">A criação de um projeto no Project Service cria automaticamente um requisito de recurso chamado Requisito principal.</span><span class="sxs-lookup"><span data-stu-id="fc0df-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="fc0df-126">Esse é um requisito vazio usado para reservar rapidamente um recurso com o Quadro de Agendamento sem precisar gerar um requisito nem criar um do zero.</span><span class="sxs-lookup"><span data-stu-id="fc0df-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="fc0df-127">Como o requisito está vazio, será necessário especificar as datas, bem como o método e as horas de alocação, se aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="fc0df-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="fc0df-128">Para reservar um recurso com o Requisito Principal, no Quadro de Agendamento, selecione a guia **Projeto**. Talvez seja necessário usar o filtro de coluna na coluna **Projeto** se você tiver muitos projetos.</span><span class="sxs-lookup"><span data-stu-id="fc0df-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="fc0df-129">![Filtros de coluna no painel Agendar](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de tela da tabela de reservas e atribuições")</span><span class="sxs-lookup"><span data-stu-id="fc0df-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="fc0df-130">Selecione o requisito que tem somente o nome do projeto como seu nome e uma duração de zero (0).</span><span class="sxs-lookup"><span data-stu-id="fc0df-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="fc0df-131">Selecione a guia **Localizar disponibilidade** que é exibida na linha.</span><span class="sxs-lookup"><span data-stu-id="fc0df-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="fc0df-132">Isso coloca o Quadro de Agendamento no modo Assistente de Agendamento e mostra os recursos disponíveis que podem ser reservados no projeto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="fc0df-133">Como um **Requisito Principal** é um requisito vazio com zero (0) de duração, será necessário definir a duração no painel **Criar Reserva de Recursos** ao selecionar e reservar um recurso.</span><span class="sxs-lookup"><span data-stu-id="fc0df-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="fc0df-134">Você também pode selecionar o **Requisito principal do projeto** na parte inferior do Quadro de Agendamento e arrastá-lo e soltá-lo em um recurso para reservá-lo.</span><span class="sxs-lookup"><span data-stu-id="fc0df-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="fc0df-135">Como o **Requisito Principal** é um requisito vazio que tem duração zero (0), será necessário definir a duração no painel **Criar Reserva de Recursos** ao selecionar e reservar um recurso.</span><span class="sxs-lookup"><span data-stu-id="fc0df-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="fc0df-136">Ao reservar um recurso por meio do **Requisito Principal** no Quadro de Agendamento, você o adiciona à equipe do projeto sem nenhuma atribuição.</span><span class="sxs-lookup"><span data-stu-id="fc0df-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="fc0df-137">Fazer reserva em um novo requisito de recurso</span><span class="sxs-lookup"><span data-stu-id="fc0df-137">Book from a new resource requirement</span></span>
<span data-ttu-id="fc0df-138">Complete as etapas a seguir para fazer uma reserva de um novo requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="fc0df-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="fc0df-139">Vá para **Requisitos de Recurso** e selecione **Novo** para criar um novo requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="fc0df-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="fc0df-140">Na guia **Projeto**, selecione um projeto para associar o requisito ao projeto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="fc0df-141">No Quadro de Agendamento, esse novo requisito é mostrado como um **Requisito em Aberto** que você pode atender.</span><span class="sxs-lookup"><span data-stu-id="fc0df-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="fc0df-142">Reserve o recurso para adicioná-lo à equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="fc0df-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="fc0df-143">Agora que o recurso está reservado, é preciso atribuir tarefas manualmente.</span><span class="sxs-lookup"><span data-stu-id="fc0df-143">Now that the resource is booked, you must assign tasks manually.</span></span>

