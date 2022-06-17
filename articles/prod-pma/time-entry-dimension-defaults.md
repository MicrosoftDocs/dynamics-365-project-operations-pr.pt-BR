---
title: Padronização de dimensões financeiras para entradas de horas do projeto
description: Esse artigo fornece informações sobre como a padronização de dimensões financeiras é aplicada a entradas de horas.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916550"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Padronização de dimensões financeiras para entradas de horas do projeto

[!include [banner](../includes/banner.md)]

Quando você usa dimensões financeiras para entradas de horas do projeto, o valor de dimensão padrão é avaliado na seguinte ordem:

1. Recurso
2. Projeto
3. Fonte de financiamento

Por exemplo, se a dimensão padrão for especificada em um recurso, o valor padrão será aplicado sobre o valor padrão que é especificado para o projeto. Da mesma forma, se a dimensão padrão for especificada em um projeto, o valor padrão será aplicado sobre o valor padrão que é especificado para a fonte de financiamento.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
