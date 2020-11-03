---
title: Estimativas de despesas
description: Este tópico fornece informações sobre como definir ou estimar despesas baseadas em projetos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071350"
---
# <a name="expense-estimates"></a><span data-ttu-id="e6fa6-103">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="e6fa6-103">Expense estimates</span></span>
<span data-ttu-id="e6fa6-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="e6fa6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e6fa6-105">Com a definição de estimativas baseadas em recursos, o Dynamics 365 Project Operations permite que os Gerentes de projeto definam as despesas baseadas em projeto para cada projeto.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="e6fa6-106">Cada item de despesa pode ser associada a uma tarefa de projeto ou categoria de despesa específica.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="e6fa6-107">As categorias de despesas são definidas normalmente no nível organizacional.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="e6fa6-108">Os preços de cada categoria de despesa é definida normalmente na seguinte hierarquia:</span><span class="sxs-lookup"><span data-stu-id="e6fa6-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="e6fa6-109">Organização</span><span class="sxs-lookup"><span data-stu-id="e6fa6-109">Organization</span></span>
- <span data-ttu-id="e6fa6-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="e6fa6-110">Customer</span></span>
- <span data-ttu-id="e6fa6-111">Cotação/contrato</span><span class="sxs-lookup"><span data-stu-id="e6fa6-111">Quote/contract</span></span>

<span data-ttu-id="e6fa6-112">Execute as seguintes etapas para exibir, adicionar ou excluir uma despesa de projeto.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="e6fa6-113">Vá para **Projetos** e selecione o projeto no qual deseja trabalhar.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="e6fa6-114">Selecione a guia **Estimativas de Projeto** e exiba a lista de despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="e6fa6-115">Selecione **Nova Despesa** para adicionar uma despesa.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="e6fa6-116">Ou, selecione uma despesa a ser excluída e, em seguida, selecione **Excluir Despesa**.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="e6fa6-117">Os seguintes atributos são definidos para cada item de linha de despesa:</span><span class="sxs-lookup"><span data-stu-id="e6fa6-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="e6fa6-118">**Categoria** : os agrupamentos comuns usados para descrever todas as despesas incorridas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="e6fa6-119">**Data de Início** : a data em que a despesa está prevista para ser incorrida.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="e6fa6-120">**Quantidade** : o número estimado de itens para uma categoria específica.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="e6fa6-121">**Preço de Custo Unitário** : o preço unitário usado para calcular o custo da despesa.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="e6fa6-122">**Preço Unitário de Venda** : o preço unitário usado para calcular os preços de venda da despesa.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

