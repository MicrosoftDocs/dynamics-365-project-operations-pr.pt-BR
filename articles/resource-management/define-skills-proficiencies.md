---
title: Definir habilidades e proficiências
description: Este tópico fornece informações sobre como configurar modelos de proficiência para avaliar recursos.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124759"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="2d55e-103">Definir habilidades e proficiências</span><span class="sxs-lookup"><span data-stu-id="2d55e-103">Define skills and proficiencies</span></span>

<span data-ttu-id="2d55e-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="2d55e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2d55e-105">As habilidades são características de recursos que são compartilhadas entre o Dynamics 365 Project Operations e, caso esteja presente, o Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="2d55e-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="2d55e-106">Para manter o repositório de habilidades no Project Operations, acesse **Recursos** \> **Habilidades de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="2d55e-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="2d55e-107">Usar modelos de proficiência para classificar recursos</span><span class="sxs-lookup"><span data-stu-id="2d55e-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="2d55e-108">As habilidades para recursos são classificadas por modelos de proficiência.</span><span class="sxs-lookup"><span data-stu-id="2d55e-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="2d55e-109">As classificações individuais estão em um modelo de proficiência.</span><span class="sxs-lookup"><span data-stu-id="2d55e-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="2d55e-110">Para criar um modelo de proficiência, acesse **Recursos** \> **Modelos de Proficiência** e, em seguida, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2d55e-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="2d55e-111">No novo modelo de classificação, especifique o valor mínimo de classificação, o valor máximo de classificação e a entidade que está sendo classificada.</span><span class="sxs-lookup"><span data-stu-id="2d55e-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="2d55e-112">Na subgrade **Valores de Classificação**, é possível definir os diferentes valores de classificação, do mínimo ao máximo.</span><span class="sxs-lookup"><span data-stu-id="2d55e-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="2d55e-113">Esses valores de classificação são exibidos nos filtros **Requisitos de Recursos**, **Painel de Agendamento** e **Assistente de Agendamento**.</span><span class="sxs-lookup"><span data-stu-id="2d55e-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
