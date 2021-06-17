---
title: Configurar taxas de custo e de vendas para produtos do catálogo - lite
description: Este tópico fornece informações sobre como configurar taxas de custo e vendas para itens em um catálogo de produtos.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004295"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="9887f-103">Configurar taxas de custo e de vendas para produtos do catálogo - lite</span><span class="sxs-lookup"><span data-stu-id="9887f-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="9887f-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="9887f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9887f-105">Configurando preços para itens do catálogo de produtos no Dynamics 365 Project Operations é o mesmo que no Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9887f-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="9887f-106">Em Project Operations, os produtos não podem ser estimados ou usados em projetos, portanto, os preços do catálogo de produtos não precisam ser definidos nas listas de preços do projeto para cotações e contratos.</span><span class="sxs-lookup"><span data-stu-id="9887f-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="9887f-107">Use o campo **Preço do produto** de uma cotação, contrato ou conta para configurar preços de catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="9887f-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="9887f-108">Não configure preços de catálogo de produtos nas listas de preços do projeto.</span><span class="sxs-lookup"><span data-stu-id="9887f-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="9887f-109">As listas de preços do projeto são exclusivas para o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9887f-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="9887f-110">A lógica de negócios específica do aplicativo copia as listas de preços de uma cotação para um contrato.</span><span class="sxs-lookup"><span data-stu-id="9887f-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="9887f-111">O resultado é uma lista de preços de projeto específica do contrato.</span><span class="sxs-lookup"><span data-stu-id="9887f-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="9887f-112">A operação de cópia pode atrasar o processo de ganho da cotação se a lista de preços do projeto na cotação ficar muito grande.</span><span class="sxs-lookup"><span data-stu-id="9887f-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="9887f-113">As listas de preços de produtos não são copiadas para criar listas de preços personalizadas em contratos.</span><span class="sxs-lookup"><span data-stu-id="9887f-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="9887f-114">Como não há cópia envolvida, o desempenho do processo de cotação não é afetado.</span><span class="sxs-lookup"><span data-stu-id="9887f-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]