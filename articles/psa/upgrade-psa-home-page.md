---
title: Home page de atualização
description: Este tópico mostra onde encontrar informações importantes sobre os recursos novos e alterados no Dynamics 365 Project Service Automation e o processo de atualização para a versão mais recente.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 838eecb1229ea20106c7d5487dc37a81e8df501b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281689"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="a3baf-103">Home page de atualização</span><span class="sxs-lookup"><span data-stu-id="a3baf-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="a3baf-104">Upgrade do PSA versão 2.x ou 1.x para a versão 3.x</span><span class="sxs-lookup"><span data-stu-id="a3baf-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="a3baf-105">Novas instâncias</span><span class="sxs-lookup"><span data-stu-id="a3baf-105">New instances</span></span>

<span data-ttu-id="a3baf-106">Desde 17 de maio de 2019, quando o Project Service Automation é selecionado durante o provisionamento de uma nova instância, a versão 3.x é instalada por padrão.</span><span class="sxs-lookup"><span data-stu-id="a3baf-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="a3baf-107">Instâncias existentes</span><span class="sxs-lookup"><span data-stu-id="a3baf-107">Existing instances</span></span>

<span data-ttu-id="a3baf-108">Anteriormente, os clientes que possuem uma instância do PSA versão 2.xe precisavam atualizar para a versão 3.x, que é a versão do PSA baseado em UCI (Interface Unificada do Cliente), deviam entrar em Suporte da Microsoft com o suporte e fornecer os detalhes da instância, para que o suporte possa ativar a instância para atualização para a versão 3.x.</span><span class="sxs-lookup"><span data-stu-id="a3baf-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="a3baf-109">A partir de 1º de março de 2020, os clientes que possuem uma instância do PSA versão 2.xe precisam atualizar para a versão 3.x, poderão atualizar suas instâncias diretamente do portal de administração sem precisar entrar em contato com o Suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3baf-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="a3baf-110">O PSA versão 3.x inclui alterações significativas.</span><span class="sxs-lookup"><span data-stu-id="a3baf-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="a3baf-111">Ele foi baseado na estrutura de Interface Unificada para ajudar a fornecer uma melhor experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="a3baf-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="a3baf-112">O aplicativo recriado oferece uma interface do usuário consistente e uniforme e segue princípios de design responsivos para uma exibição ideal em qualquer tamanho de tela ou dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3baf-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="a3baf-113">Houve outras alterações em todo o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3baf-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="a3baf-114">Algumas das áreas que foram alteradas incluem preços, reservas e designação de recursos, tempo, despesas e aprovações.</span><span class="sxs-lookup"><span data-stu-id="a3baf-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="a3baf-115">Antes de iniciar o processo de atualização, recomendamos que você conclua as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="a3baf-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="a3baf-116">Verifique se o Dynamics 365 Field Service e o Project Service Automation estão instalados na instância identificada.</span><span class="sxs-lookup"><span data-stu-id="a3baf-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="a3baf-117">Se as duas soluções estiverem instaladas, planeje atualizar as duas antes de retomar o uso regular da instância.</span><span class="sxs-lookup"><span data-stu-id="a3baf-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="a3baf-118">Analise cuidadosamente os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="a3baf-118">Carefully review the following topics.</span></span> <span data-ttu-id="a3baf-119">A conscientização e o reconhecimento das alterações entre as versões ajudarão você no processo de atualização.</span><span class="sxs-lookup"><span data-stu-id="a3baf-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="a3baf-120">Esses tópicos fornecem informações sobre as principais alterações no PSA, juntamente com considerações e recomendações para planejar sua atualização para a versão 3.x.</span><span class="sxs-lookup"><span data-stu-id="a3baf-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="a3baf-121">Novidades ou alterações no Project Service Automation versão 3</span><span class="sxs-lookup"><span data-stu-id="a3baf-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="a3baf-122">Considerações sobre atualização - Project Service Automation versão 2.x ou 1.x para a versão 3</span><span class="sxs-lookup"><span data-stu-id="a3baf-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="a3baf-123">Atualize sua instância de área restrita para avaliar as alterações em sua implementação antes de atualizar sua instância de produção.</span><span class="sxs-lookup"><span data-stu-id="a3baf-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="a3baf-124">Depois de analisar os tópicos mencionados anteriormente e estar pronto para atualizar para o PSA versão 3.x ou a versão baseada em UCI, envie uma solicitação ao suporte da Microsoft para disponibilizar a atualização no Centro de Administração.</span><span class="sxs-lookup"><span data-stu-id="a3baf-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="a3baf-125">Em sua solicitação, forneça os detalhes da sua instância.</span><span class="sxs-lookup"><span data-stu-id="a3baf-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="a3baf-126">Versões mais antigas do PSA (PSA versão 2.x) em uma instância recém-criada</span><span class="sxs-lookup"><span data-stu-id="a3baf-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="a3baf-127">Desde 17 de maio de 2019, todas as novas instâncias têm o UCI como cliente padrão.</span><span class="sxs-lookup"><span data-stu-id="a3baf-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="a3baf-128">Para alinhamento com essa alteração, o PSA versão 3.xe e o Field Service versão 8.x serão provisionados por padrão, porque essas versões foram projetadas para funcionar com o cliente de UCI.</span><span class="sxs-lookup"><span data-stu-id="a3baf-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="a3baf-129">A partir de 1º de março de 2020, os clientes do Dynamics PSA não poderão mais criar um novo ambiente com versões anteriores do PSA, por exemplo, PSA versão 2.x ou inferior.</span><span class="sxs-lookup"><span data-stu-id="a3baf-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="a3baf-130">Todos os novos ambientes serão para obter apenas a versão 3.x do PSA.</span><span class="sxs-lookup"><span data-stu-id="a3baf-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="a3baf-131">Para obter a melhor experiência ao usar versões mais antigas dos aplicativos Field Service e PSA, acesse a página **Configurações do sistema** e, no campo **Usar apenas a nova Interface Unificada (recomendado)**, selecione **Não**, já que essas versões não foram projetadas para serem carregadas corretamente na UCI.</span><span class="sxs-lookup"><span data-stu-id="a3baf-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="a3baf-132">Depois de desativar a UCI, você pode abrir e executar essas versões do Field Service e PSA usando o cliente da Web antigo.</span><span class="sxs-lookup"><span data-stu-id="a3baf-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]