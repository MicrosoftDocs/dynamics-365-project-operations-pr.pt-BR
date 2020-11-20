---
title: Novidades ou alterações na Versão de Atualização 14 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 14 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124804"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="4958a-103">Versão de Atualização 14, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="4958a-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="4958a-104">Temos o orgulho de anunciar a versão mais recente do aplicativo Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="4958a-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="4958a-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="4958a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4958a-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4958a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4958a-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="4958a-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="4958a-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4958a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4958a-109">Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 14.</span><span class="sxs-lookup"><span data-stu-id="4958a-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="4958a-110">Esta versão possui um número de compilação da V3.10.4.21 e está disponível na seguinte agenda:</span><span class="sxs-lookup"><span data-stu-id="4958a-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="4958a-111">**Disponibilidade geral (atualização automática):** Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4958a-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="4958a-112">**Atualização automática:** Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4958a-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="4958a-113">Versão de Atualização 14</span><span class="sxs-lookup"><span data-stu-id="4958a-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="4958a-114">Aprimoramentos</span><span class="sxs-lookup"><span data-stu-id="4958a-114">Enhancements</span></span>

- <span data-ttu-id="4958a-115">Sales</span><span class="sxs-lookup"><span data-stu-id="4958a-115">Sales</span></span>

     - <span data-ttu-id="4958a-116">Os valores de campos personalizados de **Detalhes da Linha de Cotação** são copiados para **Detalhes da Linha de Contrato do Projeto** quando uma cotação é atualizada para **Fechada como ganha**.</span><span class="sxs-lookup"><span data-stu-id="4958a-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="4958a-117">Os projetos confirmados podem ser **Fechado como perdido**.</span><span class="sxs-lookup"><span data-stu-id="4958a-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="4958a-118">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="4958a-118">Resource Management</span></span>

     - <span data-ttu-id="4958a-119">Ao estender as reservas, os usuários visualizarão uma caixa de diálogo de confirmação para resumir os resultados da reserva e fornecer um link para Manter reservas.</span><span class="sxs-lookup"><span data-stu-id="4958a-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="4958a-120">Correções de bugs</span><span class="sxs-lookup"><span data-stu-id="4958a-120">Bug fixes</span></span>

- <span data-ttu-id="4958a-121">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="4958a-121">Time and Expense</span></span>

     - <span data-ttu-id="4958a-122">Corrigido: Melhorou a experiência do usuário quando este não selecionava entradas a serem corrigidas.</span><span class="sxs-lookup"><span data-stu-id="4958a-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="4958a-123">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="4958a-123">Resource Management</span></span>

     - <span data-ttu-id="4958a-124">Corrigido: Reservar um recurso múltiplas vezes excede o nome do recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="4958a-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="4958a-125">Sales</span><span class="sxs-lookup"><span data-stu-id="4958a-125">Sales</span></span>

     - <span data-ttu-id="4958a-126">Corrigido: O preço de venda total não é calculado até que o usuário também insira um preço de custo para estimativas de despesas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="4958a-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="4958a-127">Corrigido: Fechar uma cotação como **Ganha** gera uma falha se o contrato do projeto associado não estiver em um estado de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="4958a-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

