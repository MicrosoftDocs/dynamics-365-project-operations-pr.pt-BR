---
title: Atribuir recursos reserváveis genéricos a uma tarefa e equipe de projeto
description: Este tópico fornece informações sobre como reservar recursos genéricos para tarefas e equipes de projeto.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071443"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="a233b-103">Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recurso</span><span class="sxs-lookup"><span data-stu-id="a233b-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a233b-104">Além de reservar e atribuir recursos nomeados ou reais ao seu projeto, você pode atribuir recursos genéricos a tarefas do projeto.</span><span class="sxs-lookup"><span data-stu-id="a233b-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="a233b-105">Esses recursos podem atuar como espaços reservados para recursos nomeados até você estar pronto para montar a equipe do seu projeto com recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="a233b-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="a233b-106">No PSA (Project Service Automation), abra a página **Projeto** e, na guia **Agendar** , insira o nome da posição do recurso genérico na célula **Recurso** da agenda.</span><span class="sxs-lookup"><span data-stu-id="a233b-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="a233b-107">Ou, clique no ícone **Recurso** da célula a fim de abrir o seletor de recursos e insira o nome do recurso genérico que deseja criar.</span><span class="sxs-lookup"><span data-stu-id="a233b-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Criando e atribuindo um membro de equipe genérico](media/RM-how-to-9.png)

<span data-ttu-id="a233b-109">Isso abrirá o painel **Criação rápida: membro da equipe do projeto**.</span><span class="sxs-lookup"><span data-stu-id="a233b-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="a233b-110">Insira a função e a unidade organizacional do membro da equipe de recurso genérico e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="a233b-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Criação rápida do membro da equipe genérico](media/RM-how-to-10.png)

3. <span data-ttu-id="a233b-112">Depois de criar o novo membro da equipe de recurso genérico, ele é atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="a233b-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="a233b-113">Você pode continuar atribuindo esse recurso genérico a outras tarefas na agenda de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a233b-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Atribuindo membro da equipe genérico existente a tarefas](media/RM-how-to-11.png)

4. <span data-ttu-id="a233b-115">Depois de atribuir o recurso genérico, você pode gerar um requisito de recurso e preenchê-lo diretamente reservando ou enviando uma solicitação de recurso a um gerente de recursos.</span><span class="sxs-lookup"><span data-stu-id="a233b-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Gerando um requisito para um membro da equipe genérico](media/RM-how-to-12.png)

<span data-ttu-id="a233b-117">Na grade do membro da equipe, além de poder usar o seletor de recursos como mencionado acima, você pode adicionar recursos genéricos diretamente.</span><span class="sxs-lookup"><span data-stu-id="a233b-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="a233b-118">Os recursos são adicionados com um requisito de recurso que se baseia nas datas de início/término e um método de alocação especificado no painel **Criação Rápida: Membro da Equipe do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a233b-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="a233b-119">É possível ver a diferença se você adicionar o membro da equipe genérico diretamente e atribuir mais tarefa ao recurso genérico do que as horas exigidas.</span><span class="sxs-lookup"><span data-stu-id="a233b-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="a233b-120">Clique em **Gerar Requisito** para regenerar o requisito a fim de equilibrar as horas exigidas em relação às atribuições.</span><span class="sxs-lookup"><span data-stu-id="a233b-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="a233b-121">Também é possível clicar no link **Requisito de recurso** na grade da equipe para abrir o requisito e adicionar habilidades, recursos preferidos, etc.</span><span class="sxs-lookup"><span data-stu-id="a233b-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Requisito de Recurso](media/RM-how-to-13.png)

