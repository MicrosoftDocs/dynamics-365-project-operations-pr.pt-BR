---
title: Criar uma solução para dimensões de precificação personalizadas
description: Esse tópico fornece informações sobre como criar soluções para dimensões de precificação personalizadas.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010322"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="2388c-103">Criar uma solução para dimensões de precificação personalizadas</span><span class="sxs-lookup"><span data-stu-id="2388c-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="2388c-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="2388c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="2388c-105">Todas as alterações de dimensão de preço personalizada devem ficar em uma solução separada.</span><span class="sxs-lookup"><span data-stu-id="2388c-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="2388c-106">Essa importante prática recomendada oferece a flexibilidade para atualizar ou remover alterações conforme a necessidade, ajuda com a reutilização do seu trabalho e facilita a locomoção dessas alterações para outras instâncias.</span><span class="sxs-lookup"><span data-stu-id="2388c-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="2388c-107">Depois de fazer todas as alterações necessárias, exporte essa solução como uma solução **Gerenciada** e importe-a em outras instâncias para a reutilização.</span><span class="sxs-lookup"><span data-stu-id="2388c-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="2388c-108">Criar uma solução para dimensões de precificação personalizadas</span><span class="sxs-lookup"><span data-stu-id="2388c-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="2388c-109">Selecione **Configurações** > **Soluções** e selecione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="2388c-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="2388c-110">Nomeie a solução *dimensões de precificação de <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="2388c-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="2388c-111">Insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="2388c-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Criação de uma solução de dimensão de precificação personalizada](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="2388c-113">Adicionar todas as entidades necessárias e componentes relacionados à Solução de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="2388c-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="2388c-114">Adicione as seguintes entidades do Project Service à sua solução de preços para fazer alterações importantes no esquema da solução de preços.</span><span class="sxs-lookup"><span data-stu-id="2388c-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="2388c-115">Depois de concluir este procedimento, as entidades reconhecerão as novas dimensões de precificação.</span><span class="sxs-lookup"><span data-stu-id="2388c-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="2388c-116">Selecione **Configurações** > **Soluções** e clique duas vezes em **dimensões de precificação da <*nome de sua organização*>**.</span><span class="sxs-lookup"><span data-stu-id="2388c-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="2388c-117">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="2388c-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="2388c-118">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="2388c-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="2388c-119">**Real**</span><span class="sxs-lookup"><span data-stu-id="2388c-119">**Actual**</span></span>
   - <span data-ttu-id="2388c-120">**Recurso Reservável**</span><span class="sxs-lookup"><span data-stu-id="2388c-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="2388c-121">**Linha de Estimativa**</span><span class="sxs-lookup"><span data-stu-id="2388c-121">**Estimate Line**</span></span>
   - <span data-ttu-id="2388c-122">**Tarefa do Projeto**</span><span class="sxs-lookup"><span data-stu-id="2388c-122">**Project Task**</span></span>
   - <span data-ttu-id="2388c-123">**Detalhe da Linha da Fatura**</span><span class="sxs-lookup"><span data-stu-id="2388c-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="2388c-124">**Linha do Diário**</span><span class="sxs-lookup"><span data-stu-id="2388c-124">**Journal Line**</span></span>
   - <span data-ttu-id="2388c-125">**Detalhe da Linha de Contrato do Projeto**</span><span class="sxs-lookup"><span data-stu-id="2388c-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="2388c-126">**Membro da Equipe do Projeto**</span><span class="sxs-lookup"><span data-stu-id="2388c-126">**Project Team Member**</span></span>
   - <span data-ttu-id="2388c-127">**Detalhes da Linha de Cotação**</span><span class="sxs-lookup"><span data-stu-id="2388c-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="2388c-128">**Markup de Preço da Função**</span><span class="sxs-lookup"><span data-stu-id="2388c-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="2388c-129">**Preço da Função**</span><span class="sxs-lookup"><span data-stu-id="2388c-129">**Role Price**</span></span>
   - <span data-ttu-id="2388c-130">**Entrada de Hora**</span><span class="sxs-lookup"><span data-stu-id="2388c-130">**Time Entry**</span></span>
 
   ![Adicionar entidades existentes à solução de dimensões de precificação](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="2388c-132">Em cada entidade, revise os componentes que estão sendo adicionados e a lista final de ativos da entidade para cada entidade.</span><span class="sxs-lookup"><span data-stu-id="2388c-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="2388c-133">Inclua todos os formulários e exibições para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="2388c-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entidades adicionadas](./media/solution-component-selection.png)


5.  <span data-ttu-id="2388c-135">Nas entidades selecionadas, quando for solicitado a incluir entidades dependentes, selecione **Não, não incluir os componentes necessários.**</span><span class="sxs-lookup"><span data-stu-id="2388c-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Incluindo entidades dependentes](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]