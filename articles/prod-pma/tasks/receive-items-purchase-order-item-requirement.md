---
title: Receber itens no pedido de compra a partir da solicitação
description: Este tópico explica como receber itens em um pedido de compra de um requisito de item.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2083516ff929113fd6db377acfe5aeb104666dd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288214"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="6f1a9-103">Receber itens no pedido de compra a partir da solicitação</span><span class="sxs-lookup"><span data-stu-id="6f1a9-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f1a9-104">Este tópico explica como receber itens em um pedido de compra de um requisito de item.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="6f1a9-105">Ao usar uma necessidade de item em vez de uma transação de item, você pode planejar a entrega pouco antes de o item ser realmente usado, criar um pedido de compra, incluir o item na estrutura do contrato comercial e incluir a necessidade do item no planejamento da produção.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="6f1a9-106">Esta tarefa usa o conjunto de dados USSI.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6f1a9-107">No painel de navegação, vá para **Módulos > Gerenciamento e contabilidade de projetos > Projetos > Todos os projetos**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="6f1a9-108">Na lista, selecione o link na linha desejada.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="6f1a9-109">No Painel de Ação, selecione **Plano**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="6f1a9-110">Selecione **Requisitos do item**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="6f1a9-111">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-111">Select **New**.</span></span>
6. <span data-ttu-id="6f1a9-112">Na nova linha, insira ou selecione um valor no campo **Número de item**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="6f1a9-113">No campo **Quantidade**, insira um número.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="6f1a9-114">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-114">Select **Save**.</span></span>
9. <span data-ttu-id="6f1a9-115">No Painel de Ação, selecione **Gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="6f1a9-116">Selecione **Funções**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-116">Select **Functions**.</span></span>
11. <span data-ttu-id="6f1a9-117">Selecione **Criar uma ordem de compra**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="6f1a9-118">Marque a caixa de seleção **Incluir todos**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="6f1a9-119">No campo **Conta do vendedor**, digite ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="6f1a9-120">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-120">Select **OK**.</span></span>
15. <span data-ttu-id="6f1a9-121">No painel de navegação, vá para **Módulos > Contas a pagar > Pedidos de compra > Todos os pedidos de compra**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="6f1a9-122">Na lista, selecione o link na linha desejada.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="6f1a9-123">No Painel de Ação, selecione **Compra**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="6f1a9-124">Selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="6f1a9-125">No Painel de Ação, selecione **Receber**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="6f1a9-126">Selecione **Recibo do produto**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="6f1a9-127">No campo **Recibo de produto**, digite um valor.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="6f1a9-128">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]