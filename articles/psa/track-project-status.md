---
title: Rastrear o status de um projeto
description: Como rastrear o status de um projeto no Project Service
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071514"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="a522a-103">Rastrear o status de um projeto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a522a-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a522a-104">Use os recursos do [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] para acompanhar o progresso do projeto de um cliente.</span><span class="sxs-lookup"><span data-stu-id="a522a-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="a522a-105">À medida que o compromisso evolui, os estágios do projeto são atualizados para refletir o estágio do compromisso:</span><span class="sxs-lookup"><span data-stu-id="a522a-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="a522a-106">**Novo**</span><span class="sxs-lookup"><span data-stu-id="a522a-106">**New**</span></span>    | <span data-ttu-id="a522a-107">Ao criar um projeto, o estágio é definido como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a522a-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="a522a-108">Se o projeto foi criado partir de um modelo, neste estágio, o projeto pode ter um cronograma, estimativas e dados da equipe.</span><span class="sxs-lookup"><span data-stu-id="a522a-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="a522a-109">Caso contrário, será a estrutura de tópicos do projeto, e você precisará inserir manualmente o restante dos componentes do projeto.</span><span class="sxs-lookup"><span data-stu-id="a522a-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="a522a-110">**Cotação**</span><span class="sxs-lookup"><span data-stu-id="a522a-110">**Quote**</span></span>   |      <span data-ttu-id="a522a-111">Ao associar um projeto a uma cotação ou criar um projeto a partir de uma cotação, o estágio do projeto é definido como **Cotação** , e a hora de início e de término estimadas são também atualizadas.</span><span class="sxs-lookup"><span data-stu-id="a522a-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="a522a-112">Quando o projeto está no estágio de cotação, os detalhes da cotação são exibidos na guia **Vendas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a522a-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="a522a-113">**Plano**</span><span class="sxs-lookup"><span data-stu-id="a522a-113">**Plan**</span></span>   |                                     <span data-ttu-id="a522a-114">Quando você vence uma cotação associada a um projeto, e quando o compromisso evolui para o estágio de contrato, o estágio do projeto é atualizado para **Plano**.</span><span class="sxs-lookup"><span data-stu-id="a522a-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="a522a-115">Os detalhes do contrato são exibidos na guia **Vendas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a522a-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="a522a-116">**Concluir**</span><span class="sxs-lookup"><span data-stu-id="a522a-116">**Complete**</span></span> |                    <span data-ttu-id="a522a-117">Quando o trabalho do projeto é concluído, você pode mudar o estágio para **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="a522a-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="a522a-118">Quando o estágio do projeto é definido como concluído, entende-se que o trabalho foi 100% concluído, mas que o projeto será mantido aberto para o registro de horas ou entradas de despesas pendentes.</span><span class="sxs-lookup"><span data-stu-id="a522a-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="a522a-119">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="a522a-119">**Close**</span></span>   |           <span data-ttu-id="a522a-120">Quando todas as transações tiverem sido registradas no projeto e nada mais precisar ser registrado, você poderá definir manualmente o estágio como **Fechado**.</span><span class="sxs-lookup"><span data-stu-id="a522a-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="a522a-121">Quando o projeto é definido como **Fechado** , não é possível registrar mais nenhuma transação nele, e ele será usado apenas para leitura.</span><span class="sxs-lookup"><span data-stu-id="a522a-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="a522a-122">Para acompanhar o status de um projeto</span><span class="sxs-lookup"><span data-stu-id="a522a-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="a522a-123">Vá para **Project Service > Projetos**.</span><span class="sxs-lookup"><span data-stu-id="a522a-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="a522a-124">Clique no projeto no qual você deseja trabalhar.</span><span class="sxs-lookup"><span data-stu-id="a522a-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="a522a-125">Na barra da parte superior da tela, selecione a seta para baixo ao lado do nome do projeto e, em seguida, clique em **Acompanhamento de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a522a-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="a522a-126">Selecione **Acompanhamento de Esforços** ou **Acompanhamento de Custos** na lista suspensa acima da lista de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a522a-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="a522a-127">Clique duas vezes em qualquer tarefa editá-la.</span><span class="sxs-lookup"><span data-stu-id="a522a-127">Double-click any task to edit it.</span></span> <span data-ttu-id="a522a-128">Você também pode mover ou redimensionar as barras no gráfico de Gantt para alterar o tempo e o progresso da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a522a-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="a522a-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a522a-129">See Also</span></span>  
 [<span data-ttu-id="a522a-130">Guia do gerente de projeto</span><span class="sxs-lookup"><span data-stu-id="a522a-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)