---
title: Reservar recursos nomeados usando requisitos do recurso
description: Este tópico fornece informações sobre como reservar recursos nomeados para um requisito de recurso genérico.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 50858d4fc55285b2e91117c6cbfb2419931b4197
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291020"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="d6450-103">Reservar recursos nomeados usando requisitos do recurso</span><span class="sxs-lookup"><span data-stu-id="d6450-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d6450-104">É possível reservar um recurso nomeado para substituir recurso genérico que tenha um requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="d6450-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="d6450-105">No PSA (Project Service Automation), na página **Projetos**, clique na guia **Equipe**.</span><span class="sxs-lookup"><span data-stu-id="d6450-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="d6450-106">Selecione na lista o recurso genérico com um requisito de recurso e clique em **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="d6450-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="d6450-107">Ou abra o requisito de recurso e clique em **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="d6450-107">Or, open the resource requirement and then click **Book**.</span></span>


![Reservando um membro de equipe genérico](media/RM-how-to-14.png)


3. <span data-ttu-id="d6450-109">Na página **Assistente de Agendamento**, selecione um recurso nomeado para reservar na equipe do seu projeto e clique em **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="d6450-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Reservando um membro de equipe genérico usando o assistente de agendamento](media/RM-how-to-15.png)

<span data-ttu-id="d6450-111">Quando a reserva é concluída e preenchida por um recurso nomeado, o recurso genérico é substituído pelo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="d6450-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Membro da equipe nomeado substituindo um membro da equipe genérico](media/RM-how-to-16.png)

<span data-ttu-id="d6450-113">As atribuições na agenda também são atualizadas com o recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="d6450-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Membro da equipe nomeado atribuído a tarefas do projeto](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="d6450-115">Preencher um recurso genérico com vários recursos nomeados</span><span class="sxs-lookup"><span data-stu-id="d6450-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="d6450-116">Atender a um requisito para um recurso genérico com vários recursos nomeados é semelhante a atribuir um único recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="d6450-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="d6450-117">Por exemplo, há uma tarefa com uma duração de cinco dias e 120 horas de esforço.</span><span class="sxs-lookup"><span data-stu-id="d6450-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="d6450-118">Essa tarefa não pode ser concluída por um recurso que trabalha um dia comum de oito horas em uma semana de cinco dias.</span><span class="sxs-lookup"><span data-stu-id="d6450-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Uma tarefa que precisa de 120 horas de esforço em cinco dias](media/RM-how-to-21.png)

<span data-ttu-id="d6450-120">O requisito é de 120 horas de engenharia robótica por cinco dias, o que significa 24 horas por dia.</span><span class="sxs-lookup"><span data-stu-id="d6450-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Requisito por dia](media/RM-how-to-22.png)

<span data-ttu-id="d6450-122">Este é um exemplo de quando vários recursos nomeados são necessários para atender a uma solicitação de recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="d6450-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="d6450-123">Você precisará reservar vários recursos para atender ao requisito.</span><span class="sxs-lookup"><span data-stu-id="d6450-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Reservando vários recursos para atender ao requisito](media/RM-how-to-23.png)

<span data-ttu-id="d6450-125">A principal diferença neste cenário é que o recurso genérico permanece na equipe atribuída à tarefa e os membros da equipe de recurso nomeados reservados não são atribuídos como parte da posição.</span><span class="sxs-lookup"><span data-stu-id="d6450-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="d6450-126">O gerente de projeto pode atribuir o trabalho conforme apropriado aos recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="d6450-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="d6450-127">A exibição **Reconciliação** pode ajudar um gerente de projeto na divisão de reservas entre vários recursos para atribuições de tarefa.</span><span class="sxs-lookup"><span data-stu-id="d6450-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="d6450-128">Isso não é feito automaticamente porque em qualquer cenário mais complicado do que o exemplo simples acima, em que você tem um pacote de tarefas, por exemplo, compondo o requisito, a intenção de como o gerente de projeto quer atribuir, precisa ser pressuposta pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="d6450-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="d6450-129">Como o sistema não pode entender a intenção, as chances são de que as suposições sejam diferentes das intencionadas e de que o resultado seja incorreto ou imprevisível.</span><span class="sxs-lookup"><span data-stu-id="d6450-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="d6450-130">O resultado previsível é que o recurso genérico permaneça atribuído até que o gerente de projeto crie atribuições deliberadamente, com a ajuda da exibição **Reconciliação**.</span><span class="sxs-lookup"><span data-stu-id="d6450-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]