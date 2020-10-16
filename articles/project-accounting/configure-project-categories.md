---
title: Configurar categorias de projeto
description: Este tópico fornece informações sobre como configurar categorias de projeto.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895952"
---
# <a name="configure-project-categories"></a><span data-ttu-id="9c137-103">Configurar categorias de projeto</span><span class="sxs-lookup"><span data-stu-id="9c137-103">Configure project categories</span></span>

<span data-ttu-id="9c137-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="9c137-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9c137-105">O Project Operations oferece funcionalidades robustas para categorizar a receita e as despesas em projetos.</span><span class="sxs-lookup"><span data-stu-id="9c137-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="9c137-106">As categorias fornecem a capacidade de relatar e analisar as transações do projeto, além de conduzir o lançamento na contabilidade.</span><span class="sxs-lookup"><span data-stu-id="9c137-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="9c137-107">O diagrama a seguir ilustra a correlação entre categorias de transação, categorias compartilhadas e categorias de projeto.</span><span class="sxs-lookup"><span data-stu-id="9c137-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="9c137-108">As categorias de transação são o agrupamento básico para transações de projeto.</span><span class="sxs-lookup"><span data-stu-id="9c137-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="9c137-109">Dentro desse agrupamento, há um conjunto de categorias compartilhadas que podem ser compartilhadas entre aplicativos e módulos.</span><span class="sxs-lookup"><span data-stu-id="9c137-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="9c137-110">Ao se aprofundar ainda mais nas especificidades, as categorias de projeto são o nível mais granular de categorias.</span><span class="sxs-lookup"><span data-stu-id="9c137-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="9c137-111">As categorias de projeto são específicas para entidade legal, módulo e aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c137-111">Project categories are specific to legal entity, module, and application.</span></span>

![Correlação entre categorias de transação, categorias compartilhadas e categorias de projeto](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="9c137-113">Categorias de transação</span><span class="sxs-lookup"><span data-stu-id="9c137-113">Transaction categories</span></span>

<span data-ttu-id="9c137-114">As categorias de transação representam o agrupamento básico de transações de projeto e não são específicas da empresa ou do tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="9c137-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="9c137-115">Por exemplo, a Contoso Robotics usa as categorias Design, Viagem, Instalação e Transação de Serviço para agrupar as Transações do projeto.</span><span class="sxs-lookup"><span data-stu-id="9c137-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="9c137-116">As categorias de transação são definidas no módulo do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9c137-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="9c137-117">Vá para **Configurações** \> **Categorias de Transação** para abrir o formulário.</span><span class="sxs-lookup"><span data-stu-id="9c137-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="9c137-118">Crie uma nova categoria de transação selecionando **Novo** ou **Importar do Excel**.</span><span class="sxs-lookup"><span data-stu-id="9c137-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="9c137-119">Categorias compartilhadas</span><span class="sxs-lookup"><span data-stu-id="9c137-119">Shared categories</span></span>

<span data-ttu-id="9c137-120">O Dynamics 365 usa o conceito de Categorias compartilhadas para categorizar despesas em aplicativos diferentes, como Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9c137-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="9c137-121">Para cada Categoria de transação criada, o Project Operations automaticamente cria quatro Categorias compartilhadas relacionadas: Horas, Despesa, Taxas e Item.</span><span class="sxs-lookup"><span data-stu-id="9c137-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="9c137-122">Você pode revisar e ajustar as categorias compartilhadas acessando **Gerenciamento e contabilidade de projeto** \> **Configurar** \> **Categorias** \> **Categorias Compartilhadas**.</span><span class="sxs-lookup"><span data-stu-id="9c137-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="9c137-123">Categorias de produto</span><span class="sxs-lookup"><span data-stu-id="9c137-123">Project categories</span></span>

<span data-ttu-id="9c137-124">As categorias de projeto representam o nível mais granular da configuração de categoria e devem ser configuradas separadamente e, para cada empresa, por um Contador do projeto.</span><span class="sxs-lookup"><span data-stu-id="9c137-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="9c137-125">Vá para **Gerenciamento e Contabilidade de Projeto** \> **Configurar** \> **Categorias** \> **Categorias de projeto**.</span><span class="sxs-lookup"><span data-stu-id="9c137-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="9c137-126">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="9c137-126">Select **New**.</span></span>
3. <span data-ttu-id="9c137-127">Selecione a **ID da Categoria** da Categoria compartilhada que você criou na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="9c137-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="9c137-128">O Project Operations permite usar somente as categorias compartilhadas que estão associadas às categorias de transação.</span><span class="sxs-lookup"><span data-stu-id="9c137-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="9c137-129">Selecione um grupo de categorias.</span><span class="sxs-lookup"><span data-stu-id="9c137-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="9c137-130">Grupos de categoria</span><span class="sxs-lookup"><span data-stu-id="9c137-130">Category groups</span></span>

<span data-ttu-id="9c137-131">Os grupos de categorias são usados para compartilhar propriedades, principalmente perfis de lançamentos, entre Categorias de projeto relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9c137-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="9c137-132">Deve haver pelo menos um grupo de categorias para cada tipo de transação e cada categoria de projeto é atribuído a um grupo.</span><span class="sxs-lookup"><span data-stu-id="9c137-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="9c137-133">As especificações de lançamento no Project Operations são definidas pelo custo do projeto e regras do perfil da receita, categorias de projeto e grupos de categorias.</span><span class="sxs-lookup"><span data-stu-id="9c137-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="9c137-134">Você pode configurar grupos de categorias acessando **Gerenciamento e contabilidade de projeto** \> **Configuração** \> **Categorias** \> **Grupos de categorias**.</span><span class="sxs-lookup"><span data-stu-id="9c137-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
