---
title: Novidades ou alterações na Versão de Atualização 32 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 32 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129652"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="fbfd8-103">Novidades ou alterações na Versão de Atualização 32 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="fbfd8-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fbfd8-104">Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="fbfd8-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fbfd8-106">É compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fbfd8-107">Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="fbfd8-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fbfd8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fbfd8-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 32.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="fbfd8-110">Esta versão tem um número de compilação de V3.10.53.108 e está geralmente disponível por meio de uma atualização automática em junho de 2021.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="fbfd8-111">Versão de Atualização 32</span><span class="sxs-lookup"><span data-stu-id="fbfd8-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fbfd8-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="fbfd8-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="fbfd8-113">Geral</span><span class="sxs-lookup"><span data-stu-id="fbfd8-113">General</span></span>

- <span data-ttu-id="fbfd8-114">Quando uma grande atualização falha, apenas os principais pontos de entrada do aplicativo devem ser bloqueados, para garantir que as entidades compartilhadas ainda estejam acessíveis.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="fbfd8-115">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="fbfd8-115">Time and Expense</span></span>

<span data-ttu-id="fbfd8-116">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="fbfd8-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbfd8-117">**TimeEntriesImportFromResourceAssignment** não mantém os horários de início e término da fatia de contorno de atribuição de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="fbfd8-118">Quando você seleciona a grade **Abrir Entrada** na grade **Entrada de Tempo**, você pode ser impedido de selecionar outros formulários.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="fbfd8-119">Enquanto você importa atribuições para entradas de tempo, a consulta do código do cliente pode gerar um URL longo que falha na consulta.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="fbfd8-120">Na grade **Entrada de Tempo**, depois que um valor é excluído de uma célula, o foco não permanece na grade.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="fbfd8-121">O botão **Rejeitar** foi removido da exibição **Processando aprovações** para aprovações modernas.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="fbfd8-122">A estabilidade e o desempenho da aprovação em massa de entrada de tempo são afetados por impasses e uma falha em lidar de forma adequada com personalizações relacionadas à entidade **Entrada de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="fbfd8-123">Planejamento do Projeto</span><span class="sxs-lookup"><span data-stu-id="fbfd8-123">Project Planning</span></span>

- <span data-ttu-id="fbfd8-124">Uma exceção de referência nula é gerada quando você atualiza um projeto que tem um valor nulo no campo **Unidade de Contratação**.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="fbfd8-125">**Atualizar Totais do Projeto** calcula incorretamente o custo restante e as vendas restantes em um projeto.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="fbfd8-126">Cálculos de preços redundantes afetam o desempenho relacionado a atualizações nos contornos de atribuição de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="fbfd8-127">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="fbfd8-127">Resource Management</span></span>

<span data-ttu-id="fbfd8-128">O seguinte problema foi corrigido:</span><span class="sxs-lookup"><span data-stu-id="fbfd8-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="fbfd8-129">Quando a capacidade do calendário de um recurso reservável for maior que 1, o Project Service Automation reconhece incorretamente a capacidade como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="fbfd8-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="fbfd8-130">Portanto, um loop infinito ocorre na exibição da agenda.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="fbfd8-131">Vendas</span><span class="sxs-lookup"><span data-stu-id="fbfd8-131">Sales</span></span>

<span data-ttu-id="fbfd8-132">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="fbfd8-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbfd8-133">Quando uma linha de diário é criada com um tipo de transação personalizado, ocorre a seguinte exceção de referência nula: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="fbfd8-134">As funções e categorias que são desativadas antes de uma cotação ser copiada não devem ser adicionadas às funções e categorias cobráveis da cotação recém-copiada.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="fbfd8-135">A data do documento e a data contábil não estão alinhadas com a data de início fornecida em um detalhe de linha de fatura criado diretamente em um rascunho de fatura.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="fbfd8-136">Exceções de referência nula são geradas em cenários relacionados à desativação de funções e categorias antes que uma cotação seja copiada.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="fbfd8-137">A ação **Atualizar Preços** na página **Projetos** não atualiza estimativas de despesas e estimativas de material.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
