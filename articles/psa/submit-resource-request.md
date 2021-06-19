---
title: Enviar solicitação de recurso
description: Esse tópico fornece informações sobre o envio de uma solicitação para um recurso do projeto.
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013157"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="eda3a-103">Enviar solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="eda3a-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eda3a-104">Você pode enviar um requisito de recurso gerado como uma solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="eda3a-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="eda3a-105">Em seguida, a solicitação é enviada para um gerenciador de recursos para aprovação.</span><span class="sxs-lookup"><span data-stu-id="eda3a-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="eda3a-106">No Project Service Automation (PSA), na página **Projetos**, clique na guia **Equipe** para visualizar uma lista de recursos reserváveis.</span><span class="sxs-lookup"><span data-stu-id="eda3a-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="eda3a-107">Selecione o recurso genérico com um requisito de recurso da lista e clique em **Enviar solicitação**.</span><span class="sxs-lookup"><span data-stu-id="eda3a-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Enviar solicitação de recurso](media/RM-how-to-18.png)

<span data-ttu-id="eda3a-109">O status da solicitação do membro da equipe genérico será alterado para **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="eda3a-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="eda3a-110">Após a solicitação ser aprovada pelo gerenciador de recursos, o recurso genérico será substituído por um recurso nomeado se o gerenciador de recurso aprovar a solicitação com a reserva de um recurso indicado.</span><span class="sxs-lookup"><span data-stu-id="eda3a-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="eda3a-111">Caso contrário, o recurso genérico permanecerá na equipe e o status de solicitação será alterado para **Precisa de revisão**, se o gerenciador de recurso tiver proposto um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="eda3a-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]