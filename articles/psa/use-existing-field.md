---
title: Usar um campo existente no Project Service como uma dimensão de precificação
description: Este tópico inclui informações sobre o uso de campos existentes do Project Service como dimensões de precificação.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008072"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Usar um campo existente no Project Service como uma dimensão de precificação

[!include [banner](../includes/psa-now-project-operations.md)]

O PSA (Project Service Automation) tem vários campos na entidade **Dados Reais** que podem ser usados como dimensões de precificação para a precificação com base em recurso em organizações de projetos. Por exemplo, um campo comum é o **Recurso Reservável**. Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de cobrança e de custo específicas para cada recurso é uma abordagem mais simples. Entretanto, conforme a equipe de trabalho faturável cresce, taxas específicas podem se tornar irreais de manter, pois as taxas de cobrança e de custo dos recursos começam a variar à medida que os recursos são promovidos, ganham mais experiência ou adquirem conjuntos de habilidades diferentes. Como essa abordagem ainda funciona para empresas de um determinado porte, consulte [Usar recurso reservável como dimensão de precificação](bookable-resource-pricing-dimension.md) para compreender como um campo existente do Project Service pode ser usado como dimensão de precificação.

Outro exemplo é a categoria de transação. Os clientes e os implementadores usavam a categoria de transação do PSA para classificar o trabalho e usavam o campo para definir o preço e o custo com base na categoria do trabalho. Para obter mais informações, consulte [Usar categoria de transação como dimensão de precificação](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]