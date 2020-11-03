---
title: Atualizar um projeto
description: Este tópico fornece informações sobre a atualização de projetos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071283"
---
# <a name="update-a-project"></a><span data-ttu-id="2597d-103">Atualizar um projeto</span><span class="sxs-lookup"><span data-stu-id="2597d-103">Update a project</span></span>

<span data-ttu-id="2597d-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="2597d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2597d-105">Veja a seguir um resumo dos campos que podem ser atualizados em um projeto após sua criação e todas as implicações aplicáveis das atualizações.</span><span class="sxs-lookup"><span data-stu-id="2597d-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="2597d-106">Campos de detalhes do projeto</span><span class="sxs-lookup"><span data-stu-id="2597d-106">Project detail fields</span></span>

- <span data-ttu-id="2597d-107">**Nome** : o título do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="2597d-108">**Descrição** : uma visão geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="2597d-109">**Cliente** : a empresa para a qual o projeto será entregue.</span><span class="sxs-lookup"><span data-stu-id="2597d-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="2597d-110">**Modelo de calendário** : as horas de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="2597d-111">Quando o campo é alterado, toda a agenda é recalculada.</span><span class="sxs-lookup"><span data-stu-id="2597d-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="2597d-112">**Moeda** : a moeda do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="2597d-113">Este campo é padronizado com base na moeda definida na unidade de contratação.</span><span class="sxs-lookup"><span data-stu-id="2597d-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="2597d-114">Quando a unidade de contratação é atualizada, o campo também é atualizado.</span><span class="sxs-lookup"><span data-stu-id="2597d-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="2597d-115">**Unidade de Contratação** : a unidade organizacional que representa o grupo ou a divisão da empresa que primariamente é responsável por efetuar vendas e gerenciar a prestação de trabalho e serviços ao cliente.</span><span class="sxs-lookup"><span data-stu-id="2597d-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="2597d-116">**Gerente de Projeto** : o membro da equipe do projeto que tem autoridade para revisar e aprovar entradas de horas e despesas.</span><span class="sxs-lookup"><span data-stu-id="2597d-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="2597d-117">Campos de estimativa</span><span class="sxs-lookup"><span data-stu-id="2597d-117">Estimate fields</span></span>

- <span data-ttu-id="2597d-118">**Data de Início Estimada** : a data de início do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="2597d-119">Quando este campo é atualizado, todas as tarefas no projeto são movidas proporcionalmente com a nova data de início.</span><span class="sxs-lookup"><span data-stu-id="2597d-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="2597d-120">**Data de Término** : a data em que o projeto está programado para terminar.</span><span class="sxs-lookup"><span data-stu-id="2597d-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="2597d-121">**Esforço** : o esforço estimado do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="2597d-122">Quando as tarefas são adicionadas ao projeto, este campo não é mais editável.</span><span class="sxs-lookup"><span data-stu-id="2597d-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="2597d-123">**Custo Estimado de Mão de Obra** : o custo estimado da mão de obra do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="2597d-124">Quando os custos de mão de obra são adicionadas ao projeto, este campo não é mais editável.</span><span class="sxs-lookup"><span data-stu-id="2597d-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="2597d-125">**Despesas Estimadas** : as despesas estimadas do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="2597d-126">Quando as despesas são adicionadas ao projeto, este campo não é mais editável.</span><span class="sxs-lookup"><span data-stu-id="2597d-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="2597d-127">Campos reais do projeto</span><span class="sxs-lookup"><span data-stu-id="2597d-127">Project actual fields</span></span>
- <span data-ttu-id="2597d-128">**Início Real** : a data de início do projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="2597d-129">**Término Real** : a ser atualizado quando um projeto for concluído.</span><span class="sxs-lookup"><span data-stu-id="2597d-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="2597d-130">Campos de status de projetos</span><span class="sxs-lookup"><span data-stu-id="2597d-130">Project status fields</span></span>

- <span data-ttu-id="2597d-131">**Status Geral do Projeto** : a integridade geral do projeto fornecida pelo gerente de projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="2597d-132">**Comentários** : uma narrativa sobre a integridade atual do projeto fornecida pelo gerente de projeto.</span><span class="sxs-lookup"><span data-stu-id="2597d-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

