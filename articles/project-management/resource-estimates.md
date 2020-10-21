---
title: Estimativas de recurso
description: Este tópico fornece informações sobre como são calculadas as estimativas de recursos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928540"
---
# <a name="resource-estimates"></a>Estimativas de recurso

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

As estimativas de recursos vêm de esforço dividido em fases que é definido na estrutura de detalhamento de trabalho junto com as dimensões de preços aplicáveis. Normalmente, o cálculo é **taxa/hora para cada função x horas**. O esforço dividido em fases para cada recurso é armazenado no registro de atribuição do recurso. O preço é armazenado em uma lista de preços predefinida. A conversão de unidades é aplicada com base na lista de preços aplicável.

![Estimativas de Recurso](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Preço de custo e moeda de custo padrão

Os preços de custo são padronizados na Unidade Organizacional.

## <a name="default-bill-rate-and-sales-currency"></a>Taxa de cobrança e moeda de vendas padrão

Os preços de venda são aplicados uma vez por negócio. A hierarquia para a lista de preços de venda é padronizada desta forma:

1. Organização
2. Cliente
3. Cotação/contrato
