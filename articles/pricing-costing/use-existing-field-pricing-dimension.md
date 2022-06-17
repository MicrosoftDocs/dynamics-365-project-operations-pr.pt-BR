---
title: Campos do Project Operations como dimensões de preço
description: Este artigo fornece informações sobre como usar campos como dimensões de preço no Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: baf2145d4df23893953a099ca3837160fa8ac764
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932788"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>Campos do Project Operations como dimensões de preço

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

A entidade **Dados Reais** tem muitos campos que podem ser usados como dimensões de precificação para preço baseada em recursos. Por exemplo, um campo comum é o **Recurso Reservável**. Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de cobrança e de custo específicas para cada recurso é uma abordagem mais simples. No entanto, à medida que a força de trabalho faturável cresce, a manutenção de taxas específicas para os recursos pode se tornar irreal. As taxas de cobrança e de custo dos recursos começam a variar conforme eles são promovidos, ganham mais experiência ou adquirem um conjunto diferente de habilidades. 

Outro exemplo é a categoria de transação. Os clientes e os implementadores usavam a categoria de transação para classificar o trabalho e usam o campo para definir o preço e o custo com base na categoria de trabalho.


[!INCLUDE[footer-include](../includes/footer-banner.md)]