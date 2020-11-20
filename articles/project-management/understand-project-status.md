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
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071300"
---
# <a name="understand-project-status"></a><span data-ttu-id="7cab9-103">Entender o status de projeto</span><span class="sxs-lookup"><span data-stu-id="7cab9-103">Understand project status</span></span>

<span data-ttu-id="7cab9-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="7cab9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7cab9-105">A seção **Status** na página **Entidade de Projeto** fornece um resumo da integridade de um projeto com base no custo e esforço.</span><span class="sxs-lookup"><span data-stu-id="7cab9-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="7cab9-106">Campos do resumo do status</span><span class="sxs-lookup"><span data-stu-id="7cab9-106">Status summary fields</span></span>

- <span data-ttu-id="7cab9-107">O campo **Status geral do projeto** é um campo editável que mostra o status geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="7cab9-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="7cab9-108">Esse campo usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco.</span><span class="sxs-lookup"><span data-stu-id="7cab9-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="7cab9-109">O campo **Comentários** permite ao gerente de projeto inserir comentários específicos sobre o status.</span><span class="sxs-lookup"><span data-stu-id="7cab9-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="7cab9-110">O campo **Status atualizado em** não é editável.</span><span class="sxs-lookup"><span data-stu-id="7cab9-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="7cab9-111">O valor neste campo é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="7cab9-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="7cab9-112">Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da grade de acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="7cab9-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="7cab9-113">Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, esses campos serão atualizados como **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="7cab9-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="7cab9-114">Quando a variação de agenda e de custo para o nó raiz for negativa, esses campos serão definidos como **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="7cab9-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>