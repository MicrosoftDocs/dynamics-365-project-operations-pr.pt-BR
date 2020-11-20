---
title: Novidades ou alterações na Versão de Atualização 15 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 15 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 2112e70d7359e7f30725ef3069a18570da651c06
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119899"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="455a8-103">Versão de Atualização 15, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="455a8-103">Project Service Automation Update Release 15, V3</span></span>

<span data-ttu-id="455a8-104">Temos o orgulho de anunciar a versão mais recente do aplicativo Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="455a8-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="455a8-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="455a8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="455a8-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="455a8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="455a8-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="455a8-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="455a8-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="455a8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="455a8-109">Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 15.</span><span class="sxs-lookup"><span data-stu-id="455a8-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="455a8-110">Esta versão tem um número de compilação de V3.10.5.28 e está geralmente disponível por meio de uma atualização automática em janeiro de 2020.</span><span class="sxs-lookup"><span data-stu-id="455a8-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="455a8-111">Versão de Atualização 15</span><span class="sxs-lookup"><span data-stu-id="455a8-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="455a8-112">Aprimoramentos</span><span class="sxs-lookup"><span data-stu-id="455a8-112">Enhancements</span></span>

- <span data-ttu-id="455a8-113">Gerenciamento de projetos</span><span class="sxs-lookup"><span data-stu-id="455a8-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="455a8-114">Correções de bugs</span><span class="sxs-lookup"><span data-stu-id="455a8-114">Bug fixes</span></span>

- <span data-ttu-id="455a8-115">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="455a8-115">Time and Expense</span></span>

  - <span data-ttu-id="455a8-116">Corrigido: Tratamento de erro de carregamento de complementos na exibição de reconciliação.</span><span class="sxs-lookup"><span data-stu-id="455a8-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="455a8-117">Corrigido: Hub de Recursos do Projeto: Renomear **Valor** para evitar ambiguidade.</span><span class="sxs-lookup"><span data-stu-id="455a8-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="455a8-118">Corrigido: Ajustar a exibição **Copiar Colunas de Entrada de Hora** para incluir o tipo.</span><span class="sxs-lookup"><span data-stu-id="455a8-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="455a8-119">Corrigido: Editar a duração da entrada de hora na exibição em grade usando números decimais resulta em erro desconhecido para alguns números.</span><span class="sxs-lookup"><span data-stu-id="455a8-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="455a8-120">Gerenciamento de projetos</span><span class="sxs-lookup"><span data-stu-id="455a8-120">Project Management</span></span>

  - <span data-ttu-id="455a8-121">Corrigido: O menu suspenso para **Usar na Exibição de Rastreamento** agora expande com base na largura das opções.</span><span class="sxs-lookup"><span data-stu-id="455a8-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="455a8-122">Corrigido: Ao gerenciar projetos no fuso horário +13, os cálculos das tarefas podem exibir resultados imprecisos.</span><span class="sxs-lookup"><span data-stu-id="455a8-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="455a8-123">Corrigido: **Horário de Término do Membro da Equipe** foi corrigido ao usar um calendário de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="455a8-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="455a8-124">Corrigido: **BPF** reativado no formulário principal **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="455a8-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="455a8-125">Corrigido: O cálculo das atribuições não ignoram mais um dia.</span><span class="sxs-lookup"><span data-stu-id="455a8-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="455a8-126">Corrigido: Um novo banner de notificações foi adicionado ao formulário do projeto quando o fuso horário difere entre usuário e projeto.</span><span class="sxs-lookup"><span data-stu-id="455a8-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="455a8-127">Sales</span><span class="sxs-lookup"><span data-stu-id="455a8-127">Sales</span></span>

  - <span data-ttu-id="455a8-128">Corrigido: A pesquisa de categoria de estimativa de despesas pode ser usada para filtrar duplicatas.</span><span class="sxs-lookup"><span data-stu-id="455a8-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="455a8-129">Corrigido: O código em **PluginDomain.ExecuteInTryCatchBlock(..)** não oculta mais a origem da exceção.</span><span class="sxs-lookup"><span data-stu-id="455a8-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="455a8-130">Corrigido: Não é mais exibida uma mensagem de erro em **Pesquisa de projeto** no formulário **Linha da cotação** quando há mais de 1000 projetos.</span><span class="sxs-lookup"><span data-stu-id="455a8-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="455a8-131">Corrigido: A grade **Estimativas** para estimativas de mão-de-obra e de despesas agora exibe o símbolo correto da moeda.</span><span class="sxs-lookup"><span data-stu-id="455a8-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="455a8-132">Corrigido: Depois que uma organização atualiza o PSA da Versão de Atualização 14 para a Versão de Atualização 15, a guia **Agendar** não aparece mais em branco no formulário **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="455a8-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
