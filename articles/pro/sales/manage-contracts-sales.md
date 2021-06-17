---
title: Gerenciar contratos de projeto
description: Este tópico fornece informações sobre a exibição de contratos baseados em projeto.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e2f182f66bd1f4fe57d19e4bf82525ac8b84c29
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003076"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="abdf5-103">Gerenciar contratos de projeto</span><span class="sxs-lookup"><span data-stu-id="abdf5-103">Manage project contracts</span></span>

<span data-ttu-id="abdf5-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="abdf5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abdf5-105">Os contratos de projeto no Dynamics 365 Project Operations capturam e gerenciam os compromissos contratualmente acordados e detalhes de cobrança de um projeto.</span><span class="sxs-lookup"><span data-stu-id="abdf5-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="abdf5-106">A estrutura de um contrato de projeto no Project Operations é adaptada para o trabalho baseado em projeto com os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="abdf5-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="abdf5-107">Linhas de contrato que identificam os componentes distintos do trabalho que serão apresentados como componentes de alto nível em uma fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="abdf5-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="abdf5-108">Detalhes da linha de contrato que identificam e estimam o trabalho para cada componente de alto nível ou linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="abdf5-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="abdf5-109">A estimativa inclui o cronograma e os aspectos financeiros do trabalho vinculado à linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="abdf5-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="abdf5-110">Modelos de contratação e componentes cobráveis são configurados para cada linha de contrato que contém o acordo de faturamento para cada linha de contrato e o contrato geral.</span><span class="sxs-lookup"><span data-stu-id="abdf5-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="abdf5-111">Exibir todos os contratos baseados em projeto</span><span class="sxs-lookup"><span data-stu-id="abdf5-111">View all project-based contracts</span></span>

<span data-ttu-id="abdf5-112">Uma lista de todos os contratos do projeto pode ser vista na página de listagem **Contratos**.</span><span class="sxs-lookup"><span data-stu-id="abdf5-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="abdf5-113">Vá para **Vendas** > **Contratos**.</span><span class="sxs-lookup"><span data-stu-id="abdf5-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="abdf5-114">É exibida uma lista de todos os contratos de projeto no sistema.</span><span class="sxs-lookup"><span data-stu-id="abdf5-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="abdf5-115">Selecione **Exibir seletor** (a seta suspensa ao lado do nome da exibição) para selecionar outras exibições filtradas.</span><span class="sxs-lookup"><span data-stu-id="abdf5-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="abdf5-116">Você pode criar suas próprias exibições com critérios de filtro personalizados.</span><span class="sxs-lookup"><span data-stu-id="abdf5-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="abdf5-117">Os contratos podem ser criados ou excluídos desta página de listagem ou de páginas de detalhes.</span><span class="sxs-lookup"><span data-stu-id="abdf5-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]