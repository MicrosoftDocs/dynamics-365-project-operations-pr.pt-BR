---
title: Criar campos e entidades personalizados
description: Este tópico explica como criar conjuntos de opções e entidades em sua própria solução na plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749140"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="360e9-103">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="360e9-103">Create custom fields and entities</span></span> 

<span data-ttu-id="360e9-104">Conclua as etapas a seguir sempre que quiser criar uma entidade ou um conjunto de opções personalizado na plataforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="360e9-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="360e9-105">Os procedimentos neste tópico devem ser concluídos usando a interface da Web do PSA (Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="360e9-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="360e9-106">É recomendável fazer todas as alterações de dimensão de preço personalizadas em outra solução.</span><span class="sxs-lookup"><span data-stu-id="360e9-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="360e9-107">Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="360e9-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="360e9-108">Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a em outras instâncias para reutilizar sua configuração de preço.</span><span class="sxs-lookup"><span data-stu-id="360e9-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="360e9-109">Criar uma solução personalizada para dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="360e9-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="360e9-110">No PSA, clique em **Configurações** > **Soluções** e em **Novo** para criar uma solução.</span><span class="sxs-lookup"><span data-stu-id="360e9-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="360e9-111">Nomeie a solução, **dimensões de preço da \<nome da sua organização>**, insira as informações necessárias restantes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="360e9-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Criando uma solução personalizada para dimensões de preço](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="360e9-113">Criar campos e conjuntos de opções personalizados na solução de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="360e9-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="360e9-114">Uma dimensão de preço pode ser um conjunto de opções ou uma entidade.</span><span class="sxs-lookup"><span data-stu-id="360e9-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="360e9-115">Ambos deve ser criados em sua solução de preço.</span><span class="sxs-lookup"><span data-stu-id="360e9-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="360e9-116">As etapas deste procedimento explicam como criar dimensões baseadas em entidade e dimensões baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="360e9-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="360e9-117">Dimensões baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="360e9-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="360e9-118">No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<nome da sua organização>**.</span><span class="sxs-lookup"><span data-stu-id="360e9-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="360e9-119">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="360e9-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="360e9-120">Clique em **Novo** para criar uma nova entidade denominada **Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="360e9-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="360e9-121">Insira as informações necessárias restantes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="360e9-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definição da entidade de cargo padrão](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="360e9-123">Dimensões baseadas em conjunto de opções</span><span class="sxs-lookup"><span data-stu-id="360e9-123">Option set-based dimensions</span></span> 
<span data-ttu-id="360e9-124">Você pode criar duas dimensões baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="360e9-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="360e9-125">Use **Local de Trabalho do Recurso** para rastrear o preço do trabalho do local **Página Inicial** e do trabalho **No Local** e use **Horas de Trabalho do Recurso** com os valores **Regular** e **Horas Extras** para aplicar um markup quando o trabalho é concluído.</span><span class="sxs-lookup"><span data-stu-id="360e9-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="360e9-126">No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<nome da sua organização>**.</span><span class="sxs-lookup"><span data-stu-id="360e9-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="360e9-127">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Conjuntos de Opções**.</span><span class="sxs-lookup"><span data-stu-id="360e9-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="360e9-128">Clique em **Novo** para criar um novo conjunto de opções, insira as informações necessárias restantes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="360e9-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="360e9-129">Dimensão de preço baseada em conjunto de opções chamada Local de Trabalho do Recurso</span><span class="sxs-lookup"><span data-stu-id="360e9-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="360e9-130">Dimensão de preço baseada em conjunto de opções chamada Horas de Trabalho do Recurso</span><span class="sxs-lookup"><span data-stu-id="360e9-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="360e9-131">Criar dados para dimensões baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="360e9-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="360e9-132">Você pode criar dados para dimensões baseadas em entidade manualmente, ou usando a importação ou as chamadas de serviço do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="360e9-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="360e9-133">Use as etapas neste procedimento para criar dois cargos padrões, **Engenheiro de Sistemas** e **Engenheiro de Sistemas Sênior** na dimensão baseada em entidade, **Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="360e9-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="360e9-134">Se os dados que quiser criar forem pequenos, como no exemplo a seguir, você poderá usar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="360e9-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="360e9-135">No PSA, clique em **Localização Avançada**.</span><span class="sxs-lookup"><span data-stu-id="360e9-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="360e9-136">Selecione a entidade **Cargo Padrão** e clique em **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="360e9-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="360e9-137">Todas as linhas na entidade **Cargo Padrão** serão mostradas.</span><span class="sxs-lookup"><span data-stu-id="360e9-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="360e9-138">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="360e9-138">Click **New**.</span></span> <span data-ttu-id="360e9-139">No campo **Nome**, insira "Engenheiro de Sistemas" e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="360e9-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="360e9-140">Feche o formulário.</span><span class="sxs-lookup"><span data-stu-id="360e9-140">Close the form.</span></span> 
4. <span data-ttu-id="360e9-141">Repita as etapas de 1 a 3 para criar outro cargo padrão para "Engenheiro de Sistemas Sênior".</span><span class="sxs-lookup"><span data-stu-id="360e9-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="360e9-142">Dados de Exemplo para a entidade Cargo Padrão</span><span class="sxs-lookup"><span data-stu-id="360e9-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="360e9-143">Adicionar todas as entidades necessárias e componentes relacionados do PSA à Solução de Dimensão de Preço</span><span class="sxs-lookup"><span data-stu-id="360e9-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="360e9-144">Você precisará adicionar as entidades a seguir do Project Service à sua solução de precificação.</span><span class="sxs-lookup"><span data-stu-id="360e9-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="360e9-145">Use as etapas neste procedimento para fazer algumas alterações importantes de esquema na solução de precificação para que as entidades se tornem conscientes das novas dimensões de preço.</span><span class="sxs-lookup"><span data-stu-id="360e9-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="360e9-146">No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<nome da sua organização>**.</span><span class="sxs-lookup"><span data-stu-id="360e9-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="360e9-147">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="360e9-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="360e9-148">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="360e9-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="360e9-149">Real</span><span class="sxs-lookup"><span data-stu-id="360e9-149">Actual</span></span>
- <span data-ttu-id="360e9-150">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="360e9-150">Bookable Resource</span></span>
- <span data-ttu-id="360e9-151">Linha de Estimativa</span><span class="sxs-lookup"><span data-stu-id="360e9-151">Estimate Line</span></span>
- <span data-ttu-id="360e9-152">Detalhes da Linha da Fatura</span><span class="sxs-lookup"><span data-stu-id="360e9-152">Invoice Line Detail</span></span>
- <span data-ttu-id="360e9-153">Linha do Diário</span><span class="sxs-lookup"><span data-stu-id="360e9-153">Journal Line</span></span>
- <span data-ttu-id="360e9-154">Detalhes da Linha de Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="360e9-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="360e9-155">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="360e9-155">Project Team Member</span></span>
- <span data-ttu-id="360e9-156">Detalhes da Linha de Cotação</span><span class="sxs-lookup"><span data-stu-id="360e9-156">Quote Line Detail</span></span>
- <span data-ttu-id="360e9-157">Markup de Preço da Função</span><span class="sxs-lookup"><span data-stu-id="360e9-157">Role Price Markup</span></span>
- <span data-ttu-id="360e9-158">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="360e9-158">Role Price</span></span> 
- <span data-ttu-id="360e9-159">Entrada de Horas</span><span class="sxs-lookup"><span data-stu-id="360e9-159">Time Entry</span></span> 

> ![Adicionar entidades existentes à solução de dimensões de preço](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="360e9-162">Certifique-se de incluir todos os formulários e exibições para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="360e9-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="360e9-163">Quando solicitado a incluir entidades dependentes para as entidades selecionadas acima, clique em **Não**.</span><span class="sxs-lookup"><span data-stu-id="360e9-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Não inclua todos os componentes selecionados](media/Do-not-include-required.png)


