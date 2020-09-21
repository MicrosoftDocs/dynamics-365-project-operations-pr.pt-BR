---
title: Configurar Project Service Automation
description: Etapas para configurar Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749058"
---
# <a name="configure-project-service"></a><span data-ttu-id="fecfd-103">Configurar Project Service</span><span class="sxs-lookup"><span data-stu-id="fecfd-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fecfd-104">Antes de usar os recursos de automatização do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] para gerenciar contas, projetos e recursos, você precisa concluir algumas etapas de configuração para garantir que sua solução de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] atenda às necessidades de sua organização.</span><span class="sxs-lookup"><span data-stu-id="fecfd-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="fecfd-105">Essas etapas incluem:</span><span class="sxs-lookup"><span data-stu-id="fecfd-105">These steps include:</span></span>  
  
-   <span data-ttu-id="fecfd-106">[Configurar unidades de tempo](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="fecfd-107">Configurar as unidades de tempo no catálogo de produtos que você usará como base para agendar e faturar seus projetos.</span><span class="sxs-lookup"><span data-stu-id="fecfd-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="fecfd-108">[Configurar moedas e taxas de câmbio](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="fecfd-109">Configurar as moedas que serão usadas para seus projetos.</span><span class="sxs-lookup"><span data-stu-id="fecfd-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="fecfd-110">[Criar unidades organizacionais](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="fecfd-111">Configurar os grupos que sua empresa usa para dividir seus negócios, seja por geografia, função comercial ou outra divisão lógica.</span><span class="sxs-lookup"><span data-stu-id="fecfd-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="fecfd-112">[Configurar frequências de fatura](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="fecfd-113">Configurar os períodos de tempo que você deseja usar para faturar seus clientes.</span><span class="sxs-lookup"><span data-stu-id="fecfd-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="fecfd-114">[Configurar categorias de transação](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="fecfd-115">Configurar as categorias de transações nas quais seus consultores podem cobrar suas despesas faturáveis e não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="fecfd-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="fecfd-116">[Configurar categorias de despesas](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="fecfd-117">Configurar as categorias nas quais seus consultores podem cobrar suas despesas faturáveis e não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="fecfd-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="fecfd-118">[Criar itens do catálogo de produtos](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="fecfd-119">Adicionar os produtos que você vende, como licenças de software, ao catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="fecfd-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="fecfd-120">[Crie uma lista de preços](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="fecfd-121">Configurar listas de preços diferentes, dependendo de quanto você deseja cobrar de seus clientes para cada função que o respectivo projeto requer.</span><span class="sxs-lookup"><span data-stu-id="fecfd-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="fecfd-122">[Configurar recursos](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="fecfd-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="fecfd-123">Adicionar habilidades, proficiências, funções de recursos e outras informações de recursos que você precisa para seus projetos.</span><span class="sxs-lookup"><span data-stu-id="fecfd-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fecfd-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fecfd-124">See Also</span></span>  
 <span data-ttu-id="fecfd-125">[Visão geral do Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="fecfd-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="fecfd-126">[Configurar Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="fecfd-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="fecfd-127">[Guia do gerente de conta](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fecfd-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="fecfd-128">[Guia do gerente de projeto](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fecfd-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="fecfd-129">[Guia do gerente de recursos](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fecfd-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="fecfd-130">Guid de tempo, despesas e colaboração</span><span class="sxs-lookup"><span data-stu-id="fecfd-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
