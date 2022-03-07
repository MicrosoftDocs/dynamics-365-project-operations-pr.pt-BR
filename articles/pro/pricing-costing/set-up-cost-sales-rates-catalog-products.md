---
title: Configurar taxas de custo e de vendas para produtos do catálogo - lite
description: Este tópico fornece informações sobre como configurar taxas de custo e vendas para itens em um catálogo de produtos.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176687"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurar taxas de custo e de vendas para produtos do catálogo - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_


A configuração de preços para itens do catálogo de produtos no Dynamics 365 Project Operations é a mesma do Dynamics 365 Sales.

Como os produtos não podem ser estimados ou usados em projetos no Project Operations, não há necessidade de definir os preços do catálogo de produtos nas listas de preços do projeto para cotações e contratos.

Os preços do catálogo de produtos devem ser configurados no campo **Preços de Produtos** de uma cotação, contrato ou conta. Não configure os preços do catálogo de produtos nas listas de preços do projeto para essas entidades. As listas de preços do projeto são exclusivas para o Project Operations. Existe uma lógica de negócios específica do aplicativo que copia as listas de preços de uma cotação para um contrato. O resultado é uma lista de preços de projeto específica do contrato. A operação de cópia pode atrasar o processo de ganho da cotação se a lista de preços do projeto na cotação ficar muito grande. As listas de preços de produtos não são copiadas para criar listas de preços personalizadas em contratos. Isso significa que as listas de preços dos produtos não afetam o desempenho do processo de ganho de cotações.
