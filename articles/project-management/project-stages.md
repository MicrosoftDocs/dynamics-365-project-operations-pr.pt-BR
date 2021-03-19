---
title: Estágios do projeto
description: Este tópico fornece informações sobre as etapas do projeto que estão disponíveis em Operações do projeto do Microsoft Dynamics.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286774"
---
# <a name="project-stages"></a><span data-ttu-id="26451-103">Estágios do projeto</span><span class="sxs-lookup"><span data-stu-id="26451-103">Project stages</span></span>

<span data-ttu-id="26451-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="26451-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26451-105">Os estágios do projeto são elaborados para refletir o estado do projeto conforme o progresso.</span><span class="sxs-lookup"><span data-stu-id="26451-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="26451-106">As personalizações podem ser usadas para atualizar os estágios automaticamente com fluxos do processo empresarial, Power Automate, ou extensões de plug-in.</span><span class="sxs-lookup"><span data-stu-id="26451-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="26451-107">Os seguintes estágios são definidos no fluxo do processo empresarial padrão:</span><span class="sxs-lookup"><span data-stu-id="26451-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="26451-108">Criar</span><span class="sxs-lookup"><span data-stu-id="26451-108">New</span></span>
- <span data-ttu-id="26451-109">Cotação</span><span class="sxs-lookup"><span data-stu-id="26451-109">Quote</span></span>
- <span data-ttu-id="26451-110">Plano</span><span class="sxs-lookup"><span data-stu-id="26451-110">Plan</span></span>
- <span data-ttu-id="26451-111">Entregar</span><span class="sxs-lookup"><span data-stu-id="26451-111">Deliver</span></span>
- <span data-ttu-id="26451-112">Complete</span><span class="sxs-lookup"><span data-stu-id="26451-112">Complete</span></span>
- <span data-ttu-id="26451-113">Fechar</span><span class="sxs-lookup"><span data-stu-id="26451-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="26451-114">Criar</span><span class="sxs-lookup"><span data-stu-id="26451-114">New</span></span>

<span data-ttu-id="26451-115">Ao criar um projeto, o estágio dele é definido como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="26451-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="26451-116">Se o projeto foi criado com base em um modelo, ele pode ter dados de agenda, estimativas e equipe.</span><span class="sxs-lookup"><span data-stu-id="26451-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="26451-117">Caso contrário, é um resumo do projeto e os componentes restantes devem ser inseridos.</span><span class="sxs-lookup"><span data-stu-id="26451-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="26451-118">Cotação</span><span class="sxs-lookup"><span data-stu-id="26451-118">Quote</span></span>

<span data-ttu-id="26451-119">Ao associar um projeto a uma cotação ou criar um projeto com base em uma cotação, o estágio do projeto é definido como **Cotação** e as datas estimadas de início e de término são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="26451-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="26451-120">Enquanto o projeto está no estágio **Cotação**, a guia **Vendas** na página **Entidade de Projeto** exibe detalhes da cotação.</span><span class="sxs-lookup"><span data-stu-id="26451-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="26451-121">Planejar</span><span class="sxs-lookup"><span data-stu-id="26451-121">Plan</span></span>

<span data-ttu-id="26451-122">Quando você vence uma cotação associada a um projeto e este é movido para a fase **Contrato**, o estágio do projeto é atualizado para **Planejar**.</span><span class="sxs-lookup"><span data-stu-id="26451-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="26451-123">Enquanto o projeto está no estágio **Planejar**, a página **Entidade de Projeto** exibe detalhes do contrato.</span><span class="sxs-lookup"><span data-stu-id="26451-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="26451-124">Entregar</span><span class="sxs-lookup"><span data-stu-id="26451-124">Deliver</span></span>

<span data-ttu-id="26451-125">Quando o plano do projeto estiver concluído e você estiver pronto para iniciar o projeto, o gerente deverá atualizar o estágio do projeto para **Entregar** a fim de mostrar que o projeto foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="26451-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="26451-126">Concluído</span><span class="sxs-lookup"><span data-stu-id="26451-126">Complete</span></span> 

<span data-ttu-id="26451-127">Quando o trabalho no projeto estiver concluído, o gerente do projeto poderá atualizar o estágio para **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="26451-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="26451-128">Ao atualizar o estágio do projeto para **Concluído**, o gerente indica que o trabalho está 100% concluído, mas que o projeto está sendo mantido aberto para que quaisquer entradas pendentes de hora ou despesa possam ser registradas.</span><span class="sxs-lookup"><span data-stu-id="26451-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="26451-129">Fechar</span><span class="sxs-lookup"><span data-stu-id="26451-129">Close</span></span>

<span data-ttu-id="26451-130">Quando todas as transações do projeto estiverem registradas, o gerente do projeto poderá atualizar o estágio para **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="26451-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="26451-131">Nesse momento, nenhuma transação pode ser registrada e o projeto é definido como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="26451-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]