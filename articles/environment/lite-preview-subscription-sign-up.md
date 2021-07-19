---
title: Inscrever-se em uma assinatura de versão preliminar - lite
description: Este tópico fornece informações sobre como assinar e implantar a implantação simplificada do Project Operations - transação para faturamento pro forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334768"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="db8ca-103">Inscreva-se para obter uma assinatura de versão preliminar – lite</span><span class="sxs-lookup"><span data-stu-id="db8ca-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="db8ca-104">Este tópico explica como assinar a oferta de avaliação e implementar a implantação lite do Dynamics 365 Project Operations - lidar com o faturamento pró-forma.</span><span class="sxs-lookup"><span data-stu-id="db8ca-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="db8ca-105">Este processo mudará nas próximas versões de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="db8ca-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="db8ca-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="db8ca-106">Prerequisites</span></span>
- <span data-ttu-id="db8ca-107">O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure.</span><span class="sxs-lookup"><span data-stu-id="db8ca-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="db8ca-108">Você pode criar um inquilino durante o primeiro resgate da oferta.</span><span class="sxs-lookup"><span data-stu-id="db8ca-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db8ca-109">Apenas uma pessoa, o administrador do locatário, em uma organização precisa executar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="db8ca-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="db8ca-110">Se você não for o assinante dessa versão, espere até que sua organização se inscreva e você receba suas credenciais de usuário.</span><span class="sxs-lookup"><span data-stu-id="db8ca-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="db8ca-111">As avaliações são de uso único no locatário.</span><span class="sxs-lookup"><span data-stu-id="db8ca-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="db8ca-112">Você só pode executar uma avaliação de cada vez.</span><span class="sxs-lookup"><span data-stu-id="db8ca-112">You can only run a trial one time.</span></span> <span data-ttu-id="db8ca-113">Recomendamos que você crie um novo locatário para o propósito de avaliação.</span><span class="sxs-lookup"><span data-stu-id="db8ca-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="db8ca-114">Avaliação do Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="db8ca-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="db8ca-115">Antes de começar, verifique se está conectado a um navegador com a conta de trabalho do usuário no locatário em que deseja ter a versão preliminar do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="db8ca-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="db8ca-116">Vá para [Avaliação do Project Operations](https://aka.ms/try-po) para resgatar o primeiro código da oferta, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="db8ca-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="db8ca-117">Confirme a ordem.</span><span class="sxs-lookup"><span data-stu-id="db8ca-117">Confirm your order.</span></span>

  <span data-ttu-id="db8ca-118">Você verá que a oferta de confirmação foi resgatada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="db8ca-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="db8ca-119">Atribuir licenças</span><span class="sxs-lookup"><span data-stu-id="db8ca-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db8ca-120">Você precisará de acesso administrativo ao Portal do Microsoft 365 da sua organização para concluir as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="db8ca-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="db8ca-121">Acesse [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças aos usuários.</span><span class="sxs-lookup"><span data-stu-id="db8ca-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="db8ca-122">Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.</span><span class="sxs-lookup"><span data-stu-id="db8ca-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="db8ca-123">Verifique se a licença do **Dynamics 365 Project Operations** foi selecionada.</span><span class="sxs-lookup"><span data-stu-id="db8ca-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="db8ca-124">Selecione **Salvar alterações**.</span><span class="sxs-lookup"><span data-stu-id="db8ca-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="db8ca-125">Criar um novo ambiente do Dataverse</span><span class="sxs-lookup"><span data-stu-id="db8ca-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="db8ca-126">Provisione um novo ambiente de implantação do Project Operations Dataverse seguindo instruções no tópico, [modelo de implantação do Dataverse](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="db8ca-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="db8ca-127">Ao selecionar o tipo de ambiente, utilize **Avaliação (baseado em assinatura)**.</span><span class="sxs-lookup"><span data-stu-id="db8ca-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Novo ambiente](./media/19CreateEnvironment.png)

2. <span data-ttu-id="db8ca-129">Selecione a configuração **Habilitar aplicações do Dynamics 365** e deixe em branco **Implantar automaticamente essas aplicações**.</span><span class="sxs-lookup"><span data-stu-id="db8ca-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="db8ca-130">Selecione **Salvar** para criar o ambiente.</span><span class="sxs-lookup"><span data-stu-id="db8ca-130">Select **Save** to create the environment.</span></span>

  ![Adicionar banco de dados](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="db8ca-132">Depois de criar o ambiente, instale a solução **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="db8ca-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instalar Solução](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="db8ca-134">Instalar uma configuração CDS e configurar dados de demonstração</span><span class="sxs-lookup"><span data-stu-id="db8ca-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="db8ca-135">Instale a configuração do CDS e defina os dados de demonstração seguindo as instruções no tópico, [Aplicar instalação de demonstração e dados de configuração](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="db8ca-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
