---
title: Estágios do projeto
description: Este tópico fornece informações sobre os estágios do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749049"
---
# <a name="project-stages"></a><span data-ttu-id="15118-103">Estágios do projeto</span><span class="sxs-lookup"><span data-stu-id="15118-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="15118-104">Os estágios do projeto são atualizados para refletir o estado do projeto conforme ele avança.</span><span class="sxs-lookup"><span data-stu-id="15118-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="15118-105">O fluxo do processo empresarial padrão atualiza automaticamente alguns estágios do projeto enquanto outros são atualizados pelo gerente de projetos.</span><span class="sxs-lookup"><span data-stu-id="15118-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="15118-106">Os estágios a seguir são definidos no BPF padrão:</span><span class="sxs-lookup"><span data-stu-id="15118-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="15118-107">Novo</span><span class="sxs-lookup"><span data-stu-id="15118-107">New</span></span>
- <span data-ttu-id="15118-108">Cotação</span><span class="sxs-lookup"><span data-stu-id="15118-108">Quote</span></span>
- <span data-ttu-id="15118-109">Planejar</span><span class="sxs-lookup"><span data-stu-id="15118-109">Plan</span></span>
- <span data-ttu-id="15118-110">Entregar</span><span class="sxs-lookup"><span data-stu-id="15118-110">Deliver</span></span>
- <span data-ttu-id="15118-111">Concluído</span><span class="sxs-lookup"><span data-stu-id="15118-111">Complete</span></span>
- <span data-ttu-id="15118-112">Fechar</span><span class="sxs-lookup"><span data-stu-id="15118-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="15118-113">Novo</span><span class="sxs-lookup"><span data-stu-id="15118-113">New</span></span>

<span data-ttu-id="15118-114">Ao criar um projeto, o estágio dele é definido como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="15118-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="15118-115">Se o projeto foi criado com base em um modelo, ele pode ter dados de agenda, estimativas e equipe.</span><span class="sxs-lookup"><span data-stu-id="15118-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="15118-116">Caso contrário, é apenas um resumo do projeto e os componentes restantes devem ser inseridos.</span><span class="sxs-lookup"><span data-stu-id="15118-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="15118-117">Cotação</span><span class="sxs-lookup"><span data-stu-id="15118-117">Quote</span></span>

<span data-ttu-id="15118-118">Ao associar um projeto a uma cotação ou criar um projeto com base em uma cotação, o estágio do projeto é definido como **Cotação** e as datas estimadas de início e de término são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="15118-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="15118-119">Enquanto o projeto está no estágio **Cotação**, a guia **Vendas** na página **Entidade de Projeto** exibe detalhes da cotação.</span><span class="sxs-lookup"><span data-stu-id="15118-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="15118-120">Planejar</span><span class="sxs-lookup"><span data-stu-id="15118-120">Plan</span></span>

<span data-ttu-id="15118-121">Quando você vence uma cotação associada a um projeto e este é movido para a fase **Contrato**, o estágio do projeto é atualizado para **Planejar**.</span><span class="sxs-lookup"><span data-stu-id="15118-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="15118-122">Enquanto o projeto está no estágio **Planejar**, a página **Entidade de Projeto** exibe detalhes do contrato.</span><span class="sxs-lookup"><span data-stu-id="15118-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="15118-123">Entregar</span><span class="sxs-lookup"><span data-stu-id="15118-123">Deliver</span></span>

<span data-ttu-id="15118-124">Quando o plano do projeto estiver concluído e você estiver pronto para iniciar o projeto, o gerente deverá atualizar o estágio do projeto para **Entregar** a fim de mostrar que o projeto foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="15118-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="15118-125">Concluído</span><span class="sxs-lookup"><span data-stu-id="15118-125">Complete</span></span> 

<span data-ttu-id="15118-126">Quando o trabalho no projeto estiver concluído, o gerente do projeto poderá atualizar o estágio para **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="15118-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="15118-127">Ao atualizar o estágio do projeto para **Concluído**, o gerente indica que o trabalho está 100% concluído, mas que o projeto está sendo mantido aberto para que quaisquer entradas pendentes de hora ou despesa possam ser registradas.</span><span class="sxs-lookup"><span data-stu-id="15118-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="15118-128">Fechar</span><span class="sxs-lookup"><span data-stu-id="15118-128">Close</span></span>

<span data-ttu-id="15118-129">Quando todas as transações do projeto estiverem registradas, o gerente do projeto poderá atualizar o estágio para **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="15118-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="15118-130">Nesse momento, nenhuma transação pode ser registrada e o projeto é definido como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="15118-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
