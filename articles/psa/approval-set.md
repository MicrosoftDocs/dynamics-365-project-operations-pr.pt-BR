---
title: Conjuntos de aprovações
description: Este tópico fornece informações sobre conjunto de aprovações, solicitações e subconjuntos dessas operações.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116857"
---
# <a name="approval-sets"></a><span data-ttu-id="65d8b-103">Conjuntos de aprovações</span><span class="sxs-lookup"><span data-stu-id="65d8b-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="65d8b-104">A aprovação define as solicitações de aprovação do grupo em subconjuntos menores de operações.</span><span class="sxs-lookup"><span data-stu-id="65d8b-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="65d8b-105">Esse agrupamento permite que as aprovações sejam processadas em ordem por Projeto e permite novas tentativas e sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="65d8b-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="65d8b-106">O agrupamento melhora a confiabilidade e rastreabilidade do processamento de aprovação para grandes volumes de aprovações.</span><span class="sxs-lookup"><span data-stu-id="65d8b-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="65d8b-107">Os conjuntos de aprovação indicam o estado geral de processamento de seus registros relacionados.</span><span class="sxs-lookup"><span data-stu-id="65d8b-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="65d8b-108">Quando um registro de aprovação é processado usando um conjunto de aprovação, o registro passa de **Enviado** para **Aprovado**, e é desvinculado do conjunto de aprovação.</span><span class="sxs-lookup"><span data-stu-id="65d8b-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="65d8b-109">Se um registro falhar quando for enviado para aprovação, o registro permanecerá em um status de **Enviado** e o conjunto de aprovações é marcado como reprovado.</span><span class="sxs-lookup"><span data-stu-id="65d8b-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="65d8b-110">O conjunto de aprovações registra a mensagem de erro da falha.</span><span class="sxs-lookup"><span data-stu-id="65d8b-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="65d8b-111">Processando aprovações e conjuntos de aprovação</span><span class="sxs-lookup"><span data-stu-id="65d8b-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="65d8b-112">As aprovações que estão na fila para processamento são visíveis na exibição **Processando Aprovações**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="65d8b-113">O sistema tenta processar todas as entradas várias vezes de forma assíncrona, incluindo uma nova tentativa de aprovação, se as tentativas anteriores falharem.</span><span class="sxs-lookup"><span data-stu-id="65d8b-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="65d8b-114">O campo **Tempo de Vida do Conjunto de Aprovações** registra o número de tentativas restantes para processar o conjunto antes de ser marcado como falha.</span><span class="sxs-lookup"><span data-stu-id="65d8b-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="65d8b-115">Aprovações e conjuntos de aprovações com falha</span><span class="sxs-lookup"><span data-stu-id="65d8b-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="65d8b-116">A exibição **Aprovações Reprovadas** lista todas as aprovações que requerem intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="65d8b-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="65d8b-117">Abra os logs do conjunto de aprovações associados para identificar a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="65d8b-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="65d8b-118">Selecionar **Tentar novamente** adiciona à contagem de tempo de vida do conjunto de aprovação, move o conjunto de aprovação de volta para um status de **Em processamento** e tenta processar os registros restantes.</span><span class="sxs-lookup"><span data-stu-id="65d8b-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="65d8b-119">Configurar conjuntos de aprovação</span><span class="sxs-lookup"><span data-stu-id="65d8b-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="65d8b-120">Habilite o recurso de conjuntos de Aprovação</span><span class="sxs-lookup"><span data-stu-id="65d8b-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="65d8b-121">Antes de ativar o recurso Conjuntos de aprovações, verifique se não há aprovações sendo processadas atualmente.</span><span class="sxs-lookup"><span data-stu-id="65d8b-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="65d8b-122">Vá para a página **Parâmetros do projeto** e selecione **Controle de Recursos** > **Habilitar Aprovações Modernas**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="65d8b-123">Desativar o recurso de conjuntos de Aprovação</span><span class="sxs-lookup"><span data-stu-id="65d8b-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="65d8b-124">Antes de desativar o recurso Conjuntos de aprovações, verifique se não há aprovações sendo processadas atualmente.</span><span class="sxs-lookup"><span data-stu-id="65d8b-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="65d8b-125">Vá para a página **Parâmetros do Projeto** e selecione **Controle de Recursos** > **Desativar Aprovações Modernas**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="65d8b-126">Configurando o limite assíncrono</span><span class="sxs-lookup"><span data-stu-id="65d8b-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="65d8b-127">Quando os conjuntos de aprovação são criados, o processamento passa para o segundo plano quando o número selecionado de registros para aprovação excede o limite indicado.</span><span class="sxs-lookup"><span data-stu-id="65d8b-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="65d8b-128">Use o campo **Limite Assíncrono** para configurar quando o processamento de aprovação deve ser executado de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="65d8b-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="65d8b-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="65d8b-129">Valid values are:</span></span>

  - <span data-ttu-id="65d8b-130">Zero: todas as solicitações devem ser processadas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="65d8b-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="65d8b-131">Números maiores que zero: as aprovações são processadas de forma assíncrona apenas quando o número de aprovações enviadas excede esse valor.</span><span class="sxs-lookup"><span data-stu-id="65d8b-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
