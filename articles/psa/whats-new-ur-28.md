---
title: Novidades ou alterações na Versão de Atualização 28 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 28 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280204"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="f1bb0-103">Novidades ou alterações na Versão de Atualização 28 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="f1bb0-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f1bb0-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f1bb0-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f1bb0-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f1bb0-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f1bb0-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f1bb0-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f1bb0-109">Este tópico lista os recursos e correções novos ou alterados para o Project Service Automation V3, versão de atualização 28 Esta versão tem um número de compilação de V 3.10.46.32 e está geralmente disponível por meio de uma atualização automática em janeiro de 2021.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="f1bb0-110">Versão de Atualização 28</span><span class="sxs-lookup"><span data-stu-id="f1bb0-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f1bb0-111">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="f1bb0-111">Bug fixes</span></span>

<span data-ttu-id="f1bb0-112">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="f1bb0-112">**Time and Expense**</span></span>

<span data-ttu-id="f1bb0-113">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="f1bb0-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="f1bb0-114">Os usuários podem usar **Edição em massa** para atualizar as entradas de tempo que foram aprovadas e enviadas.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="f1bb0-115">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="f1bb0-115">**Project Management**</span></span>

<span data-ttu-id="f1bb0-116">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="f1bb0-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="f1bb0-117">Nos casos em que o GUID da tarefa é interpretado como um número, as tarefas não podem ser abertas para edição usando **Editar Tarefa** na faixa de opções na página **Estrutura de detalhamento de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="f1bb0-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f1bb0-118">**Sales**</span></span>

<span data-ttu-id="f1bb0-119">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="f1bb0-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="f1bb0-120">Uma exceção de referência nula é gerada quando o plug-in **GetEstimatesForProject** é chamado.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="f1bb0-121">**Marcar como pronto para faturar** na grade de marcos atualiza apenas parcialmente os atributos, exceto para o atributo **InvoiceStatus**, que é atualizado.</span><span class="sxs-lookup"><span data-stu-id="f1bb0-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]