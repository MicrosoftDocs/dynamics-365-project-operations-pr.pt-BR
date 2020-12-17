---
title: Criar campos e entidades personalizados como dimensões de preços
description: Este tópico fornece informações sobre como criar conjuntos de opções ou entidades personalizadas.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642799"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="eadbd-103">Criar campos e entidades personalizados como dimensões de preços</span><span class="sxs-lookup"><span data-stu-id="eadbd-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="eadbd-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="eadbd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eadbd-105">Conclua as etapas a seguir quando quiser criar uma entidade ou um conjunto de opções personalizado para usar como dimensão de precificação.</span><span class="sxs-lookup"><span data-stu-id="eadbd-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="eadbd-106">Para obter mais informações, consulte [Visão geral de dimensões de precificação](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eadbd-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="eadbd-107">É recomendável fazer todas as alterações de dimensão de preço personalizadas em outra solução.</span><span class="sxs-lookup"><span data-stu-id="eadbd-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="eadbd-108">Esta importante prática recomendada fornece flexibilidade no futuro para atualizar ou remover as alterações conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="eadbd-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="eadbd-109">Isso também ajudará na reutilização do trabalho e facilitará a portabilidade dessas alterações para outra instância. Depois de fazer todas as alterações necessárias, exporte essa solução como **Solução gerenciada** e importe-a para outras instâncias para reutilizar a configuração de preços.</span><span class="sxs-lookup"><span data-stu-id="eadbd-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="eadbd-110">Criar campos e conjuntos de opções personalizados na solução de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="eadbd-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="eadbd-111">Uma dimensão de preço pode ser um conjunto de opções ou uma entidade.</span><span class="sxs-lookup"><span data-stu-id="eadbd-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="eadbd-112">Ambos deve ser criados em sua solução de preço.</span><span class="sxs-lookup"><span data-stu-id="eadbd-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="eadbd-113">As etapas deste procedimento explicam como criar dimensões baseadas em entidade e dimensões baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="eadbd-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="eadbd-114">Dimensões baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="eadbd-114">Entity-based dimensions</span></span>
<span data-ttu-id="eadbd-115">Para criar dimensões baseadas em entidade, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="eadbd-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="eadbd-116">Vá para **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="eadbd-117">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="eadbd-118">Selecione **Novo** para criar uma nova entidade denominada **Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="eadbd-119">Insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definição da entidade de cargo padrão](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="eadbd-121">Dimensões baseadas em conjunto de opções</span><span class="sxs-lookup"><span data-stu-id="eadbd-121">Option set-based dimensions</span></span> 
<span data-ttu-id="eadbd-122">Você pode criar duas dimensões baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="eadbd-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="eadbd-123">Use **Local de Trabalho do Recurso** para rastrear o preço do local de trabalho **Casa** e trabalho **No local**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="eadbd-124">Use **Horas de trabalho do recurso** com valores **Regular** e **Hora extra** para aplicar uma marcação quando o trabalho for concluído.</span><span class="sxs-lookup"><span data-stu-id="eadbd-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="eadbd-125">O gráfico a seguir fornece uma exibição da dimensão de **Local do Trabalho do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimensão de preço baseada em conjunto de opções chamada Local de Trabalho do Recurso](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="eadbd-127">O gráfico a seguir fornece uma exibição da dimensão de **Horas de Trabalho do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimensão de preço baseada em conjunto de opções chamada Horas de Trabalho do Recurso](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="eadbd-129">Vá para **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="eadbd-130">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Conjuntos de Opções**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="eadbd-131">Selecione **Novo** para criar um novo conjunto de opções, insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="eadbd-132">Criar dados para dimensões baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="eadbd-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="eadbd-133">Você pode criar dados para dimensões baseadas em entidade manualmente, ou usando a importação ou as chamadas de serviço do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="eadbd-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="eadbd-134">Use as etapas neste procedimento para criar dois cargos padrões, **Engenheiro de Sistemas** e **Engenheiro de Sistemas Sênior** na dimensão baseada em entidade, **Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="eadbd-135">Se os dados que quiser criar forem pequenos, como no exemplo a seguir, você poderá usar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="eadbd-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="eadbd-136">Selecione **Localização Avançada**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="eadbd-137">Selecione a entidade **Cargo Padrão** e selecione **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="eadbd-138">Todas as linhas na entidade **Cargo Padrão** serão mostradas.</span><span class="sxs-lookup"><span data-stu-id="eadbd-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="eadbd-139">Selecione **Novo** e, no campo **Nome**, insira "Engenheiro de Sistemas" e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="eadbd-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="eadbd-140">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="eadbd-140">Close the page.</span></span> 
5. <span data-ttu-id="eadbd-141">Repita as etapas de 1 a 3 para criar outro cargo padrão para "Engenheiro de Sistemas Sênior".</span><span class="sxs-lookup"><span data-stu-id="eadbd-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Dados de exemplo para a entidade Cargo Padrão](media/ST-data.png)
