---
title: Inscreva-se para obter subscrições de versão preliminar do Project Operations para cenários de recursos/sem estoque
description: Este tópico fornece informações sobre como subscrever e implantar o Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334813"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="f2858-103">Inscreva-se para obter subscrições de versão preliminar do Project Operations para cenários de recursos/sem estoque</span><span class="sxs-lookup"><span data-stu-id="f2858-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="f2858-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="f2858-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f2858-105">Este tópico explica como assinar a oferta de avaliação e implantar o ambiente do Project Operations para cenários baseados em recursos/itens sem estoque.</span><span class="sxs-lookup"><span data-stu-id="f2858-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2858-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f2858-106">Prerequisites</span></span>
- <span data-ttu-id="f2858-107">O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2858-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="f2858-108">Você pode criar um inquilino durante o primeiro resgate da oferta.</span><span class="sxs-lookup"><span data-stu-id="f2858-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="f2858-109">A implantação de um ambiente do Finance requer uma subscrição válida do Azure que será cobrada por ambiente.</span><span class="sxs-lookup"><span data-stu-id="f2858-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="f2858-110">Você pode usar a subscrição existente da sua organização ou usar uma [avaliação do Azure](https://azure.microsoft.com/en-us/free/) para começar.</span><span class="sxs-lookup"><span data-stu-id="f2858-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="f2858-111">O ambiente CDS será fornecido gratuitamente por um período limitado de 30 dias.</span><span class="sxs-lookup"><span data-stu-id="f2858-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2858-112">Apenas uma pessoa, o administrador do locatário, em uma organização precisa executar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="f2858-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="f2858-113">Se você não for o assinante dessa versão, espere até que sua organização se inscreva e você receba suas credenciais de usuário.</span><span class="sxs-lookup"><span data-stu-id="f2858-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="f2858-114">As avaliações são de uso único no locatário.</span><span class="sxs-lookup"><span data-stu-id="f2858-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="f2858-115">Você só pode executar uma avaliação de cada vez.</span><span class="sxs-lookup"><span data-stu-id="f2858-115">You can only run a trial one time.</span></span> <span data-ttu-id="f2858-116">Recomendamos que você crie um novo locatário para o propósito de avaliação.</span><span class="sxs-lookup"><span data-stu-id="f2858-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="f2858-117">Dynamics 365 Project Operations (CE) - Avaliação de Visualização</span><span class="sxs-lookup"><span data-stu-id="f2858-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="f2858-118">Antes de começar, verifique se está conectado a um navegador com a conta de trabalho do usuário no locatário em que deseja ter a versão preliminar do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f2858-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="f2858-119">Resgate o primeiro código de oferta, **Dynamics 365 Project Operations** aqui [Avaliação do Project Operations](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="f2858-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="f2858-120">Confirme a ordem.</span><span class="sxs-lookup"><span data-stu-id="f2858-120">Confirm your order.</span></span>

  <span data-ttu-id="f2858-121">Você verá que a oferta de confirmação foi resgatada com êxito.</span><span class="sxs-lookup"><span data-stu-id="f2858-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="f2858-122">Avaliação da versão preliminar do Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f2858-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="f2858-123">Vá para [Avaliação de Versão Preliminar do Dynamics 365 for Finance](https://aka.ms/trypoche) e repita as etapas da seção anterior com a oferta Inscreva-se no Ambiente Hospedado na Nuvem.</span><span class="sxs-lookup"><span data-stu-id="f2858-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="f2858-124">Atribuir licenças</span><span class="sxs-lookup"><span data-stu-id="f2858-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2858-125">Você precisará de acesso administrativo ao Portal do Microsoft 365 da sua organização para concluir as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2858-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="f2858-126">Acesse [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças aos usuários.</span><span class="sxs-lookup"><span data-stu-id="f2858-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="f2858-127">Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.</span><span class="sxs-lookup"><span data-stu-id="f2858-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="f2858-128">Verifique se a licença do **Dynamics 365 Project Operations** foi selecionada e escolha **Salvar alterações**.</span><span class="sxs-lookup"><span data-stu-id="f2858-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="f2858-129">A oferta de avaliação do Finance não precisa ser atribuída a um usuário.</span><span class="sxs-lookup"><span data-stu-id="f2858-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="f2858-130">Iniciar um novo projeto no LCS</span><span class="sxs-lookup"><span data-stu-id="f2858-130">Start a new project in LCS</span></span>

<span data-ttu-id="f2858-131">Criar um novo projeto do LCS conforme descrito no tópico [Iniciar novo projeto no LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="f2858-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="f2858-132">Adicionar uma subscrição do Azure a um projeto do LCS</span><span class="sxs-lookup"><span data-stu-id="f2858-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="f2858-133">Para concluir essa tarefa, siga as etapas no tópico [Adicionar uma subscrição do Azure ao projeto do LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="f2858-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="f2858-134">Implantar um ambiente de demonstração do Finance com o Project Operations para cenários de recursos/sem estoque</span><span class="sxs-lookup"><span data-stu-id="f2858-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="f2858-135">Siga as orientações no tópico [Provisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implantação.</span><span class="sxs-lookup"><span data-stu-id="f2858-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="f2858-136">Use o tipo de implantação [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para a versão preliminar.</span><span class="sxs-lookup"><span data-stu-id="f2858-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="f2858-137">Instalar dados de configuração do CDS</span><span class="sxs-lookup"><span data-stu-id="f2858-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="f2858-138">Instale os dados de configuração do CDS conforme descrito no tópico [Configurar e aplicar dados de configuração no Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="f2858-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="f2858-139">Conclua esta etapa somente depois que o ambiente de demonstração do Finance for implantado e os dados de demonstração estiverem prontos.</span><span class="sxs-lookup"><span data-stu-id="f2858-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
