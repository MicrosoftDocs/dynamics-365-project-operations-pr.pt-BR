---
title: Modelos de projeto
description: Este tópico fornece informações sobre como usar modelos de projeto para configuração rápida de projetos.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998262"
---
# <a name="project-templates"></a><span data-ttu-id="85772-103">Modelos de projeto</span><span class="sxs-lookup"><span data-stu-id="85772-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="85772-104">Um modelo de projeto é uma estrutura predefinida que ajuda você a iniciar um projeto com rapidez e facilidade.</span><span class="sxs-lookup"><span data-stu-id="85772-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="85772-105">Você pode usar um modelo predefinido para criar um novo projeto com um único clique.</span><span class="sxs-lookup"><span data-stu-id="85772-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="85772-106">Em relação aos projetos, é necessário definir os pré-requisitos dos modelos de projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="85772-107">Também é necessário definir um calendário de projeto para cada modelo, além disso, funções e listas de preços devem ser predefinidas na organização, para que os componentes do modelo tenham dados úteis.</span><span class="sxs-lookup"><span data-stu-id="85772-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="85772-108">Um modelo de projeto consiste em três componentes: uma agenda, estimativas de projeto e membros da equipe de projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="85772-109">Agenda</span><span class="sxs-lookup"><span data-stu-id="85772-109">Schedule</span></span>

<span data-ttu-id="85772-110">Uma agenda em um modelo de projeto tem o mesmo conjunto de elementos que uma agenda em um projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="85772-111">Você pode criar uma hierarquia de tarefas, associar funções a tarefas, definir atributos de agenda e dependências.</span><span class="sxs-lookup"><span data-stu-id="85772-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="85772-112">Uma agenda em um modelo de projeto também oferece suporte a modos de tarefa para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="85772-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="85772-113">Portanto, ela oferece suporte ao mecanismo de agendamento.</span><span class="sxs-lookup"><span data-stu-id="85772-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="85772-114">Você deve associar um calendário de projeto ao projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="85772-115">Ao criar uma agenda de trabalho, não há nenhuma diferença entre um modelo de projeto e um projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="85772-116">Estimativas de projeto</span><span class="sxs-lookup"><span data-stu-id="85772-116">Project estimates</span></span>

<span data-ttu-id="85772-117">Estimativas de projeto em um modelo de projeto funcionam da mesma forma que estimativas de projeto em um projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="85772-118">No entanto, os preços de custo e de vendas são obtidos das listas de preços de custo e de vendas padrão que estão definidas nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="85772-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="85772-119">Criar um projeto com base em um modelo</span><span class="sxs-lookup"><span data-stu-id="85772-119">Creating a project from a template</span></span>
 
<span data-ttu-id="85772-120">Há várias maneiras de criar um projeto com base em um modelo:</span><span class="sxs-lookup"><span data-stu-id="85772-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="85772-121">Ao criar um projeto com base em uma cotação, você pode selecionar um modelo de projeto na caixa de diálogo **Criação Rápida: Projeto**.</span><span class="sxs-lookup"><span data-stu-id="85772-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Caixa de diálogo Criação Rápida: Projeto](media/project-11.png)

- <span data-ttu-id="85772-123">Ao criar um projeto selecionando **Novo Projeto**, a página **Projeto** será exibida antes do salvamento do registro.</span><span class="sxs-lookup"><span data-stu-id="85772-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="85772-124">No campo **Escolher um Modelo**, selecione um dos modelos de projeto predefinidos na organização.</span><span class="sxs-lookup"><span data-stu-id="85772-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="85772-125">Use **Criar Projeto com base em um Modelo** na página **Entidade de Modelo**.</span><span class="sxs-lookup"><span data-stu-id="85772-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="85772-126">Copiar componentes de um modelo para um projeto</span><span class="sxs-lookup"><span data-stu-id="85772-126">Copying components of template to project</span></span>

<span data-ttu-id="85772-127">Quando você copia os componentes de um modelo de projeto para um projeto, algumas substituições podem ocorrer, dependendo das configurações no projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="85772-128">Copiar a agenda</span><span class="sxs-lookup"><span data-stu-id="85772-128">Copying the schedule</span></span>

<span data-ttu-id="85772-129">Quando você copia a agenda de um modelo de projeto, se o projeto tiver um calendário diferente do modelo, as horas de trabalho do calendário do projeto serão aplicadas à agenda de tarefas.</span><span class="sxs-lookup"><span data-stu-id="85772-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="85772-130">Dessa maneira, a agenda é ajustada para corresponder ao calendário de projeto subjacente.</span><span class="sxs-lookup"><span data-stu-id="85772-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="85772-131">De maneira semelhante, a primeira tarefa na agenda ocupa a data de início do projeto e a agenda do restante da hierarquia é atualizada com base na duração e nas dependências especificadas no modelo.</span><span class="sxs-lookup"><span data-stu-id="85772-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="85772-132">Copiar estimativas de projeto</span><span class="sxs-lookup"><span data-stu-id="85772-132">Copying project estimates</span></span> 

<span data-ttu-id="85772-133">Quando você copia as linhas de estimativas de projeto, as listas de preços são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="85772-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="85772-134">Na lista de preços de custo, essas atualizações são baseadas na unidade proprietária do projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="85772-135">Na lista de preços de vendas, elas são baseadas no cliente.</span><span class="sxs-lookup"><span data-stu-id="85772-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="85772-136">Em projetos associados a uma entidade de vendas, os preços de custo e de vendas da unidade são determinados com base nessas listas de preços.</span><span class="sxs-lookup"><span data-stu-id="85772-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="85772-137">Copiar uma equipe de projeto</span><span class="sxs-lookup"><span data-stu-id="85772-137">Copying a project team</span></span>

<span data-ttu-id="85772-138">Quando uma equipe de projeto é copiada de um modelo de projeto para um projeto, os recursos genéricos são copiados, juntamente com as habilidades e proficiências definidas no modelo.</span><span class="sxs-lookup"><span data-stu-id="85772-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="85772-139">As atribuições de recursos genéricos também são mantidas, pois estavam no modelo de projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="85772-140">Recursos nomeados não têm suporte em modelos de projeto.</span><span class="sxs-lookup"><span data-stu-id="85772-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]