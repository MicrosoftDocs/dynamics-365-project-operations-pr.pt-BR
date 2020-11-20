---
title: Criar um modelo de projeto
description: Como criar um modelo de projeto no Project Service
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
ms.openlocfilehash: 78d25183aad8d86593d3f2582295db59eb84cf14
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133174"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="b4828-103">Criar um modelo de projeto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b4828-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b4828-104">Os modelos de projeto economizam seu tempo se a empresa tiver lances regulares em tipos semelhantes de projetos.</span><span class="sxs-lookup"><span data-stu-id="b4828-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="b4828-105">Oferece um conjunto de direitos padrão e as horas de um tipo estimado de projeto.</span><span class="sxs-lookup"><span data-stu-id="b4828-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="b4828-106">Gerentes de conta e gerentes de projeto podem criar os projetos com base em um modelo do projeto, ou podem copiar o modelo e fazer o seu próprio.</span><span class="sxs-lookup"><span data-stu-id="b4828-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="b4828-107">Componentes do modelo do projeto</span><span class="sxs-lookup"><span data-stu-id="b4828-107">Components of project template</span></span>
 <span data-ttu-id="b4828-108">Um modelo do projeto tem três componentes:</span><span class="sxs-lookup"><span data-stu-id="b4828-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="b4828-109">**Estrutura de detalhamento de trabalho**: Uma estrutura de detalhamento de trabalho em um modelo do projeto com o mesmo conjunto de funções do projeto.</span><span class="sxs-lookup"><span data-stu-id="b4828-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="b4828-110">Você pode criar uma hierarquia da tarefa de encarregar-se de funções que defina uma agenda de dependências e exiba os dados contidos no Gantt.</span><span class="sxs-lookup"><span data-stu-id="b4828-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="b4828-111">A estrutura de detalhamento de trabalho nos modelos de projetos também oferece suporte a modos de tarefa para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="b4828-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="b4828-112">Não há um modelo diferente entre um modelo de projeto e de um projeto para criar a agenda de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4828-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="b4828-113">**Estimativas e cotações de projeto**: Estimativas de projeto nos modelos funcionam do mesmo jeito que nos projetos, exceto nas listas de preço para padronizar os preços de custo e vendas como sempre o custo de padrão e listas de preço de vendas definidos no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b4828-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="b4828-114">O restante da funcionalidade é o mesmo do projeto.</span><span class="sxs-lookup"><span data-stu-id="b4828-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="b4828-115">**Criação da equipe de projeto**: ao criar uma equipe de projeto para um modelo de projeto, você não pode reservar um recurso nomeado em um modelo.</span><span class="sxs-lookup"><span data-stu-id="b4828-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="b4828-116">Você pode usar **Gerencia a equipe de projeto** na estrutura de detalhamento de trabalho para gerar um conjunto genéricos de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4828-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="b4828-117">Também é possível especificar proficiências e habilidades e obrigatórios genéricas de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4828-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="b4828-118">Não é possível fazer um recurso genérico para reservar um recurso do projeto em modelos.</span><span class="sxs-lookup"><span data-stu-id="b4828-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="b4828-119">Criar Projeto a Partir do Modelo</span><span class="sxs-lookup"><span data-stu-id="b4828-119">Create a project from a template</span></span>  
 <span data-ttu-id="b4828-120">Você pode criar um modelo do projeto de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="b4828-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="b4828-121">Ao criar um projeto com base na cotação, você poderá escolher um modelo de projeto no formulário de criação rápida de projeto.</span><span class="sxs-lookup"><span data-stu-id="b4828-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="b4828-122">Como criar um projeto clicando em **Novo projeto**, o formulário é exibido de projetos antes de salvar o registro.</span><span class="sxs-lookup"><span data-stu-id="b4828-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="b4828-123">A partir daqui, é possível clicar em um campo **Selecionar um modelo** para escolher na lista de modelos predefinidos de projeto em sua organização.</span><span class="sxs-lookup"><span data-stu-id="b4828-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="b4828-124">Clique em **Criar projeto com base em um modelo** na página **Modelo de projeto** para criar um projeto com base no modelo.</span><span class="sxs-lookup"><span data-stu-id="b4828-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="b4828-125">Copiar componentes de um modelo a um projeto</span><span class="sxs-lookup"><span data-stu-id="b4828-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="b4828-126">Quando você copia os componentes de um projeto em um modelo, existem algumas coisas que você deve saber.</span><span class="sxs-lookup"><span data-stu-id="b4828-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="b4828-127">**Copiando uma estrutura de detalhamento de trabalho**: Quando você copia a estrutura de detalhamento de trabalho de um modelo do projeto, se houver um projeto do projeto do modelo que as horas de trabalho do projeto no serão aplicadas para tarefas de agendamento.</span><span class="sxs-lookup"><span data-stu-id="b4828-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="b4828-128">A agenda ajusta isto ao calendário do projeto na forma.</span><span class="sxs-lookup"><span data-stu-id="b4828-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="b4828-129">Da mesma forma, a primeira tarefa na estrutura de detalhamento de trabalho realiza a data de início do projeto, além o restante da agenda de trabalho da hierarquia é atualizado com base nas dependências e durações especificadas na estrutura de detalhamento de trabalho do modelo.</span><span class="sxs-lookup"><span data-stu-id="b4828-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="b4828-130">**Copiando estimativas e cotações de projeto**: Quando você copia nas linhas de estimativa de projeto, listas de preços são atualizadas com base nela para proprietário de projeto ao cliente e a lista de preço de custo na lista de preços das vendas.</span><span class="sxs-lookup"><span data-stu-id="b4828-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="b4828-131">O custo da unidade e os preços de vendas são determinadas essas listas de preços de projetos associados a uma entidade de vendas.</span><span class="sxs-lookup"><span data-stu-id="b4828-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="b4828-132">**Um copiando a equipe de projeto**: Quando você copia a equipe de projeto de modelo para um projeto, os recursos são copiados genéricos terminar, e pelas habilidades de proficiências definidas no modelo.</span><span class="sxs-lookup"><span data-stu-id="b4828-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="b4828-133">As atribuições genéricas de recursos também são mantidas no modelo do projeto.</span><span class="sxs-lookup"><span data-stu-id="b4828-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b4828-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b4828-134">See Also</span></span>  
 [<span data-ttu-id="b4828-135">Guia do gerente de projeto</span><span class="sxs-lookup"><span data-stu-id="b4828-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
