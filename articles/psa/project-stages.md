---
title: Tipos de estágio do projeto
description: Este tópico fornece informações sobre os estágios do projeto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123026"
---
# <a name="project-stage-types"></a><span data-ttu-id="a0c44-103">Tipos de estágio do projeto</span><span class="sxs-lookup"><span data-stu-id="a0c44-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a0c44-104">Os estágios do projeto são elaborados para refletir o estado do projeto conforme o progresso.</span><span class="sxs-lookup"><span data-stu-id="a0c44-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="a0c44-105">As personalizações podem ser usadas para atualizar os estágios automaticamente com fluxos do processo empresarial, Power Automate, ou extensões de plug-in.</span><span class="sxs-lookup"><span data-stu-id="a0c44-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="a0c44-106">Os estágios a seguir são definidos no BPF padrão:</span><span class="sxs-lookup"><span data-stu-id="a0c44-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="a0c44-107">Nova</span><span class="sxs-lookup"><span data-stu-id="a0c44-107">New</span></span>
- <span data-ttu-id="a0c44-108">Cotação</span><span class="sxs-lookup"><span data-stu-id="a0c44-108">Quote</span></span>
- <span data-ttu-id="a0c44-109">Planejar</span><span class="sxs-lookup"><span data-stu-id="a0c44-109">Plan</span></span>
- <span data-ttu-id="a0c44-110">Entregar</span><span class="sxs-lookup"><span data-stu-id="a0c44-110">Deliver</span></span>
- <span data-ttu-id="a0c44-111">Concluído</span><span class="sxs-lookup"><span data-stu-id="a0c44-111">Complete</span></span>
- <span data-ttu-id="a0c44-112">Fechar</span><span class="sxs-lookup"><span data-stu-id="a0c44-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="a0c44-113">Novo</span><span class="sxs-lookup"><span data-stu-id="a0c44-113">New</span></span>

<span data-ttu-id="a0c44-114">Ao criar um projeto, o estágio dele é definido como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a0c44-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="a0c44-115">Se o projeto foi criado com base em um modelo, ele pode ter dados de agenda, estimativas e equipe.</span><span class="sxs-lookup"><span data-stu-id="a0c44-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="a0c44-116">Caso contrário, é apenas um resumo do projeto e os componentes restantes devem ser inseridos.</span><span class="sxs-lookup"><span data-stu-id="a0c44-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="a0c44-117">Cotação</span><span class="sxs-lookup"><span data-stu-id="a0c44-117">Quote</span></span>

<span data-ttu-id="a0c44-118">Ao associar um projeto a uma cotação ou criar um projeto com base em uma cotação, o estágio do projeto é definido como **Cotação** e as datas estimadas de início e de término são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="a0c44-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="a0c44-119">Enquanto o projeto está no estágio **Cotação**, a guia **Vendas** na página **Entidade de Projeto** exibe detalhes da cotação.</span><span class="sxs-lookup"><span data-stu-id="a0c44-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="a0c44-120">Planejar</span><span class="sxs-lookup"><span data-stu-id="a0c44-120">Plan</span></span>

<span data-ttu-id="a0c44-121">Quando você vence uma cotação associada a um projeto e este é movido para a fase **Contrato**, o estágio do projeto é atualizado para **Planejar**.</span><span class="sxs-lookup"><span data-stu-id="a0c44-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="a0c44-122">Enquanto o projeto está no estágio **Planejar**, a página **Entidade de Projeto** exibe detalhes do contrato.</span><span class="sxs-lookup"><span data-stu-id="a0c44-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="a0c44-123">Entregar</span><span class="sxs-lookup"><span data-stu-id="a0c44-123">Deliver</span></span>

<span data-ttu-id="a0c44-124">Quando o plano do projeto estiver concluído e você estiver pronto para iniciar o projeto, o gerente deverá atualizar o estágio do projeto para **Entregar** a fim de mostrar que o projeto foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="a0c44-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="a0c44-125">Concluído</span><span class="sxs-lookup"><span data-stu-id="a0c44-125">Complete</span></span> 

<span data-ttu-id="a0c44-126">Quando o trabalho no projeto estiver concluído, o gerente do projeto poderá atualizar o estágio para **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="a0c44-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="a0c44-127">Ao atualizar o estágio do projeto para **Concluído**, o gerente indica que o trabalho está 100% concluído, mas que o projeto está sendo mantido aberto para que quaisquer entradas pendentes de hora ou despesa possam ser registradas.</span><span class="sxs-lookup"><span data-stu-id="a0c44-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="a0c44-128">Fechar</span><span class="sxs-lookup"><span data-stu-id="a0c44-128">Close</span></span>

<span data-ttu-id="a0c44-129">Quando todas as transações do projeto estiverem registradas, o gerente do projeto poderá atualizar o estágio para **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="a0c44-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="a0c44-130">Nesse momento, nenhuma transação pode ser registrada e o projeto é definido como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a0c44-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>