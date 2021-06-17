---
title: Processamento de recibo de despesas
description: Este tópico fornece informações sobre o processamento de reconhecimento óptico de caracteres (OCR) para recibos. Esse recurso foi projetado para melhorar a experiência do usuário ao criar relatórios de despesas no Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993492"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="11f16-104">Processamento de recibo de despesas</span><span class="sxs-lookup"><span data-stu-id="11f16-104">Expense receipt processing</span></span>

<span data-ttu-id="11f16-105">A entrada de despesas foi aprimorada com a introdução do processamento de reconhecimento óptico de caracteres (OCR) para recibos.</span><span class="sxs-lookup"><span data-stu-id="11f16-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="11f16-106">Esse recurso foi projetado para melhorar a experiência do usuário ao criar relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="11f16-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="11f16-107">Recursos principais</span><span class="sxs-lookup"><span data-stu-id="11f16-107">Key features</span></span>

- <span data-ttu-id="11f16-108">O nome do comerciante, a data e o valor total são extraídos dos recibos.</span><span class="sxs-lookup"><span data-stu-id="11f16-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="11f16-109">O recurso tenta combinar os recibos não anexados com as transações de despesas não anexadas.</span><span class="sxs-lookup"><span data-stu-id="11f16-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="11f16-110">Usuários podem criar transações de despesas inseridas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="11f16-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="11f16-111">Exemplos de uso</span><span class="sxs-lookup"><span data-stu-id="11f16-111">Usage examples</span></span>

<span data-ttu-id="11f16-112">Para anexar automaticamente recibos que incluam transações de cartão de crédito quando um relatório de despesas for criado, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="11f16-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="11f16-113">Abra o espaço de trabalho **Gerenciamento de despesas**.</span><span class="sxs-lookup"><span data-stu-id="11f16-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="11f16-114">Na guia **Recibos**, verifique se existem recibos não anexados.</span><span class="sxs-lookup"><span data-stu-id="11f16-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="11f16-115">Você também pode carregar recibos na guia **Recibos**.</span><span class="sxs-lookup"><span data-stu-id="11f16-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="11f16-116">Na guia **Despesas**, verifique se existem despesas não anexadas.</span><span class="sxs-lookup"><span data-stu-id="11f16-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="11f16-117">Normalmente, o administrador de despesas importa essas despesas da operadora do cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="11f16-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="11f16-118">Selecione **Novo relatório de despesas**.</span><span class="sxs-lookup"><span data-stu-id="11f16-118">Select **New expense report**.</span></span> <span data-ttu-id="11f16-119">Observe que você também pode incluir despesas e recibos ao criar um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="11f16-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="11f16-120">Se você adicionar despesas e recibos, a comparação automática dos recibos com as despesas será disparada.</span><span class="sxs-lookup"><span data-stu-id="11f16-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="11f16-121">Para criar uma despesa ou comparar uma despesa de um recibo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="11f16-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="11f16-122">Em um relatório de despesas, na v **Recibos**, anexe um recibo selecionando **Adicionar recibos**.</span><span class="sxs-lookup"><span data-stu-id="11f16-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="11f16-123">Abaixo da imagem carregada do recibo, observe as opções **Criar** e **Comparar**.</span><span class="sxs-lookup"><span data-stu-id="11f16-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="11f16-124">Selecione **Criar** para criar uma transação de despesas inserida manualmente e preencha os valores que são extraídos do recibo.</span><span class="sxs-lookup"><span data-stu-id="11f16-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="11f16-125">Se você selecionar **Comparar**, o sistema tentará corresponder uma despesa existente ao recibo.</span><span class="sxs-lookup"><span data-stu-id="11f16-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="11f16-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="11f16-126">Installation</span></span>

<span data-ttu-id="11f16-127">Este recurso funciona em combinação com o recurso **Relatórios de despesas reinventados** para ajudar a simplificar a experiência de despesas.</span><span class="sxs-lookup"><span data-stu-id="11f16-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="11f16-128">Este recurso está disponível apenas para ambientes Nível 2+, que são Área restrita e Produção.</span><span class="sxs-lookup"><span data-stu-id="11f16-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="11f16-129">Para usar esses recursos avançados de despesas, instale o suplemento Expense Management Service para o Microsoft Dynamics 365 Finance e ative os recursos em sua instância.</span><span class="sxs-lookup"><span data-stu-id="11f16-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="11f16-130">Você pode acessar o suplemento do seu projeto no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="11f16-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="11f16-131">Entre no LCS e abra o ambiente desejado.</span><span class="sxs-lookup"><span data-stu-id="11f16-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="11f16-132">Vá para **Detalhes completos**.</span><span class="sxs-lookup"><span data-stu-id="11f16-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="11f16-133">Selecione **Manter** ou role para baixo até a FastTab **Suplementos de ambiente**.</span><span class="sxs-lookup"><span data-stu-id="11f16-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="11f16-134">Selecione **Instalar um novo suplemento**.</span><span class="sxs-lookup"><span data-stu-id="11f16-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="11f16-135">Selecione **Serviço de Gerenciamento de Despesas**.</span><span class="sxs-lookup"><span data-stu-id="11f16-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="11f16-136">Siga o guia de instalação e concorde com os termos e condições.</span><span class="sxs-lookup"><span data-stu-id="11f16-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="11f16-137">Selecione **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="11f16-137">Select **Install**.</span></span>

<span data-ttu-id="11f16-138">No espaço de trabalho **Gerenciamento de recursos**, ative os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="11f16-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="11f16-139">Relatórios de despesas reinventados</span><span class="sxs-lookup"><span data-stu-id="11f16-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="11f16-140">Faça a correspondência automática e crie despesas a partir do recibo</span><span class="sxs-lookup"><span data-stu-id="11f16-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="11f16-141">Quando você ativa esses recursos, ocorrem as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="11f16-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="11f16-142">O espaço de trabalho **Gerenciamento de despesas** existente é substituído pelo novo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="11f16-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="11f16-143">Um novo item de menu para visibilidade do campo de despesas é adicionado.</span><span class="sxs-lookup"><span data-stu-id="11f16-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="11f16-144">Você ainda pode abrir a página **Relatórios de despesas** anterior acessando **Gerenciamento de despesas > Minhas despesas > Relatórios de despesas**.</span><span class="sxs-lookup"><span data-stu-id="11f16-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="11f16-145">Fluxos de trabalho e aprovações ainda levam você para a página de relatórios de despesas existentes.</span><span class="sxs-lookup"><span data-stu-id="11f16-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="11f16-146">Os recibos serão processados por meio de Microsoft Azure Cognitive Services e metadados serão extraídos e adicionados.</span><span class="sxs-lookup"><span data-stu-id="11f16-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="11f16-147">Foi adicionada uma opção que permite criar um relatório de despesas que inclui recibos não anexados correspondentes.</span><span class="sxs-lookup"><span data-stu-id="11f16-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="11f16-148">Uma opção adicionada aos relatórios de despesas permite que você crie uma linha de despesas a partir de um recibo ou tente fazer a correspondência de um recibo existente com uma linha de despesas existente.</span><span class="sxs-lookup"><span data-stu-id="11f16-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="11f16-149">Para obter mais informações sobre o recurso Relatórios de despesas reinventados, consulte [Relatórios de despesas reinventados](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="11f16-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="11f16-150">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="11f16-150">Frequently asked questions</span></span>

<span data-ttu-id="11f16-151">**A Microsoft usa meus dados nos modelos dela?**</span><span class="sxs-lookup"><span data-stu-id="11f16-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="11f16-152">Não, a Microsoft criou um modelo geral de aprendizado de máquina para o serviço de processamento de recibos.</span><span class="sxs-lookup"><span data-stu-id="11f16-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="11f16-153">Este modelo não se baseia nos recibos carregados.</span><span class="sxs-lookup"><span data-stu-id="11f16-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="11f16-154">**Onde este recurso está disponível e é processado?**</span><span class="sxs-lookup"><span data-stu-id="11f16-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="11f16-155">Atualmente, há suporte para os Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="11f16-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="11f16-156">**Para onde vão meus recibos?**</span><span class="sxs-lookup"><span data-stu-id="11f16-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="11f16-157">O departamento de finanças entrará em contato com Serviços Cognitivos para extrair dados do campo.</span><span class="sxs-lookup"><span data-stu-id="11f16-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="11f16-158">Os Serviços Cognitivos manterão uma cópia do seu recibo por até 24 horas durante o processamento.</span><span class="sxs-lookup"><span data-stu-id="11f16-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="11f16-159">Após a conclusão do processamento, os Serviços Cognitivos removerão o recibo.</span><span class="sxs-lookup"><span data-stu-id="11f16-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="11f16-160">Os recibos ainda estão armazenados em Finanças.</span><span class="sxs-lookup"><span data-stu-id="11f16-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="11f16-161">Para obter mais informações, consulte [Habilite a compreensão do recibo com o novo recurso de Reconhecimento de Formulários](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="11f16-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]