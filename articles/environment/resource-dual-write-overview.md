---
title: Integração de gravação dupla do Project Operations
description: Este tópico fornece uma visão geral da integração de gravação dupla do Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955644"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="54ebc-103">Visão geral de integração de gravação dupla do Project Operations</span><span class="sxs-lookup"><span data-stu-id="54ebc-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="54ebc-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="54ebc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="54ebc-105">O Project Operations usa [capacidades de gravação dupla](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar dados no Microsoft Dataverse e no Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="54ebc-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="54ebc-106">A ilustração a seguir mostra como os dados são sincronizados como parte desta integração entre o Dataverse e o Finance.</span><span class="sxs-lookup"><span data-stu-id="54ebc-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Visão geral de fluxos de dados do Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="54ebc-108">O Project Operations no Dataverse fornece uma interface de usuário (IU) moderna e extensibilidade fácil sem código/com pouco código usando recursos do Power Platform.</span><span class="sxs-lookup"><span data-stu-id="54ebc-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="54ebc-109">Gerentes de projeto, gerentes de recursos, membros da equipe do projeto e outras personas da linha de frente, realizam atividades no Project Operations no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="54ebc-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="54ebc-110">O Project Operations no Finance fornece suporte para contabilidade de projetos e reconhecimento de receita.</span><span class="sxs-lookup"><span data-stu-id="54ebc-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="54ebc-111">O Project Operations se conecta à estrutura financeira do Finance para cálculo de impostos, taxas de câmbio, relatórios de dimensão financeira e muito mais.</span><span class="sxs-lookup"><span data-stu-id="54ebc-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="54ebc-112">As experiências do contador do projeto se baseiam principalmente no Finance.</span><span class="sxs-lookup"><span data-stu-id="54ebc-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="54ebc-113">A integração do Project Operations consiste na seguinte integração de componentes:</span><span class="sxs-lookup"><span data-stu-id="54ebc-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="54ebc-114">Configuração do Project Operations e integração de dados de configuração</span><span class="sxs-lookup"><span data-stu-id="54ebc-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="54ebc-115">Estimativas e dados reais do projeto</span><span class="sxs-lookup"><span data-stu-id="54ebc-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="54ebc-116">Faturas do projeto</span><span class="sxs-lookup"><span data-stu-id="54ebc-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="54ebc-117">Gerenciamento de despesas</span><span class="sxs-lookup"><span data-stu-id="54ebc-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="54ebc-118">Fatura de fornecedor</span><span class="sxs-lookup"><span data-stu-id="54ebc-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
