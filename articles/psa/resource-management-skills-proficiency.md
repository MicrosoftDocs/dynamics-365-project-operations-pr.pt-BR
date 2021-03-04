---
title: Modelos de proficiência e habilidades
description: Este tópico fornece informações sobre como usar os modelos de proficiência e habilidades.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: c7da8b2a7eda51b2aa7cf04e325a92f33d834efc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147459"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="65a29-103">Modelos de proficiência e habilidades</span><span class="sxs-lookup"><span data-stu-id="65a29-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="65a29-104">As habilidades são características de recursos que são compartilhadas entre o Dynamics 365 Project Service Automation e, caso esteja presente, o Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="65a29-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="65a29-105">Para manter o repositório de habilidades no Project Service Automation, acesse **Recursos** \> **Habilidades de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="65a29-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Habilidades de Recursos](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="65a29-107">Usar modelos de proficiência para classificar recursos</span><span class="sxs-lookup"><span data-stu-id="65a29-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="65a29-108">As habilidades para recursos são classificadas por modelos de proficiência.</span><span class="sxs-lookup"><span data-stu-id="65a29-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="65a29-109">As classificações individuais estão em um modelo de proficiência.</span><span class="sxs-lookup"><span data-stu-id="65a29-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="65a29-110">Para criar um modelo de proficiência, acesse **Recursos** \> **Modelos de Proficiência** e, em seguida, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="65a29-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="65a29-111">No novo modelo de classificação, especifique o valor mínimo de classificação, o valor máximo de classificação e a entidade que está sendo classificada.</span><span class="sxs-lookup"><span data-stu-id="65a29-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="65a29-112">Na subgrade **Valores de Classificação**, é possível definir os diferentes valores de classificação, do mínimo ao máximo.</span><span class="sxs-lookup"><span data-stu-id="65a29-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Classificações mínimas e máximas definidas](media/Resource-Management-image85.png)

<span data-ttu-id="65a29-114">Esses valores de classificação são exibidos nos filtros **Requisitos de Recursos**, **Painel de Agendamento** e **Assistente de Agendamento**.</span><span class="sxs-lookup"><span data-stu-id="65a29-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
