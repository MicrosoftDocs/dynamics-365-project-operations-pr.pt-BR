---
title: Fornecer estimativas de trabalho para um projeto durante o processo de vendas
description: Como fornecer estimativas de trabalho a um projeto durante o processo de vendas no Project Service
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120574"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="0ccd2-103">Fornecer estimativas de trabalho a um projeto durante o processo de vendas (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0ccd2-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0ccd2-104">Durante o processo de vendas, você pode calcular estimativas de vendas completas com linhas de cotação.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="0ccd2-105">Os recursos do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] fornecem uma maneira mais científica e determinística de propor estimativas de vendas detalhando itens de trabalho e associando atributos relevantes que contribuem para as estimativas do projeto na estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="0ccd2-106">Depois de ganhar a venda, você pode usar a estrutura de detalhamento de trabalho associada em seu plano de projeto, refinando-a conforme necessário para a conclusão bem-sucedida do projeto.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="0ccd2-107">Vincular um projeto a uma linha de cotação</span><span class="sxs-lookup"><span data-stu-id="0ccd2-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="0ccd2-108">Ao criar uma linha de cotação baseada em projeto, você pode criar um novo projeto a partir da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="0ccd2-109">Você pode usar os modelos de projetos, que são planos de projetos padrão pré-configurados e estimativas financeiras comuns a sua organização ou uma cópia de um plano de projeto e das estimativas de um projeto do passado.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="0ccd2-110">Ao criar um projeto, a escolha de um modelo de projeto fornece uma base para restringir o plano de projeto, as estimativas e os requisitos de funções.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="0ccd2-111">Ao criar seu projeto a partir de uma cotação, o projeto é automaticamente associado à linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="0ccd2-112">Componentes de estimativa do projeto</span><span class="sxs-lookup"><span data-stu-id="0ccd2-112">Project estimate components</span></span>  
 <span data-ttu-id="0ccd2-113">A estrutura de detalhamento de trabalho em um projeto fornece uma maneira de detalhar o trabalho em tarefas, manter uma hierarquia de tarefas e atribuir uma estimativa do esforço necessário para executar cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="0ccd2-114">Você também pode associar funções a uma tarefa para indicar uma estimativa do tipo de recurso necessário para concluir uma tarefa e uma agenda.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="0ccd2-115">A estrutura de detalhamento do trabalho ajuda você a determinar estimativas do esforço e da agenda do trabalho.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="0ccd2-116">Por padrão, o projeto usa listas de preços padrão que você define anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="0ccd2-117">Os preços de custo e de vendas definidos nas listas de preços ajudam a determinar estimativas financeiras para detalhamento do trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="0ccd2-118">Se seu projeto estiver associado a uma cotação, e a cotação tiver uma lista de preços diferente do padrão, a lista de preços da cotação será usada para estimativas financeiras.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="0ccd2-119">Importar estimativas de um projeto em uma cotação</span><span class="sxs-lookup"><span data-stu-id="0ccd2-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="0ccd2-120">Assim que obter as estimativas do projeto, importe essas estimativas na linha de cotação:</span><span class="sxs-lookup"><span data-stu-id="0ccd2-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="0ccd2-121">Em **Detalhes da Linha de Cotação**, clique em **Importar das estimativas**.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="0ccd2-122">Selecione se as estimativas do projeto devem ser importadas resumidas por tipo de transação, função ou nível de nó da estrutura de detalhamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0ccd2-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0ccd2-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0ccd2-123">See Also</span></span>  
 [<span data-ttu-id="0ccd2-124">Guia do gerente de projeto</span><span class="sxs-lookup"><span data-stu-id="0ccd2-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
