---
title: Enviar solicitação de recurso
description: Esse tópico fornece informações sobre o envio de uma solicitação para um recurso do projeto.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071521"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="6c4d3-103">Enviar solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="6c4d3-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6c4d3-104">Você pode enviar um requisito de recurso gerado como uma solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="6c4d3-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="6c4d3-105">Em seguida, a solicitação é enviada para um gerenciador de recursos para aprovação.</span><span class="sxs-lookup"><span data-stu-id="6c4d3-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="6c4d3-106">No Project Service Automation (PSA), na página **Projetos** , clique na guia **Equipe** para visualizar uma lista de recursos reserváveis.</span><span class="sxs-lookup"><span data-stu-id="6c4d3-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="6c4d3-107">Selecione o recurso genérico com um requisito de recurso da lista e clique em **Enviar solicitação**.</span><span class="sxs-lookup"><span data-stu-id="6c4d3-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Enviar solicitação de recurso](media/RM-how-to-18.png)

<span data-ttu-id="6c4d3-109">O status da solicitação do membro da equipe genérico será alterado para **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="6c4d3-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="6c4d3-110">Após a solicitação ser aprovada pelo gerenciador de recursos, o recurso genérico será substituído por um recurso nomeado se o gerenciador de recurso aprovar a solicitação com a reserva de um recurso indicado.</span><span class="sxs-lookup"><span data-stu-id="6c4d3-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="6c4d3-111">Caso contrário, o recurso genérico permanecerá na equipe e o status de solicitação será alterado para **Precisa de revisão** , se o gerenciador de recurso tiver proposto um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="6c4d3-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review** , if the resource manager has proposed a named resource.</span></span>
