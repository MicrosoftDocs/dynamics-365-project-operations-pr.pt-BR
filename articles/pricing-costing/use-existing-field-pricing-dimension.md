---
title: Campos do Project Operations como dimensões de precificação
description: Este tópico fornece informações sobre o uso de campos como dimensões de precificação no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071491"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>Campos do Project Operations como dimensões de precificação

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

A entidade **Dados Reais** tem muitos campos que podem ser usados como dimensões de precificação para precificação baseada em recursos. Por exemplo, um campo comum é o **Recurso Reservável**. Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de cobrança e de custo específicas para cada recurso é uma abordagem mais simples. No entanto, à medida que a força de trabalho faturável cresce, a manutenção de taxas específicas para os recursos pode se tornar irreal. As taxas de cobrança e de custo dos recursos começam a variar conforme eles são promovidos, ganham mais experiência ou adquirem um conjunto diferente de habilidades. 

Outro exemplo é a categoria de transação. Os clientes e os implementadores usavam a categoria de transação para classificar o trabalho e usam o campo para definir o preço e o custo com base na categoria de trabalho.
