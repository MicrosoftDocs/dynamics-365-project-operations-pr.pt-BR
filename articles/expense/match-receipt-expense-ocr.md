---
title: Capturar um recibo usando OCR
description: Este tópico fornece informações sobre o processamento de reconhecimento óptico de caracteres (OCR) para recibos.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c7fa8a805acbf7c75edd49c4c49aa159493f525
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001997"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="6a2ce-103">Capturar um recibo usando OCR</span><span class="sxs-lookup"><span data-stu-id="6a2ce-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="6a2ce-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="6a2ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a2ce-105">A entrada de despesas foi aprimorada com a introdução do processamento de reconhecimento óptico de caracteres (OCR) para recibos.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="6a2ce-106">Essa funcionalidade foi projetada para melhorar a experiência do usuário ao criar relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="6a2ce-107">Recursos principais</span><span class="sxs-lookup"><span data-stu-id="6a2ce-107">Key features</span></span>

- <span data-ttu-id="6a2ce-108">O sistema extrai o nome do comerciante, a data e o valor total dos recibos.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="6a2ce-109">O sistema tentará combinar os recibos não anexados com as transações de despesas não anexadas.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="6a2ce-110">Você pode criar transações de despesas inseridas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="6a2ce-111">Anexe recibos a um relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="6a2ce-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="6a2ce-112">Para anexar automaticamente recibos que incluam transações de cartão de crédito quando um relatório de despesas for criado, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="6a2ce-113">Abra o espaço de trabalho **Gerenciamento de despesas**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="6a2ce-114">Na guia **Recibos**, verifique se existem recibos não anexados.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="6a2ce-115">Você também pode carregar recibos na guia **Recibos**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="6a2ce-116">Na guia **Despesas**, verifique se existem despesas não anexadas.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="6a2ce-117">Normalmente, o administrador de despesas importa essas despesas da operadora do cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="6a2ce-118">Selecione **Novo relatório de despesas**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-118">Select **New expense report**.</span></span> <span data-ttu-id="6a2ce-119">Observe que você também pode incluir despesas e recibos ao criar um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="6a2ce-120">Se você adicionar despesas e recibos, a comparação automática dos recibos com as despesas será disparada.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="6a2ce-121">Criar ou comparar recibos a um relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="6a2ce-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="6a2ce-122">Para criar uma despesa ou comparar uma despesa de um recibo, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="6a2ce-123">Em um relatório de despesas, na v **Recibos**, anexe um recibo selecionando **Adicionar recibos**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="6a2ce-124">Abaixo da imagem carregada do recibo, observe as opções **Criar** e **Comparar**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="6a2ce-125">Selecione **Criar** para criar uma transação de despesas inserida manualmente e preencha os valores que são extraídos do recibo.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="6a2ce-126">Se você selecionar **Comparar**, o sistema tentará corresponder uma despesa existente ao recibo.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="6a2ce-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="6a2ce-127">Installation</span></span>

<span data-ttu-id="6a2ce-128">Para usar esses recursos avançados de despesas, instale o suplemento Expense Management Service para o Microsoft Dynamics 365 Finance e ative os recursos em sua instância.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="6a2ce-129">Você pode acessar o suplemento do seu projeto no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6a2ce-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="6a2ce-130">Entre no LCS e abra o ambiente desejado.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="6a2ce-131">Vá para **Detalhes completos**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="6a2ce-132">Selecione **Manter** ou role para baixo até a FastTab **Suplementos de ambiente**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="6a2ce-133">Selecione **Instalar um novo suplemento**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="6a2ce-134">Selecione **Serviço de Gerenciamento de Despesas**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="6a2ce-135">Siga o guia de instalação e concorde com os termos e condições.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="6a2ce-136">Selecione **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-136">Select **Install**.</span></span>

<span data-ttu-id="6a2ce-137">No espaço de trabalho **Gerenciamento de recursos**, ative os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="6a2ce-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="6a2ce-138">Relatórios de despesas reinventados</span><span class="sxs-lookup"><span data-stu-id="6a2ce-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="6a2ce-139">Faça a correspondência automática e crie despesas a partir do recibo</span><span class="sxs-lookup"><span data-stu-id="6a2ce-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="6a2ce-140">Quando você ativa esses recursos, ocorrem as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="6a2ce-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="6a2ce-141">O espaço de trabalho **Gerenciamento de despesas** existente é substituído pelo novo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="6a2ce-142">Um novo item de menu para visibilidade do campo de despesas é adicionado.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="6a2ce-143">Você ainda pode abrir a página **Relatórios de despesas** anterior acessando **Gerenciamento de despesas > Minhas despesas > Relatórios de despesas**.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="6a2ce-144">Fluxos de trabalho e aprovações ainda levam você para a página de relatórios de despesas existentes.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="6a2ce-145">Os recibos serão processados por meio de Microsoft Azure Cognitive Services e metadados serão extraídos e adicionados.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="6a2ce-146">Foi adicionada uma opção que permite criar um relatório de despesas que inclui recibos não anexados correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="6a2ce-147">Uma opção adicionada aos relatórios de despesas permite que você crie uma linha de despesas a partir de um recibo ou tente fazer a correspondência de um recibo existente com uma linha de despesas existente.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6a2ce-148">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="6a2ce-148">Frequently asked questions</span></span>

<span data-ttu-id="6a2ce-149">**A Microsoft usa meus dados nos modelos dela?**</span><span class="sxs-lookup"><span data-stu-id="6a2ce-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="6a2ce-150">Não, a Microsoft criou um modelo geral de aprendizado de máquina para o serviço de processamento de recibos.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="6a2ce-151">Este modelo não se baseia nos recibos carregados.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="6a2ce-152">**Onde este recurso está disponível e é processado?**</span><span class="sxs-lookup"><span data-stu-id="6a2ce-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="6a2ce-153">Atualmente, há suporte para os Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="6a2ce-154">**Para onde vão meus recibos?**</span><span class="sxs-lookup"><span data-stu-id="6a2ce-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="6a2ce-155">O departamento de finanças entrará em contato com Serviços Cognitivos para extrair dados do campo.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="6a2ce-156">Os Serviços Cognitivos manterão uma cópia do seu recibo por até 24 horas durante o processamento.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="6a2ce-157">Após a conclusão do processamento, os Serviços Cognitivos removerão o recibo.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="6a2ce-158">Os recibos ainda estão armazenados em Finanças.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="6a2ce-159">Para obter mais informações, consulte [Habilite a compreensão do recibo com o novo recurso de Reconhecimento de Formulários](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="6a2ce-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
