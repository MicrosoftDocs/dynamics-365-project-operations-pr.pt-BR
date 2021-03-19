---
title: Pedidos de compra de um projeto
description: Este artigo descreve os vários métodos que você pode usar para criar pedidos de compra para um projeto. O método que você utiliza depende da finalidade do pedido de compra e de quando os itens adquiridos são consumidos e cobrados de um projeto.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289175"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="2662b-104">Pedidos de compra de um projeto</span><span class="sxs-lookup"><span data-stu-id="2662b-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2662b-105">Este artigo descreve os vários métodos que você pode usar para criar pedidos de compra para um projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="2662b-106">O método que você utiliza depende da finalidade do pedido de compra e de quando os itens adquiridos são consumidos e cobrados de um projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="2662b-107">Métodos para criar um pedido de compra</span><span class="sxs-lookup"><span data-stu-id="2662b-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="2662b-108">Você pode usar um dos métodos a seguir para criar um pedido de compra no gerenciamento e contabilidade de projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="2662b-109">A finalidade do pedido de compra determina quando o pedido de compra é consumido e, portanto, quando os itens são cobrados de um projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2662b-110">Método</span><span class="sxs-lookup"><span data-stu-id="2662b-110">Method</span></span></th>
<th><span data-ttu-id="2662b-111">Finalidade</span><span class="sxs-lookup"><span data-stu-id="2662b-111">Purpose</span></span></th>
<th><span data-ttu-id="2662b-112">Consumo de itens</span><span class="sxs-lookup"><span data-stu-id="2662b-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2662b-113">Crie um pedido de compra diretamente em um projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="2662b-114">Use esse método para comprar itens de um fornecedor externo para consumo em um projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="2662b-115">Você pode criar o pedido de compra de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="2662b-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="2662b-116">No próprio projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-116">From the project itself.</span></span> <span data-ttu-id="2662b-117">Nesse caso, o projeto já está definido para o pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="2662b-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="2662b-118">Navegando até o pedido de compra do projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="2662b-119">Você deve selecionar o fornecedor e o projeto para o qual criar o pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="2662b-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="2662b-120">Os itens são consumidos quando a fatura do fornecedor é atualizada.</span><span class="sxs-lookup"><span data-stu-id="2662b-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2662b-121">Crie um pedido de compra em um pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="2662b-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="2662b-122">Use esse método para comprar itens ao criar um pedido de venda em um projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="2662b-123">Os itens são consumidos quando o pedido de venda é faturado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="2662b-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2662b-124">Crie um pedido de compra em uma solicitação de item.</span><span class="sxs-lookup"><span data-stu-id="2662b-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="2662b-125">Use esse método para comprar itens ao criar uma solicitação de item em um projeto.</span><span class="sxs-lookup"><span data-stu-id="2662b-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="2662b-126">Os itens são consumidos quando a guia de remessa da solicitação do item é atualizada.</span><span class="sxs-lookup"><span data-stu-id="2662b-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="2662b-127">Quando você atualiza a fatura do fornecedor ou a guia de remessa, é solicitado que atualize a guia de remessa na solicitação do item.</span><span class="sxs-lookup"><span data-stu-id="2662b-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="2662b-128">Para obter mais informações, consulte [Receber itens no pedido de compra em uma solicitação de item](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="2662b-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]