---
title: Desempenho de agendamento de recursos do projeto
description: Este tópico fornece informações sobre como melhorar o desempenho do agendamento de recursos para um grande número de projetos.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288995"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="be42b-103">Desempenho de agendamento de recursos do projeto</span><span class="sxs-lookup"><span data-stu-id="be42b-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="be42b-104">Problemas de desempenho relacionados ao agendamento de recursos podem ocorrer quando o número de projetos chega aos milhares.</span><span class="sxs-lookup"><span data-stu-id="be42b-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="be42b-105">Para melhorar o desempenho do agendamento de recursos, está disponível um recurso que permite aos usuários reduzir o tempo que leva para iniciar o formulário de disponibilidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="be42b-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="be42b-106">Especificamente, isso remove o processo de sincronização de acúmulo da capacidade do recurso e usa a tabela **ResProjectResource** para acelerar a pesquisa de recursos.</span><span class="sxs-lookup"><span data-stu-id="be42b-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="be42b-107">Observe que a tabela **ResRollup** não será mais usada.</span><span class="sxs-lookup"><span data-stu-id="be42b-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be42b-108">Se houver uma dependência do processo de sincronização de acumulação de capacidade do recurso ou da tabela **ResProjectResource**, não use o recurso.</span><span class="sxs-lookup"><span data-stu-id="be42b-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="be42b-109">Habilitar melhoria de desempenho de agendamento de recursos</span><span class="sxs-lookup"><span data-stu-id="be42b-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="be42b-110">Para habilitar o aprimoramento de desempenho do agendamento de recursos, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="be42b-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="be42b-111">Acesse **Gerenciamento de recursos** > **Tudo** e, na lista de recursos, localize **Habilitar recurso de aprimoramento de desempenho de agendamento de recursos do projeto**.</span><span class="sxs-lookup"><span data-stu-id="be42b-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="be42b-112">Selecione **Habilitar agora**.</span><span class="sxs-lookup"><span data-stu-id="be42b-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="be42b-113">Se você não conseguir encontrar o recurso na lista, selecione **Verificar se há atualizações** para atualizar a lista.</span><span class="sxs-lookup"><span data-stu-id="be42b-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="be42b-114">Atualize seu navegador e acesse **Gerenciamento e contabilidade de projeto** > **Periódico** > **Recursos do projeto** > **Sincronizar a capacidade dos calendários de recursos em todas as empresas**.</span><span class="sxs-lookup"><span data-stu-id="be42b-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="be42b-115">Defina **Remover os registros de capacidade existentes** como **Sim** para remover dados anteriores.</span><span class="sxs-lookup"><span data-stu-id="be42b-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="be42b-116">Se você quiser gerar dados incrementais, defina-o como **Não**.</span><span class="sxs-lookup"><span data-stu-id="be42b-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="be42b-117">No campo **Código de período**, selecione o período em que os dados devem ser gerados.</span><span class="sxs-lookup"><span data-stu-id="be42b-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="be42b-118">Se você selecionar um código de período, uma data de início e de término não precisa ser definida.</span><span class="sxs-lookup"><span data-stu-id="be42b-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="be42b-119">Se você deixar o campo **Código de período** em branco, selecione datas de início e término específicas para gerar dados.</span><span class="sxs-lookup"><span data-stu-id="be42b-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="be42b-120">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="be42b-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="be42b-121">Isso distribuirá dados gerais para a tabela **ResCalendarCapacity** em todas as empresas em seu ambiente, de modo que o trabalho em lote só precisa ser executado em uma entidade legal.</span><span class="sxs-lookup"><span data-stu-id="be42b-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="be42b-122">Os dados nesse trabalho em lote são necessários para calcular a capacidade do recurso por meio do calendário associado.</span><span class="sxs-lookup"><span data-stu-id="be42b-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="be42b-123">Acesse **Gerenciamento e contabilidade de projeto** > **Periódico** > **Recursos do projeto** > **PPreencher os recursos do projeto em todas as empresas** e selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="be42b-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="be42b-124">Este é o script de atualização de dados para dados gerais nas tabelas **ResProjectResource**, **ResCalendarDateTimeRange** e **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="be42b-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="be42b-125">Os valores do campo **PSAPRojSchedRole.RootActivity** também são atualizados.</span><span class="sxs-lookup"><span data-stu-id="be42b-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="be42b-126">Se não for executado, você receberá um aviso ao tentar executar operações de agendamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="be42b-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="be42b-127">Desligar melhoria de desempenho de agendamento de recursos</span><span class="sxs-lookup"><span data-stu-id="be42b-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="be42b-128">Acesse **Gerenciamento de recursos** > **Tudo** e pesquise **Habilitar recurso de aprimoramento de desempenho de agendamento de recursos do projeto**.</span><span class="sxs-lookup"><span data-stu-id="be42b-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="be42b-129">Selecione o recurso e, em seguida, selecione o botão **Desabilitar**.</span><span class="sxs-lookup"><span data-stu-id="be42b-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="be42b-130">Atualize seu navegador.</span><span class="sxs-lookup"><span data-stu-id="be42b-130">Refresh your browser.</span></span>
4. <span data-ttu-id="be42b-131">Acesse **Gerenciamento e contabilidade de projeto** > **Periódico** > **Sincronização de capacidade** > **Sincronizar acúmulos de capacidade de recursos**.</span><span class="sxs-lookup"><span data-stu-id="be42b-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="be42b-132">Na página **Sincronização de acúmulo de capacidade**, defina **Remover os registros de capacidade existentes** como **Sim** para remover dados anteriores.</span><span class="sxs-lookup"><span data-stu-id="be42b-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="be42b-133">Se você quiser gerar dados incrementais, defina-o como **Não**.</span><span class="sxs-lookup"><span data-stu-id="be42b-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="be42b-134">No campo **Código de período**, selecione o período em que os dados devem ser gerados.</span><span class="sxs-lookup"><span data-stu-id="be42b-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="be42b-135">Se você selecionar um código de período, uma data de início e de término não precisa ser definida.</span><span class="sxs-lookup"><span data-stu-id="be42b-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="be42b-136">Se você deixar o campo **Código de período** em branco, selecione datas de início e término específicas para gerar dados.</span><span class="sxs-lookup"><span data-stu-id="be42b-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="be42b-137">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="be42b-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="be42b-138">Isso distribuirá dados gerais para a tabela **ResRollup** em todas as empresas em seu ambiente, de modo que o trabalho em lote só precisa ser executado em uma entidade legal.</span><span class="sxs-lookup"><span data-stu-id="be42b-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="be42b-139">Esse trabalho em lote é necessário para todas as exibições **Disponibilidade do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="be42b-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="be42b-140">Se esse trabalho em lote não for executado, os dados **ResRollup** serão gerados imediatamente, o que pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="be42b-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]