---
title: Desativar listas de preços
description: Este tópico explica como desativar ou remover listas de preços antigas ou não utilizadas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001322"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="35d53-103">Desativar listas de preços</span><span class="sxs-lookup"><span data-stu-id="35d53-103">Deactivate price lists</span></span> 

<span data-ttu-id="35d53-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="35d53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="35d53-105">Para remover listas de preços antigas ou não utilizadas do Dynamics 365 Project Operations, há duas etapas que você deve concluir.</span><span class="sxs-lookup"><span data-stu-id="35d53-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="35d53-106">Remova ou exclua a lista de preços de páginas específicas.</span><span class="sxs-lookup"><span data-stu-id="35d53-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="35d53-107">Desative ou exclua a lista de preços das listas de preços ativas na página **Lista de Preços**.</span><span class="sxs-lookup"><span data-stu-id="35d53-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="35d53-108">Você deve concluir as duas etapas para remover totalmente uma lista de preços.</span><span class="sxs-lookup"><span data-stu-id="35d53-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="35d53-109">Apenas executar a etapa 2, que é excluir ou desativar diretamente a lista de preços da exibição Listas de Preços Ativas, não é suficiente.</span><span class="sxs-lookup"><span data-stu-id="35d53-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="35d53-110">Você também deve excluir a associação desta lista de preços de todos os locais mencionados na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="35d53-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="35d53-111">Exclua a lista de preços de páginas específicas</span><span class="sxs-lookup"><span data-stu-id="35d53-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="35d53-112">Para excluir uma lista de preços do Project Operations, vá para as seguintes páginas:</span><span class="sxs-lookup"><span data-stu-id="35d53-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="35d53-113">Página **Parâmetros do projeto** > guia **Listas de Preços**</span><span class="sxs-lookup"><span data-stu-id="35d53-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="35d53-114">Página **Unidade Organizacional** > grade **Listas de Preços**</span><span class="sxs-lookup"><span data-stu-id="35d53-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="35d53-115">Página **Conta** > grade **Listas de Preços do Projeto**</span><span class="sxs-lookup"><span data-stu-id="35d53-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="35d53-116">Página **Cotações do Projeto** > grade **Listas de Preços do Projeto**: Isso se aplica a todas as cotações de projetos ativos.</span><span class="sxs-lookup"><span data-stu-id="35d53-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="35d53-117">Página **Contratos do Projeto** > grade **Listas de Preços do Projeto**: Isso se aplica a todos os contratos de projetos ativos.</span><span class="sxs-lookup"><span data-stu-id="35d53-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="35d53-118">Para cada página, você precisa selecionar a lista de preços que deseja excluir e, em seguida, selecionar **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="35d53-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="35d53-119">Exclua ou desativa a lista de preços da página Listas de Preços</span><span class="sxs-lookup"><span data-stu-id="35d53-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="35d53-120">Para excluir uma lista de preços das listas de preços ativas, vá para **Vendas** > **Clientes** > **Lista de Preços**.</span><span class="sxs-lookup"><span data-stu-id="35d53-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="35d53-121">Selecione a lista de preços que deseja excluir e escolha **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="35d53-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="35d53-122">Se a lista de preços for referenciada em qualquer transação existente, você não poderá excluí-la.</span><span class="sxs-lookup"><span data-stu-id="35d53-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="35d53-123">Se isso acontecer, você pode desativar a lista de preços para que ela não apareça em nenhuma visualização.</span><span class="sxs-lookup"><span data-stu-id="35d53-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="35d53-124">Para desativar a lista de preços, selecione a lista de preços novamente e escolha **Desativar**.</span><span class="sxs-lookup"><span data-stu-id="35d53-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
