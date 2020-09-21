---
title: Novidades na Versão de Atualização 14 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 14 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749073"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="e524b-103">Novidades na Versão de Atualização 14 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="e524b-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="e524b-104">Temos o orgulho de anunciar a versão mais recente do aplicativo do Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e524b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e524b-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="e524b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e524b-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e524b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e524b-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="e524b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e524b-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e524b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e524b-109">Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 14.</span><span class="sxs-lookup"><span data-stu-id="e524b-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="e524b-110">Esta versão possui um número de compilação da V3.10.4.21 e está disponível na seguinte agenda:</span><span class="sxs-lookup"><span data-stu-id="e524b-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="e524b-111">**Disponibilidade geral (atualização automática):** Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e524b-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="e524b-112">**Atualização automática:** Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e524b-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="e524b-113">Versão de Atualização 14</span><span class="sxs-lookup"><span data-stu-id="e524b-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="e524b-114">Aprimoramentos</span><span class="sxs-lookup"><span data-stu-id="e524b-114">Enhancements</span></span>

- <span data-ttu-id="e524b-115">Sales</span><span class="sxs-lookup"><span data-stu-id="e524b-115">Sales</span></span>

     - <span data-ttu-id="e524b-116">Os valores de campos personalizados de **Detalhes da Linha de Cotação** são copiados para **Detalhes da Linha de Contrato do Projeto** quando uma cotação é atualizada para **Fechada como ganha**.</span><span class="sxs-lookup"><span data-stu-id="e524b-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="e524b-117">Os projetos confirmados podem ser **Fechado como perdido**.</span><span class="sxs-lookup"><span data-stu-id="e524b-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="e524b-118">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="e524b-118">Resource Management</span></span>

     - <span data-ttu-id="e524b-119">Ao estender as reservas, os usuários visualizarão uma caixa de diálogo de confirmação para resumir os resultados da reserva e fornecer um link para Manter reservas.</span><span class="sxs-lookup"><span data-stu-id="e524b-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="e524b-120">Correções de bugs</span><span class="sxs-lookup"><span data-stu-id="e524b-120">Bug fixes</span></span>

- <span data-ttu-id="e524b-121">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="e524b-121">Time and Expense</span></span>

     - <span data-ttu-id="e524b-122">Corrigido: Melhorou a experiência do usuário quando este não selecionava entradas a serem corrigidas.</span><span class="sxs-lookup"><span data-stu-id="e524b-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="e524b-123">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="e524b-123">Resource Management</span></span>

     - <span data-ttu-id="e524b-124">Corrigido: Reservar um recurso múltiplas vezes excede o nome do recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="e524b-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="e524b-125">Sales</span><span class="sxs-lookup"><span data-stu-id="e524b-125">Sales</span></span>

     - <span data-ttu-id="e524b-126">Corrigido: O preço de venda total não é calculado até que o usuário também insira um preço de custo para estimativas de despesas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="e524b-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="e524b-127">Corrigido: Fechar uma cotação como **Ganha** gera uma falha se o contrato do projeto associado não estiver em um estado de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="e524b-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

