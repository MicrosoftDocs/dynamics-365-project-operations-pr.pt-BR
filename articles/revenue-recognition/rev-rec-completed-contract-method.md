---
title: Gerenciar estimativas de receita
description: Este tópico fornece informações sobre como trabalhar com estimativas de receita para projetos.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531351"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="64d5f-103">Gerenciar estimativas de receita</span><span class="sxs-lookup"><span data-stu-id="64d5f-103">Manage revenue estimates</span></span>

<span data-ttu-id="64d5f-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="64d5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="64d5f-105">Você pode criar, calcular, lançar, reverter ou eliminar estimativas de receita.</span><span class="sxs-lookup"><span data-stu-id="64d5f-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="64d5f-106">Você pode fazer isso manualmente ou usando um processo periódico.</span><span class="sxs-lookup"><span data-stu-id="64d5f-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="64d5f-107">Este tópico fornece informações sobre como trabalhar com estimativas de receita para projetos.</span><span class="sxs-lookup"><span data-stu-id="64d5f-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="64d5f-108">Gerenciar estimativas de receita manualmente</span><span class="sxs-lookup"><span data-stu-id="64d5f-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="64d5f-109">No projeto de estimativa de receita de preço fixo ou na página **Consulta de estimativa** (**Gerenciamento e contabilidade de projeto** > **Relatórios e consultas** > **Consultas de estimativas e relatórios**), selecione **Estimativas**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="64d5f-110">Gerenciar estimativas de receita usando um processo periódico</span><span class="sxs-lookup"><span data-stu-id="64d5f-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="64d5f-111">Acesse **Gerenciamento e contabilidade de projeto** > **Atividades Periódicas** > **Estimativas** e selecione o processo correspondente.</span><span class="sxs-lookup"><span data-stu-id="64d5f-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="64d5f-112">Crie uma estimativa de receita</span><span class="sxs-lookup"><span data-stu-id="64d5f-112">Create a revenue estimate</span></span>

<span data-ttu-id="64d5f-113">Conclua as etapas a seguir para criar uma estimativa de receita.</span><span class="sxs-lookup"><span data-stu-id="64d5f-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="64d5f-114">Acesse **Gerenciamento e contabilidade de projeto** > **Atividades Periódicas** > **Estimativas**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="64d5f-115">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-115">Select **New**.</span></span> <span data-ttu-id="64d5f-116">Na página **Criação de estimativa**, selecione os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="64d5f-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="64d5f-117">**Código do período**: esse código determina a frequência com que as estimativas são lançadas.</span><span class="sxs-lookup"><span data-stu-id="64d5f-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="64d5f-118">**Data da estimativa**: a data em que a estimativa é processada.</span><span class="sxs-lookup"><span data-stu-id="64d5f-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="64d5f-119">**Contínua**: marque essa caixa de seleção para criar estimativas somente se as estimativas foram lançadas no período anterior ou se a estimativa é a primeira estimativa que foi criada.</span><span class="sxs-lookup"><span data-stu-id="64d5f-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="64d5f-120">Se não for selecionada, as estimativas serão criadas mesmo se as estimativas não foram lançadas no período anterior.</span><span class="sxs-lookup"><span data-stu-id="64d5f-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="64d5f-121">**Custo para concluir o método**: defina como estimar o trabalho restante do projeto.</span><span class="sxs-lookup"><span data-stu-id="64d5f-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="64d5f-122">Para obter mais informações, consulte [Custo para concluir os métodos](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="64d5f-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="64d5f-123">**Método de conclusão**: selecione um método de conclusão entre as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="64d5f-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="64d5f-124">**Automático**: a porcentagem de conclusão é calculada automaticamente e com base nas linhas de custo incluídas no cálculo.</span><span class="sxs-lookup"><span data-stu-id="64d5f-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="64d5f-125">O modelo de custo define as linhas de custo que são incluídas.</span><span class="sxs-lookup"><span data-stu-id="64d5f-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="64d5f-126">**Manual**: a porcentagem de conclusão é igual à porcentagem de conclusão da última estimativa.</span><span class="sxs-lookup"><span data-stu-id="64d5f-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="64d5f-127">Depois que a estimativa for criada, você poderá alterar o **Cálculo manual** na página **Estimativas**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="64d5f-128">**Do modelo de custo**: uma combinação dos métodos automático e manual.</span><span class="sxs-lookup"><span data-stu-id="64d5f-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="64d5f-129">Essa opção é definida automática ou manualmente, dependendo do valor padrão no modelo de custo.</span><span class="sxs-lookup"><span data-stu-id="64d5f-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="64d5f-130">**Modelo de previsão**: selecione um modelo de previsão para a estimativa.</span><span class="sxs-lookup"><span data-stu-id="64d5f-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="64d5f-131">**Imprimir lista de estimativa**: crie e exiba uma lista de orçamentos.</span><span class="sxs-lookup"><span data-stu-id="64d5f-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="64d5f-132">A lista contém o status da função atual.</span><span class="sxs-lookup"><span data-stu-id="64d5f-132">The list contains the status of the current function.</span></span> <span data-ttu-id="64d5f-133">Você pode imprimir qualquer aviso sobre a estimativa no relatório.</span><span class="sxs-lookup"><span data-stu-id="64d5f-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="64d5f-134">As seguintes condições fazem com que avisos sejam exibidos na lista de estimativas:</span><span class="sxs-lookup"><span data-stu-id="64d5f-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="64d5f-135">Uma porcentagem de conclusão maior que 100%.</span><span class="sxs-lookup"><span data-stu-id="64d5f-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="64d5f-136">Uma porcentagem de conclusão menor que 0%.</span><span class="sxs-lookup"><span data-stu-id="64d5f-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="64d5f-137">Um valor negativo na coluna **Para concluir**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="64d5f-138">Uma estimativa sem valor de contrato correspondente.</span><span class="sxs-lookup"><span data-stu-id="64d5f-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="64d5f-139">Uma estimativa sem estimativa de custo anexada.</span><span class="sxs-lookup"><span data-stu-id="64d5f-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="64d5f-140">**Mostrar Infolog**: selecione esta opção para receber uma mensagem que contenha informações sobre os projetos de estimativa que foram processados quando o trabalho foi executado.</span><span class="sxs-lookup"><span data-stu-id="64d5f-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="64d5f-141">Lançar WIP ou acúmulos</span><span class="sxs-lookup"><span data-stu-id="64d5f-141">Post WIP or accruals</span></span>

<span data-ttu-id="64d5f-142">Depois que as estimativas forem avaliadas, elas serão mantidas, diminuídas ou aumentadas.</span><span class="sxs-lookup"><span data-stu-id="64d5f-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="64d5f-143">Você poderá, então, lançar o WIP quando trabalhar com o princípio de avaliação **Contrato concluído** ou lançar os acúmulos quando trabalhar com o princípio de avaliação **Porcentagem concluída**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="64d5f-144">O status do período de estimativa mudará de **Criado** para **Lançado**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="64d5f-145">Reverter WIP ou acúmulos</span><span class="sxs-lookup"><span data-stu-id="64d5f-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="64d5f-146">Use a opção de reversão para creditar WIP ou acúmulos já lançados e, em seguida, crie estimativas para o período.</span><span class="sxs-lookup"><span data-stu-id="64d5f-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="64d5f-147">Para reverter um período que está entre outros períodos, reverta os períodos de estimativa necessários e, em seguida, lance-os novamente.</span><span class="sxs-lookup"><span data-stu-id="64d5f-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="64d5f-148">Como todos os períodos subsequentes dependem das estimativas do período anterior, não pule nenhum período.</span><span class="sxs-lookup"><span data-stu-id="64d5f-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="64d5f-149">Elimine o projeto previsto e conclua o projeto</span><span class="sxs-lookup"><span data-stu-id="64d5f-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="64d5f-150">A etapa final no processo de estimativa é eliminar o projeto previsto e encerrar o projeto de preço fixo quando a porcentagem de conclusão atingir 100%.</span><span class="sxs-lookup"><span data-stu-id="64d5f-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="64d5f-151">Quando você executa a eliminação, ocorrerá o seguinte:</span><span class="sxs-lookup"><span data-stu-id="64d5f-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="64d5f-152">Para um projeto de preço fixo com um contrato concluído, os valores de WIP são eliminados das contas de saldo e lançados nas contas de lucros e perdas.</span><span class="sxs-lookup"><span data-stu-id="64d5f-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="64d5f-153">Para um projeto de preço fixo com uma porcentagem concluída, os acúmulos são removidos das contas de lucros e perdas.</span><span class="sxs-lookup"><span data-stu-id="64d5f-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="64d5f-154">A estimativa mudará o status para **Eliminado**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="64d5f-155">Em casos especiais, a porcentagem pode ultrapassar 100%.</span><span class="sxs-lookup"><span data-stu-id="64d5f-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="64d5f-156">Quando isso acontecer, reduza a porcentagem de conclusão usando o método **Definir custo a ser concluído como zero** para atingir 100%.</span><span class="sxs-lookup"><span data-stu-id="64d5f-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="64d5f-157">Reverter eliminação</span><span class="sxs-lookup"><span data-stu-id="64d5f-157">Reverse elimination</span></span>

1. <span data-ttu-id="64d5f-158">Acesse **Gerenciamento e contabilidade de projeto** > **Atividades Periódicas** > **Estimativas** > **Reverter eliminação**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="64d5f-159">No Painel de Ações, na guia **Processo**, no grupo **Manter**, selecione **Estimativa**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="64d5f-160">Selecione **Reverter eliminação**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="64d5f-161">Use esta página para reverter todas as eliminações com uma data de estimativa especificada e com um status de estimativa de **Eliminado**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="64d5f-162">O status da transação será alterado depois que você selecionar os campos apropriados.</span><span class="sxs-lookup"><span data-stu-id="64d5f-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="64d5f-163">Isso também alterará automaticamente o status do projeto para **Em andamento** se o estágio do projeto estiver definido como concluído.</span><span class="sxs-lookup"><span data-stu-id="64d5f-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="64d5f-164">O status da estimativa do período do projeto será aletrado de volta para **Lançado**.</span><span class="sxs-lookup"><span data-stu-id="64d5f-164">The estimate status of the project period changes back to **Posted**.</span></span>
