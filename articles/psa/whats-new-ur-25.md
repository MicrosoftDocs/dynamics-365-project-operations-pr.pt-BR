---
title: Novidades ou alterações na Versão de Atualização 25 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 25 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 92dd74378457cf877e8ec26eb85a7883dda97d51
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000197"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="c08a1-103">Novidades ou alterações na Versão de Atualização 25 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="c08a1-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c08a1-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c08a1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c08a1-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="c08a1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c08a1-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c08a1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c08a1-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="c08a1-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c08a1-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c08a1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c08a1-109">Este tópico lista os recursos e correções novos ou alterados para Project Service Automation V3, Versão de Atualização 25. Esta versão tem um número de compilação de V 3.10.43.76 e está geralmente disponível por meio de uma atualização automática em outubro de 2020.</span><span class="sxs-lookup"><span data-stu-id="c08a1-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="c08a1-110">Versão de Atualização 25</span><span class="sxs-lookup"><span data-stu-id="c08a1-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c08a1-111">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="c08a1-111">Bug fixes</span></span>

<span data-ttu-id="c08a1-112">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="c08a1-112">**Time and Expense**</span></span>

<span data-ttu-id="c08a1-113">O seguinte problema foi corrigido:</span><span class="sxs-lookup"><span data-stu-id="c08a1-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="c08a1-114">O gráfico de entrada de tempo mostrando dados adicionais baseados em um intervalo muito grande sendo recuperado.</span><span class="sxs-lookup"><span data-stu-id="c08a1-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="c08a1-115">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="c08a1-115">**Resource Management**</span></span>

<span data-ttu-id="c08a1-116">O seguinte problema foi corrigido:</span><span class="sxs-lookup"><span data-stu-id="c08a1-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="c08a1-117">Código do package deployer adicionado para ignorar a importação de patch do Universal Resource Scheduling caso já exista um patch de versão superior.</span><span class="sxs-lookup"><span data-stu-id="c08a1-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="c08a1-118">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="c08a1-118">**Project Management**</span></span>

<span data-ttu-id="c08a1-119">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="c08a1-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="c08a1-120">Arredondamento corrigido e discrepâncias da taxa de câmbio resultando em custo planejado incorreto na grade de rastreamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="c08a1-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="c08a1-121">Compatível com a exibição de duas ou mais grades de reação no formulário do **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="c08a1-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="c08a1-122">Validação fornecida para abordar a capacidade de atribuir uma tarefa após a data de término do calendário, resultando na falha de atribuição de recursos.</span><span class="sxs-lookup"><span data-stu-id="c08a1-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="c08a1-123">Melhoria no tratamento de erros para abordar a Exceção de Referência Nula gerada a partir do seguinte:</span><span class="sxs-lookup"><span data-stu-id="c08a1-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="c08a1-124">Plug-in **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="c08a1-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="c08a1-125">**PreValidateProjectTaskCreate** quando uma tarefa de projeto é criada sem um projeto associado</span><span class="sxs-lookup"><span data-stu-id="c08a1-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="c08a1-126">Plug-in **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="c08a1-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="c08a1-127">Plug-in **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="c08a1-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="c08a1-128">Plug-in **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="c08a1-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="c08a1-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c08a1-129">**Sales**</span></span>

<span data-ttu-id="c08a1-130">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="c08a1-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="c08a1-131">Melhoria do tratamento de erros para abordar as Exceções de Referência Nula geradas de **Copiar Projeto: Gerenciamento de Estimativas do HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="c08a1-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="c08a1-132">**Não pronto para faturamento** em um **Registro Acumulado de Hora e Material** não limpa o status de cobrança.</span><span class="sxs-lookup"><span data-stu-id="c08a1-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="c08a1-133">Correção dos botões **Preços** incorretamente rotulados na guia **Preço da Função** e **Itens de Catálogo**.</span><span class="sxs-lookup"><span data-stu-id="c08a1-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]