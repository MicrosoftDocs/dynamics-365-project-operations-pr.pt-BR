---
title: Gerenciar projetos e reservas no seu calendário do Office 365
description: Como gerenciar projetos e reservas no seu calendário do Office 365
author: ruhercul
manager: kfend
ms.service: project-operations
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 1df4864ca8dbf6948ca88a7c82a6c0a676e3bd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275029"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="93183-103">Gerenciar projetos e reservas em seu calendário (Project Service)</span><span class="sxs-lookup"><span data-stu-id="93183-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="93183-104">PRETERIDO: esse recurso foi preterido e não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="93183-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="93183-105">Exibir compromissos pessoais, reservas de trabalho de projeto, e atribuições de ordem de serviço do Field Service usando o calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="93183-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="93183-106">Com tudo em um local, é fácil gerenciar seu dia.</span><span class="sxs-lookup"><span data-stu-id="93183-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="93183-107">Suas reuniões, compromissos, reservas e tarefas estão disponíveis em seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="93183-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="93183-108">Se você estiver usando [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], você também pode inserir seus compromissos pessoais na visualização de entrada de tempo do Project Service.</span><span class="sxs-lookup"><span data-stu-id="93183-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="93183-109">Isso permite que os gerentes de projeto saibam sua disponibilidade para projetos.</span><span class="sxs-lookup"><span data-stu-id="93183-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="93183-110">Isso também poupa tempo, porque não precisa inserir informações sobre seus compromissos pessoais duas vezes.</span><span class="sxs-lookup"><span data-stu-id="93183-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="93183-111">Você pode simplesmente importar seus compromissos do calendário e projetar exibição para a entrada de tempo do Project Service.</span><span class="sxs-lookup"><span data-stu-id="93183-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="93183-112">Seu calendário sincronizará os registros de pedido de trabalho e projeto nas próximas quatro semanas.</span><span class="sxs-lookup"><span data-stu-id="93183-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="93183-113">Essa configuração não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="93183-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="93183-114">A sincronização funciona somente de uma forma, do PSA para o calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="93183-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="93183-115">Você pode sincronizar na ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="93183-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="93183-116">Para saber como usar seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] , consulte [Calendário no Outlook na Web para negócios](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span><span class="sxs-lookup"><span data-stu-id="93183-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="93183-117">Configuração</span><span class="sxs-lookup"><span data-stu-id="93183-117">Setup</span></span>  
 <span data-ttu-id="93183-118">Antes de poder ver e gerenciar as reservas em seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], será necessário configurar algumas coisas.</span><span class="sxs-lookup"><span data-stu-id="93183-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="93183-119">Você precisará ter as credenciais de Administrador Global ou Administrador do Sistema do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="93183-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="93183-120">O Admin precisará configurar o perfil do servidor de email, e cada usuário precisará configurar sua caixa de e-mail.</span><span class="sxs-lookup"><span data-stu-id="93183-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="93183-121">[Configurar o processamento de email por meio da sincronização no servidor](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span><span class="sxs-lookup"><span data-stu-id="93183-121">[Set up email processing through server-side synchronization](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="93183-122">Ativar a sincronização para sua organização do (tarefa de administrador)</span><span class="sxs-lookup"><span data-stu-id="93183-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="93183-123">No menu principal, clique em **Configurações** > **Administração**.</span><span class="sxs-lookup"><span data-stu-id="93183-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="93183-124">Clique em **Configurações do Sistema**.</span><span class="sxs-lookup"><span data-stu-id="93183-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="93183-125">Clique na guia **Sincronização**.</span><span class="sxs-lookup"><span data-stu-id="93183-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="93183-126">Em **Selecionar habilitar sincronização do registro de recurso com**, marque **Sincronizar registro de recurso com Outlook**.</span><span class="sxs-lookup"><span data-stu-id="93183-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="93183-127">Ative a sincronização para seu perfil de usuário (tarefa de usuário)</span><span class="sxs-lookup"><span data-stu-id="93183-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="93183-128">Clique no botão **Configurações** no canto superior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="93183-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="93183-129">Clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="93183-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="93183-130">Clique na guia **Sincronização**.</span><span class="sxs-lookup"><span data-stu-id="93183-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="93183-131">Em **Sincronização de recursos com Outlook**, marque **Sincronizar registro de recurso com Outlook**.</span><span class="sxs-lookup"><span data-stu-id="93183-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="93183-132">Importar seus compromissos pessoais (tarefa de usuário)</span><span class="sxs-lookup"><span data-stu-id="93183-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="93183-133">Somente é possível importar seus compromissos do calendário e projetar exibição para a entrada do tempo de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="93183-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="93183-134">Abra o calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] e clique em **Importar dados**.</span><span class="sxs-lookup"><span data-stu-id="93183-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="93183-135">Na tela Filtros, selecione **Compromissos para troca** e então clique em **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="93183-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="93183-136">O sistema colocará os compromissos na exibição de entrada de tempo com as entradas sugeridas da semana atual.</span><span class="sxs-lookup"><span data-stu-id="93183-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="93183-137">Para adicionar entradas de outra semana, clique em **Anterior** ou **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="93183-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="93183-138">Selecione o compromisso que deseja adicionar à exibição de entrada do tempo de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="93183-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="93183-139">Na caixa pop-up **Entrada de hora**, selecione as opções apropriadas para converter o compromisso para uma exibição de entrada do tempo de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="93183-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="93183-140">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="93183-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="93183-141">Consulte também</span><span class="sxs-lookup"><span data-stu-id="93183-141">See Also</span></span>  
 [<span data-ttu-id="93183-142">Guia de tempo, despesas e colaboração</span><span class="sxs-lookup"><span data-stu-id="93183-142">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]