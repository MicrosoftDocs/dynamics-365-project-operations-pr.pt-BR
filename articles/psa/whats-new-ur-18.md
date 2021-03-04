---
title: Novidades ou alterações na Versão de Atualização 18 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 18 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147189"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="23962-103">Versão de Atualização 18, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="23962-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="23962-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="23962-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="23962-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="23962-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="23962-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="23962-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="23962-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="23962-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="23962-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="23962-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="23962-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 18.</span><span class="sxs-lookup"><span data-stu-id="23962-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="23962-110">Esta versão apresenta o número de build V3.10.8.12 e geralmente está disponível por meio de uma atualização automática de abril de 2020.</span><span class="sxs-lookup"><span data-stu-id="23962-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="23962-111">Versão de Atualização 18</span><span class="sxs-lookup"><span data-stu-id="23962-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="23962-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="23962-112">Bug fixes</span></span>

<span data-ttu-id="23962-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="23962-113">**Time and Expense**</span></span>

- <span data-ttu-id="23962-114">Corrigido: os fluxos **Recuperar**, **Solicitar** e **Cancelar Aprovação** lançam exceções com mensagens de erro pouco claras.</span><span class="sxs-lookup"><span data-stu-id="23962-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="23962-115">Corrigido: quando **Cancelar Aprovação** falha em uma despesa, um erro de exceção relevante não é lançado.</span><span class="sxs-lookup"><span data-stu-id="23962-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="23962-116">Corrigido: a grade de Entrada de Horário trata incorretamente os dias não úteis na Austrália após a troca do horário de verão (DST) em outubro.</span><span class="sxs-lookup"><span data-stu-id="23962-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="23962-117">Corrigido: a lógica padrão incorreta impede o envio de despesas.</span><span class="sxs-lookup"><span data-stu-id="23962-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="23962-118">Corrigido: quando ocorre falha na aprovação de entrada de horário, a aprovação permanece em estado **Pendente**.</span><span class="sxs-lookup"><span data-stu-id="23962-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="23962-119">Corrigido: erros de SQL em aprovações em massa (deadlock/tempo limite).</span><span class="sxs-lookup"><span data-stu-id="23962-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="23962-120">Corrigido: problemas significativos de desempenho na experiência do usuário causados pela atualização de membros da equipe ao aprovar entradas de horário.</span><span class="sxs-lookup"><span data-stu-id="23962-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="23962-121">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="23962-121">**Project Management**</span></span>

- <span data-ttu-id="23962-122">Corrigido: notificação de fuso horário movida da exibição **Reconciliação** para o formulário principal **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="23962-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="23962-123">Corrigido: o modelo de calendário não está sendo padronizado corretamente quando um novo formulário de projeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="23962-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="23962-124">Corrigido: para navegadores baseados em cromo, os usuários não conseguem selecionar facilmente as tarefas anteriores a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="23962-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="23962-125">Corrigido: criar ou copiar **Projeto do Modelo Vazio** busca atribuições não relacionadas.</span><span class="sxs-lookup"><span data-stu-id="23962-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="23962-126">Corrigido: em casos de externos específicos, a criação de uma nova atribuição a partir da grade de tarefas resulta na criação de registros duplicados.</span><span class="sxs-lookup"><span data-stu-id="23962-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="23962-127">Corrigido: no modo manual, os usuários não conseguem atualizar as datas de início da tarefa para serem posteriores à data atual salva.</span><span class="sxs-lookup"><span data-stu-id="23962-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="23962-128">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="23962-128">**Resource Management**</span></span>

- <span data-ttu-id="23962-129">Corrigido: a linha do subtotal da exibição **Reconciliação** calcula incorretamente a variação das reservas após estender as reservas.</span><span class="sxs-lookup"><span data-stu-id="23962-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="23962-130">Corrigido: a exibição **Reconciliação** mostra incorretamente as atribuições de recurso quando o recurso que pode ser reservado tem um calendário que não corresponde ao calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="23962-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="23962-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="23962-131">**Sales**</span></span>

- <span data-ttu-id="23962-132">Corrigido: quando as entradas de horário são aprovadas novamente (**Aprovar > Cancelar >** aprovar novamente), uma duplicata real não cobrável é criada.</span><span class="sxs-lookup"><span data-stu-id="23962-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
