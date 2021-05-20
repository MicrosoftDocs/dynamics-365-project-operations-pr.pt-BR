---
title: Adicionar uma subscrição do Azure a um projeto do LCS
description: Este tópico fornece informações sobre como conectar sua subscrição do Azure a um projeto do LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880524"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="b729c-103">Adicionar uma subscrição do Azure a um projeto do LCS</span><span class="sxs-lookup"><span data-stu-id="b729c-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="b729c-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="b729c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b729c-105">Ambientes hospedados em nuvem devem ser implantados usando uma subscrição existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="b729c-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="b729c-106">Este tópico explica como conectar sua subscrição existente do Azure a um projeto do LCS.</span><span class="sxs-lookup"><span data-stu-id="b729c-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="b729c-107">Conceder consentimento do administrador</span><span class="sxs-lookup"><span data-stu-id="b729c-107">Grant admin consent</span></span>

1. <span data-ttu-id="b729c-108">Em seu projeto do LCS, na seção **Ambientes**, selecione **Configurações do Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="b729c-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Configurações do Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="b729c-110">Na página **Configurações do projeto**, na guia **Conectores do Azure**, selecione **Autorizar**.</span><span class="sxs-lookup"><span data-stu-id="b729c-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="b729c-111">Isso permite que ambientes sejam implantados neste projeto.</span><span class="sxs-lookup"><span data-stu-id="b729c-111">This allows environments to be deployed to this project.</span></span>

![Conectores do Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="b729c-113">Selecione **Autorizar** novamente para fornecer consentimento do administrador.</span><span class="sxs-lookup"><span data-stu-id="b729c-113">Select **Authorize** again to provide admin consent.</span></span>

![Conceder Consentimento do Administrador](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="b729c-115">Aceite a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="b729c-115">Accept the permissions request.</span></span>

![Aceitar a Solicitação de Permissão](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="b729c-117">A autorização agora está concluída.</span><span class="sxs-lookup"><span data-stu-id="b729c-117">The authorization is now complete.</span></span> 

![Autorização bem sucedida](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="b729c-119">Fornecer ao Dynamics Deployment Services acesso à sua subscrição do Azure</span><span class="sxs-lookup"><span data-stu-id="b729c-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="b729c-120">Acesse [cobrança do Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e selecione sua subscrição.</span><span class="sxs-lookup"><span data-stu-id="b729c-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="b729c-121">O Dynamics Deployment Services precisa acessar essa subscrição para poder implantar ambientes.</span><span class="sxs-lookup"><span data-stu-id="b729c-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Detalhes da subscrição do Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="b729c-123">Selecione **Controle de Acesso (IAM)** no painel de navegação e selecione **Adicionar atribuição de função**.</span><span class="sxs-lookup"><span data-stu-id="b729c-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="b729c-124">No controle deslizante do lado direito, selecione **Função Parceiro** e, na lista fornecida, localize e selecione **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="b729c-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="b729c-125">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="b729c-125">Select **Save**.</span></span>

![Acesso à Subscrição](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="b729c-127">Adicionar um conector de subscrição a um projeto do LCS</span><span class="sxs-lookup"><span data-stu-id="b729c-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="b729c-128">Em seu projeto do LCS, na página **Configurações do Microsoft Azure**, selecione **Adicionar** para adicionar um novo conector.</span><span class="sxs-lookup"><span data-stu-id="b729c-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="b729c-129">Insira sua ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b729c-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="b729c-130">Você pode encontrar sua ID da assinatura do Azure no [portal do Azure](https://ms.portal.azure.com/), em **Configurações** no canto inferior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="b729c-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="b729c-131">No campo **Configurar para usar o Azure Resource Manager**, selecione **Sim**.</span><span class="sxs-lookup"><span data-stu-id="b729c-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="b729c-132">Certifique-se de que o Domínio de Locatário do AAD de Subscrição do Azure corresponda à subscrição do Azure proprietária do domínio que você está usando e selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b729c-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="b729c-133">Na tela **Configuração do Microsoft Azure**, selecione **Avançar** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="b729c-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="b729c-134">Se ocorrer um erro nessa tela, volte para a seção [Fornecer ao Dynamics Deployment Services acesso à sua subscrição do Azure](#provide) neste tópico e certifique-se de ter concluído todas as etapas.</span><span class="sxs-lookup"><span data-stu-id="b729c-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="b729c-135">Baixe o Certificado de Gerenciamento do Azure para uma pasta local em seu computador.</span><span class="sxs-lookup"><span data-stu-id="b729c-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="b729c-136">Peça ao administrador de assinatura do Azure para carregar o certificado no Portal de Gerenciamento do Azure selecionando a assinatura e acessando **Configurações** > **Certificados de Gerenciamento**.</span><span class="sxs-lookup"><span data-stu-id="b729c-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="b729c-137">Este certificado permite que o LCS se comunique com o Azure em seu nome.</span><span class="sxs-lookup"><span data-stu-id="b729c-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="b729c-138">Você poderá pular essa etapa se seu usuário tiver acesso à subscrição.</span><span class="sxs-lookup"><span data-stu-id="b729c-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="b729c-139">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b729c-139">Select  **Next**.</span></span>
8. <span data-ttu-id="b729c-140">Selecione a região do Azure para implantar e selecione um data center próximo ao local onde você planeja usar este sistema.</span><span class="sxs-lookup"><span data-stu-id="b729c-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="b729c-141">Selecione **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="b729c-141">Select  **Connect**.</span></span>

<span data-ttu-id="b729c-142">Você conectou sua subscrição do Azure com êxito.</span><span class="sxs-lookup"><span data-stu-id="b729c-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="b729c-143">Agora você pode implantar ambientes hospedados em nuvem do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b729c-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
