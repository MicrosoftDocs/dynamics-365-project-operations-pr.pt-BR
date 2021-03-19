---
title: Configurar integração de cartão de crédito
description: Este tópico explica como importar e manter transações de cartão de crédito relacionadas a despesas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276154"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="fac8a-103">Configurar integração de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="fac8a-103">Set up credit card integration</span></span>

<span data-ttu-id="fac8a-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="fac8a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fac8a-105">As transações de cartão de crédito relacionadas a despesas podem ser configuradas para serem importadas automaticamente em um cronograma recorrente.</span><span class="sxs-lookup"><span data-stu-id="fac8a-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="fac8a-106">Como alternativa, elas podem ser importadas manualmente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="fac8a-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="fac8a-107">As transações de cartão de crédito são importadas por meio da entidade de dados Transações de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="fac8a-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="fac8a-108">Importar transações de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="fac8a-108">Import credit card transactions</span></span>

1. <span data-ttu-id="fac8a-109">Na página **Transações de cartão de crédito**, selecione **Importar transações**.</span><span class="sxs-lookup"><span data-stu-id="fac8a-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="fac8a-110">Se você estiver abrindo o gerenciamento de dados pela primeira vez, o sistema deverá atualizar a lista de entidades de dados para que seja possível continuar.</span><span class="sxs-lookup"><span data-stu-id="fac8a-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="fac8a-111">No campo **Nome**, insira uma descrição exclusiva do trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="fac8a-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="fac8a-112">No campo **Formato de dados de origem**, selecione o formato do arquivo que contém as transações de cartão de crédito a serem importadas.</span><span class="sxs-lookup"><span data-stu-id="fac8a-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="fac8a-113">Selecione **Carregar** e, em seguida, localize e selecione o arquivo a ser importado.</span><span class="sxs-lookup"><span data-stu-id="fac8a-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="fac8a-114">Depois que o arquivo for carregado, valide o mapeamento do arquivo de transações de cartão de crédito e as colunas da entidade de dados Transações de cartão de crédito selecionando o link **Exibir mapa** no bloco.</span><span class="sxs-lookup"><span data-stu-id="fac8a-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="fac8a-115">Se houver erros de mapeamento ou se você precisar alterá-lo, faça as alterações na guia **Visualização de mapeamento** ou na guia **Detalhes de mapeamento**.</span><span class="sxs-lookup"><span data-stu-id="fac8a-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="fac8a-116">Para automatizar as transações de cartão de crédito, selecione **Criar trabalho de dados recorrente**.</span><span class="sxs-lookup"><span data-stu-id="fac8a-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="fac8a-117">Você pode configurar a recorrência que define a frequência com que as transações de cartão de crédito devem ser importadas.</span><span class="sxs-lookup"><span data-stu-id="fac8a-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="fac8a-118">Ao concluir, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="fac8a-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="fac8a-119">Para importar o arquivo selecionado agora, selecione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="fac8a-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="fac8a-120">Se ocorrerem erros durante a importação, você pode visualizar o log de execução ou os dados de preparo para ver os erros que devem ser corrigidos para ajudar a garantir uma importação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fac8a-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="fac8a-121">Se você precisar importar mais de um formato de arquivo, deverá criar trabalhos de importação separados para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="fac8a-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="fac8a-122">Reatribuir as transações de cartão de crédito de funcionários despedidos</span><span class="sxs-lookup"><span data-stu-id="fac8a-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="fac8a-123">Quando um registro de funcionário é encerrado, a conta do Active Directory Domain Services (AD DS) desse funcionário é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="fac8a-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="fac8a-124">No entanto, pode haver transações de cartão de crédito ativas que ainda devem ser contabilizadas como despesas e reembolsadas.</span><span class="sxs-lookup"><span data-stu-id="fac8a-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="fac8a-125">Na página **Transações de cartão de crédito**, você pode reatribuir um funcionário em qualquer transação de cartão de crédito na qual o funcionário associado tenha sido despedido.</span><span class="sxs-lookup"><span data-stu-id="fac8a-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="fac8a-126">Selecione uma ou mais transações de cartão de crédito e, em seguida, selecione **Reatribuir transações**.</span><span class="sxs-lookup"><span data-stu-id="fac8a-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="fac8a-127">Você pode selecionar outro funcionário ao qual atribuir as transações de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="fac8a-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="fac8a-128">Depois que as transações de cartão de crédito forem reatribuídas, elas poderão ser selecionadas para um relatório de despesas e pagas por meio do processo normal de reembolso de relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="fac8a-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]