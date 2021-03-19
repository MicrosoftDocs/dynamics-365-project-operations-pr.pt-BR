---
title: Sincronizar capacidade do recurso
description: Este tópico fornece informações sobre como sincronizar a capacidade de um recurso entre calendários e projetos.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288545"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="72d0a-103">Sincronizar capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="72d0a-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72d0a-104">Os processos de sincronização de recursos ajudam a garantir que as informações do calendário e do calendário base se encaixem no agendamento de recursos do projeto.</span><span class="sxs-lookup"><span data-stu-id="72d0a-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="72d0a-105">Se o calendário for alterado, os processos farão as atualizações necessárias no agendamento dos recursos do projeto.</span><span class="sxs-lookup"><span data-stu-id="72d0a-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="72d0a-106">Os processos também ajudam a melhorar o desempenho, porque as informações dos recursos do calendário são sincronizadas com antecedência.</span><span class="sxs-lookup"><span data-stu-id="72d0a-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="72d0a-107">Portanto, as atualizações nas informações de agendamento de recursos ocorrem mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="72d0a-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="72d0a-108">Recomendamos que você agende os processos em lote, em vez de um de cada vez.</span><span class="sxs-lookup"><span data-stu-id="72d0a-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="72d0a-109">Caso contrário, existe o risco de alguém se esquecer das datas inclusivas da última sincronização das informações.</span><span class="sxs-lookup"><span data-stu-id="72d0a-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="72d0a-110">Se não forem usadas datas inclusivas, podem ocorrer lacunas durante a sincronização de datas.</span><span class="sxs-lookup"><span data-stu-id="72d0a-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sincronização de calendário](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="72d0a-112">Sincronizar acúmulos de capacidade dos recursos</span><span class="sxs-lookup"><span data-stu-id="72d0a-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="72d0a-113">O processo de sincronização foi projetado para sincronizar todas as informações do calendário de recursos.</span><span class="sxs-lookup"><span data-stu-id="72d0a-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="72d0a-114">Essas informações incluem informações básicas do calendário sobre quaisquer alterações na tabela de capacidade do calendário de recursos do projeto.</span><span class="sxs-lookup"><span data-stu-id="72d0a-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="72d0a-115">Se novos recursos forem adicionados ao projeto, a sincronização ajudará a garantir que as informações atualizadas do calendário estejam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="72d0a-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="72d0a-116">Essa sincronização pode ser feita a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="72d0a-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="72d0a-117">É recomendável usar atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="72d0a-117">We recommend that you use a batch.</span></span> <span data-ttu-id="72d0a-118">As opções estão disponíveis durante a sincronização das reservas de capacidade.</span><span class="sxs-lookup"><span data-stu-id="72d0a-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="72d0a-119">Selecione **Gerenciamento e contabilidade de projeto** &gt; **Periódico** &gt; **Sincronização de capacidade** &gt; **Sincronizar acúmulos de capacidade de recursos**.</span><span class="sxs-lookup"><span data-stu-id="72d0a-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="72d0a-120">Defina as opções na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="72d0a-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="72d0a-121">Opção</span><span class="sxs-lookup"><span data-stu-id="72d0a-121">Option</span></span>      | <span data-ttu-id="72d0a-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="72d0a-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="72d0a-123">Código de período</span><span class="sxs-lookup"><span data-stu-id="72d0a-123">Period code</span></span> | <span data-ttu-id="72d0a-124">Opcionalmente, selecione o código de intervalo de datas do razão geral para definir as datas de início e de término do processo de sincronização para os acúmulos de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="72d0a-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="72d0a-125">Data de Início</span><span class="sxs-lookup"><span data-stu-id="72d0a-125">Start date</span></span>  | <span data-ttu-id="72d0a-126">Insira a data de início do processo de sincronização para os acúmulos de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="72d0a-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="72d0a-127">Data de término</span><span class="sxs-lookup"><span data-stu-id="72d0a-127">End date</span></span>    | <span data-ttu-id="72d0a-128">Insira a data de término do processo de sincronização para os acúmulos de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="72d0a-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="72d0a-129">[![Processo de sincronização](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="72d0a-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]