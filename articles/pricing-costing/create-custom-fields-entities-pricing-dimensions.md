---
title: Criar campos e entidades personalizados como dimensões de preços
description: Este tópico fornece informações sobre como criar conjuntos de opções ou entidades personalizadas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130879"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="bdf12-103">Criar campos e entidades personalizados como dimensões de preços</span><span class="sxs-lookup"><span data-stu-id="bdf12-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="bdf12-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="bdf12-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bdf12-105">Conclua as etapas a seguir sempre que quiser criar uma entidade ou um conjunto de opções personalizado.</span><span class="sxs-lookup"><span data-stu-id="bdf12-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bdf12-106">É recomendável fazer todas as alterações de dimensão de preço personalizadas em outra solução.</span><span class="sxs-lookup"><span data-stu-id="bdf12-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="bdf12-107">Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="bdf12-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="bdf12-108">Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a em outras instâncias para reutilizar sua configuração de preço.</span><span class="sxs-lookup"><span data-stu-id="bdf12-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="bdf12-109">Criar uma solução personalizada para dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="bdf12-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="bdf12-110">Vá para **Configurações** > **Soluções** e selecione **Novo** para criar uma nova solução.</span><span class="sxs-lookup"><span data-stu-id="bdf12-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="bdf12-111">Nomeie a solução, **dimensões de preço da \<your organization name>**, insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="bdf12-112">Criar campos e conjuntos de opções personalizados na solução de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="bdf12-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="bdf12-113">Uma dimensão de preço pode ser um conjunto de opções ou uma entidade.</span><span class="sxs-lookup"><span data-stu-id="bdf12-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="bdf12-114">Ambos deve ser criados em sua solução de preço.</span><span class="sxs-lookup"><span data-stu-id="bdf12-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="bdf12-115">As etapas deste procedimento explicam como criar dimensões baseadas em entidade e dimensões baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="bdf12-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="bdf12-116">Dimensões baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="bdf12-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="bdf12-117">Vá para **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="bdf12-118">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="bdf12-119">Selecione **Novo** para criar uma nova entidade denominada **Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="bdf12-120">Insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="bdf12-121">Dimensões baseadas em conjunto de opções</span><span class="sxs-lookup"><span data-stu-id="bdf12-121">Option set-based dimensions</span></span> 
<span data-ttu-id="bdf12-122">Você pode criar duas dimensões baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="bdf12-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="bdf12-123">Use **Local de Trabalho do Recurso** para rastrear o preço do trabalho do local **Página Inicial** e do trabalho **No Local** e use **Horas de Trabalho do Recurso** com os valores **Regular** e **Horas Extras** para aplicar um markup quando o trabalho é concluído.</span><span class="sxs-lookup"><span data-stu-id="bdf12-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="bdf12-124">Vá para **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="bdf12-125">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Conjuntos de Opções**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="bdf12-126">Selecione **Novo** para criar um novo conjunto de opções, insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="bdf12-127">Criar dados para dimensões baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="bdf12-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="bdf12-128">Você pode criar dados para dimensões baseadas em entidade manualmente, ou usando a importação ou as chamadas de serviço do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bdf12-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="bdf12-129">Use as etapas neste procedimento para criar dois cargos padrões, **Engenheiro de Sistemas** e **Engenheiro de Sistemas Sênior** na dimensão baseada em entidade, **Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="bdf12-130">Se os dados que quiser criar forem pequenos, como no exemplo a seguir, você poderá usar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="bdf12-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="bdf12-131">Selecione **Pesquisa Avançada**, a entidade **Cargo Padrão** e, depois, **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="bdf12-132">Todas as linhas na entidade **Cargo Padrão** serão mostradas.</span><span class="sxs-lookup"><span data-stu-id="bdf12-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="bdf12-133">Selecione **Novo** e, no campo **Nome**, insira "Engenheiro de Sistemas" e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="bdf12-134">Fechar o formulário.</span><span class="sxs-lookup"><span data-stu-id="bdf12-134">Close the form.</span></span> 
4. <span data-ttu-id="bdf12-135">Repita as etapas de 1 a 3 para criar outro cargo padrão para "Engenheiro de Sistemas Sênior".</span><span class="sxs-lookup"><span data-stu-id="bdf12-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="bdf12-136">Adicionar todas as entidades necessárias e componentes relacionados à Solução de Dimensão de Preço</span><span class="sxs-lookup"><span data-stu-id="bdf12-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="bdf12-137">Você precisará adicionar as entidades a seguir à solução de preço.</span><span class="sxs-lookup"><span data-stu-id="bdf12-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="bdf12-138">Use as etapas neste procedimento para fazer algumas alterações importantes de esquema na solução de precificação para que as entidades se tornem conscientes das novas dimensões de preço.</span><span class="sxs-lookup"><span data-stu-id="bdf12-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="bdf12-139">Selecione **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="bdf12-140">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="bdf12-141">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="bdf12-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="bdf12-142">Real</span><span class="sxs-lookup"><span data-stu-id="bdf12-142">Actual</span></span>
  - <span data-ttu-id="bdf12-143">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="bdf12-143">Bookable Resource</span></span>
  - <span data-ttu-id="bdf12-144">Linha de Estimativa</span><span class="sxs-lookup"><span data-stu-id="bdf12-144">Estimate Line</span></span>
  - <span data-ttu-id="bdf12-145">Detalhes da Linha da Fatura</span><span class="sxs-lookup"><span data-stu-id="bdf12-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="bdf12-146">Linha do Diário</span><span class="sxs-lookup"><span data-stu-id="bdf12-146">Journal Line</span></span>
  - <span data-ttu-id="bdf12-147">Detalhes da Linha de Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="bdf12-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="bdf12-148">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="bdf12-148">Project Team Member</span></span>
  - <span data-ttu-id="bdf12-149">Detalhe da Linha de Cotação</span><span class="sxs-lookup"><span data-stu-id="bdf12-149">Quote Line Detail</span></span>
  - <span data-ttu-id="bdf12-150">Markup de Preço da Função</span><span class="sxs-lookup"><span data-stu-id="bdf12-150">Role Price Markup</span></span>
  - <span data-ttu-id="bdf12-151">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="bdf12-151">Role Price</span></span> 
  - <span data-ttu-id="bdf12-152">Entrada de Hora</span><span class="sxs-lookup"><span data-stu-id="bdf12-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="bdf12-153">Certifique-se de incluir todos os formulários e exibições para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="bdf12-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="bdf12-154">Quando solicitado a incluir entidades dependentes para as entidades selecionadas acima, selecione **Não**.</span><span class="sxs-lookup"><span data-stu-id="bdf12-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

