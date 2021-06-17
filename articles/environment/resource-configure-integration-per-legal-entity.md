---
title: Configurar a integração do Project Operations por entidade legal
description: Este tópico fornece informações sobre como configurar a integração por entidade legal no Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000062"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="7e255-103">Configurar a integração do Project Operations por entidade legal</span><span class="sxs-lookup"><span data-stu-id="7e255-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="7e255-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="7e255-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7e255-105">Este tópico orienta você ao longo das etapas necessárias para configurar o Dynamics 365 Project Operations por entidade legal.</span><span class="sxs-lookup"><span data-stu-id="7e255-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="7e255-106">Habilitar teclas de função no Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="7e255-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="7e255-107">Conclua as etapas a seguir para habilitar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="7e255-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="7e255-108">No Dynamics 365 Finance, acesse o espaço de trabalho **Gerenciamento de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="7e255-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="7e255-109">Na **Lista de recursos**, encontre e ative os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="7e255-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="7e255-110">**Habilitar várias linhas de contrato para um projeto**</span><span class="sxs-lookup"><span data-stu-id="7e255-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="7e255-111">**Habilitar o Project Operations no Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="7e255-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="7e255-112">Se você não vir **Teclas de recursos** listadas, verifique se sua versão do Finance atende ao requisito de versão mínima (versão do aplicativo 10.0.13 com todas as atualizações de qualidade aplicadas ou superior).</span><span class="sxs-lookup"><span data-stu-id="7e255-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="7e255-113">Selecione **Verificar se há atualizações** para atualizar a lista de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e255-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="7e255-114">Definir o cenário de implantação do Project Operations para uma entidade legal</span><span class="sxs-lookup"><span data-stu-id="7e255-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="7e255-115">Você pode habilitar o Project Operations no Dynamics 365 Customer Engagement em um nível de entidade legal.</span><span class="sxs-lookup"><span data-stu-id="7e255-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="7e255-116">Você pode ter uma entidade legal usando o Project Operations no Dynamics 365 Customer Engagement para cenários baseados em recursos/sem estoque.</span><span class="sxs-lookup"><span data-stu-id="7e255-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="7e255-117">No mesmo ambiente, você pode ter outra entidade legal usando o Project Operations para cenários com estoque/ordem de produção.</span><span class="sxs-lookup"><span data-stu-id="7e255-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="7e255-118">No Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projeto** > **Configuração** > **Parâmetros globais de gerenciamento e contabilidade de projeto**.</span><span class="sxs-lookup"><span data-stu-id="7e255-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="7e255-119">Na lista de entidades legais disponíveis, selecione as entidades onde várias linhas de contrato e recursos do Project Operations no Dynamics 365 Customer Engagement serão habilitados.</span><span class="sxs-lookup"><span data-stu-id="7e255-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="7e255-120">Deixe desmarcadas as entidades legais que usarão o Project Operations para cenários com estoque/ordem de produção.</span><span class="sxs-lookup"><span data-stu-id="7e255-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="7e255-121">Uma entidade legal pode ser selecionada apenas se não tiver nenhum projeto existente.</span><span class="sxs-lookup"><span data-stu-id="7e255-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="7e255-122">Configurar parâmetros de gerenciamento e contabilidade de projeto</span><span class="sxs-lookup"><span data-stu-id="7e255-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="7e255-123">Cada entidade legal que usa o Project Operations no Dynamics 365 Customer Engagement precisa de um conjunto de parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="7e255-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="7e255-124">Esses parâmetros são configurados na guia **Project Operations** da página **Parâmetros de gerenciamento e contabilidade de projeto**.</span><span class="sxs-lookup"><span data-stu-id="7e255-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="7e255-125">Os parâmetros são:</span><span class="sxs-lookup"><span data-stu-id="7e255-125">The parameters are:</span></span>

  - <span data-ttu-id="7e255-126">**Padrões de tipo de cobrança**: o Project Operations usa um conjunto fixo de padrões de tipo de cobrança que deve ser mapeado para as propriedades de linha Finance.</span><span class="sxs-lookup"><span data-stu-id="7e255-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="7e255-127">Crie um registro para cada tipo de cobrança: **Não especificado**, **Passível de Cobrança**, **Não Passível de Cobrança**, **Complementar** e **Não disponível**.</span><span class="sxs-lookup"><span data-stu-id="7e255-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="7e255-128">**Padrões de categoria de projeto**: selecione as categorias de projeto padrão a serem usadas para cada tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="7e255-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="7e255-129">Esses padrões serão usados no **Diário de integração de operações do projeto** e em estimativas onde nenhuma categoria de transação é especificada para o projeto real.</span><span class="sxs-lookup"><span data-stu-id="7e255-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="7e255-130">**Previsões**: selecione o modelo de previsão a ser usado para estimativas de tempo e despesas.</span><span class="sxs-lookup"><span data-stu-id="7e255-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]