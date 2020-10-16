---
title: Entender o status de projeto
description: Este tópico oferece informações sobre o status atribuído a projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965662"
---
# <a name="understand-project-status"></a><span data-ttu-id="90531-103">Entender o status de projeto</span><span class="sxs-lookup"><span data-stu-id="90531-103">Understand project status</span></span>

<span data-ttu-id="90531-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="90531-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="90531-105">A seção **Status** na página **Entidade de Projeto** fornece um resumo da integridade de um projeto com base no custo e esforço.</span><span class="sxs-lookup"><span data-stu-id="90531-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="90531-106">Campos do resumo do status</span><span class="sxs-lookup"><span data-stu-id="90531-106">Status summary fields</span></span>

- <span data-ttu-id="90531-107">O campo **Status geral do projeto** é um campo editável que mostra o status geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="90531-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="90531-108">Esse campo usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco.</span><span class="sxs-lookup"><span data-stu-id="90531-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="90531-109">O campo **Comentários** permite ao gerente de projeto inserir comentários específicos sobre o status.</span><span class="sxs-lookup"><span data-stu-id="90531-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="90531-110">O campo **Status atualizado em** não é editável.</span><span class="sxs-lookup"><span data-stu-id="90531-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="90531-111">O valor neste campo é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="90531-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="90531-112">Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da grade de acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="90531-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="90531-113">Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, esses campos serão atualizados como **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="90531-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="90531-114">Quando a variação de agenda e de custo para o nó raiz for negativa, esses campos serão definidos como **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="90531-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
