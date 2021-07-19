---
title: Implantar manualmente o aplicativo Dataverse do Project Operations com suporte à gravação dupla
description: Este tópico explica como implantar manualmente o aplicativo Dataverse do Project Operations para que ele suporte gravação dupla.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273994"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="5affd-103">Implantar manualmente o aplicativo Dataverse do Project Operations com suporte à gravação dupla</span><span class="sxs-lookup"><span data-stu-id="5affd-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="5affd-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="5affd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5affd-105">Este tópico explica como implantar manualmente o Microsoft Dynamics 365 Project Operations no Microsoft Dataverse, de forma que ele suporte gravação dupla.</span><span class="sxs-lookup"><span data-stu-id="5affd-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="5affd-106">O Project Operations detecta a configuração do ambiente e adiciona suporte adicional para gravação dupla, se os pré-requisitos forem atendidos.</span><span class="sxs-lookup"><span data-stu-id="5affd-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="5affd-107">Durante a implantação por meio do Microsoft Dynamics Lifecycle Services (LCS), se você seguiu as instruções neste tópico, poderá pular a implantação da integração do Microsoft Power Platform (anteriormente conhecido como o ambiente do Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="5affd-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="5affd-108">O processo de implantação do Project Operations no Dataverse para que seja compatível com gravação dupla tem quatro etapas principais:</span><span class="sxs-lookup"><span data-stu-id="5affd-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="5affd-109">[Criar um novo ambiente no Dataverse que suporta gravação dupla](#create).</span><span class="sxs-lookup"><span data-stu-id="5affd-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="5affd-110">[Adicionar pré-requisitos de gravação dupla ao ambiente](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="5affd-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="5affd-111">[Adicionar o aplicativo Dataverse do Project Operations](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="5affd-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="5affd-112">[Vincular seus ambientes](#link).</span><span class="sxs-lookup"><span data-stu-id="5affd-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="5affd-113">Criar um novo ambiente no Dataverse que suporta gravação dupla</span><span class="sxs-lookup"><span data-stu-id="5affd-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="5affd-114">Para concluir este procedimento, você deve se conectar como administrador.</span><span class="sxs-lookup"><span data-stu-id="5affd-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="5affd-115">Abra o [centro de administração do Power Platform](https://admin.powerplatform.com) e entre como administrador.</span><span class="sxs-lookup"><span data-stu-id="5affd-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="5affd-116">Crie um novo ambiente e dê um nome a ele.</span><span class="sxs-lookup"><span data-stu-id="5affd-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="5affd-117">Selecione o tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="5affd-117">Select the environment type.</span></span> <span data-ttu-id="5affd-118">Se você se inscreveu para a oferta de avaliação, selecione **Avaliação (baseada em assinatura)**.</span><span class="sxs-lookup"><span data-stu-id="5affd-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="5affd-119">Confirme a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="5affd-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="5affd-120">Ative a opção **Criar um banco de dados para este ambiente**.</span><span class="sxs-lookup"><span data-stu-id="5affd-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="5affd-121">Confirme o idioma e, em seguida, confirme se a moeda corresponde à moeda de seu aplicativo Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5affd-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="5affd-122">Ative a opção **Aplicativos Dynamics 365** e confirme se o campo **Implantar esses aplicativos automaticamente** está definido como **Nenhum**.</span><span class="sxs-lookup"><span data-stu-id="5affd-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="5affd-123">Adicione um grupo de segurança, se um grupo de segurança for necessário.</span><span class="sxs-lookup"><span data-stu-id="5affd-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="5affd-124">Selecione **Salvar** para criar o ambiente.</span><span class="sxs-lookup"><span data-stu-id="5affd-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="5affd-125">Espere até que a implantação seja concluída e o ambiente atinja o estado **Pronto**.</span><span class="sxs-lookup"><span data-stu-id="5affd-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="5affd-126">Adicionar pré-requisitos de gravação dupla ao ambiente</span><span class="sxs-lookup"><span data-stu-id="5affd-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="5affd-127">O suporte de gravação dupla inclui campos adicionais que são adicionados às principais entidades, como a entidade **Empresa**.</span><span class="sxs-lookup"><span data-stu-id="5affd-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="5affd-128">Se você estiver adicionando suporte de gravação dupla a um ambiente existente, pode ser necessário atualizar os dados para ativar o suporte.</span><span class="sxs-lookup"><span data-stu-id="5affd-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="5affd-129">Para obter informações sobre como inicializar os dados, consulte [Dados da empresa de bootstrap](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="5affd-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="5affd-130">Para obter mais informações sobre gravação dupla, consulte [Requisitos de sistema de gravação dupla](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="5affd-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="5affd-131">Conclua este procedimento para adicionar os pré-requisitos de gravação dupla ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="5affd-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="5affd-132">Abra o ambiente que você acabou de criar e vá para **Recurso** \> **Aplicativos do Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5affd-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="5affd-133">Selecione **Solução principal de gravação dupla** na lista de aplicativos e instale-a.</span><span class="sxs-lookup"><span data-stu-id="5affd-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="5affd-134">Aguarde até que a instalação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5affd-134">Wait until the installation is completed.</span></span> <span data-ttu-id="5affd-135">Em seguida, selecione **Solução principal de gravação dupla** na lista de aplicativos e instale-a.</span><span class="sxs-lookup"><span data-stu-id="5affd-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="5affd-136">Adicionar o aplicativo Dataverse do Project Operations</span><span class="sxs-lookup"><span data-stu-id="5affd-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="5affd-137">Você pode concluir este procedimento apenas se tiver concluído os procedimentos anteriores antes de instalar o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5affd-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="5affd-138">Durante a instalação, o sistema analisa a configuração do ambiente e adiciona suporte para gravação dupla, se necessário.</span><span class="sxs-lookup"><span data-stu-id="5affd-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="5affd-139">Abra o ambiente que você criou anteriormente e vá para **Recurso** \> **aplicativos Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5affd-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="5affd-140">Selecione **Microsoft Dynamics 365 Project Operations** na lista de aplicativos e instale-o.</span><span class="sxs-lookup"><span data-stu-id="5affd-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="5affd-141">Vincular seus ambientes</span><span class="sxs-lookup"><span data-stu-id="5affd-141">Link your environments</span></span>

<span data-ttu-id="5affd-142">Depois que o ambiente do Dataverse for implantado, você pode configurar o link em seu aplicativo do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5affd-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="5affd-143">Siga as etapas em [Usar o assistente de gravação dupla para vincular seus ambientes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="5affd-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>