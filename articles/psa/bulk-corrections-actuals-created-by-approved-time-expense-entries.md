---
title: Correções em massa de valores criados por entradas de hora e despesa aprovadas
description: Este tópico explica como um administrador pode realizar correções separadamente ou em massa a entradas de hora e despesa aprovadas anteriormente se o faturamento não tiver sido concluído.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290885"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="5ca75-103">Correções em massa de valores criados por entradas de hora e despesa aprovadas</span><span class="sxs-lookup"><span data-stu-id="5ca75-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5ca75-104">Ocasionalmente, uma entrada de hora ou de despesa pode ser inserida incorretamente.</span><span class="sxs-lookup"><span data-stu-id="5ca75-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="5ca75-105">Por exemplo, um consultor pode selecionar a data erada ao criar uma entrada de hora ou pode transpor os números ao inserir uma despesa.</span><span class="sxs-lookup"><span data-stu-id="5ca75-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="5ca75-106">Se um consultor não puder atualizar as entradas enviadas, um administrador pode corrigir a entrada de um projeto diretamente.</span><span class="sxs-lookup"><span data-stu-id="5ca75-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="5ca75-107">Para concluir os procedimentos neste tópico, será necessário ter permissões de Administrador.</span><span class="sxs-lookup"><span data-stu-id="5ca75-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="5ca75-108">Corrigir entradas de hora aprovadas</span><span class="sxs-lookup"><span data-stu-id="5ca75-108">Correct approved time entries</span></span>     

<span data-ttu-id="5ca75-109">Siga as etapas para corrigir uma ou várias entradas de hora de um projeto.</span><span class="sxs-lookup"><span data-stu-id="5ca75-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="5ca75-110">Na área **Vendas**, selecione **Transações** e depois selecione **Hora Aprovada**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="5ca75-111">Na lista **Hora Aprovada**, localize e selecione uma ou mais entradas de hora aprovadas para corrigir.</span><span class="sxs-lookup"><span data-stu-id="5ca75-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="5ca75-112">Você pode usar o filtro para localizar entradas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5ca75-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="5ca75-113">Por exemplo, você pode filtrar uma ID de Projeto e selecionar todas as horas aprovadas com essa ID de Projeto.</span><span class="sxs-lookup"><span data-stu-id="5ca75-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="5ca75-114">Selecione **Corrigir entradas**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-114">Select **Correct entries**.</span></span> <span data-ttu-id="5ca75-115">Um novo diário de correção é criado automaticamente com o tipo de **Correção de hora** atribuído.</span><span class="sxs-lookup"><span data-stu-id="5ca75-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="5ca75-116">As entradas selecionadas são adicionadas ao diário.</span><span class="sxs-lookup"><span data-stu-id="5ca75-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="5ca75-117">Na página **Novo Diário**, insira uma **Descrição** para o diário de correção e selecione a guia **Correções de Entrada de Hora**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="5ca75-118">Na seção **Novos Valores para Entradas de Hora**, atualize os campos com as informações corretas, conforme a necessidade.</span><span class="sxs-lookup"><span data-stu-id="5ca75-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="5ca75-119">Por exemplo, é possível alterar o projeto atribuído ou o recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="5ca75-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="5ca75-120">Selecione **Versão Prévia**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-120">Select **Preview**.</span></span> <span data-ttu-id="5ca75-121">Na caixa de diálogo, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="5ca75-122">Na guia **Linhas do diário**, é possível visualizar uma lista dos dados reais originais relacionados às entradas de hora selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.</span><span class="sxs-lookup"><span data-stu-id="5ca75-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="5ca75-123">Se forem necessárias correções adicionais, repita as etapas 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="5ca75-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ca75-124">Todos os dados reais corrigidos terão os mesmos valores selecionados na seção **Novos valores para Entradas de Hora**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="5ca75-125">Se as correções aparecerem conforme o esperado, selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="5ca75-126">Na caixa de diálogo, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="5ca75-127">Volte para a área **Vendas** e selecione **Projetos**, depois abra o projeto para o qual atualizou as entradas de hora.</span><span class="sxs-lookup"><span data-stu-id="5ca75-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="5ca75-128">Na página **Projetos**, na guia **Dados Reais**, exiba as alterações feitas.</span><span class="sxs-lookup"><span data-stu-id="5ca75-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ca75-129">Se a guia **Dados Reais** não estiver visível, selecione **Relacionados** > **Dados Reais**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="5ca75-130">Na lista **Exibição Associada de Dados Reais**, é possível ver que as entradas de hora originais que foram revertidas ainda estão listadas, assim como as entradas de hora corrigidas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="5ca75-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="5ca75-131">Por exemplo, no gráfico a seguir, há dois itens de linha com uma quantidade igual a 8,00 com débitos listados na coluna Valor.</span><span class="sxs-lookup"><span data-stu-id="5ca75-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="5ca75-132">Além disso, há dois itens de linha com uma quantidade igual a -8,00 que mostram quantidades creditadas na coluna Valor.</span><span class="sxs-lookup"><span data-stu-id="5ca75-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="5ca75-133">Essas correções definem a quantidade como zero.</span><span class="sxs-lookup"><span data-stu-id="5ca75-133">These corrections bring the quantity to zero.</span></span>

![Lista de exibição associada de dados reais](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="5ca75-135">Corrigir entradas de despesa aprovadas</span><span class="sxs-lookup"><span data-stu-id="5ca75-135">Correct approved expense entries</span></span>

<span data-ttu-id="5ca75-136">Siga as etapas para corrigir uma ou mais entradas de despesa.</span><span class="sxs-lookup"><span data-stu-id="5ca75-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="5ca75-137">Na área **Vendas**, no painel de navegação à esquerda, em **Transações**, selecione **Despesas Aprovadas**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="5ca75-138">Na lista **Despesas Aprovadas**, selecione o projeto que deseja corrigir e selecione **Entradas corretas**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="5ca75-139">Um novo diário de correção será criado automaticamente com o tipo de **Correção de despesa** atribuído.</span><span class="sxs-lookup"><span data-stu-id="5ca75-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="5ca75-140">Na página **Novo Diário**, insira uma **Descrição** para a correção e, na guia **Correção de Despesa**, na seção **Novos Valores para Despesas**, selecione os campos de dados que deseja corrigir para as linhas de despesa selecionadas.</span><span class="sxs-lookup"><span data-stu-id="5ca75-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="5ca75-141">Por exemplo, é possível atribuir a despesa a outro **Projeto** ou corrigir a **Categoria de Despesa**, **Data da Despesa** ou **Recurso Reservável**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="5ca75-142">Selecione **Versão Prévia**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-142">Select **Preview**.</span></span> <span data-ttu-id="5ca75-143">Na caixa de diálogo, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="5ca75-144">Verifique as correções na guia **Linhas do diário**. É possível visualizar uma lista dos dados reais originais relacionados às entradas de despesa selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.</span><span class="sxs-lookup"><span data-stu-id="5ca75-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="5ca75-145">Se os valores das correções aparecerem conforme o esperado, selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="5ca75-146">Na caixa de diálogo, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="5ca75-147">Se os valores não estiverem sendo exibidos conforme o esperado, selecione **Cancelar** para voltar para a lista de **Despesas Aprovadas**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="5ca75-148">Repita as etapas 2 a 5.</span><span class="sxs-lookup"><span data-stu-id="5ca75-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ca75-149">Os dados reais corrigidos terão os mesmos valores selecionados na seção **Novos valores para Despesas**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="5ca75-150">Depois de confirmar o diário de correção, navegue de volta até os projetos atualizados para exibir as alterações.</span><span class="sxs-lookup"><span data-stu-id="5ca75-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="5ca75-151">Na página do projeto, na guia **Dados Reais**, revise a **Exibição Associada de Dados Reais**.</span><span class="sxs-lookup"><span data-stu-id="5ca75-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="5ca75-152">As entradas originais e as entradas corrigidas serão listadas.</span><span class="sxs-lookup"><span data-stu-id="5ca75-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="5ca75-153">O gráfico a seguir mostra os valores de entrada de despesa originais e os valores de entrada de despesa correspondentes corrigidos.</span><span class="sxs-lookup"><span data-stu-id="5ca75-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Dados reais de despesa](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]