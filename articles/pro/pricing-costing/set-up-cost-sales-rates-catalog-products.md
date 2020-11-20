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
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="73ce0-103">Configurar taxas de custo e de vendas para produtos do catálogo - lite</span><span class="sxs-lookup"><span data-stu-id="73ce0-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="73ce0-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="73ce0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="73ce0-105">A configuração de preços para itens do catálogo de produtos no Dynamics 365 Project Operations é a mesma do Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="73ce0-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="73ce0-106">Como os produtos não podem ser estimados ou usados em projetos no Project Operations, não há necessidade de definir os preços do catálogo de produtos nas listas de preços do projeto para cotações e contratos.</span><span class="sxs-lookup"><span data-stu-id="73ce0-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="73ce0-107">Os preços do catálogo de produtos devem ser configurados no campo **Preços de Produtos** de uma cotação, contrato ou conta.</span><span class="sxs-lookup"><span data-stu-id="73ce0-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="73ce0-108">Não configure os preços do catálogo de produtos nas listas de preços do projeto para essas entidades.</span><span class="sxs-lookup"><span data-stu-id="73ce0-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="73ce0-109">As listas de preços do projeto são exclusivas para o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="73ce0-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="73ce0-110">Existe uma lógica de negócios específica do aplicativo que copia as listas de preços de uma cotação para um contrato.</span><span class="sxs-lookup"><span data-stu-id="73ce0-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="73ce0-111">O resultado é uma lista de preços de projeto específica do contrato.</span><span class="sxs-lookup"><span data-stu-id="73ce0-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="73ce0-112">A operação de cópia pode atrasar o processo de ganho da cotação se a lista de preços do projeto na cotação ficar muito grande.</span><span class="sxs-lookup"><span data-stu-id="73ce0-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="73ce0-113">As listas de preços de produtos não são copiadas para criar listas de preços personalizadas em contratos.</span><span class="sxs-lookup"><span data-stu-id="73ce0-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="73ce0-114">Isso significa que as listas de preços dos produtos não afetam o desempenho do processo de ganho de cotações.</span><span class="sxs-lookup"><span data-stu-id="73ce0-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
