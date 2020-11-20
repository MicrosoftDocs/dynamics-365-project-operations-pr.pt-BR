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
ms.openlocfilehash: 92735262ebc4b48dd1143af57349d77e1fe3061c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124174"
---
# <a name="skills-and-proficiency-models"></a>Modelos de proficiência e habilidades

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As habilidades são características de recursos que são compartilhadas entre o Dynamics 365 Project Service Automation e, caso esteja presente, o Dynamics 365 Field Service. 

Para manter o repositório de habilidades no Project Service Automation, acesse **Recursos** \> **Habilidades de Recursos**. 

> ![Habilidades de Recursos](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Usar modelos de proficiência para classificar recursos

As habilidades para recursos são classificadas por modelos de proficiência. As classificações individuais estão em um modelo de proficiência. 

1. Para criar um modelo de proficiência, acesse **Recursos** \> **Modelos de Proficiência** e, em seguida, selecione **Novo**.
2. No novo modelo de classificação, especifique o valor mínimo de classificação, o valor máximo de classificação e a entidade que está sendo classificada.
3. Na subgrade **Valores de Classificação**, é possível definir os diferentes valores de classificação, do mínimo ao máximo.

> ![Classificações mínimas e máximas definidas](media/Resource-Management-image85.png)

Esses valores de classificação são exibidos nos filtros **Requisitos de Recursos**, **Painel de Agendamento** e **Assistente de Agendamento**.
