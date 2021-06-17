---
title: Configurar integração do cartão de crédito
description: Este tópico explica como trabalhar com transações de cartão de crédito relacionadas a despesas.
author: suvaidya
ms.date: 04/02/2021
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
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001787"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="82818-103">Configurar integração do cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="82818-103">Set up credit card integration</span></span>

<span data-ttu-id="82818-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="82818-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="82818-105">As transações de cartão de crédito relacionadas a despesas podem ser configuradas para serem importadas automaticamente em um cronograma recorrente.</span><span class="sxs-lookup"><span data-stu-id="82818-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="82818-106">Como alternativa, elas podem ser importadas manualmente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="82818-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="82818-107">As transações de cartão de crédito são importadas por meio da entidade de dados transações de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="82818-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="82818-108">Importar transações de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="82818-108">Import credit card transactions</span></span>

<span data-ttu-id="82818-109">Para importar transações de cartão de crédito, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="82818-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="82818-110">Na página **Transações de cartão de crédito**, selecione **Importar transações**.</span><span class="sxs-lookup"><span data-stu-id="82818-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="82818-111">Se você estiver abrindo o gerenciamento de dados pela primeira vez, o sistema deverá atualizar a lista de entidades de dados para que seja possível continuar.</span><span class="sxs-lookup"><span data-stu-id="82818-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="82818-112">No campo **Nome**, insira uma descrição exclusiva para o trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="82818-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="82818-113">No campo **Formato de dados de origem**, selecione o formato do arquivo que contém as transações de cartão de crédito a serem importadas.</span><span class="sxs-lookup"><span data-stu-id="82818-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="82818-114">Selecione **Carregar** e, em seguida, localize e selecione o arquivo a ser importado.</span><span class="sxs-lookup"><span data-stu-id="82818-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="82818-115">Depois que o arquivo for carregado, valide o mapeamento do arquivo de transações de cartão de crédito e as colunas da entidade de dados transações de cartão de crédito selecionando o link **Exibir mapa** no bloco.</span><span class="sxs-lookup"><span data-stu-id="82818-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="82818-116">Se houver erros de mapeamento ou se você precisar alterá-lo, faça as alterações na guia **Visualização de mapeamento** ou na guia **Detalhes de mapeamento**.</span><span class="sxs-lookup"><span data-stu-id="82818-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="82818-117">Para automatizar as transações de cartão de crédito, selecione **Criar trabalho de dados recorrente**.</span><span class="sxs-lookup"><span data-stu-id="82818-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="82818-118">Você pode configurar a recorrência que define a frequência com que as transações de cartão de crédito devem ser importadas.</span><span class="sxs-lookup"><span data-stu-id="82818-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="82818-119">Ao concluir, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="82818-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="82818-120">Para importar o arquivo selecionado agora, selecione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="82818-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="82818-121">Se ocorrerem erros durante a importação, você poderá visualizar o log de execução ou os dados de preparo para ver os erros que devem ser corrigidos para ajudar a garantir uma importação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="82818-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="82818-122">Se você precisar importar mais de um formato de arquivo, deverá criar trabalhos de importação separados para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="82818-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="82818-123">Reatribuir as transações de cartão de crédito de funcionários despedidos</span><span class="sxs-lookup"><span data-stu-id="82818-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="82818-124">Quando um registro de funcionário é encerrado, a conta do Active Directory Domain Services (AD DS) desse funcionário é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="82818-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="82818-125">No entanto, pode haver transações de cartão de crédito ativas que ainda devem ser contabilizadas como despesas e reembolsadas.</span><span class="sxs-lookup"><span data-stu-id="82818-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="82818-126">Na página **Transações de cartão de crédito**, você pode reatribuir o funcionário a qualquer transação de cartão de crédito em que o funcionário associado foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="82818-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="82818-127">Selecione uma ou mais transações de cartão de crédito e, em seguida, selecione **Reatribuir transações**.</span><span class="sxs-lookup"><span data-stu-id="82818-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="82818-128">Você pode selecionar outro funcionário ao qual atribuir as transações de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="82818-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="82818-129">Depois que as transações de cartão de crédito forem reatribuídas, elas poderão ser selecionadas para um relatório de despesas e pagas por meio do processo normal de reembolso de relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="82818-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="82818-130">Excluir transações de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="82818-130">Delete credit card transactions</span></span> 

<span data-ttu-id="82818-131">Às vezes, depois que as transações de cartão de crédito são importadas, talvez seja preciso excluir certas transações.</span><span class="sxs-lookup"><span data-stu-id="82818-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="82818-132">Isso pode ocorrer porque as transações são duplicadas ou porque os dados podem não ser precisos.</span><span class="sxs-lookup"><span data-stu-id="82818-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="82818-133">Os administradores podem usar o recurso **"Excluir transações de cartão de crédito"** para selecionar e excluir transações de cartão de crédito que **não são anexadas** a um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="82818-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="82818-134">Acesse **Tarefas periódicas** > **Excluir transações de cartão de crédito**.</span><span class="sxs-lookup"><span data-stu-id="82818-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="82818-135">Selecione **Filtro** e forneça informações para identificar os registros a serem incluídos.</span><span class="sxs-lookup"><span data-stu-id="82818-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="82818-136">Selecione **OK** para excluir os registros.</span><span class="sxs-lookup"><span data-stu-id="82818-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
