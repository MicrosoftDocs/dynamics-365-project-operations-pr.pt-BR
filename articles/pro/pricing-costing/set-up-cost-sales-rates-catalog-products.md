---
title: Configurar taxas de custo e de vendas para produtos do catálogo - lite
description: Este tópico fornece informações sobre como configurar taxas de custo e vendas para itens em um catálogo de produtos.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996017"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurar taxas de custo e de vendas para produtos do catálogo - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_


Configurando preços para itens do catálogo de produtos no Dynamics 365 Project Operations é o mesmo que no Dynamics 365 Sales.

Em Project Operations, os produtos não podem ser estimados ou usados em projetos, portanto, os preços do catálogo de produtos não precisam ser definidos nas listas de preços do projeto para cotações e contratos.

Use o campo **Preço do produto** de uma cotação, contrato ou conta para configurar preços de catálogo de produtos. Não configure preços de catálogo de produtos nas listas de preços do projeto. As listas de preços do projeto são exclusivas para o Project Operations. A lógica de negócios específica do aplicativo copia as listas de preços de uma cotação para um contrato. O resultado é uma lista de preços de projeto específica do contrato. A operação de cópia pode atrasar o processo de ganho da cotação se a lista de preços do projeto na cotação ficar muito grande. As listas de preços de produtos não são copiadas para criar listas de preços personalizadas em contratos. Como não há cópia envolvida, o desempenho do processo de cotação não é afetado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]