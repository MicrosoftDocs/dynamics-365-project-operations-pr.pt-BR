---
title: Configurar Project Service Automation
description: Etapas para configurar Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002808"
---
# <a name="configure-project-service"></a><span data-ttu-id="f077b-103">Configurar Project Service</span><span class="sxs-lookup"><span data-stu-id="f077b-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f077b-104">Antes de usar os recursos de automatização do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] para gerenciar contas, projetos e recursos, você precisa concluir algumas etapas de configuração para garantir que sua solução de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] atenda às necessidades de sua organização.</span><span class="sxs-lookup"><span data-stu-id="f077b-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="f077b-105">Essas etapas incluem:</span><span class="sxs-lookup"><span data-stu-id="f077b-105">These steps include:</span></span>  
  
-   <span data-ttu-id="f077b-106">[Configurar unidades de tempo](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="f077b-107">Configurar as unidades de tempo no catálogo de produtos que você usará como base para agendar e faturar seus projetos.</span><span class="sxs-lookup"><span data-stu-id="f077b-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="f077b-108">[Configurar moedas e taxas de câmbio](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="f077b-109">Configurar as moedas que serão usadas para seus projetos.</span><span class="sxs-lookup"><span data-stu-id="f077b-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="f077b-110">[Criar unidades organizacionais](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="f077b-111">Configurar os grupos que sua empresa usa para dividir seus negócios, seja por geografia, função comercial ou outra divisão lógica.</span><span class="sxs-lookup"><span data-stu-id="f077b-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="f077b-112">[Configurar frequências de fatura](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="f077b-113">Configurar os períodos de tempo que você deseja usar para faturar seus clientes.</span><span class="sxs-lookup"><span data-stu-id="f077b-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="f077b-114">[Configurar categorias de transação](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="f077b-115">Configurar as categorias de transações nas quais seus consultores podem cobrar suas despesas faturáveis e não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="f077b-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f077b-116">[Configurar categorias de despesas](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="f077b-117">Configurar as categorias nas quais seus consultores podem cobrar suas despesas faturáveis e não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="f077b-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f077b-118">[Criar itens do catálogo de produtos](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="f077b-119">Adicionar os produtos que você vende, como licenças de software, ao catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="f077b-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="f077b-120">[Crie uma lista de preços](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="f077b-121">Configurar listas de preços diferentes, dependendo de quanto você deseja cobrar de seus clientes para cada função que o respectivo projeto requer.</span><span class="sxs-lookup"><span data-stu-id="f077b-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="f077b-122">[Configurar recursos](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f077b-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="f077b-123">Adicionar habilidades, proficiências, funções de recursos e outras informações de recursos que você precisa para seus projetos.</span><span class="sxs-lookup"><span data-stu-id="f077b-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f077b-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f077b-124">See Also</span></span>  
 <span data-ttu-id="f077b-125">[Visão geral do Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="f077b-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="f077b-126">[Configurar Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="f077b-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="f077b-127">[Guia do gerente de conta](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f077b-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="f077b-128">[Guia do gerente de projeto](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f077b-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="f077b-129">[Guia do gerente de recursos](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f077b-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="f077b-130">Guid de tempo, despesas e colaboração</span><span class="sxs-lookup"><span data-stu-id="f077b-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]