---
title: Linhas de contrato de cotação baseadas em produto
description: Este tópico fornece informações sobre criação
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4071659"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="3aba7-103">Linhas de contrato de cotação baseadas em produto</span><span class="sxs-lookup"><span data-stu-id="3aba7-103">Costing product-based contract lines</span></span>

<span data-ttu-id="3aba7-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="3aba7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3aba7-105">As linhas de contrato com base em produto no Dynamics 365 Project Operations incluem o campo **Preço de Custo** , que armazena o preço de custo do produto para cálculos de lucratividade posteriores.</span><span class="sxs-lookup"><span data-stu-id="3aba7-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="3aba7-106">Quando uma linha de contrato baseada em produto é criada para um produto de catálogo, o custo da linha de contrato baseada em produto assume o padrão do campo **Custo Padrão** no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="3aba7-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3aba7-107">O campo **Custo Padrão** no catálogo de produtos é configurado na moeda base da Organização.</span><span class="sxs-lookup"><span data-stu-id="3aba7-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3aba7-108">Quando o custo unitário é padronizado na linha do contrato, ele é convertido para a moeda de venda no contrato.</span><span class="sxs-lookup"><span data-stu-id="3aba7-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="3aba7-109">Custo unitário em uma linha de contrato baseada em produto</span><span class="sxs-lookup"><span data-stu-id="3aba7-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="3aba7-110">Ter um custo unitário em uma linha de contrato baseada em produto permite custos diferentes para um produto em cada venda de uma unidade.</span><span class="sxs-lookup"><span data-stu-id="3aba7-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="3aba7-111">Embora nem sempre seja necessário, há certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="3aba7-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="3aba7-112">Considere este cenário:</span><span class="sxs-lookup"><span data-stu-id="3aba7-112">Consider the following scenario:</span></span>

<span data-ttu-id="3aba7-113">A Fabrikam Robotics está instalando braços robóticos nas linhas de montagem da Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="3aba7-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="3aba7-114">A Fabrikam fornece serviços de instalação, mas os braços robóticos são adquiridos da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3aba7-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="3aba7-115">Se a instalação de braços robóticos na Adatum Corporation abrir uma nova vertical de setor para a Trey Research, a Trey poderá oferecer um desconto especial referente a esse negócio à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="3aba7-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="3aba7-116">Nesse caso, a Fabrikam cria uma linha de contrato com base em produto para Braços Robóticos e insere um custo por unidade para esse contrato, que é diferente do custo padrão de braços robóticos da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3aba7-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
