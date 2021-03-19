---
title: Reservar requisitos de forma flexível
description: Este tópico fornece informações sobre como reservar requisitos de forma flexível.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282904"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="08a77-103">Reservar requisitos de forma flexível</span><span class="sxs-lookup"><span data-stu-id="08a77-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="08a77-104">Um requisito de recurso pode ser reservado de forma fixa.</span><span class="sxs-lookup"><span data-stu-id="08a77-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="08a77-105">Uma reserva fixa cria uma proposta que consome a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="08a77-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="08a77-106">A proposta então é enviada de volta ao solicitante para aprovação.</span><span class="sxs-lookup"><span data-stu-id="08a77-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="08a77-107">Uma reserva flexível provisoriamente adiciona um recurso a uma equipe de projeto e tem um status diferente no Painel de Agendamento, mas não consome a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="08a77-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="08a77-108">Para reservar um recurso de forma flexível no Painel de Agendamento, defina o campo **Status da Reserva** como **Flexível**.</span><span class="sxs-lookup"><span data-stu-id="08a77-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Status da reserva definido como Flexível](media/Resource-Management-image77.png)

<span data-ttu-id="08a77-110">Quando a guia **Equipe** estiver na exibição **Membros da Equipe Nomeados**, o recurso aparecerá lá.</span><span class="sxs-lookup"><span data-stu-id="08a77-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="08a77-111">As horas com reserva flexível são relatadas na coluna **Horas com Reserva Flexível**.</span><span class="sxs-lookup"><span data-stu-id="08a77-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Horas com reserva flexível na exibição Membros da Equipe Nomeados](media/Resource-Management-image78.png)

<span data-ttu-id="08a77-113">Os membros da equipe com reserva flexível podem ser atribuídos a tarefas.</span><span class="sxs-lookup"><span data-stu-id="08a77-113">Soft-booked team members can be assigned to tasks.</span></span>

![Membro da equipe com reserva flexível atribuído a uma tarefa](media/Resource-Management-image79.png)

<span data-ttu-id="08a77-115">Na guia **Reconciliação**, nenhuma reserva é exibida para um recurso com reserva flexível, pois a guia **Reconciliação** considera apenas reservas fixas.</span><span class="sxs-lookup"><span data-stu-id="08a77-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Recurso com reserva flexível sem reservas na guia Reconciliação](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="08a77-117">Não é possível reservar um recurso de forma flexível de um requisito que foi gerado com base em um membro genérico da equipe.</span><span class="sxs-lookup"><span data-stu-id="08a77-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="08a77-118">No Painel de Agendamento, uma coloração diferente é usada para reservas flexíveis de um recurso.</span><span class="sxs-lookup"><span data-stu-id="08a77-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Reservas flexíveis no Painel de Agendamento](media/Resource-Management-image81.png)

<span data-ttu-id="08a77-120">Para converter uma reserva flexível em uma reserva fixa, no Painel de Agendamento, clique com o botão direito do mouse na reserva flexível e, em seguida, selecione **Alterar Status** \> **Reserva Fixa** \> **Fixa**.</span><span class="sxs-lookup"><span data-stu-id="08a77-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Alterar o status da reserva para Fixa](media/Resource-Management-image82.png)

<span data-ttu-id="08a77-122">A reserva é alterada, e o status é alterado no Painel de Agendamento.</span><span class="sxs-lookup"><span data-stu-id="08a77-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="08a77-123">Como o status da reserva agora é **Fixa**, o recurso é exibido como reservado e sua capacidade e disponibilidade são ajustadas.</span><span class="sxs-lookup"><span data-stu-id="08a77-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="08a77-124">Você pode usar o mesmo método para cancelar uma reserva fixa ou flexível no Painel de Agendamento.</span><span class="sxs-lookup"><span data-stu-id="08a77-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="08a77-125">Para converter um recurso com reserva flexível em um com reserva fixa na guia **Equipe** do projeto, selecione o recurso e, em seguida, selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="08a77-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Confirmar comando](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]