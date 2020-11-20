---
title: Determinar o tipo de implantação
description: Este tópico fornece informações para ajudar a determinar o tipo de implantação correto do Project Operations para a sua empresa.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401204"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="b58aa-103">Determinar o tipo de implantação</span><span class="sxs-lookup"><span data-stu-id="b58aa-103">Determine your deployment type</span></span>

<span data-ttu-id="b58aa-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="b58aa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b58aa-105">Após comprar a licença, comece aqui para determinar o melhor modelo de implantação do Dynamics 365 Project Operations usando o [Fluxo de instalação guiada](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="b58aa-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="b58aa-106">Depois de concluir o Fluxo de instalação guiada, você será direcionado para o portal de gerenciamento correto para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="b58aa-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="b58aa-107">Veja os detalhes de implantação para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="b58aa-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="b58aa-108">Clientes existentes de Dynamics usando Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b58aa-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="b58aa-109">O Project Operations inclui as funcionalidades fornecidas com o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b58aa-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="b58aa-110">Um caminho de atualização será lançado para esses clientes no ciclo de lançamentos 1 de 2021.</span><span class="sxs-lookup"><span data-stu-id="b58aa-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="b58aa-111">Clientes existentes do Dynamics 365 Finance usando o Gerenciamento e contabilidade de projeto</span><span class="sxs-lookup"><span data-stu-id="b58aa-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="b58aa-112">Os clientes existentes do Finance que usam a funcionalidade de gerenciamento e contabilidade de projeto podem continuar usando-a da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="b58aa-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="b58aa-113">Consulte [Project Operations para cenários de pedido baseado em estoque/produção](#pma).</span><span class="sxs-lookup"><span data-stu-id="b58aa-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="b58aa-114">Tipos de implantação</span><span class="sxs-lookup"><span data-stu-id="b58aa-114">Deployment types</span></span>
<span data-ttu-id="b58aa-115">O Project Operations oferece suporte a várias opções de implantação para atender aos seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="b58aa-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="b58aa-116">Seja você um cliente novo ou existente do Dynamics 365, o Project Operations pode dar suporte às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="b58aa-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="b58aa-117">Nosso [Questionário de implantação](https://aka.ms/provisionprojectoperations) ajudará você a determinar a implantação correta.</span><span class="sxs-lookup"><span data-stu-id="b58aa-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="b58aa-118">Os resultados guiarão você para um dos seguintes tipos de implantação:</span><span class="sxs-lookup"><span data-stu-id="b58aa-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="b58aa-119">Implantação lite - gerenciar faturamento pro forma</span><span class="sxs-lookup"><span data-stu-id="b58aa-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="b58aa-120">Project Operations para cenários baseados em recursos/itens sem estoque</span><span class="sxs-lookup"><span data-stu-id="b58aa-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="b58aa-121">Project Operations para cenários de pedido baseado em estoque/produção</span><span class="sxs-lookup"><span data-stu-id="b58aa-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="b58aa-122">O Project Operations oferece suporte a cenários com estoque/ordem de produção e cenários baseados em recursos/sem estoque no mesmo ambiente por meio de configurações no nível de entidade legal.</span><span class="sxs-lookup"><span data-stu-id="b58aa-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="b58aa-123">Por exemplo, a Contoso pode usar os recursos de pedido baseado em estoque/produção em instalações de manufatura nos EUA (entidade legal = Contoso Manufacturing Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="b58aa-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="b58aa-124">A Contoso pode usar os recursos não estocados/baseados em recursos em instalações de serviço da Contoso Robotics Arms no Reino Unido (entidade legal = Contoso Robotics Reino Unido).</span><span class="sxs-lookup"><span data-stu-id="b58aa-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="b58aa-125">Implantação lite - gerenciar faturamento pro forma</span><span class="sxs-lookup"><span data-stu-id="b58aa-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="b58aa-126">A implantação lite inclui as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="b58aa-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="b58aa-127">Processo de vendas para projetos que estende as experiências do aplicativo Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="b58aa-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="b58aa-128">Planejamento de projetos usando Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="b58aa-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="b58aa-129">Precificação multidimensional</span><span class="sxs-lookup"><span data-stu-id="b58aa-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="b58aa-130">Gerenciamento unificado de recursos</span><span class="sxs-lookup"><span data-stu-id="b58aa-130">Unified resource management</span></span>
- <span data-ttu-id="b58aa-131">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="b58aa-131">Time tracking</span></span>
- <span data-ttu-id="b58aa-132">Despesa básica</span><span class="sxs-lookup"><span data-stu-id="b58aa-132">Basic expense</span></span>
- <span data-ttu-id="b58aa-133">Faturamento pro forma e voltado ao cliente</span><span class="sxs-lookup"><span data-stu-id="b58aa-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="b58aa-134">Etapas de implantação</span><span class="sxs-lookup"><span data-stu-id="b58aa-134">Deployment steps</span></span>
<span data-ttu-id="b58aa-135">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="b58aa-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="b58aa-136">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](lite-preview-subscription-sign-up.md) e [Provisionar novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="b58aa-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="b58aa-137">Project Operations para cenários baseados em recursos/itens sem estoque</span><span class="sxs-lookup"><span data-stu-id="b58aa-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="b58aa-138">O Project Operations para cenários de recursos/sem estoque inclui as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="b58aa-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="b58aa-139">Processo de vendas para projetos que estende o aplicativo Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="b58aa-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="b58aa-140">Planejamento de projetos usando Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="b58aa-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="b58aa-141">Precificação multidimensional</span><span class="sxs-lookup"><span data-stu-id="b58aa-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="b58aa-142">Gerenciamento unificado de recursos</span><span class="sxs-lookup"><span data-stu-id="b58aa-142">Unified resource management</span></span>
- <span data-ttu-id="b58aa-143">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="b58aa-143">Time tracking</span></span>
- <span data-ttu-id="b58aa-144">Despesa básica</span><span class="sxs-lookup"><span data-stu-id="b58aa-144">Basic expense</span></span>
- <span data-ttu-id="b58aa-145">Despesa total</span><span class="sxs-lookup"><span data-stu-id="b58aa-145">Full expense</span></span>
- <span data-ttu-id="b58aa-146">OCR de recibo</span><span class="sxs-lookup"><span data-stu-id="b58aa-146">Receipt OCR</span></span>
- <span data-ttu-id="b58aa-147">Faturamento pro forma e voltado ao cliente</span><span class="sxs-lookup"><span data-stu-id="b58aa-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="b58aa-148">Reconhecimento de receita para projetos</span><span class="sxs-lookup"><span data-stu-id="b58aa-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="b58aa-149">Etapas de implantação</span><span class="sxs-lookup"><span data-stu-id="b58aa-149">Deployment steps</span></span>
<span data-ttu-id="b58aa-150">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="b58aa-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="b58aa-151">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](resource-sign-up-preview-subscription.md) e [Provisionar novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b58aa-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="b58aa-152">Project Operations para cenários de pedido baseado em estoque/produção</span><span class="sxs-lookup"><span data-stu-id="b58aa-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="b58aa-153">Planejamento de projeto usando WBS</span><span class="sxs-lookup"><span data-stu-id="b58aa-153">Project planning using WBS</span></span>
- <span data-ttu-id="b58aa-154">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="b58aa-154">Resource Management</span></span>
- <span data-ttu-id="b58aa-155">Controle de horas</span><span class="sxs-lookup"><span data-stu-id="b58aa-155">Time Tracking</span></span>
- <span data-ttu-id="b58aa-156">Despesa total</span><span class="sxs-lookup"><span data-stu-id="b58aa-156">Full Expense</span></span>
- <span data-ttu-id="b58aa-157">OCR de recibo</span><span class="sxs-lookup"><span data-stu-id="b58aa-157">Receipt OCR</span></span>
- <span data-ttu-id="b58aa-158">Faturamento Completo</span><span class="sxs-lookup"><span data-stu-id="b58aa-158">Full Invoicing</span></span>
- <span data-ttu-id="b58aa-159">Reconhecimento de Receita</span><span class="sxs-lookup"><span data-stu-id="b58aa-159">Revenue Recognition</span></span>
- <span data-ttu-id="b58aa-160">Ordens de Produção</span><span class="sxs-lookup"><span data-stu-id="b58aa-160">Production Orders</span></span>
- <span data-ttu-id="b58aa-161">Suporte a materiais</span><span class="sxs-lookup"><span data-stu-id="b58aa-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="b58aa-162">Etapas de implantação</span><span class="sxs-lookup"><span data-stu-id="b58aa-162">Deployment steps</span></span>
<span data-ttu-id="b58aa-163">Determine o melhor modelo de implantação do Project Operations usando o [Questionário de implantação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="b58aa-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="b58aa-164">Para esta implantação, consulte [Inscreva-se para obter assinaturas de versão preliminar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Provisionar novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b58aa-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

