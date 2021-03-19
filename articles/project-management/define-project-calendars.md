---
title: Definir calendários de projeto
description: Este tópico fornece informações sobre como usar um calendário de projeto para controlar o cronograma do projeto.
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286954"
---
# <a name="define-project-calendars"></a><span data-ttu-id="2cb18-103">Definir calendários de projeto</span><span class="sxs-lookup"><span data-stu-id="2cb18-103">Define project calendars</span></span>

<span data-ttu-id="2cb18-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="2cb18-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2cb18-105">Para criar uma agenda de projeto, crie um modelo de calendário de projeto que defina o número de horas de trabalho por dia e todos os feriados comerciais.</span><span class="sxs-lookup"><span data-stu-id="2cb18-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="2cb18-106">Para criar um modelo de calendário de projeto, associe um modelo de trabalho ao campo **Modelo de calendário** do projeto.</span><span class="sxs-lookup"><span data-stu-id="2cb18-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="2cb18-107">Siga estas etapas para criar um modelo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2cb18-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="2cb18-108">No painel de navegação à esquerda, selecione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="2cb18-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="2cb18-109">Na página de lista **Recursos**, abra um registro de usuário e selecione **Mostrar Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="2cb18-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="2cb18-110">Certifique-se de permitir pop-ups na página do navegador.</span><span class="sxs-lookup"><span data-stu-id="2cb18-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="2cb18-111">Isso permite ver as horas de trabalho definidas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="2cb18-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="2cb18-112">Na guia **Exibição Mensal**, selecione **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="2cb18-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="2cb18-113">Uma lista de três opções é exibida:</span><span class="sxs-lookup"><span data-stu-id="2cb18-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="2cb18-114">Nova Agenda Semanal</span><span class="sxs-lookup"><span data-stu-id="2cb18-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="2cb18-115">Agenda de Trabalho para Um Dia</span><span class="sxs-lookup"><span data-stu-id="2cb18-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="2cb18-116">Folga</span><span class="sxs-lookup"><span data-stu-id="2cb18-116">Time Off</span></span>

4. <span data-ttu-id="2cb18-117">Selecione **Nova Agenda Semanal** e defina as opções para essa agenda de recurso.</span><span class="sxs-lookup"><span data-stu-id="2cb18-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="2cb18-118">Você pode definir uma agenda semanal recorrente, parâmetros de hora diários, feriados comerciais e muito mais.</span><span class="sxs-lookup"><span data-stu-id="2cb18-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="2cb18-119">Defina um intervalo de datas, selecione **Salvar** e **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="2cb18-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="2cb18-120">Volte para a página de lista **Recursos** e selecione o recurso para o qual você definiu as horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2cb18-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="2cb18-121">Selecione **Definir Calendário como** para definir o modelo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2cb18-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="2cb18-122">Na caixa de diálogo **Modelo de Trabalho**, insira um nome para o modelo de trabalho e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="2cb18-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="2cb18-123">Agora é possível associar o modelo de trabalho a um modelo de calendário de projeto.</span><span class="sxs-lookup"><span data-stu-id="2cb18-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]