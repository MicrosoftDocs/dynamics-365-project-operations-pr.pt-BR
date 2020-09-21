---
title: Configurações do projeto
description: Este tópico fornece informações sobre configurações de gerenciamento do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749050"
---
# <a name="project-settings"></a><span data-ttu-id="32237-103">Configurações do projeto</span><span class="sxs-lookup"><span data-stu-id="32237-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="32237-104">Use as configurações a seguir para acessar os recursos de planejamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="32237-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="32237-105">Modelo de trabalho</span><span class="sxs-lookup"><span data-stu-id="32237-105">Work template</span></span>

<span data-ttu-id="32237-106">Para criar uma agenda de projeto, crie um modelo de calendário de projeto que defina o número de horas de trabalho por dia e todos os feriados comerciais.</span><span class="sxs-lookup"><span data-stu-id="32237-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="32237-107">Para criar um modelo de calendário de projeto, associe um modelo de trabalho ao campo **Modelo de calendário** do projeto.</span><span class="sxs-lookup"><span data-stu-id="32237-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="32237-108">Siga estas etapas para criar um modelo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="32237-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="32237-109">No PSA, no painel de navegação à esquerda, clique em **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="32237-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="32237-110">Na página de lista **Recursos**, abra um registro de usuário e selecione **Mostrar Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="32237-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="32237-111">Certifique-se de permitir pop-ups na página do navegador.</span><span class="sxs-lookup"><span data-stu-id="32237-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="32237-112">Isso permite ver as horas de trabalho definidas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="32237-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="32237-113">Na guia **Exibição Mensal**, clique em **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="32237-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="32237-114">Uma lista de três opções é exibida:</span><span class="sxs-lookup"><span data-stu-id="32237-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="32237-115">Nova Agenda Semanal</span><span class="sxs-lookup"><span data-stu-id="32237-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="32237-116">Agenda de Trabalho para Um Dia</span><span class="sxs-lookup"><span data-stu-id="32237-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="32237-117">Folga</span><span class="sxs-lookup"><span data-stu-id="32237-117">Time Off</span></span>

> ![Configurar opções](media/project-13.png)

4. <span data-ttu-id="32237-119">Selecione **Nova Agenda Semanal** e defina as opções para essa agenda de recurso.</span><span class="sxs-lookup"><span data-stu-id="32237-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="32237-120">Você pode definir uma agenda semanal recorrente, parâmetros de hora diários, feriados comerciais e muito mais.</span><span class="sxs-lookup"><span data-stu-id="32237-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="32237-121">Defina um intervalo de datas, selecione **Salvar** e clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="32237-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="32237-122">Volte para a página de lista **Recursos** e selecione o recurso para o qual você definiu as horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="32237-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="32237-123">Selecione **Definir Calendário como** para definir o modelo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="32237-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="32237-124">Na caixa de diálogo **Modelo de Trabalho**, insira um nome para o modelo de trabalho e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="32237-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="32237-125">Agora é possível associar o modelo de trabalho a um modelo de calendário de projeto.</span><span class="sxs-lookup"><span data-stu-id="32237-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="32237-126">Funções do recurso</span><span class="sxs-lookup"><span data-stu-id="32237-126">Resource roles</span></span>

<span data-ttu-id="32237-127">O termo *função do recurso* se refere ao conjunto de habilidades, competências e certificações que uma pessoa deve ter para realizar um conjunto de tarefas específicas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="32237-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="32237-128">O PSA permite orçar e cobrar o tempo de um recurso com base na função à qual esse recurso está associado.</span><span class="sxs-lookup"><span data-stu-id="32237-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="32237-129">Cada organização deve configurar essas funções usando o painel de navegação à esquerda no menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="32237-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="32237-130">Cada organização deve configurar essas funções na página **Categorias de Recursos Ativos**.</span><span class="sxs-lookup"><span data-stu-id="32237-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="32237-131">Para abrir essa página, no painel de navegação à esquerda, selecione **Funções do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="32237-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="32237-132">Listas de preços</span><span class="sxs-lookup"><span data-stu-id="32237-132">Price lists</span></span>

<span data-ttu-id="32237-133">As listas de preços permitem definir preços de custo e vendas para funções do recurso, categorias de despesa, produtos e outros elementos em uma organização.</span><span class="sxs-lookup"><span data-stu-id="32237-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="32237-134">Antes de definir estimativas financeiras para o trabalho que deve ser entregue para um projeto, você deve criar uma listas de preços de custo e vendas de apoio.</span><span class="sxs-lookup"><span data-stu-id="32237-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="32237-135">Na seção de parâmetros, você também deve configurar uma lista de preços de custo e vendas padrão que se aplica a todos os projetos que são criados na organização.</span><span class="sxs-lookup"><span data-stu-id="32237-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="32237-136">Na página **Parâmetros do Projeto Ativos**, certifique-se de configurar uma lista de preços de custo e vendas padrão.</span><span class="sxs-lookup"><span data-stu-id="32237-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
