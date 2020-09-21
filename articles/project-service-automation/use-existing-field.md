---
title: Usar um campo existente no Project Service como uma dimensão de precificação
description: Este tópico inclui informações sobre o uso de campos existentes do Project Service como dimensões de precificação.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749081"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Usar um campo existente no Project Service como uma dimensão de precificação

O PSA (Project Service Automation) tem vários campos na entidade **Dados Reais** que podem ser usados como dimensões de precificação para a precificação com base em recurso em organizações de projetos. Por exemplo, um campo comum é o **Recurso Reservável**. Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de cobrança e de custo específicas para cada recurso é uma abordagem mais simples. Entretanto, conforme a equipe de trabalho faturável cresce, isso pode se tornar irreal de manter, pois as taxas de cobrança e de custo dos recursos começam a variar à medida que os recursos são promovidos, ganham mais experiência ou adquirem conjuntos de habilidades diferentes. Como essa abordagem ainda funciona para empresas de um determinado porte, consulte o tópico [Usar recurso reservável como dimensão de precificação](bookable-resource-pricing-dimension.md) para compreender como um campo existente do Project Service pode ser usado como dimensão de precificação.

Outro exemplo é a categoria de transação. Os clientes e os implementadores usavam a categoria de transação do PSA para classificar o trabalho e usavam o campo para definir o preço e o custo com base na categoria do trabalho. Para obter mais informações, consulte [Usar categoria de transação como dimensão de precificação](transaction-category-pricing-dimension.md).
