---
title: Novidades ou alterações na Versão de Atualização 29 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 29 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664629"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="dcbc8-103">Novidades ou alterações na Versão de Atualização 29 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="dcbc8-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dcbc8-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="dcbc8-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="dcbc8-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dcbc8-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="dcbc8-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dcbc8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dcbc8-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 29.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="dcbc8-110">Esta versão tem um número de compilação de V3.10.47.7 e está geralmente disponível por meio de uma atualização automática em fevereiro de 2021.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="dcbc8-111">Versão de Atualização 29</span><span class="sxs-lookup"><span data-stu-id="dcbc8-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dcbc8-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="dcbc8-112">Bug fixes</span></span>

<span data-ttu-id="dcbc8-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="dcbc8-113">**Time and Expense**</span></span>

<span data-ttu-id="dcbc8-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="dcbc8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="dcbc8-115">Os usuários não podem ver as horas de trabalho registradas em dias não úteis na grade de entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="dcbc8-116">As entradas de despesas aprovadas podem ser editadas na grade.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="dcbc8-117">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="dcbc8-117">**Project Management**</span></span>

<span data-ttu-id="dcbc8-118">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="dcbc8-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="dcbc8-119">Lógica de validação ausente para garantir que as horas de esforço de atribuição de recursos não possam ser negativas.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="dcbc8-120">A ação personalizada **AssignResourcesForTask** atualiza todos os campos em vez de somente os campos alterados.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="dcbc8-121">Ao copiar um projeto em um ambiente com plug-ins ou fluxos de trabalho que estão registrados no evento **CreateProject**, o atributo **msdyn_bulkgenerationstatus** não é atualizado se houver falha em **CopyWBSToProject**.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="dcbc8-122">Ao expandir o calendário do projeto, os dias úteis não são classificados em ordem ascendente, gerando falha em algumas atualizações de tarefa do projeto.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="dcbc8-123">Alterar o Gerente de Projeto em um projeto existente aciona a lógica de uso padrão da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="dcbc8-124">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="dcbc8-124">**Sales**</span></span>

<span data-ttu-id="dcbc8-125">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="dcbc8-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="dcbc8-126">A guia **Desempenho do Contrato** na página **Contrato** falha silenciosamente durante a inicialização quando não houver linhas de contrato presentes.</span><span class="sxs-lookup"><span data-stu-id="dcbc8-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
