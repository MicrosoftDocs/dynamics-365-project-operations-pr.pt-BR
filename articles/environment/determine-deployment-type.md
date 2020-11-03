---
title: Determinar o tipo de implantação
description: Este tópico fornece informações para ajudar a determinar o tipo de implantação correto do Project Operations para a sua empresa.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071432"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="215e0-103">Determinar o tipo de implantação</span><span class="sxs-lookup"><span data-stu-id="215e0-103">Determine your deployment type</span></span>

<span data-ttu-id="215e0-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="215e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="215e0-105">Após comprar a licença, comece aqui para determinar o melhor modelo de implantação do Dynamics 365 Project Operations usando o [Fluxo de instalação guiada](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="215e0-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="215e0-106">Depois de concluir o Fluxo de instalação guiada, você será direcionado para o portal de gerenciamento correto para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="215e0-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="215e0-107">Veja os detalhes de implantação para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="215e0-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="215e0-108">Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="215e0-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="215e0-109">O Project Operations inclui as funcionalidades fornecidas com o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="215e0-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="215e0-110">Um caminho de atualização será lançado para esses clientes no futuro.</span><span class="sxs-lookup"><span data-stu-id="215e0-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="215e0-111">Clientes existentes do Dynamics 365 Finance usando o Gerenciamento e contabilidade de projeto</span><span class="sxs-lookup"><span data-stu-id="215e0-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="215e0-112">Os clientes existentes do Finance que usam a funcionalidade Gerenciamento e contabilidade de projeto podem continuar usando-a como tal.</span><span class="sxs-lookup"><span data-stu-id="215e0-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="215e0-113">Consulte [Project Operations para cenários de pedido baseado em estoque/produção](#pma).</span><span class="sxs-lookup"><span data-stu-id="215e0-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="215e0-114">Tipos de implantação</span><span class="sxs-lookup"><span data-stu-id="215e0-114">Deployment types</span></span>
<span data-ttu-id="215e0-115">O Project Operations oferece suporte a várias opções de implantação para atender aos seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="215e0-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="215e0-116">Seja você um cliente novo ou existente do Dynamics 365, o Project Operations pode dar suporte às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="215e0-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="215e0-117">Nosso [Questionário de implantação](https://aka.ms/provisionprojectoperations) ajudará você a determinar a implantação correta.</span><span class="sxs-lookup"><span data-stu-id="215e0-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="215e0-118">Os resultados guiarão você para um dos seguintes tipos de implantação:</span><span class="sxs-lookup"><span data-stu-id="215e0-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="215e0-119">Implantação lite - gerenciar faturamento pro forma</span><span class="sxs-lookup"><span data-stu-id="215e0-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="215e0-120">Project Operations para cenários baseados em recursos/itens sem estoque</span><span class="sxs-lookup"><span data-stu-id="215e0-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="215e0-121">Project Operations para cenários de pedido baseado em estoque/produção</span><span class="sxs-lookup"><span data-stu-id="215e0-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="215e0-122">O Project Operations oferece suporte a cenários com estoque/ordem de produção e cenários baseados em recursos/sem estoque no mesmo ambiente por meio de configurações no nível de entidade legal.</span><span class="sxs-lookup"><span data-stu-id="215e0-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="215e0-123">Por exemplo, a Contoso pode usar os recursos de pedido baseado em estoque/produção em instalações de manufatura nos EUA (entidade legal = Contoso Manufacturing Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="215e0-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="215e0-124">A Contoso pode usar os recursos não estocados/baseados em recursos em instalações de serviço da Contoso Robotics Arms no Reino Unido (entidade legal = Contoso Robotics Reino Unido).</span><span class="sxs-lookup"><span data-stu-id="215e0-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="215e0-125">Implantação lite - gerenciar faturamento pro forma</span><span class="sxs-lookup"><span data-stu-id="215e0-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="215e0-126">A implantação lite inclui as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="215e0-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="215e0-127">Planejamento de projetos usando Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="215e0-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="215e0-128">Precificação multidimensional</span><span class="sxs-lookup"><span data-stu-id="215e0-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="215e0-129">Gerenciamento Unificado de Recursos</span><span class="sxs-lookup"><span data-stu-id="215e0-129">Unified Resource Management</span></span>
- <span data-ttu-id="215e0-130">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="215e0-130">Time Tracking</span></span>
- <span data-ttu-id="215e0-131">Despesa Básica</span><span class="sxs-lookup"><span data-stu-id="215e0-131">Basic Expense</span></span>
- <span data-ttu-id="215e0-132">Proposta de Fatura</span><span class="sxs-lookup"><span data-stu-id="215e0-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="215e0-133">Etapas de implantação</span><span class="sxs-lookup"><span data-stu-id="215e0-133">Deployment steps</span></span>
<span data-ttu-id="215e0-134">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="215e0-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="215e0-135">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](lite-preview-subscription-sign-up.md) e [Provisionar novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="215e0-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="215e0-136">Project Operations para cenários baseados em recursos/itens sem estoque</span><span class="sxs-lookup"><span data-stu-id="215e0-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="215e0-137">O Project Operations para cenários de recursos/sem estoque inclui as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="215e0-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="215e0-138">Planejamento de projetos usando Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="215e0-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="215e0-139">Precificação multidimensional</span><span class="sxs-lookup"><span data-stu-id="215e0-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="215e0-140">Gerenciamento Unificado de Recursos</span><span class="sxs-lookup"><span data-stu-id="215e0-140">Unified Resource Management</span></span>
- <span data-ttu-id="215e0-141">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="215e0-141">Time Tracking</span></span>
- <span data-ttu-id="215e0-142">Despesa Básica</span><span class="sxs-lookup"><span data-stu-id="215e0-142">Basic Expense</span></span>
- <span data-ttu-id="215e0-143">Despesa total</span><span class="sxs-lookup"><span data-stu-id="215e0-143">Full Expense</span></span>
- <span data-ttu-id="215e0-144">OCR de recibo</span><span class="sxs-lookup"><span data-stu-id="215e0-144">Receipt OCR</span></span>
- <span data-ttu-id="215e0-145">Faturamento Completo</span><span class="sxs-lookup"><span data-stu-id="215e0-145">Full Invoicing</span></span>
- <span data-ttu-id="215e0-146">Reconhecimento de Receita</span><span class="sxs-lookup"><span data-stu-id="215e0-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="215e0-147">Etapas de implantação</span><span class="sxs-lookup"><span data-stu-id="215e0-147">Deployment steps</span></span>
<span data-ttu-id="215e0-148">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="215e0-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="215e0-149">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](resource-sign-up-preview-subscription.md) e [Provisionar novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="215e0-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="215e0-150">Project Operations para cenários de pedido baseado em estoque/produção</span><span class="sxs-lookup"><span data-stu-id="215e0-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="215e0-151">Planejamento de projeto usando WBS</span><span class="sxs-lookup"><span data-stu-id="215e0-151">Project planning using WBS</span></span>
- <span data-ttu-id="215e0-152">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="215e0-152">Resource Management</span></span>
- <span data-ttu-id="215e0-153">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="215e0-153">Time Tracking</span></span>
- <span data-ttu-id="215e0-154">Despesa total</span><span class="sxs-lookup"><span data-stu-id="215e0-154">Full Expense</span></span>
- <span data-ttu-id="215e0-155">OCR de recibo</span><span class="sxs-lookup"><span data-stu-id="215e0-155">Receipt OCR</span></span>
- <span data-ttu-id="215e0-156">Faturamento Completo</span><span class="sxs-lookup"><span data-stu-id="215e0-156">Full Invoicing</span></span>
- <span data-ttu-id="215e0-157">Reconhecimento de Receita</span><span class="sxs-lookup"><span data-stu-id="215e0-157">Revenue Recognition</span></span>
- <span data-ttu-id="215e0-158">Ordens de Produção</span><span class="sxs-lookup"><span data-stu-id="215e0-158">Production Orders</span></span>
- <span data-ttu-id="215e0-159">Suporte a materiais</span><span class="sxs-lookup"><span data-stu-id="215e0-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="215e0-160">Etapas de implantação</span><span class="sxs-lookup"><span data-stu-id="215e0-160">Deployment steps</span></span>
<span data-ttu-id="215e0-161">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="215e0-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="215e0-162">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Provisionar novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="215e0-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

