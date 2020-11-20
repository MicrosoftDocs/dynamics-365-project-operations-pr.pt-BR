---
title: Perguntas frequentes sobre gerenciamento de recursos
description: Este tópico fornece respostas às perguntas frequentes sobre gerenciamento de recursos.
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
ms.openlocfilehash: 38d9509768323a5a1d78683a2e65ade241adc65f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120124"
---
# <a name="resource-management-faq"></a><span data-ttu-id="a72d8-103">Perguntas frequentes sobre gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="a72d8-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="a72d8-104">Qual é a diferença entre um membro da equipe e um requisito de recurso?</span><span class="sxs-lookup"><span data-stu-id="a72d8-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="a72d8-105">Um membro da equipe do projeto pode ser atribuído a tarefas, reservado ou reservado em excesso e definido como um aprovador.</span><span class="sxs-lookup"><span data-stu-id="a72d8-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="a72d8-106">Um requisito de recurso pode existir sem um membro da equipe do projeto, como uma anotação de rascunho da demanda.</span><span class="sxs-lookup"><span data-stu-id="a72d8-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="a72d8-107">Qual é a diferença entre horas com reserva flexível e propostas?</span><span class="sxs-lookup"><span data-stu-id="a72d8-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="a72d8-108">As horas propostas e as horas com reserva flexível diferem em visibilidade.</span><span class="sxs-lookup"><span data-stu-id="a72d8-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="a72d8-109">As horas propostas são visíveis apenas para gerentes de recursos e o gerente de projetos que iniciou a demanda usando uma solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="a72d8-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="a72d8-110">As horas com reserva flexível são visíveis para qualquer pessoa que tenha acesso ao Painel de Agendamento.</span><span class="sxs-lookup"><span data-stu-id="a72d8-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="a72d8-111">Como posso ver as horas com reserva flexível para recursos em uma equipe?</span><span class="sxs-lookup"><span data-stu-id="a72d8-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="a72d8-112">As reservas flexíveis podem ser feitas ao reservar um requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="a72d8-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="a72d8-113">Os recursos com reserva flexível em uma equipe do projeto aparecem como membros da equipe que possuem horas com reserva flexível.</span><span class="sxs-lookup"><span data-stu-id="a72d8-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="a72d8-114">Eles também aparecem no Painel de Agendamento.</span><span class="sxs-lookup"><span data-stu-id="a72d8-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="a72d8-115">Como faço para alterar as horas necessárias e as datas de início e término de um recurso (genérico ou nomeado) que reservei?</span><span class="sxs-lookup"><span data-stu-id="a72d8-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="a72d8-116">Depois de reservar os recursos, selecione **Manter Reservas** para fazer quaisquer alterações necessárias.</span><span class="sxs-lookup"><span data-stu-id="a72d8-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="a72d8-117">A quais tipos de recursos o Project Service Automation oferece suporte?</span><span class="sxs-lookup"><span data-stu-id="a72d8-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="a72d8-118">**Usuário** e **Contato** são os únicos tipos de recursos com suporte no Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a72d8-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="a72d8-119">Embora seja possível criar outros tipos de recursos (por exemplo, **Equipamento** e **Grupo**), nenhum caso de uso completo terá suporte para eles.</span><span class="sxs-lookup"><span data-stu-id="a72d8-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="a72d8-120">Qual é a diferença entre uma atribuição e uma reserva?</span><span class="sxs-lookup"><span data-stu-id="a72d8-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="a72d8-121">As atribuições são a atribuição de recursos a tarefas do projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="a72d8-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="a72d8-122">Os recursos podem ser reais ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="a72d8-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="a72d8-123">As reservas são a alocação fixa ou flexível de recursos para um projeto.</span><span class="sxs-lookup"><span data-stu-id="a72d8-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="a72d8-124">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="a72d8-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="a72d8-125">O ideal é que, para recursos reais, as reservas e atribuições sejam correspondentes, pois elas não diferem.</span><span class="sxs-lookup"><span data-stu-id="a72d8-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="a72d8-126">No entanto, o PSA não impõe essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="a72d8-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="a72d8-127">A exibição Reconciliação mostra a um gerente de projetos os locais em que as reservas e atribuições de um recurso não correspondem.</span><span class="sxs-lookup"><span data-stu-id="a72d8-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
