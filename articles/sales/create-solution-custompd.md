---
title: Criar uma solução para dimensões de precificação personalizadas
description: Esse tópico fornece informações sobre como criar soluções para dimensões de precificação personalizadas.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513957"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="73e42-103">Criar uma solução para dimensões de precificação personalizadas</span><span class="sxs-lookup"><span data-stu-id="73e42-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="73e42-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="73e42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="73e42-105">Todas as alterações de dimensão de preço personalizada devem ficar em uma solução separada.</span><span class="sxs-lookup"><span data-stu-id="73e42-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="73e42-106">Essa importante prática recomendada oferece a flexibilidade para atualizar ou remover alterações conforme a necessidade, ajuda com a reutilização do seu trabalho e facilita a locomoção dessas alterações para outras instâncias.</span><span class="sxs-lookup"><span data-stu-id="73e42-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="73e42-107">Depois de fazer todas as alterações necessárias, exporte essa solução como uma solução **Gerenciada** e importe-a em outras instâncias para a reutilização.</span><span class="sxs-lookup"><span data-stu-id="73e42-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="73e42-108">Criar uma solução para dimensões de precificação personalizadas</span><span class="sxs-lookup"><span data-stu-id="73e42-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="73e42-109">Selecione **Configurações** > **Soluções** e selecione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="73e42-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="73e42-110">Nomeie a solução *dimensões de precificação de <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="73e42-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="73e42-111">Insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="73e42-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Criação de uma solução de dimensão de precificação personalizada](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="73e42-113">Adicionar todas as entidades necessárias e componentes relacionados à Solução de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="73e42-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="73e42-114">Adicione as seguintes entidades do Project Service à sua solução de preços para fazer alterações importantes no esquema da solução de preços.</span><span class="sxs-lookup"><span data-stu-id="73e42-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="73e42-115">Depois de concluir este procedimento, as entidades reconhecerão as novas dimensões de precificação.</span><span class="sxs-lookup"><span data-stu-id="73e42-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="73e42-116">Selecione **Configurações** > **Soluções** e clique duas vezes em **dimensões de precificação da <*nome de sua organização*>**.</span><span class="sxs-lookup"><span data-stu-id="73e42-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="73e42-117">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="73e42-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="73e42-118">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="73e42-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="73e42-119">**Real**</span><span class="sxs-lookup"><span data-stu-id="73e42-119">**Actual**</span></span>
   - <span data-ttu-id="73e42-120">**Recurso Reservável**</span><span class="sxs-lookup"><span data-stu-id="73e42-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="73e42-121">**Linha de Estimativa**</span><span class="sxs-lookup"><span data-stu-id="73e42-121">**Estimate Line**</span></span>
   - <span data-ttu-id="73e42-122">**Tarefa do Projeto**</span><span class="sxs-lookup"><span data-stu-id="73e42-122">**Project Task**</span></span>
   - <span data-ttu-id="73e42-123">**Detalhe da Linha da Fatura**</span><span class="sxs-lookup"><span data-stu-id="73e42-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="73e42-124">**Linha do Diário**</span><span class="sxs-lookup"><span data-stu-id="73e42-124">**Journal Line**</span></span>
   - <span data-ttu-id="73e42-125">**Detalhe da Linha de Contrato do Projeto**</span><span class="sxs-lookup"><span data-stu-id="73e42-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="73e42-126">**Membro da Equipe do Projeto**</span><span class="sxs-lookup"><span data-stu-id="73e42-126">**Project Team Member**</span></span>
   - <span data-ttu-id="73e42-127">**Detalhes da Linha de Cotação**</span><span class="sxs-lookup"><span data-stu-id="73e42-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="73e42-128">**Markup de Preço da Função**</span><span class="sxs-lookup"><span data-stu-id="73e42-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="73e42-129">**Preço da Função**</span><span class="sxs-lookup"><span data-stu-id="73e42-129">**Role Price**</span></span>
   - <span data-ttu-id="73e42-130">**Entrada de Hora**</span><span class="sxs-lookup"><span data-stu-id="73e42-130">**Time Entry**</span></span>
 
   ![Adicionar entidades existentes à solução de dimensões de precificação](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="73e42-132">Em cada entidade, revise os componentes que estão sendo adicionados e a lista final de ativos da entidade para cada entidade.</span><span class="sxs-lookup"><span data-stu-id="73e42-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="73e42-133">Inclua todos os formulários e exibições para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="73e42-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entidades adicionadas](./media/solution-component-selection.png)


5.  <span data-ttu-id="73e42-135">Nas entidades selecionadas, quando for solicitado a incluir entidades dependentes, selecione **Não, não incluir os componentes necessários.**</span><span class="sxs-lookup"><span data-stu-id="73e42-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Incluindo entidades dependentes](./media/Do-not-include-required.png)
