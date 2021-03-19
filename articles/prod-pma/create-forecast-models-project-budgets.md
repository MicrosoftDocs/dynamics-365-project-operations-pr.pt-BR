---
title: Criar modelos de previsão para orçamentos de projeto
description: Este tópico descreve como criar um modelo de previsão para os orçamentos restantes.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271024"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="21081-103">Criar modelos de previsão para orçamentos de projeto</span><span class="sxs-lookup"><span data-stu-id="21081-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21081-104">Este tópico descreve como criar um modelo de previsão para os orçamentos restantes.</span><span class="sxs-lookup"><span data-stu-id="21081-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="21081-105">Um projeto sujeito a controle de orçamento usa dois tipos de orçamento: original e restante.</span><span class="sxs-lookup"><span data-stu-id="21081-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="21081-106">Ao criar um orçamento de projeto, você deverá especificar os modelos de previsão de orçamento original e restante que foram criados na página **Modelos de previsão**.</span><span class="sxs-lookup"><span data-stu-id="21081-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="21081-107">Os orçamentos do projeto com base nos modelos especificados são criados quando você compromete o orçamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="21081-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="21081-108">Um modelo de previsão usado para controle de orçamento não pode ter um submodelo ou ser usado como um submodelo.</span><span class="sxs-lookup"><span data-stu-id="21081-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="21081-109">Selecione **Gerenciamento e contabilidade de projeto** > **Configuração** > **Previsões**  > **Modelos de previsão**.</span><span class="sxs-lookup"><span data-stu-id="21081-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="21081-110">Selecione **Novo** para criar um novo modelo de previsão e, em seguida, insira um número de ID de modelo e nome para o novo modelo.</span><span class="sxs-lookup"><span data-stu-id="21081-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="21081-111">Defina a opção **Parado** como **Sim** para evitar quaisquer alterações nas linhas de previsão do modelo de previsão.</span><span class="sxs-lookup"><span data-stu-id="21081-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="21081-112">Se as linhas de previsão às quais o modelo está associado tiverem de gerar previsões de fluxo de caixa no razão geral, defina **Incluir nas previsões de Fluxo de caixa** como **Sim.**</span><span class="sxs-lookup"><span data-stu-id="21081-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="21081-113">Para usar a data do projeto como data da fatura, defina **Previsão da data da fatura** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="21081-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="21081-114">No campo **Tipo de orçamento**, selecione um dos seguintes tipos de modelo:</span><span class="sxs-lookup"><span data-stu-id="21081-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="21081-115">**Orçamento original**: use os valores do orçamento original comprometidos quando o orçamento inicial for criado e aprovado.</span><span class="sxs-lookup"><span data-stu-id="21081-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="21081-116">**Orçamento restante**: use os valores de orçamento restante durante a vida do projeto.</span><span class="sxs-lookup"><span data-stu-id="21081-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="21081-117">Os saldos neste modelo de previsão são reduzidos por transações reais e aumentados ou diminuídos por revisões de orçamento.</span><span class="sxs-lookup"><span data-stu-id="21081-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="21081-118">**Transferência**: use os valores do orçamento de transferência para o projeto.</span><span class="sxs-lookup"><span data-stu-id="21081-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="21081-119">Transporte é um processo opcional que pode ser executado para transferir valores de orçamento não utilizados de um ano fiscal para outro.</span><span class="sxs-lookup"><span data-stu-id="21081-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="21081-120">Defina as seguintes opções como necessário:</span><span class="sxs-lookup"><span data-stu-id="21081-120">Set the following options as required:</span></span>

   - <span data-ttu-id="21081-121">Habilite **Previsão da data da fatura** para usar a data do projeto como a data da fatura.</span><span class="sxs-lookup"><span data-stu-id="21081-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="21081-122">Habilite **Previsão com WIP** para prever com base no trabalho em andamento (WIP) e, em seguida, selecione o tipo de WIP.</span><span class="sxs-lookup"><span data-stu-id="21081-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="21081-123">Você pode manter o **Tipo de orçamento** padrão como **Nenhum** ou insira um novo tipo.</span><span class="sxs-lookup"><span data-stu-id="21081-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="21081-124">O tipo de orçamento não poderá ser alterado após a alteração de um registro.</span><span class="sxs-lookup"><span data-stu-id="21081-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="21081-125">Se você alterar o tipo de orçamento padrão, todas as outras opções ficarão indisponíveis para atualizações e você não poderá reutilizar esse modelo de previsão.</span><span class="sxs-lookup"><span data-stu-id="21081-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]