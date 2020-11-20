---
title: Definir calendários de recurso
description: Este tópico fornece informações sobre como definir os calendários de horas de trabalho para recursos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: daa49cf8ba9ba005a16777f590c4c06d024de529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123904"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="61865-103">Definir calendários de recurso</span><span class="sxs-lookup"><span data-stu-id="61865-103">Define resource calendars</span></span>

<span data-ttu-id="61865-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="61865-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="61865-105">Todos os recursos reserváveis que estiverem trabalhando em um projeto devem ter um calendário de horas de trabalho para definir sua disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="61865-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="61865-106">As horas de trabalho de um recurso podem ser definidas de duas formas:</span><span class="sxs-lookup"><span data-stu-id="61865-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="61865-107">Definir regras de calendário individuais para um recurso</span><span class="sxs-lookup"><span data-stu-id="61865-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="61865-108">Aplicar um modelo de calendário existente para o recurso</span><span class="sxs-lookup"><span data-stu-id="61865-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="61865-109">Definir as horas de trabalho de um recurso</span><span class="sxs-lookup"><span data-stu-id="61865-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="61865-110">No menu **Recursos**, selecione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="61865-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="61865-111">Na visualização de grade, selecione o **Recurso Reservável** aplicável.</span><span class="sxs-lookup"><span data-stu-id="61865-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="61865-112">Na página **Detalhes do Recurso**, selecione a guia **Horas de Trabalho**. Por padrão, o calendário de recursos reserváveis é padronizado com as horas de trabalho do modelo padrão de horas de trabalho definido pela organização.</span><span class="sxs-lookup"><span data-stu-id="61865-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="61865-113">Para atualizar as horas de trabalho, clique com o botão direito na data de início da regra de calendário proposta que será definida.</span><span class="sxs-lookup"><span data-stu-id="61865-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="61865-114">Use o menu de regra de calendário para definir a regra de calendário para um dia específico, o restante da série ou todo o calendário.</span><span class="sxs-lookup"><span data-stu-id="61865-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="61865-115">Depois de selecionar a opção, é possível definir:</span><span class="sxs-lookup"><span data-stu-id="61865-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="61865-116">O dia da semana ao qual as horas de trabalho serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="61865-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="61865-117">As horas de trabalho de cada dia.</span><span class="sxs-lookup"><span data-stu-id="61865-117">The working times within each day.</span></span>
    - <span data-ttu-id="61865-118">O fuso horário da regra de calendário.</span><span class="sxs-lookup"><span data-stu-id="61865-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="61865-119">Se aplicável, o tempo de folga também poderá ser especificado para a regra.</span><span class="sxs-lookup"><span data-stu-id="61865-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="61865-120">Aplicando um modelo de calendário a um recurso</span><span class="sxs-lookup"><span data-stu-id="61865-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="61865-121">No menu **Recursos**, selecione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="61865-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="61865-122">Na visualização de grade, selecione até 25 **Recursos Reserváveis** para atualizar.</span><span class="sxs-lookup"><span data-stu-id="61865-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="61865-123">Selecione **Definir Calendário** e uma caixa de diálogo exibirá uma lista de modelos de horas de trabalho disponíveis.</span><span class="sxs-lookup"><span data-stu-id="61865-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="61865-124">Selecione o modelo que deseja usar e depois selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="61865-124">Select the template you want to use, and then select **Apply**.</span></span>
