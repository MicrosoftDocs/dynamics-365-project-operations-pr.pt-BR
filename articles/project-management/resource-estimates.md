---
title: Estimativas de recurso
description: Este tópico fornece informações sobre como são calculadas as estimativas de recursos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286504"
---
# <a name="resource-estimates"></a>Estimativas de recurso

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As estimativas de recursos vêm de esforço dividido em fases que é definido na estrutura de detalhamento de trabalho junto com as dimensões de preços aplicáveis. Normalmente, o cálculo é **taxa/hora para cada função x horas**. O esforço dividido em fases para cada recurso é armazenado no registro de atribuição do recurso. O preço é armazenado em uma lista de preços predefinida. A conversão de unidades é aplicada com base na lista de preços aplicável.

![Estimativas de Recurso](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Preço de custo e moeda de custo padrão

Os preços de custo são padronizados na Unidade Organizacional.

## <a name="default-bill-rate-and-sales-currency"></a>Taxa de cobrança e moeda de vendas padrão

Os preços de venda são aplicados uma vez por negócio. A hierarquia para a lista de preços de venda é padronizada desta forma:

1. Organização
2. Cliente
3. Cotação/contrato


[!INCLUDE[footer-include](../includes/footer-banner.md)]