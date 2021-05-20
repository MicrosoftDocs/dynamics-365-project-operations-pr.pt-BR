---
title: Criar um modelo de horas de trabalho
description: Este tópico descreve como criar um modelo de horas de trabalho no Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981241"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="19ab7-103">Criar um modelo de horário de trabalho (Project Service)</span><span class="sxs-lookup"><span data-stu-id="19ab7-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="19ab7-104">Para criar e gerenciar um projeto, você deve aplicar um modelo de calendário ao projeto.</span><span class="sxs-lookup"><span data-stu-id="19ab7-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="19ab7-105">O modelo de calendário define os seguintes atributos de projeto:</span><span class="sxs-lookup"><span data-stu-id="19ab7-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="19ab7-106">Horas de trabalho, incluindo horário de início e término</span><span class="sxs-lookup"><span data-stu-id="19ab7-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="19ab7-107">Dias úteis</span><span class="sxs-lookup"><span data-stu-id="19ab7-107">Working days</span></span>
- <span data-ttu-id="19ab7-108">Exceções de calendário, como dias não úteis</span><span class="sxs-lookup"><span data-stu-id="19ab7-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="19ab7-109">O modelo de calendário aplicado a um projeto é uma cópia do modelo de calendário definido nas configurações da sua organização.</span><span class="sxs-lookup"><span data-stu-id="19ab7-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="19ab7-110">Se você alterar o modelo de calendário, essas alterações não se propagarão para as horas de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="19ab7-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="19ab7-111">Para alterar as horas de trabalho do projeto, um novo modelo deve ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="19ab7-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="19ab7-112">Para criar um modelo de calendário para sua organização, existem dois requisitos principais:</span><span class="sxs-lookup"><span data-stu-id="19ab7-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="19ab7-113">Defina as horas de trabalho desejadas do modelo usando um recurso reservável novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="19ab7-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="19ab7-114">Crie um novo modelo de calendário e associe o modelo ao recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="19ab7-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="19ab7-115">**Defina as horas de trabalho do modelo**</span><span class="sxs-lookup"><span data-stu-id="19ab7-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="19ab7-116">Vá para **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="19ab7-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="19ab7-117">Crie um novo recurso para fazer referência no modelo de calendário ou selecione um recurso existente.</span><span class="sxs-lookup"><span data-stu-id="19ab7-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="19ab7-118">Selecione a guia **Horas de Trabalho** do recurso e complete as instruções em [Definir horas de trabalho para um recurso](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) para configurar as regras de calendário.</span><span class="sxs-lookup"><span data-stu-id="19ab7-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="19ab7-119">**Criar um novo modelo de calendário**</span><span class="sxs-lookup"><span data-stu-id="19ab7-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="19ab7-120">Acesse **Configurações** \> **Modelo de Calendário**.</span><span class="sxs-lookup"><span data-stu-id="19ab7-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="19ab7-121">Selecione **Novo** e insira um nome, uma descrição e um recurso de modelo.</span><span class="sxs-lookup"><span data-stu-id="19ab7-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="19ab7-122">Quando um recurso é referenciado em um modelo de calendário, uma cópia do calendário do recurso é associada ao modelo de calendário.</span><span class="sxs-lookup"><span data-stu-id="19ab7-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="19ab7-123">Se as horas de trabalho do modelo copiado mudarem, essas alterações não serão propagadas no modelo de calendário.</span><span class="sxs-lookup"><span data-stu-id="19ab7-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="19ab7-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="19ab7-124">See Also</span></span>  
 [<span data-ttu-id="19ab7-125">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="19ab7-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
