---
title: Definir calendários de projeto
description: Este tópico fornece informações sobre como aplicar um modelo de calendário a um projeto para rastrear a agenda do projeto.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998982"
---
# <a name="define-project-calendars"></a><span data-ttu-id="24214-103">Definir calendários de projeto</span><span class="sxs-lookup"><span data-stu-id="24214-103">Define project calendars</span></span>

<span data-ttu-id="24214-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="24214-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="24214-105">Para criar e gerenciar um projeto, você deve aplicar um modelo de calendário ao projeto.</span><span class="sxs-lookup"><span data-stu-id="24214-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="24214-106">O modelo de calendário define os seguintes atributos de projeto:</span><span class="sxs-lookup"><span data-stu-id="24214-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="24214-107">Horas de trabalho, incluindo horário de início e término</span><span class="sxs-lookup"><span data-stu-id="24214-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="24214-108">Dias úteis</span><span class="sxs-lookup"><span data-stu-id="24214-108">Working days</span></span>
- <span data-ttu-id="24214-109">Exceções de calendário, como dias não úteis</span><span class="sxs-lookup"><span data-stu-id="24214-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="24214-110">O modelo de calendário aplicado a um projeto é uma cópia do modelo de calendário definido nas configurações da sua organização.</span><span class="sxs-lookup"><span data-stu-id="24214-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="24214-111">Se você alterar o modelo de calendário, essas alterações não se propagarão para as horas de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="24214-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="24214-112">Para alterar as horas de trabalho do projeto, um novo modelo deve ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="24214-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="24214-113">Para criar um modelo de calendário para sua organização, existem dois requisitos principais:</span><span class="sxs-lookup"><span data-stu-id="24214-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="24214-114">Defina as horas de trabalho desejadas do modelo usando um recurso reservável novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="24214-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="24214-115">Crie um novo modelo de calendário e associe o modelo ao recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="24214-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="24214-116">**Defina as horas de trabalho do modelo**</span><span class="sxs-lookup"><span data-stu-id="24214-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="24214-117">Vá para **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="24214-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="24214-118">Crie um novo recurso para fazer referência no modelo de calendário ou selecione um recurso existente.</span><span class="sxs-lookup"><span data-stu-id="24214-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="24214-119">Selecione a guia **Horas de Trabalho** do recurso e complete as instruções em [Definir horas de trabalho para um recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar as regras de calendário.</span><span class="sxs-lookup"><span data-stu-id="24214-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="24214-120">**Criar um novo modelo de calendário**</span><span class="sxs-lookup"><span data-stu-id="24214-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="24214-121">Acesse **Configurações** \> **Modelo de Calendário**.</span><span class="sxs-lookup"><span data-stu-id="24214-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="24214-122">Selecione **Novo** e insira um nome, uma descrição e um recurso de modelo.</span><span class="sxs-lookup"><span data-stu-id="24214-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="24214-123">Quando um recurso é referenciado em um modelo de calendário, uma cópia do calendário do recurso é associada ao modelo de calendário.</span><span class="sxs-lookup"><span data-stu-id="24214-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="24214-124">Se as horas de trabalho do modelo copiado mudarem, essas alterações não serão propagadas no modelo de calendário.</span><span class="sxs-lookup"><span data-stu-id="24214-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="24214-125">Agora é possível associar o modelo de trabalho a um modelo de calendário de projeto.</span><span class="sxs-lookup"><span data-stu-id="24214-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

