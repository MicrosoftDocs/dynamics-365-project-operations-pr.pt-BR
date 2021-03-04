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
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127332"
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