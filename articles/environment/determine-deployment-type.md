---
title: Tipos de implantação
description: Este tópico fornece informações para ajudar a determinar o tipo de implantação correto do Project Operations para a sua empresa.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948738"
---
# <a name="deployment-types"></a><span data-ttu-id="66ea3-103">Tipos de implantação</span><span class="sxs-lookup"><span data-stu-id="66ea3-103">Deployment types</span></span>

<span data-ttu-id="66ea3-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="66ea3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66ea3-105">Após comprar a licença, comece aqui para determinar o melhor modelo de implantação do Dynamics 365 Project Operations usando o [Fluxo de instalação guiada](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="66ea3-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="66ea3-106">Depois de concluir o Fluxo de instalação guiada, você será direcionado para o portal de gerenciamento correto para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="66ea3-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="66ea3-107">Veja os detalhes de implantação abaixo para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="66ea3-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="66ea3-108">Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="66ea3-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="66ea3-109">O Project Operations inclui as funcionalidades fornecidas com o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="66ea3-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="66ea3-110">Um caminho de atualização será lançado para esses clientes no futuro.</span><span class="sxs-lookup"><span data-stu-id="66ea3-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="66ea3-111">Clientes existentes do Dynamics 365 Finance usando o Gerenciamento e contabilidade de projeto</span><span class="sxs-lookup"><span data-stu-id="66ea3-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="66ea3-112">Os clientes existentes do Finance que usam a funcionalidade Gerenciamento e contabilidade de projeto podem continuar usando-o como está.</span><span class="sxs-lookup"><span data-stu-id="66ea3-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="66ea3-113">Consulte [Project Operations para cenários de pedido baseado em estoque/produção](#pma).</span><span class="sxs-lookup"><span data-stu-id="66ea3-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="66ea3-114">O Project Operations oferece suporte a várias opções de implantação para atender aos seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="66ea3-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="66ea3-115">Independentemente de ser um cliente novo ou existente do Dynamics 365, o Project Operations pode oferecer suporte às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="66ea3-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="66ea3-116">Nosso [Questionário de implantação](https://aka.ms/provisionprojectoperations) ajudará você a determinar a implantação correta.</span><span class="sxs-lookup"><span data-stu-id="66ea3-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="66ea3-117">Os resultados guiarão você para um dos seguintes tipos de implantação:</span><span class="sxs-lookup"><span data-stu-id="66ea3-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="66ea3-118">Implantação lite - gerenciar faturamento pro forma</span><span class="sxs-lookup"><span data-stu-id="66ea3-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="66ea3-119">Project Operations para cenários baseados em recursos/itens sem estoque</span><span class="sxs-lookup"><span data-stu-id="66ea3-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="66ea3-120">Project Operations para cenários de pedido baseado em estoque/produção</span><span class="sxs-lookup"><span data-stu-id="66ea3-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="66ea3-121">O Project Operations oferece suporte a cenários com estoque/ordem de produção e cenários baseados em recursos/sem estoque no mesmo ambiente por meio de configurações no nível de entidade legal.</span><span class="sxs-lookup"><span data-stu-id="66ea3-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="66ea3-122">Por exemplo, Contoso pode usar as funcionalidades com estoque/ordem de produção em suas instalações de manufatura dos EUA (Entidade legal = Contoso Manufacturing Estados Unidos) e funcionalidades sem estoque/baseados em recursos na instalação de serviço da Contoso Robotics Arms (Entidade legal = Contoso Robotics Reino Unido).</span><span class="sxs-lookup"><span data-stu-id="66ea3-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="66ea3-123"><a name="lite"><a/>Implantação lite - gerenciar faturamento pro forma</span><span class="sxs-lookup"><span data-stu-id="66ea3-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="66ea3-124">A implantação lite inclui as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="66ea3-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="66ea3-125">Planejamento de projetos usando Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="66ea3-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="66ea3-126">Precificação multidimensional</span><span class="sxs-lookup"><span data-stu-id="66ea3-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="66ea3-127">Gerenciamento Unificado de Recursos</span><span class="sxs-lookup"><span data-stu-id="66ea3-127">Unified Resource Management</span></span>
- <span data-ttu-id="66ea3-128">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="66ea3-128">Time Tracking</span></span>
- <span data-ttu-id="66ea3-129">Despesa Básica</span><span class="sxs-lookup"><span data-stu-id="66ea3-129">Basic Expense</span></span>
- <span data-ttu-id="66ea3-130">Proposta de Fatura</span><span class="sxs-lookup"><span data-stu-id="66ea3-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="66ea3-131">Etapas de implantação:</span><span class="sxs-lookup"><span data-stu-id="66ea3-131">Deployment steps:</span></span>
<span data-ttu-id="66ea3-132">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="66ea3-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="66ea3-133">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](lite-preview-subscription-sign-up.md) e [Provisionar novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="66ea3-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="66ea3-134"><a name="integrated"><a/>Project Operations para cenários baseados em recursos/itens sem estoque</span><span class="sxs-lookup"><span data-stu-id="66ea3-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="66ea3-135">O Project Operations para cenários de recursos/sem estoque inclui as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="66ea3-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="66ea3-136">Planejamento de projetos usando Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="66ea3-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="66ea3-137">Precificação multidimensional</span><span class="sxs-lookup"><span data-stu-id="66ea3-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="66ea3-138">Gerenciamento Unificado de Recursos</span><span class="sxs-lookup"><span data-stu-id="66ea3-138">Unified Resource Management</span></span>
- <span data-ttu-id="66ea3-139">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="66ea3-139">Time Tracking</span></span>
- <span data-ttu-id="66ea3-140">Despesa Básica</span><span class="sxs-lookup"><span data-stu-id="66ea3-140">Basic Expense</span></span>
- <span data-ttu-id="66ea3-141">Despesa total</span><span class="sxs-lookup"><span data-stu-id="66ea3-141">Full Expense</span></span>
- <span data-ttu-id="66ea3-142">OCR de recibo</span><span class="sxs-lookup"><span data-stu-id="66ea3-142">Receipt OCR</span></span>
- <span data-ttu-id="66ea3-143">Faturamento Completo</span><span class="sxs-lookup"><span data-stu-id="66ea3-143">Full Invoicing</span></span>
- <span data-ttu-id="66ea3-144">Reconhecimento de Receita</span><span class="sxs-lookup"><span data-stu-id="66ea3-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="66ea3-145">Etapas de implantação:</span><span class="sxs-lookup"><span data-stu-id="66ea3-145">Deployment steps:</span></span>
<span data-ttu-id="66ea3-146">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="66ea3-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="66ea3-147">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](resource-sign-up-preview-subscription.md) e [Provisionar novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="66ea3-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="66ea3-148">Project Operations para cenários de pedido baseado em estoque/produção</span><span class="sxs-lookup"><span data-stu-id="66ea3-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="66ea3-149">Planejamento de projeto usando WBS</span><span class="sxs-lookup"><span data-stu-id="66ea3-149">Project planning using WBS</span></span>
- <span data-ttu-id="66ea3-150">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="66ea3-150">Resource Management</span></span>
- <span data-ttu-id="66ea3-151">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="66ea3-151">Time Tracking</span></span>
- <span data-ttu-id="66ea3-152">Despesa total</span><span class="sxs-lookup"><span data-stu-id="66ea3-152">Full Expense</span></span>
- <span data-ttu-id="66ea3-153">OCR de recibo</span><span class="sxs-lookup"><span data-stu-id="66ea3-153">Receipt OCR</span></span>
- <span data-ttu-id="66ea3-154">Faturamento Completo</span><span class="sxs-lookup"><span data-stu-id="66ea3-154">Full Invoicing</span></span>
- <span data-ttu-id="66ea3-155">Reconhecimento de Receita</span><span class="sxs-lookup"><span data-stu-id="66ea3-155">Revenue Recognition</span></span>
- <span data-ttu-id="66ea3-156">Ordens de Produção</span><span class="sxs-lookup"><span data-stu-id="66ea3-156">Production Orders</span></span>
- <span data-ttu-id="66ea3-157">Suporte a materiais</span><span class="sxs-lookup"><span data-stu-id="66ea3-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="66ea3-158">Etapas de implantação:</span><span class="sxs-lookup"><span data-stu-id="66ea3-158">Deployment steps:</span></span>
<span data-ttu-id="66ea3-159">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="66ea3-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="66ea3-160">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Provisionar novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="66ea3-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



