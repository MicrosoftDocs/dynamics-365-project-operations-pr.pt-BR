---
title: Novidades ou alterações na Versão de Atualização 24 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 24 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 956dcd2a06fad1eec488ad81bec2de4bd0550e82
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948901"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="4c47d-103">Versão de Atualização 24, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="4c47d-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4c47d-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4c47d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4c47d-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="4c47d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4c47d-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4c47d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4c47d-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="4c47d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4c47d-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4c47d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4c47d-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 24.</span><span class="sxs-lookup"><span data-stu-id="4c47d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="4c47d-110">Esta versão tem um número de build V 3.10.42.43 e foi disponibilizada para o público em geral por meio de uma atualização automática em outubro de 2020.</span><span class="sxs-lookup"><span data-stu-id="4c47d-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="4c47d-111">Versão de Atualização 24</span><span class="sxs-lookup"><span data-stu-id="4c47d-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4c47d-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="4c47d-112">Bug fixes</span></span>

<span data-ttu-id="4c47d-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4c47d-113">**Sales**</span></span>

<span data-ttu-id="4c47d-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="4c47d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c47d-115">Problema ao configurar a lista de preços padrão de produtos.</span><span class="sxs-lookup"><span data-stu-id="4c47d-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="4c47d-116">O desempenho de Ganho de cotação é lento devido à lista de preços inserida e à cópia dos registros de preços da função.</span><span class="sxs-lookup"><span data-stu-id="4c47d-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="4c47d-117">**Contrato de Projeto/Hub de Vendas** > **Item de Linha de Produtos/Quantidade de Linhas da Ordem** é automaticamente arredondado para o próximo inteiro.</span><span class="sxs-lookup"><span data-stu-id="4c47d-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="4c47d-118">Eleve aos privilégios do sistema ao ler listas de preços.</span><span class="sxs-lookup"><span data-stu-id="4c47d-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="4c47d-119">Copie os campos de endereço do cliente **address1_freighttermscode** e **address1_shippingmethodcode** para Cotação/Ordem.</span><span class="sxs-lookup"><span data-stu-id="4c47d-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="4c47d-120">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="4c47d-120">**Time and Expense**</span></span>

<span data-ttu-id="4c47d-121">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="4c47d-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c47d-122">A **Grade de Entrada de Hora** não é compatível com o comportamento de hora de **Somente Data**.</span><span class="sxs-lookup"><span data-stu-id="4c47d-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="4c47d-123">**Entrada de Hora** não está sendo atualizado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4c47d-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="4c47d-124">É necessária uma atualização manual.</span><span class="sxs-lookup"><span data-stu-id="4c47d-124">A manual refresh is required.</span></span>
- <span data-ttu-id="4c47d-125">Não ser possível importar as entradas de hora de uma atribuição quando houver um intervalo (0 horas) nas atribuições de um recurso.</span><span class="sxs-lookup"><span data-stu-id="4c47d-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="4c47d-126">Ao criar uma entrada de hora, defina o início como uma data igual a **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="4c47d-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="4c47d-127">Reabilite a edição em massa para entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="4c47d-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="4c47d-128">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="4c47d-128">**Resource Management**</span></span>

<span data-ttu-id="4c47d-129">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="4c47d-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c47d-130">Tentar atualizar o status de uma reserva entre dias sem um requisito gerará uma exceção de referência nula.</span><span class="sxs-lookup"><span data-stu-id="4c47d-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="4c47d-131">Erro ao carregar a **Exibição de Reconciliação**.</span><span class="sxs-lookup"><span data-stu-id="4c47d-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="4c47d-132">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="4c47d-132">**Project Management**</span></span>

<span data-ttu-id="4c47d-133">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="4c47d-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c47d-134">Na **Agenda do Projeto**, ao mudar de **Manual** para **Automático**, o salvamento automático não está sendo concluído.</span><span class="sxs-lookup"><span data-stu-id="4c47d-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="4c47d-135">Os custos de despesas não devem ser calculados em relação à variação na **Grade de Rastreamento de Projetos**.</span><span class="sxs-lookup"><span data-stu-id="4c47d-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="4c47d-136">Comportamento inconsistente para colunas da **marca Estimativas** durante o carregamento versus a alteração do tipo **Fase do Tempo**.</span><span class="sxs-lookup"><span data-stu-id="4c47d-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="4c47d-137">O custo real de um projeto pode não refletir os totais de **Dados Reais**.</span><span class="sxs-lookup"><span data-stu-id="4c47d-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="4c47d-138">**Data Estimada de Conclusão** na guia **Resumo** não corresponde à **Agenda da WBS**.</span><span class="sxs-lookup"><span data-stu-id="4c47d-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="4c47d-139">**Atualizar Horas Reais** no recuo à esquerda não funciona corretamente.</span><span class="sxs-lookup"><span data-stu-id="4c47d-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="4c47d-140">Um gerente de projeto fora da raiz **BU** não consegue criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="4c47d-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="4c47d-141">As alterações feitas na tarefa ou categoria em **Estimativas de Despesas** não são persistentes.</span><span class="sxs-lookup"><span data-stu-id="4c47d-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="4c47d-142">**Cópia do contrato** copia as agendas da fatura e o status de execução.</span><span class="sxs-lookup"><span data-stu-id="4c47d-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="4c47d-143">O botão **Atualizar Dados Reais** calcula incorretamente tarefas de resumo.</span><span class="sxs-lookup"><span data-stu-id="4c47d-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="4c47d-144">Suplemento do Microsoft Project: corrija o erro de referência nula se algum membro da equipe tiver uma unidade de recursos vazia.</span><span class="sxs-lookup"><span data-stu-id="4c47d-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]