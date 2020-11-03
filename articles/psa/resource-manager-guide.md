---
title: Guia do gerente de recursos
description: Um guia para gerenciamento de recurso no Project Service
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
ms.openlocfilehash: 4a26a384dfaf6b974ed35105434152e655ff6444
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071636"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="c965b-103">Guia do gerente de recurso (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c965b-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c965b-104">Os recursos do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ajudam você a encontrar os recursos certos na hora certa para o projeto certo e a verificar se todos os recursos são utilizados de maneira eficiente.</span><span class="sxs-lookup"><span data-stu-id="c965b-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="c965b-105">Implantar os consultores da empresa de modo eficiente e efetivo com [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="c965b-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="c965b-106">Esses recursos fornecem as ferramentas necessárias para agendar recursos com base nos requisitos e nas agendas dos projetos de consultoria e nas habilidades e na disponibilidade dos consultores.</span><span class="sxs-lookup"><span data-stu-id="c965b-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="c965b-107">Você pode localizar rapidamente os consultores mais qualificados disponíveis para trabalhar em projetos e ver facilmente como agendá-los melhor durante a duração do projeto.</span><span class="sxs-lookup"><span data-stu-id="c965b-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="c965b-108">O agendamento de recursos ajuda você a fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c965b-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="c965b-109">Corresponder os recursos aos projetos com base na melhor correspondência de seus níveis de habilidades e proficiências com os requisitos de recursos do projeto.</span><span class="sxs-lookup"><span data-stu-id="c965b-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="c965b-110">Corresponder a agenda de um recurso ao calendário de um projeto com base em sua disponibilidade e folgas agendadas.</span><span class="sxs-lookup"><span data-stu-id="c965b-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="c965b-111">O calendário codificado por cores fornece dicas visuais sobre a disponibilidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="c965b-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="c965b-112">Revise a capacidade de cada consultor e determine como a capacidade é usada no momento.</span><span class="sxs-lookup"><span data-stu-id="c965b-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="c965b-113">Isso pode ajudar a descobrir onde um consultor pode estar subutilizado ou superutilizado ou se ele está trabalhando na capacidade.</span><span class="sxs-lookup"><span data-stu-id="c965b-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="c965b-114">Atribuir uma porcentagem ou um número específico de horas à capacidade de um trabalhador para um projeto.</span><span class="sxs-lookup"><span data-stu-id="c965b-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="c965b-115">Fazer reservas de recursos de grupos.</span><span class="sxs-lookup"><span data-stu-id="c965b-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="c965b-116">Fazer reservas de recursos flexíveis ou fixas, e converter horas de reservas flexíveis para horas de reservas fixas em uma etapa.</span><span class="sxs-lookup"><span data-stu-id="c965b-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="c965b-117">Formar uma equipe de projeto automaticamente com base nos recursos definidos em uma estrutura de detalhamento de trabalho para um projeto.</span><span class="sxs-lookup"><span data-stu-id="c965b-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="c965b-118">Atender às solicitações dos recursos (reserve, proponha, localize recursos substitutos).</span><span class="sxs-lookup"><span data-stu-id="c965b-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="c965b-119">Atribua recursos de acordo com um modelo central (o gerente dos recursos atribui) ou híbrido (o gerente dos recursos e outros gerentes podem atribuir).</span><span class="sxs-lookup"><span data-stu-id="c965b-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="c965b-120">Para obter mais informações sobre como definir um modelo de gerenciamento de recursos central versus híbrido, consulte [Configurar as definições dos parâmetros adicionais (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c965b-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="c965b-121">Você pode gerenciar recursos de maneira eficiente entre projetos e garantir que os projetos sejam providos de recursos de maneira adequada.</span><span class="sxs-lookup"><span data-stu-id="c965b-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="c965b-122">Você precisará executar as tarefas a seguir:</span><span class="sxs-lookup"><span data-stu-id="c965b-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="c965b-123">[Gerenciar solicitações de recursos](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="c965b-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="c965b-124">Corresponder as habilidades e proficiências de seus consultores aos projetos certos.</span><span class="sxs-lookup"><span data-stu-id="c965b-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="c965b-125">[Exibir a disponibilidade de recursos](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="c965b-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="c965b-126">Verificar a disponibilidade dos consultores em uma exibição de calendário.</span><span class="sxs-lookup"><span data-stu-id="c965b-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="c965b-127">[Exibir a utilização de recursos](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="c965b-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="c965b-128">Ver a porcentagem de tempo que os consultores estão reservados no momento.</span><span class="sxs-lookup"><span data-stu-id="c965b-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="c965b-129">[Agendar recursos para um projeto](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="c965b-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="c965b-130">Agendar consultores para um projeto.</span><span class="sxs-lookup"><span data-stu-id="c965b-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="c965b-131">Para obter mais informações sobre o envio de solicitações de recursos para projetos individuais, consulte [Enviar solicitações de recursos](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="c965b-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c965b-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c965b-132">See Also</span></span>  
 <span data-ttu-id="c965b-133">[Visão geral do Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="c965b-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="c965b-134">[Guia do Administrador](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="c965b-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="c965b-135">[Guia do Gerente de Conta](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="c965b-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="c965b-136">[Guia do gerente de projeto](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="c965b-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="c965b-137">Guia de tempo, despesas e colaboração</span><span class="sxs-lookup"><span data-stu-id="c965b-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
