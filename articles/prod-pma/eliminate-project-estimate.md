---
title: Eliminar um estimativa de projeto
description: Este tópico fornece informações sobre como eliminar uma estimativa do projeto após sua conclusão.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006902"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="9fd02-103">Eliminar um estimativa de projeto</span><span class="sxs-lookup"><span data-stu-id="9fd02-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fd02-104">As estimativas de projeto fornecem a visão financeira do trabalho estimado e agendado para um projeto.</span><span class="sxs-lookup"><span data-stu-id="9fd02-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="9fd02-105">Para trabalhar com estimativas de projeto, você deve anexar o projeto a uma estimativa de projeto.</span><span class="sxs-lookup"><span data-stu-id="9fd02-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="9fd02-106">Uma estimativa de projeto é sempre baseada em um projeto existente; no entanto, vários projetos podem se referir a uma única estimativa de projeto.</span><span class="sxs-lookup"><span data-stu-id="9fd02-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="9fd02-107">Apenas os projetos de preço fixo e de investimento podem ser anexados às estimativas de projetos. Esses projetos devem pertencer ao mesmo grupo de projetos que a estimativa do projeto.</span><span class="sxs-lookup"><span data-stu-id="9fd02-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="9fd02-108">Para eliminar uma estimativa de projeto, ela deve ser concluída.</span><span class="sxs-lookup"><span data-stu-id="9fd02-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="9fd02-109">As etapas a seguir explicam como eliminar uma estimativa.</span><span class="sxs-lookup"><span data-stu-id="9fd02-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="9fd02-110">Vá para **Gerenciamento e contabilidade de projetos** > **Todos os Projetos** e abra o projeto.</span><span class="sxs-lookup"><span data-stu-id="9fd02-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="9fd02-111">Na guia **Gerenciar**, selecione **Estimativas**. Na página **Estimativa**, selecione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="9fd02-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="9fd02-112">Na página **Eliminar estimativa** na guia **Geral**, defina as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="9fd02-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="9fd02-113">**Código de período**: selecione o código do período para escolher as estimativas de projeto apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9fd02-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="9fd02-114">**Data estimada**: selecione a data estimada apropriada para eliminação.</span><span class="sxs-lookup"><span data-stu-id="9fd02-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="9fd02-115">**Eliminar com avisos WIP**: habilite esta opção para fornecer notificação quando uma estimativa associada a um trabalho em andamento (WIP) for eliminada.</span><span class="sxs-lookup"><span data-stu-id="9fd02-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="9fd02-116">Quando esta opção não estiver habilitada, a eliminação não poderá continuar se houver transações não estimadas.</span><span class="sxs-lookup"><span data-stu-id="9fd02-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="9fd02-117">Esta opção está disponível apenas quando a eliminação é aplicada a uma estimativa de projeto.</span><span class="sxs-lookup"><span data-stu-id="9fd02-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="9fd02-118">Ela não estará disponível se você estiver usando postagens periódicas.</span><span class="sxs-lookup"><span data-stu-id="9fd02-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="9fd02-119">Esta configuração funciona com as configurações na guia **Estimativa** na página **Parâmetros do projeto**, no grupo de campos **Permitir eliminação quando houver transações não estimadas**.</span><span class="sxs-lookup"><span data-stu-id="9fd02-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="9fd02-120">**Definir estágio como Concluído**: habilite esta opção para definir o estágio de estimativa do projeto como **Concluído** depois de executar a eliminação.</span><span class="sxs-lookup"><span data-stu-id="9fd02-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="9fd02-121">**Imprimir lista de estimativa**: selecione as informações a serem incluídas quando a lista de orçamentos for impressa.</span><span class="sxs-lookup"><span data-stu-id="9fd02-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="9fd02-122">**Mostrar Log de Informações**: habilite esta opção para exibir o log de informações.</span><span class="sxs-lookup"><span data-stu-id="9fd02-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="9fd02-123">**Data de postagem**: escolha a data de lançamento contábil da estimativa.</span><span class="sxs-lookup"><span data-stu-id="9fd02-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="9fd02-124">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fd02-124">Select **OK**.</span></span>
5. <span data-ttu-id="9fd02-125">Após a conclusão do processo de eliminação, a estimativa do projeto eliminada é exibida com um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="9fd02-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="9fd02-126">Se você não pretendia eliminar uma estimativa, poderá selecionar a estimativa eliminada e selecionar **Reverter eliminação**.</span><span class="sxs-lookup"><span data-stu-id="9fd02-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]