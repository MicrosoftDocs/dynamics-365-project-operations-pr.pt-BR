---
title: Mapear projetos e tarefas para uma linha de cotação baseada em projeto
description: Este tópico fornece informações sobre como mapear projetos e tarefas para uma linha de tarefa baseada em projeto.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272734"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="7d98b-103">Mapear projetos e tarefas para uma linha de cotação baseada em projeto</span><span class="sxs-lookup"><span data-stu-id="7d98b-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="7d98b-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="7d98b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d98b-105">Em linhas de cotação baseadas em projeto, você pode mapear as tarefas específicas de um projeto que já está associado a uma linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="7d98b-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="7d98b-106">Quando você mapeia tarefas para uma linha de cotação, os seguintes itens definidos na linha de cotação só se aplicam a essas tarefas:</span><span class="sxs-lookup"><span data-stu-id="7d98b-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="7d98b-107">Método de cobrança</span><span class="sxs-lookup"><span data-stu-id="7d98b-107">Billing method</span></span>
- <span data-ttu-id="7d98b-108">Opções de encargos</span><span class="sxs-lookup"><span data-stu-id="7d98b-108">Chargeability options</span></span>
- <span data-ttu-id="7d98b-109">Limites máximos</span><span class="sxs-lookup"><span data-stu-id="7d98b-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="7d98b-110">Clientes</span><span class="sxs-lookup"><span data-stu-id="7d98b-110">Customers</span></span>

<span data-ttu-id="7d98b-111">Por exemplo, você pode ter um projeto em que uma fase tem preço fixo e todas as outras fases são tempo e materiais.</span><span class="sxs-lookup"><span data-stu-id="7d98b-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="7d98b-112">Nesse caso, você pode associar a primeira fase, e todas as suas tarefas filho, à linha de cotação para essa fase com um método de cobrança de preço fixo.</span><span class="sxs-lookup"><span data-stu-id="7d98b-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="7d98b-113">Você pode então associar todas as outras fases à linha de cotação baseada em tempo e materiais.</span><span class="sxs-lookup"><span data-stu-id="7d98b-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="7d98b-114">Associar tarefas a linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="7d98b-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="7d98b-115">Você pode associar tarefas a linhas de cotação dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="7d98b-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="7d98b-116">Página **Projeto** > guia **Cobrança de tarefas** (ideal)</span><span class="sxs-lookup"><span data-stu-id="7d98b-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="7d98b-117">Página **Linha de cotação** > guia **Tarefas cobráveis**</span><span class="sxs-lookup"><span data-stu-id="7d98b-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="7d98b-118">Na página Projeto</span><span class="sxs-lookup"><span data-stu-id="7d98b-118">From the Project page</span></span>

<span data-ttu-id="7d98b-119">A página **Projeto** fornece a experiência ideal para associar tarefas a linhas de cotação.</span><span class="sxs-lookup"><span data-stu-id="7d98b-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="7d98b-120">Você pode usar esta página para selecionar várias tarefas e associar todas elas, além de suas tarefas filho, à linha de cotação selecionada.</span><span class="sxs-lookup"><span data-stu-id="7d98b-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="7d98b-121">Na guia **Geral** de uma linha de cotação baseada em projeto, verifique se o campo **Projeto** está preenchido.</span><span class="sxs-lookup"><span data-stu-id="7d98b-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="7d98b-122">No campo **Tarefas incluídas**, selecione **Somente tarefas selecionadas**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="7d98b-123">Salve a linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="7d98b-123">Save the project-based quote line.</span></span> <span data-ttu-id="7d98b-124">Quando o formulário é atualizado, a guia **Tarefas cobráveis** é exibida.</span><span class="sxs-lookup"><span data-stu-id="7d98b-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="7d98b-125">Na guia **Geral**, selecione o link para o projeto no campo **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="7d98b-126">Na página **Projetos**, selecione a guia **Cobrança de tarefas**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="7d98b-127">Na segunda grade, que se aplica à configuração de cobrança de tarefas específicas, selecione uma ou mais tarefas e selecione **Associar linhas de cotação**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="7d98b-128">Na página da caixa de diálogo que aparece, selecione uma linha de cotação que exibe linhas de cotação baseadas em projeto na cotação.</span><span class="sxs-lookup"><span data-stu-id="7d98b-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="7d98b-129">No campo **Tipo de cobrança**, indique se essas tarefas são cobráveis ou não.</span><span class="sxs-lookup"><span data-stu-id="7d98b-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="7d98b-130">Marque a caixa de seleção para indicar se a associação deve incluir tarefas filho das tarefas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="7d98b-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="7d98b-131">Ao marcar a caixa, você associará as tarefas filho das tarefas selecionadas à linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="7d98b-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="7d98b-132">Selecione **OK** para fechar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7d98b-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="7d98b-133">Na página Linha de cotação</span><span class="sxs-lookup"><span data-stu-id="7d98b-133">From the Quote line page</span></span>

<span data-ttu-id="7d98b-134">Você pode associar tarefas de projeto a linhas de cotação na guia **Tarefas cobráveis** na página **Linha de cotação**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="7d98b-135">O lugar ideal para associar tarefas de projeto a linhas de cotação é na guia **Cobrança de tarefas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="7d98b-136">Se você associar tarefas na guia **Tarefas cobráveis** na página **Linha de cotação**, você deverá associar manualmente cada projeto.</span><span class="sxs-lookup"><span data-stu-id="7d98b-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="7d98b-137">Na guia **Geral** de uma linha de cotação baseada em projeto, verifique se há um projeto selecionado no campo **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="7d98b-138">No campo **Tarefas incluídas**, selecione **Somente tarefas selecionadas**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="7d98b-139">Salve a linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="7d98b-139">Save the project-based quote line.</span></span> <span data-ttu-id="7d98b-140">Quando o formulário é atualizado, a guia **Tarefas cobráveis** é exibida.</span><span class="sxs-lookup"><span data-stu-id="7d98b-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="7d98b-141">Na guia **Tarefas cobráveis**, selecione **Adicionar uma tarefa de linha de cotação**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="7d98b-142">Na página **Tarefa de linha de cotação**, no campo **Tarefas**, selecione a tarefa e no campo **Tipo de cobrança**, selecione **Salve**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="7d98b-143">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="7d98b-143">Close the page.</span></span> <span data-ttu-id="7d98b-144">A tarefa selecionada agora é associada à linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="7d98b-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="7d98b-145">Desassociar tarefas de linhas de cotação baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="7d98b-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="7d98b-146">Na página Projeto</span><span class="sxs-lookup"><span data-stu-id="7d98b-146">From the Project page</span></span>

<span data-ttu-id="7d98b-147">Este método fornece a experiência ideal para desassociar tarefas de linhas de cotação.</span><span class="sxs-lookup"><span data-stu-id="7d98b-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="7d98b-148">Você pode usar esta página para selecionar várias tarefas e desassociar todas elas, além de suas tarefas filho, da linha de cotação selecionada.</span><span class="sxs-lookup"><span data-stu-id="7d98b-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="7d98b-149">Na guia **Geral** de uma linha de cotação baseada em projeto, no campo **Projeto**, selecione o link do projeto.</span><span class="sxs-lookup"><span data-stu-id="7d98b-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="7d98b-150">Na página **Projetos**, selecione a guia **Cobrança de tarefas**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="7d98b-151">Na segunda grade, que se aplica à configuração de cobrança de tarefas específicas, selecione uma ou mais tarefas e selecione **Desassociar linhas de cotação**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="7d98b-152">Na página de diálogo que aparece, selecione uma linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="7d98b-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="7d98b-153">Marque a caixa de seleção para indicar se a associação também deve ser removida das tarefas filho das tarefas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="7d98b-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="7d98b-154">Ao marcar a caixa, você também desassociará as tarefas filho das tarefas selecionadas à linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="7d98b-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="7d98b-155">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-155">Select **OK**.</span></span> <span data-ttu-id="7d98b-156">Uma mensagem de aviso informa que, se você remover essa associação, quaisquer dados reais registrados anteriormente na tarefa podem ser revertidos.</span><span class="sxs-lookup"><span data-stu-id="7d98b-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="7d98b-157">Selecione **OK** para continuar e remover a associação entre a tarefa e a linha de cotação baseada no projeto.</span><span class="sxs-lookup"><span data-stu-id="7d98b-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="7d98b-158">Na página Linha de cotação</span><span class="sxs-lookup"><span data-stu-id="7d98b-158">From the Quote line page</span></span>

<span data-ttu-id="7d98b-159">Você pode também desassociar tarefas de projeto a linhas de cotação na guia **Tarefas cobráveis** na página **Linha de cotação**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="7d98b-160">Na guia **Tarefas cobráveis**, selecione **Excluir uma tarefa de linha de cotação**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="7d98b-161">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d98b-161">Select **OK**.</span></span> <span data-ttu-id="7d98b-162">Uma mensagem de aviso informa que, se você remover essa associação, quaisquer dados reais registrados anteriormente na tarefa podem ser revertidos.</span><span class="sxs-lookup"><span data-stu-id="7d98b-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="7d98b-163">Selecione **OK** para continuar e remover a associação entre a tarefa e a linha de cotação baseada no projeto.</span><span class="sxs-lookup"><span data-stu-id="7d98b-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="7d98b-164">Este procedimento não exclui a tarefa do projeto.</span><span class="sxs-lookup"><span data-stu-id="7d98b-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="7d98b-165">Ele apenas remove a associação de tarefa da linha de cotação baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="7d98b-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]