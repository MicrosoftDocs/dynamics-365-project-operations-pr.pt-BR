---
title: Estimativas e projetos de vendas
description: Este tópico fornece informações sobre como aproveitar a agenda e as estimativas no processo de vendas.
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
ms.openlocfilehash: 49d109be3d55e7f208edb2698e420f40bb7843df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998397"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="66d0b-103">Estimativas e projetos de vendas</span><span class="sxs-lookup"><span data-stu-id="66d0b-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="66d0b-104">Durante o processo de vendas, você pode criar estimativas de vendas vinculando um projeto a uma cotação de vendas.</span><span class="sxs-lookup"><span data-stu-id="66d0b-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="66d0b-105">Dessa forma, a estimativa determinista pode ocorrer durante o processo de vendas para aproveitar os recursos de estimativa e agendamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="66d0b-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="66d0b-106">Se as vendas se consumarem, a agenda que foi usada para fins de estimativa poderá ser usada como a base para mais refinamento do plano de projeto.</span><span class="sxs-lookup"><span data-stu-id="66d0b-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="66d0b-107">Vinculando um projeto a uma linha de cotação</span><span class="sxs-lookup"><span data-stu-id="66d0b-107">Linking a project to a quote line</span></span>

<span data-ttu-id="66d0b-108">Quando você cria uma linha de cotação baseada em projeto, é possível criar um novo projeto ou associar um projeto existente na página **Linha de Cotação**.</span><span class="sxs-lookup"><span data-stu-id="66d0b-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulário de linha de cotação](media/project-8.png)
 
<span data-ttu-id="66d0b-110">Quando você cria um novo projeto com base nos detalhes da linha de cotação, é possível aproveitar os modelos do projeto.</span><span class="sxs-lookup"><span data-stu-id="66d0b-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="66d0b-111">Os modelos do projeto são projetos modelo que representam planos de projeto padrão e estimativas financeiras que são típicas em uma organização.</span><span class="sxs-lookup"><span data-stu-id="66d0b-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="66d0b-112">Eles também representam cópias de planos de projeto e estimativas de projetos passados.</span><span class="sxs-lookup"><span data-stu-id="66d0b-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detalhes da linha de cotação](media/project-9.png)
  
<span data-ttu-id="66d0b-114">Quando você cria o projeto com base na cotação, o projeto é automaticamente associado à linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="66d0b-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="66d0b-115">Componentes de estimativas em um projeto</span><span class="sxs-lookup"><span data-stu-id="66d0b-115">Components of estimates in a project</span></span>

<span data-ttu-id="66d0b-116">Uma agenda permite dividir o trabalho em tarefas, manter uma hierarquia de tarefas, determinar quais recursos são exigidos para concluir uma tarefa e atribuir uma estimativas do esforço que é exigido para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="66d0b-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="66d0b-117">Você pode definir as estimativas de agenda e esforço de trabalho usando os campos na guia **Agendar** da página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="66d0b-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="66d0b-118">Como uma lista de preços é associada ao projeto, as estimativas financeiras são calculadas usando preços de custo e vendas que são definidos na lista de preços.</span><span class="sxs-lookup"><span data-stu-id="66d0b-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="66d0b-119">Importando estimativas de um projeto em uma cotação</span><span class="sxs-lookup"><span data-stu-id="66d0b-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="66d0b-120">Após definição de estimativas do projeto, você pode importá-las na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="66d0b-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="66d0b-121">Na página **Detalhes da Linha de Cotação**, selecione na faixa de opções **Importar de estimativas** para resumir as estimativas do projeto por tipo de transação, função ou nível da tarefa.</span><span class="sxs-lookup"><span data-stu-id="66d0b-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]