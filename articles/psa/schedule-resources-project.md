---
title: Agendar recursos para um projeto
description: Como agendar recursos de um projeto no Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071634"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="d9461-103">Agendar recursos de um projeto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d9461-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d9461-104">Você pode verificar a disponibilidade dos recursos para obter uma visão geral das reservas já feitas ou filtrar a exibição por habilidades, equipe, localização e outras opções.</span><span class="sxs-lookup"><span data-stu-id="d9461-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="d9461-105">O painel de agendamento mostra a lista de recursos e sua disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d9461-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="d9461-106">Selecione um modo de exibição para exibir disponibilidade por **Horas** , **Dia** , **Semana** ou **Mês**.</span><span class="sxs-lookup"><span data-stu-id="d9461-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="d9461-107">Antes de usar o painel de agendamento, é importante configurá-lo.</span><span class="sxs-lookup"><span data-stu-id="d9461-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="d9461-108">Para obter mais informações, consulte [Configurar o painel de agendamento (Field Service ou Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="d9461-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="d9461-109">Se estiver usando uma versão mais antiga, para disponibilidade de recurso, consulte [Exibir a disponibilidade dos recursos](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="d9461-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="d9461-110">Para usar a funcionalidade de agendamento de registro de agenda, geocodificação, e serviços de localização, você precisa ligar os mapas.</span><span class="sxs-lookup"><span data-stu-id="d9461-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="d9461-111">No menu principal, selecione **Agendamento de Recursos** > **Administração**.</span><span class="sxs-lookup"><span data-stu-id="d9461-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="d9461-112">Clique em **Parâmetros de Agendamento**.</span><span class="sxs-lookup"><span data-stu-id="d9461-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="d9461-113">Abra o registro e role para baixo até a seção **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="d9461-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="d9461-114">No campo **Conectar aos mapas** , escolha **Sim**.</span><span class="sxs-lookup"><span data-stu-id="d9461-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="d9461-115">Aceite os termos e salve o registro.</span><span class="sxs-lookup"><span data-stu-id="d9461-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="d9461-116">No menu principal, selecione **Project Service** > **Painel de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="d9461-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="d9461-117">Aqui, existem diversas maneiras de agendar manualmente um requisito de reserva.</span><span class="sxs-lookup"><span data-stu-id="d9461-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="d9461-118">Selecione o método que funciona para você.</span><span class="sxs-lookup"><span data-stu-id="d9461-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="d9461-119">Localizar recursos disponíveis</span><span class="sxs-lookup"><span data-stu-id="d9461-119">Find available resources</span></span>

1.  <span data-ttu-id="d9461-120">Na lista **Requisito de Reserva** , clique com o botão direito do mouse em uma reserva não agendada e escolha uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="d9461-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="d9461-121">Escolha **Encontrar disponibilidade - Recursos atuais** para encontrar um recurso disponível da lista de painel de agendamento.</span><span class="sxs-lookup"><span data-stu-id="d9461-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="d9461-122">Escolha **Encontrar disponibilidade - Todos recursos** , para encontrar um recurso disponível dos recursos no sistema</span><span class="sxs-lookup"><span data-stu-id="d9461-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="d9461-123">Depois que você fizer isso, os filtros mostrarão as opções para o requisito de registro selecionado.</span><span class="sxs-lookup"><span data-stu-id="d9461-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="d9461-124">Quando você vir um slot disponível, clique com o botão direito do mouse no slot de tempo no painel de agendamento e escolha **Reservar Aqui**.</span><span class="sxs-lookup"><span data-stu-id="d9461-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="d9461-125">Ou, arrastar e soltar o requisito do registro para o slot de tempo disponível.</span><span class="sxs-lookup"><span data-stu-id="d9461-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="d9461-126">Registre um recurso usando a exibição diária e encontre quem está agendado</span><span class="sxs-lookup"><span data-stu-id="d9461-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="d9461-127">No painel de agendamento, selecione **Modo de exibição** e selecione **Dias**.</span><span class="sxs-lookup"><span data-stu-id="d9461-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="d9461-128">Isso mostra uma exibição em grade de quantas horas um recurso é agendado por dia e quais dias eles são livres.</span><span class="sxs-lookup"><span data-stu-id="d9461-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="d9461-129">Clique no nome do recurso que você deseja registrar, e selecione **Agendar**.</span><span class="sxs-lookup"><span data-stu-id="d9461-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="d9461-130">Na caixa de diálogo **Agendamento de recurso (criar)** , escolha o projeto que você deseja registrar o recurso ao longo com o método de agendamento e horário de início e fim.</span><span class="sxs-lookup"><span data-stu-id="d9461-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="d9461-131">Ao concluir, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="d9461-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="d9461-132">Exibir no painel de agendamento</span><span class="sxs-lookup"><span data-stu-id="d9461-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="d9461-133">Selecione o requisito de reserva não agendada da lista na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="d9461-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="d9461-134">Arraste a requisição de registro para um recurso/intervalo de tempo disponível no painel de agendamento.</span><span class="sxs-lookup"><span data-stu-id="d9461-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="d9461-135">Ao concluir, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="d9461-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="d9461-136">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="d9461-136">Additional resources</span></span>  
 [<span data-ttu-id="d9461-137">Guia do gerente de recursos</span><span class="sxs-lookup"><span data-stu-id="d9461-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
