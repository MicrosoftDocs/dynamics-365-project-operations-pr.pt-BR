---
title: Atendimento a requisitos de recursos genéricos
description: Este tópico fornece informações sobre como reservar recursos nomeados para um requisito de recurso genérico.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e36875a0d5dcb24d9669e2ea989c6fc7db7bcd7c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005822"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="5deef-103">Atendimento a requisitos de recursos genéricos</span><span class="sxs-lookup"><span data-stu-id="5deef-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="5deef-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="5deef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5deef-105">É possível reservar um recurso nomeado para substituir recurso genérico que tenha um requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="5deef-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="5deef-106">Na página **Projetos**, selecione a guia **Equipe**.</span><span class="sxs-lookup"><span data-stu-id="5deef-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="5deef-107">Selecione o recurso genérico com um requisito de recurso na lista e selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="5deef-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="5deef-108">Ou abra o requisito de recurso e selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="5deef-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="5deef-109">Na página **Assistente de Agendamento**, selecione um recurso nomeado para reservar na equipe do projeto e selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="5deef-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="5deef-110">Quando a reserva é concluída e preenchida por um recurso nomeado, o recurso genérico é substituído pelo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="5deef-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="5deef-111">As atribuições na agenda também são atualizadas com o recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="5deef-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="5deef-112">Preencher um recurso genérico com vários recursos nomeados</span><span class="sxs-lookup"><span data-stu-id="5deef-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="5deef-113">Atender a um requisito para um recurso genérico com vários recursos nomeados é semelhante a atribuir um único recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="5deef-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="5deef-114">Por exemplo, há uma tarefa com uma duração de cinco dias e 120 horas de esforço.</span><span class="sxs-lookup"><span data-stu-id="5deef-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="5deef-115">Essa tarefa não pode ser concluída por um recurso que trabalha em um dia comum de oito horas em uma semana de cinco dias.</span><span class="sxs-lookup"><span data-stu-id="5deef-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="5deef-116">O requisito é de 120 horas de engenharia robótica por cinco dias, o que significa 24 horas por dia.</span><span class="sxs-lookup"><span data-stu-id="5deef-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="5deef-117">Este é um exemplo de quando vários recursos nomeados são necessários para atender a uma solicitação de recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="5deef-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="5deef-118">Você precisará reservar vários recursos para atender ao requisito.</span><span class="sxs-lookup"><span data-stu-id="5deef-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="5deef-119">A principal diferença neste cenário é que o recurso genérico permanece na equipe atribuída à tarefa e os membros da equipe de recurso nomeados reservados não são atribuídos como parte da posição.</span><span class="sxs-lookup"><span data-stu-id="5deef-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="5deef-120">O gerente de projeto pode atribuir o trabalho conforme apropriado aos recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="5deef-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="5deef-121">A exibição **Reconciliação** pode ajudar um gerente de projeto na divisão de reservas entre vários recursos para atribuições de tarefa.</span><span class="sxs-lookup"><span data-stu-id="5deef-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="5deef-122">Isso não é feito automaticamente porque em qualquer cenário mais complicado do que o exemplo simples acima, como quando você tem um pacote de tarefas compondo o requisito ou a intenção de como o gerente de projeto deseja atribuir, isso precisa ser pressuposto pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="5deef-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="5deef-123">Como o sistema não pode entender a intenção, é provável que as suposições sejam diferentes das pretensões e um resultado incorreto ou imprevisível seja obtido.</span><span class="sxs-lookup"><span data-stu-id="5deef-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="5deef-124">O resultado previsível é que o recurso genérico permaneça atribuído até que o gerente de projeto crie atribuições deliberadamente, com a ajuda da exibição **Reconciliação**.</span><span class="sxs-lookup"><span data-stu-id="5deef-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]