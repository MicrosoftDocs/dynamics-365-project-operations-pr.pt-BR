---
title: Novidades ou alterações na Versão de Atualização 23 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 23 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131104"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="2ce94-103">Versão de Atualização 23, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="2ce94-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="2ce94-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2ce94-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2ce94-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="2ce94-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2ce94-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2ce94-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2ce94-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="2ce94-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2ce94-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2ce94-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2ce94-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 23.</span><span class="sxs-lookup"><span data-stu-id="2ce94-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="2ce94-110">Esta versão tem um número de build V 3.10.34.30 e foi disponibilizada para o público em geral por meio de uma atualização automática em agosto de 2020.</span><span class="sxs-lookup"><span data-stu-id="2ce94-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="2ce94-111">Versão de Atualização 23</span><span class="sxs-lookup"><span data-stu-id="2ce94-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2ce94-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="2ce94-112">Bug fixes</span></span>

<span data-ttu-id="2ce94-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="2ce94-113">**Time and Expense**</span></span>

<span data-ttu-id="2ce94-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="2ce94-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="2ce94-115">Lide com um caso de borda em **Exclusão de Membro da Equipe de Projeto** para fornecer uma exceção significativa.</span><span class="sxs-lookup"><span data-stu-id="2ce94-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="2ce94-116">A importação de atribuição resulta em uma tela de remoção em branco.</span><span class="sxs-lookup"><span data-stu-id="2ce94-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="2ce94-117">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="2ce94-117">**Resource Management**</span></span>

<span data-ttu-id="2ce94-118">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="2ce94-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="2ce94-119">O **Cartão de recursos da grade de utilização de recursos** mostra dados incorretos quando a escala de tempo é superior a cinco dias.</span><span class="sxs-lookup"><span data-stu-id="2ce94-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="2ce94-120">Quando os clientes criam um recurso reservável, o plug-in falha de forma intermitente ao adicionar automaticamente o recurso a um grupo do Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="2ce94-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="2ce94-121">A exibição **Reconciliação** mostra os contornos manuais incorretamente na exibição **Semana** ou **Mês**.</span><span class="sxs-lookup"><span data-stu-id="2ce94-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="2ce94-122">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="2ce94-122">**Project Management**</span></span>

<span data-ttu-id="2ce94-123">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="2ce94-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="2ce94-124">Um número excessivo de entidades **RetrieveMultiple para usersettings** estão causando degradação do desempenho para aprovações de projetos e outras operações.</span><span class="sxs-lookup"><span data-stu-id="2ce94-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="2ce94-125">A pesquisa de recursos de grade **Planejamento de Tarefas** limita-se a mostrar apenas até cinco membros da equipe de projeto.</span><span class="sxs-lookup"><span data-stu-id="2ce94-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="2ce94-126">A pesquisa de recursos de grade **Planejamento de Tarefas** não filtra recursos inativos.</span><span class="sxs-lookup"><span data-stu-id="2ce94-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="2ce94-127">O modo manual não está funcionando como esperado na estrutura de detalhamento de trabalho do planejamento de projeto.</span><span class="sxs-lookup"><span data-stu-id="2ce94-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="2ce94-128">A grade **Planejamento de Tarefas** mostra **Categorias de Transações Inativas**.</span><span class="sxs-lookup"><span data-stu-id="2ce94-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="2ce94-129">A grade **Atribuição de Recursos** é arredondada incorretamente quando uma tarefa tem várias atribuições.</span><span class="sxs-lookup"><span data-stu-id="2ce94-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="2ce94-130">Os valores de arredondamento são diferentes entre o custo planejado e o custo real para uma única tarefa.</span><span class="sxs-lookup"><span data-stu-id="2ce94-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="2ce94-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2ce94-131">**Sales**</span></span>

<span data-ttu-id="2ce94-132">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="2ce94-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="2ce94-133">Dar um clique duplo em **Obter Todas as Categorias de Transação** cria várias linhas.</span><span class="sxs-lookup"><span data-stu-id="2ce94-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
