---
title: Importar e manter transações de cartão de crédito
description: Este tópico explica como importar e manter transações de cartão de crédito relacionadas a despesas. Essas transações podem ser configuradas para que sejam importadas automaticamente em uma programação recorrente ou podem ser importadas manualmente conforme necessário.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071581"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="dc7af-104">Importar e manter transações de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="dc7af-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc7af-105">As transações de cartão de crédito relacionadas a despesas podem ser configuradas para serem importadas automaticamente em um cronograma recorrente.</span><span class="sxs-lookup"><span data-stu-id="dc7af-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="dc7af-106">Como alternativa, elas podem ser importadas manualmente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="dc7af-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="dc7af-107">As transações de cartão de crédito são importadas por meio da entidade de dados Transações de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="dc7af-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="dc7af-108">Para obter mais informações sobre entidades de dados, consulte [Entidades de dados](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="dc7af-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="dc7af-109">Importar transações de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="dc7af-109">Import credit card transactions</span></span>

1. <span data-ttu-id="dc7af-110">Na página **Transações de cartão de crédito** , selecione **Importar transações**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="dc7af-111">Se você estiver abrindo o gerenciamento de dados pela primeira vez, o sistema deverá atualizar a lista de entidades de dados para que seja possível continuar.</span><span class="sxs-lookup"><span data-stu-id="dc7af-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="dc7af-112">No campo **Nome** , insira uma descrição exclusiva do trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="dc7af-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="dc7af-113">No campo **Formato de dados de origem** , selecione o formato do arquivo que contém as transações de cartão de crédito a serem importadas.</span><span class="sxs-lookup"><span data-stu-id="dc7af-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="dc7af-114">Selecione **Carregar** e, em seguida, localize e selecione o arquivo a ser importado.</span><span class="sxs-lookup"><span data-stu-id="dc7af-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="dc7af-115">Depois que o arquivo for carregado, valide o mapeamento do arquivo de transações de cartão de crédito e as colunas da entidade de dados Transações de cartão de crédito selecionando o link **Exibir mapa** no bloco.</span><span class="sxs-lookup"><span data-stu-id="dc7af-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="dc7af-116">Se houver erros de mapeamento ou se você precisar alterá-lo, faça as alterações na guia **Visualização de mapeamento** ou na guia **Detalhes de mapeamento**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="dc7af-117">Para automatizar as transações de cartão de crédito, selecione **Criar trabalho de dados recorrente**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="dc7af-118">Você pode configurar a recorrência que define a frequência com que as transações de cartão de crédito devem ser importadas.</span><span class="sxs-lookup"><span data-stu-id="dc7af-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="dc7af-119">Ao concluir, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="dc7af-120">Para importar o arquivo selecionado agora, selecione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="dc7af-121">Se ocorrerem erros durante a importação, você pode visualizar o log de execução ou os dados de preparo para ver os erros que devem ser corrigidos para ajudar a garantir uma importação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dc7af-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="dc7af-122">Se você precisar importar mais de um formato de arquivo, deverá criar trabalhos de importação separados para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="dc7af-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="dc7af-123">Reatribuir as transações de cartão de crédito de funcionários despedidos</span><span class="sxs-lookup"><span data-stu-id="dc7af-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="dc7af-124">Quando um registro de funcionário é encerrado, a conta do Active Directory Domain Services (AD DS) desse funcionário é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="dc7af-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="dc7af-125">No entanto, pode haver transações de cartão de crédito ativas que ainda devem ser contabilizadas como despesas e reembolsadas.</span><span class="sxs-lookup"><span data-stu-id="dc7af-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="dc7af-126">Na página **Transações de cartão de crédito** , você pode reatribuir um funcionário em qualquer transação de cartão de crédito na qual o funcionário associado tenha sido despedido.</span><span class="sxs-lookup"><span data-stu-id="dc7af-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="dc7af-127">Selecione uma ou mais transações de cartão de crédito e, em seguida, selecione **Reatribuir transações**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="dc7af-128">Você pode selecionar outro funcionário ao qual atribuir as transações de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="dc7af-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="dc7af-129">Depois que as transações de cartão de crédito forem reatribuídas, elas poderão ser selecionadas para um relatório de despesas e pagas por meio do processo normal de reembolso de relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="dc7af-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
