---
title: Configurar taxas de custo e de vendas para produtos do catálogo - lite
description: Este artigo fornece informações sobre como configurar taxas de custo e vendas para itens em um catálogo de produtos.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917378"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurar taxas de custo e de vendas para produtos do catálogo - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_


Configurando preços para itens do catálogo de produtos no Dynamics 365 Project Operations é o mesmo que no Dynamics 365 Sales.

Em Project Operations, os produtos não podem ser estimados ou usados em projetos, portanto, os preços do catálogo de produtos não precisam ser definidos nas listas de preços do projeto para cotações e contratos.

Use o campo **Preço do produto** de uma cotação, contrato ou conta para configurar preços de catálogo de produtos. Não configure preços de catálogo de produtos nas listas de preços do projeto. As listas de preços do projeto são exclusivas para o Project Operations. A lógica de negócios específica do aplicativo copia as listas de preços de uma cotação para um contrato. O resultado é uma lista de preços de projeto específica do contrato. A operação de cópia pode atrasar o processo de ganho da cotação se a lista de preços do projeto na cotação ficar muito grande. As listas de preços de produtos não são copiadas para criar listas de preços personalizadas em contratos. Como não há cópia envolvida, o desempenho do processo de cotação não é afetado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]