---
title: Gerenciar fusos horários
description: Quando um projeto é criado, seu fuso horário é baseado no fuso horário definido no modelo de hora de trabalho aplicado.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997722"
---
# <a name="manage-time-zones"></a><span data-ttu-id="1306c-103">Gerenciar fusos horários</span><span class="sxs-lookup"><span data-stu-id="1306c-103">Manage time zones</span></span>

<span data-ttu-id="1306c-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="1306c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="1306c-105">Projetos</span><span class="sxs-lookup"><span data-stu-id="1306c-105">Projects</span></span>

<span data-ttu-id="1306c-106">Quando um projeto é criado, o fuso horário é baseado no fuso horário definido no modelo de hora de trabalho aplicado.</span><span class="sxs-lookup"><span data-stu-id="1306c-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="1306c-107">No **Projeto**, as datas são sempre relativas ao fuso horário do usuário que está conectado em cada guia, exceto a guia **Tarefa**. Quando você visualiza a estrutura de detalhamento de trabalho, as datas sempre serão exibidas no fuso horário do projeto.</span><span class="sxs-lookup"><span data-stu-id="1306c-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="1306c-108">Tarefas</span><span class="sxs-lookup"><span data-stu-id="1306c-108">Tasks</span></span>

<span data-ttu-id="1306c-109">Quando uma tarefa é criada, a hora de início, hora de término e horas/dia são controlados pelas horas de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="1306c-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="1306c-110">Por exemplo, se uma tarefa for criada com um projeto cujo fuso horário é -8 PST e tem as seguintes horas de trabalho: 9h00 às 17h00 de segunda a sexta-feira, qualquer tarefa criada sem uma atribuição respeitará a hora de início e hora de término do calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="1306c-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="1306c-111">Gerenciar recursos com fusos horários</span><span class="sxs-lookup"><span data-stu-id="1306c-111">Manage resources with time zones</span></span>

<span data-ttu-id="1306c-112">Para obter resultados precisos e previsíveis ao usar **Estender reserva**, há dois pré-requisitos principais que devem ser atendidos:</span><span class="sxs-lookup"><span data-stu-id="1306c-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="1306c-113">O usuário deve configurar o fuso horário de seu dispositivo para corresponder ao fuso horário definido nas **Configurações de personalização** do sistema.</span><span class="sxs-lookup"><span data-stu-id="1306c-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Configurações de fuso horário no Windows 10](media/reconcile-assignments-03.png)

  ![Configurações de fuso horário nas configurações de personalização](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="1306c-116">O recurso reservável deve ter pelo menos um minuto de tempo de trabalho que se sobreponha aos contornos usados para definir a extensão solicitada.</span><span class="sxs-lookup"><span data-stu-id="1306c-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="1306c-117">Por exemplo, os seguintes recursos com horários de trabalho entre 9h00 e 19h00.</span><span class="sxs-lookup"><span data-stu-id="1306c-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Comparação de contornos de recursos](media/reconcile-assignments-05.png)

<span data-ttu-id="1306c-119">As listas de tabela a seguir mostra:</span><span class="sxs-lookup"><span data-stu-id="1306c-119">The following table shows:</span></span>

- <span data-ttu-id="1306c-120">Um modelo de calendário de projeto</span><span class="sxs-lookup"><span data-stu-id="1306c-120">A project calendar template</span></span>
- <span data-ttu-id="1306c-121">Recurso A: este recurso tem o mesmo calendário e está no mesmo fuso horário do projeto.</span><span class="sxs-lookup"><span data-stu-id="1306c-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="1306c-122">O horário de início das reservas será 9:00.</span><span class="sxs-lookup"><span data-stu-id="1306c-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="1306c-123">Recurso B: este recurso está localizado em um fuso horário diferente do projeto e começa às 7h00 em seu fuso horário.</span><span class="sxs-lookup"><span data-stu-id="1306c-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="1306c-124">No entanto, as reservas começarão às 9h, já que é o horário de início mais cedo do contorno da tarefa.</span><span class="sxs-lookup"><span data-stu-id="1306c-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="1306c-125">Recursos C e D: os recursos estão localizados em fusos horários diferentes, ambos diferentes uns dos outros e do projeto, e suas reservas não começam antes de seus respectivos horários de início disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1306c-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="1306c-126">Entidade</span><span class="sxs-lookup"><span data-stu-id="1306c-126">Entity</span></span>  |<span data-ttu-id="1306c-127">Calendário</span><span class="sxs-lookup"><span data-stu-id="1306c-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="1306c-128">Modelo de calendário de projeto</span><span class="sxs-lookup"><span data-stu-id="1306c-128">Project calendar template</span></span>   | ![calendário de projeto](media/reconcile-assignments-06.png) |
|<span data-ttu-id="1306c-130">Recurso A</span><span class="sxs-lookup"><span data-stu-id="1306c-130">Resource A</span></span>  | ![Calendário do Recurso A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="1306c-132">Recurso B</span><span class="sxs-lookup"><span data-stu-id="1306c-132">Resource B</span></span>  |  ![Calendário do Recurso B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="1306c-134">Recurso C</span><span class="sxs-lookup"><span data-stu-id="1306c-134">Resource C</span></span>  |  ![Calendário do Recurso C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="1306c-136">Recurso D</span><span class="sxs-lookup"><span data-stu-id="1306c-136">Resource D</span></span>  | ![Calendário do Recurso D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="1306c-138">Quando você navegar até a exibição **Reconciliação**, as atribuições de recursos e as faltas de reserva associadas são exibidas.</span><span class="sxs-lookup"><span data-stu-id="1306c-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Exibição de reconciliação antes da extensão](media/reconcile-assignments-10.png)

<span data-ttu-id="1306c-140">Depois que a funcionalidade de reserva estendida tiver sido usada para cada recurso, as reservas são estendidas com êxito para cada recurso porque as horas de trabalho de cada recurso corresponderam aos contornos da falta.</span><span class="sxs-lookup"><span data-stu-id="1306c-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Exibição de reconciliação após a extensão da reserva](media/reconcile-assignments-11.png) 

<span data-ttu-id="1306c-142">Observe que uma análise mais detalhada dos detalhes das reservas mostra diferenças na hora de início das reservas.</span><span class="sxs-lookup"><span data-stu-id="1306c-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="1306c-143">As reservas não começam antes da hora de início do contorno da atribuição nem antes da hora de início disponível do recurso.</span><span class="sxs-lookup"><span data-stu-id="1306c-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Novas reservas de recursos no quadro de horários](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]