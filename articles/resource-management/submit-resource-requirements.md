---
title: Enviar uma solicitação de recurso
description: Você pode enviar um requisito de recurso gerado como uma solicitação de recurso. Em seguida, a solicitação é enviada para um gerenciador de recursos para aprovação.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961680"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="cc761-104">Enviar uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="cc761-104">Submit a resource request</span></span>

<span data-ttu-id="cc761-105">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="cc761-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc761-106">Você pode enviar um requisito de recurso gerado como uma solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="cc761-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="cc761-107">Em seguida, a solicitação é enviada para um gerenciador de recursos para aprovação.</span><span class="sxs-lookup"><span data-stu-id="cc761-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="cc761-108">No Dynamics 365 Project Operations, na página **Projetos**, selecione a guia **Equipe** para visualizar uma lista de recursos reserváveis.</span><span class="sxs-lookup"><span data-stu-id="cc761-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="cc761-109">Selecione o recurso genérico com um requisito de recurso da lista e clique em **Enviar Solicitação**.</span><span class="sxs-lookup"><span data-stu-id="cc761-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="cc761-110">O status da solicitação do membro da equipe genérico será alterado para **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="cc761-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="cc761-111">Após a solicitação ser aprovada, o recurso genérico será substituído por um recurso nomeado se o gerente de recursos aprovar a solicitação ao reservar um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="cc761-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="cc761-112">Caso contrário, se o gerente de recursos propuser um recurso nomeado, o recurso genérico permanecerá na equipe e o status de solicitação será alterado para **Precisa de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="cc761-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
