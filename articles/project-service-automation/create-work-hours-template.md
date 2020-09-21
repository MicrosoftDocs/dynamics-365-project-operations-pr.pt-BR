---
title: Criar um modelo de horas de trabalho.
description: Como criar um modelo de horário de trabalho no Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749102"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="463ce-103">Criar um modelo de horário de trabalho (Project Service)</span><span class="sxs-lookup"><span data-stu-id="463ce-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="463ce-104">Para poder criar agendas de projetos, você precisa configurar um calendário de projeto que defina o número de horas de trabalho a serem acomodadas por dia na agenda e todos os feriados comerciais.</span><span class="sxs-lookup"><span data-stu-id="463ce-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="463ce-105">Você faz isso com um modelo de horário de trabalho, que contém detalhes sobre o horário de trabalho por dia, folgas e outros feriados comerciais.</span><span class="sxs-lookup"><span data-stu-id="463ce-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="463ce-106">Ao criar um projeto, você associa um modelo de trabalho ao calendário de projeto para aplicar a agenda ao projeto.</span><span class="sxs-lookup"><span data-stu-id="463ce-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="463ce-107">Há duas maneiras de criar um modelo de horário de trabalho:</span><span class="sxs-lookup"><span data-stu-id="463ce-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="463ce-108">Criar um modelo de horário de trabalho baseado no calendário do recurso.</span><span class="sxs-lookup"><span data-stu-id="463ce-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="463ce-109">Criar um novo modelo de horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="463ce-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="463ce-110">Para criar um modelo de horário de trabalho baseado no calendário do recurso</span><span class="sxs-lookup"><span data-stu-id="463ce-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="463ce-111">Vá para **Project Service > Recursos**.</span><span class="sxs-lookup"><span data-stu-id="463ce-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="463ce-112">Selecione o recurso no qual você deseja basear seu horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="463ce-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="463ce-113">Clique em **Salvar Calendário Como**, insira um nome para o modelo de horário de trabalho e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="463ce-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="463ce-114">Ao concluir a alteração das opções, clique em **Salvar e Fechar**.</span><span class="sxs-lookup"><span data-stu-id="463ce-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="463ce-115">Clique no botão **Salvar** no canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="463ce-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="463ce-116">Para criar um novo modelo de horário de trabalho</span><span class="sxs-lookup"><span data-stu-id="463ce-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="463ce-117">Vá para **Project Service > Modelos de Horário de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="463ce-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="463ce-118">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="463ce-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="463ce-119">Insira um nome para o modelo de horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="463ce-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="463ce-120">Selecione um recurso no qual basear o horário de trabalho e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="463ce-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="463ce-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="463ce-121">See Also</span></span>  
 [<span data-ttu-id="463ce-122">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="463ce-122">Set up resources</span></span>](../project-service/set-up-resources.md)
