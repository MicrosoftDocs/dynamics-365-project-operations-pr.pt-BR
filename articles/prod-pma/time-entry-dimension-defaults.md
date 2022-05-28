---
title: Padronização de dimensões financeiras para entradas de horas do projeto
description: Esse tópico fornece informações sobre como a padronização de dimensões financeiras é aplicada a entradas de horas.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597922"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Padronização de dimensões financeiras para entradas de horas do projeto

[!include [banner](../includes/banner.md)]

Quando você usa dimensões financeiras para entradas de horas do projeto, o valor de dimensão padrão é avaliado na seguinte ordem:

1. Recurso
2. Project
3. Fonte de financiamento

Por exemplo, se a dimensão padrão for especificada em um recurso, o valor padrão será aplicado sobre o valor padrão que é especificado para o projeto. Da mesma forma, se a dimensão padrão for especificada em um projeto, o valor padrão será aplicado sobre o valor padrão que é especificado para a fonte de financiamento.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
