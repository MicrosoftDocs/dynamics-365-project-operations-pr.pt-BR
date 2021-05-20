---
title: Novidades ou alterações na Versão de Atualização 31 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 31 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945521"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="b360b-103">Novidades ou alterações na Versão de Atualização 31 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="b360b-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b360b-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b360b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b360b-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="b360b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b360b-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b360b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b360b-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="b360b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b360b-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b360b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b360b-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 31.</span><span class="sxs-lookup"><span data-stu-id="b360b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="b360b-110">Esta versão apresenta o número de compilação V3.10.52.77 e está disponível para o público em geral por meio de uma atualização automática de maio de 2021.</span><span class="sxs-lookup"><span data-stu-id="b360b-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="b360b-111">Versão de Atualização 31</span><span class="sxs-lookup"><span data-stu-id="b360b-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b360b-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="b360b-112">Bug fixes</span></span>

<span data-ttu-id="b360b-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="b360b-113">**Time and Expense**</span></span>

<span data-ttu-id="b360b-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="b360b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b360b-115">Os botões de comando de controle de entrada de hora na página **Recurso Reservável** eram confusos.</span><span class="sxs-lookup"><span data-stu-id="b360b-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="b360b-116">Uma exceção de referência nula foi gerada em **Project.SetTrackingFields** ao aprovar uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="b360b-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="b360b-117">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="b360b-117">**Resource Management**</span></span>

<span data-ttu-id="b360b-118">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="b360b-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="b360b-119">**Criar Membro da Equipe** não exibe corretamente a configuração de metadados de configuração de reserva para **Status Comprometido de Reserva Padrão**.</span><span class="sxs-lookup"><span data-stu-id="b360b-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="b360b-120">Ao atualizar de PSA 1.X para 3.X, há falha no processo de atualização em **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="b360b-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="b360b-121">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="b360b-121">**Sales**</span></span>

<span data-ttu-id="b360b-122">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="b360b-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="b360b-123">A receita real converte os valores para a moeda do projeto na grade de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="b360b-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="b360b-124">O padrão da moeda não fica claro durante a criação de linhas do diário, linhas de cotação e linhas de contrato em cenários em que a moeda base de uma organização é diferente da moeda do projeto.</span><span class="sxs-lookup"><span data-stu-id="b360b-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="b360b-125">A consulta **Validação do diário de correção pendente** não filtra por projeto.</span><span class="sxs-lookup"><span data-stu-id="b360b-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="b360b-126">As vendas restantes são calculadas incorretamente em um projeto.</span><span class="sxs-lookup"><span data-stu-id="b360b-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="b360b-127">Há falha nas cotações baseadas em um contato quando são criadas sem uma lista de preços.</span><span class="sxs-lookup"><span data-stu-id="b360b-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="b360b-128">Nenhum controle giratório de processamento é exibido ao selecionar **Confirmar fatura**.</span><span class="sxs-lookup"><span data-stu-id="b360b-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="b360b-129">Nenhum controle giratório de processamento é exibido ao selecionar **Criar fatura**.</span><span class="sxs-lookup"><span data-stu-id="b360b-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="b360b-130">Fechar uma cotação como perdida não cancela as reservas.</span><span class="sxs-lookup"><span data-stu-id="b360b-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







