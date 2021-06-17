---
title: Criar campos e entidades personalizados
description: Este tópico explica como criar conjuntos de opções e entidades em sua própria solução na plataforma Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998937"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="4608b-103">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="4608b-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4608b-104">Conclua as etapas a seguir sempre que quiser criar uma entidade ou um conjunto de opções personalizado na plataforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="4608b-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="4608b-105">Os procedimentos neste tópico devem ser concluídos usando a interface da Web do PSA (Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="4608b-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4608b-106">É recomendável fazer todas as alterações de dimensão de preço personalizadas em outra solução.</span><span class="sxs-lookup"><span data-stu-id="4608b-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="4608b-107">Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="4608b-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="4608b-108">Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a em outras instâncias para reutilizar sua configuração de preço.</span><span class="sxs-lookup"><span data-stu-id="4608b-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="4608b-109">Criar campos e conjuntos de opções personalizados na solução de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="4608b-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="4608b-110">Uma dimensão de preço pode ser um conjunto de opções ou uma entidade.</span><span class="sxs-lookup"><span data-stu-id="4608b-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="4608b-111">Ambos deve ser criados em sua solução de preço.</span><span class="sxs-lookup"><span data-stu-id="4608b-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="4608b-112">As etapas deste procedimento explicam como criar dimensões baseadas em entidade e dimensões baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="4608b-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="4608b-113">Dimensões baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="4608b-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="4608b-114">No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **Dimensões de preços do(a) \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="4608b-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="4608b-115">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="4608b-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="4608b-116">Clique em **Novo** para criar uma nova entidade denominada **Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="4608b-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="4608b-117">Insira as informações necessárias restantes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="4608b-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definição da entidade de cargo padrão](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="4608b-119">Dimensões baseadas em conjunto de opções</span><span class="sxs-lookup"><span data-stu-id="4608b-119">Option set-based dimensions</span></span> 
<span data-ttu-id="4608b-120">Você pode criar duas dimensões baseadas em conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="4608b-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="4608b-121">Use **Local de Trabalho do Recurso** para rastrear o preço do trabalho do local **Página Inicial** e do trabalho **No Local** e use **Horas de Trabalho do Recurso** com os valores **Regular** e **Horas Extras** para aplicar um markup quando o trabalho é concluído.</span><span class="sxs-lookup"><span data-stu-id="4608b-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="4608b-122">No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **Dimensões de preços do(a) \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="4608b-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="4608b-123">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Conjuntos de Opções**.</span><span class="sxs-lookup"><span data-stu-id="4608b-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="4608b-124">Clique em **Novo** para criar um novo conjunto de opções, insira as informações necessárias restantes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="4608b-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="4608b-125">Dimensão de preço baseada em conjunto de opções chamada Local de Trabalho do Recurso</span><span class="sxs-lookup"><span data-stu-id="4608b-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="4608b-126">Dimensão de preço baseada em conjunto de opções chamada Horas de Trabalho do Recurso</span><span class="sxs-lookup"><span data-stu-id="4608b-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="4608b-127">Criar dados para dimensões baseadas em entidade</span><span class="sxs-lookup"><span data-stu-id="4608b-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="4608b-128">Você pode criar dados para dimensões baseadas em entidade manualmente, ou usando a importação ou as chamadas de serviço do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4608b-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="4608b-129">Use as etapas neste procedimento para criar dois cargos padrões, **Engenheiro de Sistemas** e **Engenheiro de Sistemas Sênior** na dimensão baseada em entidade, **Cargo Padrão**.</span><span class="sxs-lookup"><span data-stu-id="4608b-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="4608b-130">Se os dados que quiser criar forem pequenos, como no exemplo a seguir, você poderá usar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="4608b-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="4608b-131">No PSA, clique em **Localização Avançada**.</span><span class="sxs-lookup"><span data-stu-id="4608b-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="4608b-132">Selecione a entidade **Cargo Padrão** e clique em **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="4608b-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="4608b-133">Todas as linhas na entidade **Cargo Padrão** serão mostradas.</span><span class="sxs-lookup"><span data-stu-id="4608b-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="4608b-134">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="4608b-134">Click **New**.</span></span> <span data-ttu-id="4608b-135">No campo **Nome**, insira "Engenheiro de Sistemas" e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="4608b-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="4608b-136">Feche o formulário.</span><span class="sxs-lookup"><span data-stu-id="4608b-136">Close the form.</span></span> 
4. <span data-ttu-id="4608b-137">Repita as etapas de 1 a 3 para criar outro cargo padrão para "Engenheiro de Sistemas Sênior".</span><span class="sxs-lookup"><span data-stu-id="4608b-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="4608b-138">Dados de Exemplo para a entidade Cargo Padrão</span><span class="sxs-lookup"><span data-stu-id="4608b-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]