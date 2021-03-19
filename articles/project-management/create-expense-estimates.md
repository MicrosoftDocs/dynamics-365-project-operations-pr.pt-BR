---
title: Estimativas de despesas
description: Este tópico fornece informações sobre como definir ou estimar despesas baseadas em projetos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287044"
---
# <a name="expense-estimates"></a><span data-ttu-id="3851c-103">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="3851c-103">Expense estimates</span></span>
<span data-ttu-id="3851c-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="3851c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3851c-105">Junto com a definição de estimativas baseadas em recursos, o Dynamics 365 Project Operations permite que os Gerentes de projeto definam despesas baseadas para cada projeto.</span><span class="sxs-lookup"><span data-stu-id="3851c-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="3851c-106">Cada item de despesa pode ser associada a uma tarefa de projeto ou categoria de despesa específica.</span><span class="sxs-lookup"><span data-stu-id="3851c-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="3851c-107">As categorias de despesas são definidas normalmente no nível organizacional.</span><span class="sxs-lookup"><span data-stu-id="3851c-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="3851c-108">Os preços de cada categoria de despesa é definida normalmente na seguinte hierarquia:</span><span class="sxs-lookup"><span data-stu-id="3851c-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="3851c-109">Organização</span><span class="sxs-lookup"><span data-stu-id="3851c-109">Organization</span></span>
- <span data-ttu-id="3851c-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="3851c-110">Customer</span></span>
- <span data-ttu-id="3851c-111">Cotação/contrato</span><span class="sxs-lookup"><span data-stu-id="3851c-111">Quote/contract</span></span>

<span data-ttu-id="3851c-112">Execute as seguintes etapas para exibir, adicionar ou excluir uma despesa de projeto.</span><span class="sxs-lookup"><span data-stu-id="3851c-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="3851c-113">Vá para **Projetos** e selecione o projeto no qual deseja trabalhar.</span><span class="sxs-lookup"><span data-stu-id="3851c-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="3851c-114">Selecione a guia **Estimativas de Projeto** e exiba a lista de despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="3851c-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="3851c-115">Selecione **Nova Despesa** para adicionar uma despesa.</span><span class="sxs-lookup"><span data-stu-id="3851c-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="3851c-116">Ou, selecione uma despesa a ser excluída e, em seguida, selecione **Excluir Despesa**.</span><span class="sxs-lookup"><span data-stu-id="3851c-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="3851c-117">Os seguintes atributos são definidos para cada item de linha de despesa:</span><span class="sxs-lookup"><span data-stu-id="3851c-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="3851c-118">**Categoria**: os agrupamentos comuns usados para descrever todas as despesas incorridas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="3851c-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="3851c-119">**Data de Início**: a data em que a despesa está prevista para ser incorrida.</span><span class="sxs-lookup"><span data-stu-id="3851c-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="3851c-120">**Quantidade**: o número estimado de itens para uma categoria específica.</span><span class="sxs-lookup"><span data-stu-id="3851c-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="3851c-121">**Preço de Custo Unitário**: o preço unitário usado para calcular o custo da despesa.</span><span class="sxs-lookup"><span data-stu-id="3851c-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="3851c-122">**Preço Unitário de Venda**: o preço unitário usado para calcular os preços de venda da despesa.</span><span class="sxs-lookup"><span data-stu-id="3851c-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]