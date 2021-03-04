---
title: Novidades ou alterações na Versão de Atualização 26 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 26 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143544"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="81f32-103">Versão de Atualização 26, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="81f32-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="81f32-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="81f32-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="81f32-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="81f32-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="81f32-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="81f32-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="81f32-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="81f32-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="81f32-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="81f32-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="81f32-109">Este tópico lista os recursos e as correções novas ou alteradas do Project Service Automation Versão de Atualização 26, V3.</span><span class="sxs-lookup"><span data-stu-id="81f32-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="81f32-110">Esta versão tem um número de compilação de V3.10.44.59 e está geralmente disponível por meio de uma atualização automática em dezembro de 2020.</span><span class="sxs-lookup"><span data-stu-id="81f32-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="81f32-111">Versão de Atualização 26</span><span class="sxs-lookup"><span data-stu-id="81f32-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="81f32-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="81f32-112">Bug fixes</span></span>

<span data-ttu-id="81f32-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="81f32-113">**Time and Expense**</span></span>

<span data-ttu-id="81f32-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="81f32-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="81f32-115">Os usuários podem alterar a tarefa em uma entrada de hora que foi aprovada/enviada.</span><span class="sxs-lookup"><span data-stu-id="81f32-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="81f32-116">Erro "Referência do Objeto não Definida" ao salvar a entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="81f32-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="81f32-117">A importação de entradas de horas de atribuições de recursos cria entradas de hora com os valores DateTime incorretos.</span><span class="sxs-lookup"><span data-stu-id="81f32-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="81f32-118">Quando o Project Service Automation e o aplicativo Field Service estão instalados, o botão **Novo** é exibido duas vezes na barra de comandos para entradas de hora no aplicativo Field Service.</span><span class="sxs-lookup"><span data-stu-id="81f32-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="81f32-119">As células **Permitir Unidade** e **Grupo de unidades** atualizam agora o trabalho na grade **Estimativas de Despesas**.</span><span class="sxs-lookup"><span data-stu-id="81f32-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="81f32-120">O formulário **Atualizar Edição de Entrada de Hora** inclui **Linha do tempo**.</span><span class="sxs-lookup"><span data-stu-id="81f32-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="81f32-121">A aprovação de tempo para entradas de hora que não são do projeto bloqueia o sistema ao pesquisar uma função de aprovador de projeto.</span><span class="sxs-lookup"><span data-stu-id="81f32-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="81f32-122">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="81f32-122">**Resource Management**</span></span>

<span data-ttu-id="81f32-123">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="81f32-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="81f32-124">Validação adicionada no plug-in **PostProjectCreate** para verificar um requisito principal antes de criar um.</span><span class="sxs-lookup"><span data-stu-id="81f32-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="81f32-125">O formulário de criação rápida de **Membro da Equipe do Projeto** lançará uma exceção de referência nula se campos forem removidos do formulário.</span><span class="sxs-lookup"><span data-stu-id="81f32-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="81f32-126">A geração de requisitos para 12 horas em 1 ano falhará.</span><span class="sxs-lookup"><span data-stu-id="81f32-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="81f32-127">Exceção de referência nula de mensagem de erro aprimorada durante a criação do requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="81f32-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="81f32-128">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="81f32-128">**Project Management**</span></span>

<span data-ttu-id="81f32-129">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="81f32-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="81f32-130">Validação aprimorada para abordar a exceção de referência nula gerada no plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="81f32-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="81f32-131">Os projetos publicados pelo suplemento da área de trabalho do Microsoft Project excluem atribuições não atribuídas.</span><span class="sxs-lookup"><span data-stu-id="81f32-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="81f32-132">Nova validação adicionada quando a referência de projeto de uma tarefa é inválida devido à exceção de referência nula no plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="81f32-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="81f32-133">A grade Membro da Equipe não mostra atribuições distintas no registro do membro da equipe.</span><span class="sxs-lookup"><span data-stu-id="81f32-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="81f32-134">Novas mensagens de validação e de erro adicionadas devido à exceção de referência nula no plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="81f32-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="81f32-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="81f32-135">**Sales**</span></span>

<span data-ttu-id="81f32-136">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="81f32-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="81f32-137">Ao selecionar uma linha baseada em projeto na cotação ou contrato, o botão **Sugestão** só deve estar visível ao selecionar uma linha baseada em produto associada a um produto existente.</span><span class="sxs-lookup"><span data-stu-id="81f32-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="81f32-138">Divida privilégio **Create_Product** de privilégio **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="81f32-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="81f32-139">Excluir uma linha de fatura causa falha de referência nula em **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="81f32-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
