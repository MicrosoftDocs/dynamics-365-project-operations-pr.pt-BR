---
title: Agendar um projeto com uma estrutura de detalhamento de trabalho
description: Como agendar um projeto com uma estrutura de detalhamento de trabalho no Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071610"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="6dcc9-103">Agendar um projeto com uma estrutura de detalhamento de trabalho (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6dcc9-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6dcc9-104">O cronograma de um projeto comunica o trabalho que precisa ser executado, os recursos que executarão o trabalho e o período de tempo em que o trabalho precisa ser concluído.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="6dcc9-105">O cronograma de um projeto reflete qualquer trabalho associado à entrega do projeto dentro do prazo.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="6dcc9-106">Uma das primeiras etapas de fase de iniciação do projeto é apresentar um cronograma do projeto.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="6dcc9-107">Para estabelecer um cronograma de projeto, é necessário criar uma estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="6dcc9-108">Criar uma estrutura de projeto com uma estrutura de detalhamento de trabalho ajuda você a:</span><span class="sxs-lookup"><span data-stu-id="6dcc9-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="6dcc9-109">Dividir o trabalho em tarefas gerenciáveis</span><span class="sxs-lookup"><span data-stu-id="6dcc9-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="6dcc9-110">Estimar o tempo necessário para concluir uma tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="6dcc9-111">Definir dependências e a duração da tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="6dcc9-112">Determinar as funções necessárias para concluir cada tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="6dcc9-113">O cronograma do projeto na estrutura de detalhamento de trabalho tem um aspecto familiar, finalizado com um gráfico de Gantt interativo.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="6dcc9-114">Criar uma estrutura de detalhamento de trabalho de um projeto</span><span class="sxs-lookup"><span data-stu-id="6dcc9-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="6dcc9-115">Crie uma estrutura da detalhamento de trabalho para representar a sequência de tarefas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="6dcc9-116">A estrutura de detalhamento de trabalho inclui tarefas, requisitos para cada tarefa e informações de receita e custo.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="6dcc9-117">Na estrutura da detalhamento de trabalho, você pode adicionar:</span><span class="sxs-lookup"><span data-stu-id="6dcc9-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="6dcc9-118">A sequência das tarefas em uma hierarquia</span><span class="sxs-lookup"><span data-stu-id="6dcc9-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="6dcc9-119">Outras tarefas, se existirem, que devem ser concluídas antes que uma tarefa seja iniciada</span><span class="sxs-lookup"><span data-stu-id="6dcc9-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="6dcc9-120">A data de início, a data de término e a duração de uma tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="6dcc9-121">O número de horas necessárias para uma tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="6dcc9-122">As habilidades e qualificações necessárias do trabalhador</span><span class="sxs-lookup"><span data-stu-id="6dcc9-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="6dcc9-123">Os trabalhadores atribuídos a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="6dcc9-124">A receita e os custos estimados</span><span class="sxs-lookup"><span data-stu-id="6dcc9-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="6dcc9-125">Tipos de tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-125">Task types</span></span>  
<span data-ttu-id="6dcc9-126">Você usará os seguintes tipos de tarefa para criar a estrutura de detalhamento de trabalho:</span><span class="sxs-lookup"><span data-stu-id="6dcc9-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="6dcc9-127">**Nó raiz do projeto**</span><span class="sxs-lookup"><span data-stu-id="6dcc9-127">**Project root node**</span></span> | <span data-ttu-id="6dcc9-128">A tarefa resumo de nível superior do projeto.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-128">The top-level summary task for the project.</span></span> <span data-ttu-id="6dcc9-129">Todas as outras tarefas do projeto são criadas nele.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-129">All other project tasks are created under it.</span></span> <span data-ttu-id="6dcc9-130">O nome da tarefa raiz é o nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-130">The name of the root task is the project name.</span></span> <span data-ttu-id="6dcc9-131">O esforço, as datas e a duração do nó raiz são baseados nos valores da hierarquia abaixo deles.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="6dcc9-132">Você não pode editar as propriedades do nó raiz ou excluir o nó raiz.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="6dcc9-133">**Tarefas de contêiner ou resumo**</span><span class="sxs-lookup"><span data-stu-id="6dcc9-133">**Summary or container tasks**</span></span> | <span data-ttu-id="6dcc9-134">A tarefa resumo é uma tarefa que contém subtarefas abaixo nela.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="6dcc9-135">Uma tarefa resumo não tem nenhum esforço de trabalho nem custo próprio.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="6dcc9-136">Seus esforços e custo de trabalho são o valor acumulado de suas subtarefas.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="6dcc9-137">Você pode alterar o nome de uma tarefa resumo, mas não pode alterar o esforço, as datas ou a duração, pois esses valores são calculados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="6dcc9-138">A exclusão de uma tarefa resumo excluirá a tarefa e todas as suas subtarefas.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="6dcc9-139">**Tarefas do nó folha**</span><span class="sxs-lookup"><span data-stu-id="6dcc9-139">**Leaf node tasks**</span></span> | <span data-ttu-id="6dcc9-140">Uma tarefa de nó folha representa o trabalho mais detalhado do projeto.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="6dcc9-141">Ela tem um esforço estimado, um número planejado de recursos, datas de início e de término e uma a duração.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="6dcc9-142">Hierarquia da tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-142">Task hierarchy</span></span>  
 <span data-ttu-id="6dcc9-143">Você tem as opções a seguir na criação de uma hierarquia de tarefas:</span><span class="sxs-lookup"><span data-stu-id="6dcc9-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="6dcc9-144">**Adicionar uma tarefa**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-144">**Add task**.</span></span>   <span data-ttu-id="6dcc9-145">Você pode adicionar uma tarefa a uma posição escolhida na hierarquia de tarefas.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="6dcc9-146">Se você não selecionar uma posição, a nova tarefa aparecerá no fim.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="6dcc9-147">**Recuar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-147">**Indent task**.</span></span>   <span data-ttu-id="6dcc9-148">Recuar uma tarefa para torná-la secundária em relação a uma tarefa imediatamente acima dela.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="6dcc9-149">**Recuar tarefa para a esquerda**</span><span class="sxs-lookup"><span data-stu-id="6dcc9-149">**Outdent task**.</span></span>   <span data-ttu-id="6dcc9-150">Recuar uma tarefa para a esquerda para que ela não seja mais uma subtarefa da tarefa principal original.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="6dcc9-151">**Mover para cima e mover para baixo**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-151">**Move up and Move down**.</span></span>   <span data-ttu-id="6dcc9-152">Mover tarefas para cima e para baixo na hierarquia da tarefa principal.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="6dcc9-153">Mover uma tarefa para cima ou para baixo não afeta seu esforço, custo, datas ou duração.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="6dcc9-154">Atributos da tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-154">Task attributes</span></span>  
 <span data-ttu-id="6dcc9-155">O nome de uma tarefa descreve o trabalho que precisa ser concluído.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="6dcc9-156">Você usa vários atributos de tarefa para descrever o cronograma e as necessidades de pessoal para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="6dcc9-157">Atributos da agenda</span><span class="sxs-lookup"><span data-stu-id="6dcc9-157">Schedule attributes</span></span>

 - <span data-ttu-id="6dcc9-158">Atribua valores a **Horas de esforço** , **Número de recursos** , **Data inicial** , **Data final** e **Duração** para determinar a agenda da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-158">Assign values to **Effort hours** , **Number of resources** , **Start date** , **End date** , and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="6dcc9-159">O **Esforço** é uma estimativa das horas necessárias para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="6dcc9-160">O **Número de recursos** é uma estimativa que o gerente de projetos atribui à tarefa para ajudar a apresentar o melhor cronograma possível.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="6dcc9-161">A **Duração** (em dias) indica o número de dias úteis necessário para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="6dcc9-162">Atributos de pessoal</span><span class="sxs-lookup"><span data-stu-id="6dcc9-162">Staffing attributes</span></span>

 - <span data-ttu-id="6dcc9-163">Os valores **Função** , **Unidade organizacional do recurso** , **Número de recursos** e **Recursos** descrevem as necessidades de pessoal para a realização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-163">**Role** , **Resource organizational unit** , **Number of resources** , and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="6dcc9-164">A **Função** descreve o tipo de recurso necessário executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="6dcc9-165">A **Unidade organizacional do recurso** indica a unidade organizacional à qual os recursos devem ser fornecidos para a realização da tarefa; isso também afeta a estimativa de vendas e custos da tarefa, pois ela é registrada no momento em que o preço unitário de venda é determinado para o recurso.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="6dcc9-166">Os **Recursos** retêm um recurso genérico ou um recurso nomeado quando um dele é localizado.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="6dcc9-167">Dependências da tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-167">Task dependencies</span></span>  
 <span data-ttu-id="6dcc9-168">Você pode criar relacionamentos predecessores entre uma ou mais tarefas na estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="6dcc9-169">Você pode definir um ou mais valores no campo para tarefas predecessoras para indicar as tarefas das quais ela será dependente.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="6dcc9-170">Quando você atribuir um valor predecessor a uma tarefa, a tarefa só poderá ser iniciada quando todas as tarefas predecessoras forem concluídas.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="6dcc9-171">A definição dessa dependência desta tarefa resultará no recálculo da data de início prevista para a tarefa como a última data de término de todas as suas predecessoras.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="6dcc9-172">Os impactos relacionados às predecessoras em um cronograma não são limitados pelo modo de tarefa definido na tarefa.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="6dcc9-173">Modo de tarefa</span><span class="sxs-lookup"><span data-stu-id="6dcc9-173">Task mode</span></span>  
 <span data-ttu-id="6dcc9-174">O modo de tarefa é um dos fatores importantes que determinam o agendamento de tarefas de nó folha.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="6dcc9-175">Há dois modos para cada tarefa: modo de agendamento automático e modo de agendamento manual.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="6dcc9-176">**Agendamento automático**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-176">**Auto scheduling**.</span></span>   <span data-ttu-id="6dcc9-177">Ao definir o modo da tarefa para Agendado Automaticamente, o mecanismo de agendamento da tarefa usa as regras de agendamento nos seguintes atributos da tarefa para determinar a agenda para a tarefa:</span><span class="sxs-lookup"><span data-stu-id="6dcc9-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="6dcc9-178">Antecessoras</span><span class="sxs-lookup"><span data-stu-id="6dcc9-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="6dcc9-179">Esforço</span><span class="sxs-lookup"><span data-stu-id="6dcc9-179">Effort</span></span>  
  
    -   <span data-ttu-id="6dcc9-180">Número de recursos</span><span class="sxs-lookup"><span data-stu-id="6dcc9-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="6dcc9-181">Datas de início e término</span><span class="sxs-lookup"><span data-stu-id="6dcc9-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="6dcc9-182">**Regras de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-182">**Scheduling rules**.</span></span>   <span data-ttu-id="6dcc9-183">A data de início de uma tarefa de nó folha que não possui predecessoras assume como padrão a data de início do agendamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="6dcc9-184">A duração de uma tarefa de nó folha é sempre calculada como o número de dias úteis entre as datas de início e término.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="6dcc9-185">Quando uma tarefa é agendada automaticamente, o mecanismo de agendamento segue as regras abaixo:</span><span class="sxs-lookup"><span data-stu-id="6dcc9-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="6dcc9-186">As datas de início e término de uma tarefa devem ser sempre dias úteis de acordo com o calendário de agendamento do projeto</span><span class="sxs-lookup"><span data-stu-id="6dcc9-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="6dcc9-187">A data de início de uma tarefa que tem predecessoras assume como padrão a data de término mais recente de suas predecessoras</span><span class="sxs-lookup"><span data-stu-id="6dcc9-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="6dcc9-188">Esforço = Número de pessoas \* Duração \* horas em um dia útil padrão do calendário do projeto</span><span class="sxs-lookup"><span data-stu-id="6dcc9-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="6dcc9-189">**Agendamento manual**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-189">**Manual scheduling**.</span></span>   <span data-ttu-id="6dcc9-190">Em alguns casos, talvez você queira desconsiderar essas regras.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="6dcc9-191">Nesses casos, você pode definir o modo de tarefa para que seja agendado manualmente.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="6dcc9-192">Isso faz com que o mecanismo de agendamento pare de calcular os valores para outros atributos de agendamento.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="6dcc9-193">A definição de tarefas predecessoras sempre afeta a data de início da tarefa dependente.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="6dcc9-194">Criar uma estrutura de detalhamento de trabalho</span><span class="sxs-lookup"><span data-stu-id="6dcc9-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="6dcc9-195">Vá para **Project Service > Projetos**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="6dcc9-196">Clique no projeto no qual você deseja trabalhar.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="6dcc9-197">Na barra da parte superior da tela, selecione a seta para baixo ao lado do nome do projeto e, em seguida, clique em Estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="6dcc9-198">Para adicionar uma tarefa, clique em **Adicionar Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="6dcc9-199">Preencha os campos da tarefa e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="6dcc9-200">Continue adicionando tarefas até que sua estrutura de detalhamento de trabalho esteja completa.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="6dcc9-201">Ao criar a estrutura de detalhamento de trabalho, é possível fazer o seguinte para organizar suas tarefas:</span><span class="sxs-lookup"><span data-stu-id="6dcc9-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="6dcc9-202">Selecione uma tarefa e clique em **Recuar** para movê-la para baixo de outra tarefa ou clique em Recuar para a esquerda para movê-la um nível.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="6dcc9-203">Selecione uma tarefa e clique em **Mover para Cima** ou **Mover para Baixo** para movê-la para cima ou para baixo na lista.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="6dcc9-204">Clique em **Ocultar Gantt** para ocultar o gráfico de Gantt e clique em **Mostrar Gantt** para exibi-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="6dcc9-205">Selecione um período diferente para o gráfico de Gantt em **Escala de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="6dcc9-206">Para adicionar as funções especificadas na estrutura de detalhamento de trabalho aos membros da equipe do projeto, clique em **Gerenciar Equipe do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="6dcc9-207">Ao terminar de fazer as alterações, clique no botão **Salvar** no canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="6dcc9-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6dcc9-208">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6dcc9-208">See Also</span></span>  
 [<span data-ttu-id="6dcc9-209">Guia do gerente de projeto</span><span class="sxs-lookup"><span data-stu-id="6dcc9-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
