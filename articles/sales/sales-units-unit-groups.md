---
title: Unidades e grupos de unidades
description: Este tópico fornece informações sobre como criar unidades e grupos de unidades no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071551"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="84d8c-103">Unidades e grupos de unidades</span><span class="sxs-lookup"><span data-stu-id="84d8c-103">Units and unit groups</span></span>

<span data-ttu-id="84d8c-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="84d8c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="84d8c-105">As unidades são as quantidades ou as medidas em que você vende seus produtos ou serviços.</span><span class="sxs-lookup"><span data-stu-id="84d8c-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="84d8c-106">Por exemplo, se você vende produtos de jardinagem, é possível vender sementes em unidades de pacotes, caixas e paletes.</span><span class="sxs-lookup"><span data-stu-id="84d8c-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="84d8c-107">Um grupo de unidades é uma coleção dessas unidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="84d8c-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="84d8c-108">Para concluir as etapas neste tópico, verifique se você foi atribuído à função Administrador do Sistema ou Gerente do Sales Professional ou se tem permissões equivalentes.</span><span class="sxs-lookup"><span data-stu-id="84d8c-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="84d8c-109">Criar um grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="84d8c-109">Create a unit group</span></span>

1. <span data-ttu-id="84d8c-110">No mapa do site, selecione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="84d8c-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="84d8c-111">Selecione **Novo** e, na caixa de diálogo **Criar Grupo de Unidades** , insira o nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="84d8c-111">Select **New** , and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="84d8c-112">No campo **Unidade principal** , insira a menor unidade de medida comum em que o produto será vendido.</span><span class="sxs-lookup"><span data-stu-id="84d8c-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="84d8c-113">Por exemplo, você pode inserir "peça" ou "onça".</span><span class="sxs-lookup"><span data-stu-id="84d8c-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="84d8c-114">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="84d8c-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="84d8c-115">Adicionar unidades a um grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="84d8c-115">Add units to a unit group</span></span>

1. <span data-ttu-id="84d8c-116">Abra um grupo de unidades e, na guia **Relacionado** , selecione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="84d8c-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="84d8c-117">Você verá que a unidade principal já foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="84d8c-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="84d8c-118">Selecione **Adicionar Nova Unidade** e, na página **Criação Rápida: Unidade** , no campo **Nome** , insira o nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="84d8c-118">Select **Add New Unit** , and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="84d8c-119">No campo **Quantidade** , insira a quantidade que a unidade conterá.</span><span class="sxs-lookup"><span data-stu-id="84d8c-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="84d8c-120">Por exemplo, se uma caixa contiver duas peças, insira "2".</span><span class="sxs-lookup"><span data-stu-id="84d8c-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="84d8c-121">No campo **Unidade base** , selecione uma unidade base para estabelecer a menor unidade de medida para a unidade.</span><span class="sxs-lookup"><span data-stu-id="84d8c-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="84d8c-122">Por exemplo, você pode selecionar "Peça".</span><span class="sxs-lookup"><span data-stu-id="84d8c-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="84d8c-123">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="84d8c-123">Select **Save** :</span></span>
