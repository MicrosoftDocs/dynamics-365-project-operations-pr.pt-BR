---
title: Linhas de custos de cotação baseadas em produto
description: Este tópico fornece informações sobre como aplicar um preço de custo a uma linha de cotação baseada em produto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118909"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="35069-103">Linhas de custos de cotação baseadas em produto</span><span class="sxs-lookup"><span data-stu-id="35069-103">Costing product-based quote lines</span></span>

<span data-ttu-id="35069-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="35069-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="35069-105">As linhas de cotação baseadas em produto no Dynamics 365 Project Operations também têm um campo **Preço de Custo**.</span><span class="sxs-lookup"><span data-stu-id="35069-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="35069-106">Esse campo é usado para rastrear o preço de custo do produto na linha de cotação e para cálculos de lucratividade posteriores.</span><span class="sxs-lookup"><span data-stu-id="35069-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="35069-107">Quando uma linha de cotação baseada em produto é criada para um produto de catálogo, o custo da linha de cotação baseada em produto assume o padrão do campo **Custo padrão** no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="35069-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="35069-108">O campo de custo padrão no catálogo de produtos é configurado na moeda base da Organização.</span><span class="sxs-lookup"><span data-stu-id="35069-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="35069-109">O custo unitário padrão na linha de cotação baseada em produto é convertido para a moeda de venda na cotação.</span><span class="sxs-lookup"><span data-stu-id="35069-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="35069-110">Custo unitário em uma linha de cotação baseada em produto</span><span class="sxs-lookup"><span data-stu-id="35069-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="35069-111">O objetivo de ter um custo unitário em uma linha de cotação baseada em produto é permitir custos diferentes para um produto em cada venda.</span><span class="sxs-lookup"><span data-stu-id="35069-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="35069-112">Este não é um cenário comum, mas às vezes o custo do produto pode ser descontado pelo fornecedor dependendo do cliente da venda final.</span><span class="sxs-lookup"><span data-stu-id="35069-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="35069-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="35069-113">For example:</span></span>

<span data-ttu-id="35069-114">A Fabrikam Robotics está instalando braços robóticos nas linhas de montagem da A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="35069-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="35069-115">A Fabrikam fornece serviços de instalação, mas os braços robóticos são adquiridos da robótica da Trey.</span><span class="sxs-lookup"><span data-stu-id="35069-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="35069-116">Se a instalação de braços robóticos na A Datum Corporation abrir uma nova vertical de indústria para os braços robóticos da Trey, a Trey poderá oferecer um desconto especial referente a esse negócio à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="35069-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="35069-117">Nesse caso, a Fabrikam criará uma linha de cotação baseada em produto para Braços Robóticos e inserirá um custo especial por unidade para essa cotação.</span><span class="sxs-lookup"><span data-stu-id="35069-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="35069-118">Esse custo é diferente do custo padrão de Braços Robóticos da Trey.</span><span class="sxs-lookup"><span data-stu-id="35069-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>