---
title: Visão geral dos modos de gerenciamento de recursos
description: Este tópico oferece informações sobre a funcionalidade Gerenciamento de recursos no Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118504"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="389f7-103">Visão geral dos modos de gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="389f7-103">Resource management modes overview</span></span>

<span data-ttu-id="389f7-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="389f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="389f7-105">O Dynamics 365 Project Operations é compatível com dois modos para que você execute o fluxo geral de reserva.</span><span class="sxs-lookup"><span data-stu-id="389f7-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="389f7-106">O modo de gerenciamento é definido como um parâmetro do projeto e poderá ser modificado se as necessidades de negócios mudarem.</span><span class="sxs-lookup"><span data-stu-id="389f7-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="389f7-107">Modo Central</span><span class="sxs-lookup"><span data-stu-id="389f7-107">Central mode</span></span>
<span data-ttu-id="389f7-108">Para organizações que centralizam a alocação de recursos para projetos, o modo Central fornece uma maneira de garantir que os gerentes de projeto possam definir os requisitos de recursos no nível do projeto.</span><span class="sxs-lookup"><span data-stu-id="389f7-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="389f7-109">O atendimento dos requisitos de recursos é delegado a um gerente de recursos.</span><span class="sxs-lookup"><span data-stu-id="389f7-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="389f7-110">Os gerentes de projeto podem aceitar ou rejeitar recursos propostos pelo gerente de recursos.</span><span class="sxs-lookup"><span data-stu-id="389f7-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Modo Central](./media/resource-management-central.png)

<span data-ttu-id="389f7-112">Para gerenciar recursos com o modo Central, consulte:</span><span class="sxs-lookup"><span data-stu-id="389f7-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="389f7-113">Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="389f7-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="389f7-114">Reservar recursos indicados a partir de requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="389f7-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="389f7-115">Enviar uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="389f7-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="389f7-116">Atender uma solicitação de recursos</span><span class="sxs-lookup"><span data-stu-id="389f7-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="389f7-117">Aceitar ou rejeitar um recurso de projeto proposto de uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="389f7-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="389f7-118">Modo Híbrido</span><span class="sxs-lookup"><span data-stu-id="389f7-118">Hybrid mode</span></span>
<span data-ttu-id="389f7-119">Para organizações que exigem flexibilidade na alocação de recursos, o modo híbrido permite que gerentes de projeto e gerentes de recursos reservem recursos.</span><span class="sxs-lookup"><span data-stu-id="389f7-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Modo Híbrido](./media/resource-management-hybrid.png)

<span data-ttu-id="389f7-121">Além do processo do modo Central compatível, consulte os tópicos a seguir para gerenciar todos os outros fluxos de reserva compatíveis no modo Híbrido:</span><span class="sxs-lookup"><span data-stu-id="389f7-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="389f7-122">Reservar um recurso diretamente em um projeto:</span><span class="sxs-lookup"><span data-stu-id="389f7-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="389f7-123">Reservar recursos reserváveis nomeados a uma equipe de projeto e atribuir tarefas</span><span class="sxs-lookup"><span data-stu-id="389f7-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="389f7-124">Reservar um recurso de um requisito de recursos:</span><span class="sxs-lookup"><span data-stu-id="389f7-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="389f7-125">Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="389f7-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="389f7-126">Reservar recursos indicados a partir de requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="389f7-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
