---
title: Implantar o Project Operations - lite
description: Este tópico fornece informações sobre como instalar a implantação simplificada do Project Operations - transação para faturamento pro forma.
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995517"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="1c1fb-103">Implantar o Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="1c1fb-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="1c1fb-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="1c1fb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1c1fb-105">O Project Operations oferece suporte a vários modelos de implantação.</span><span class="sxs-lookup"><span data-stu-id="1c1fb-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="1c1fb-106">Para determinar o melhor modelo de implantação, consulte [Tipos de implantação](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="1c1fb-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="1c1fb-107">Esta implantação, implantação Lite - lidar com faturamento pro forma, resulta em uma implantação apenas de **Common Data Service do Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="1c1fb-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="1c1fb-108">Instalar Project Operations em um novo ambiente CDS</span><span class="sxs-lookup"><span data-stu-id="1c1fb-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="1c1fb-109">Instale em um ambiente CDS existente</span><span class="sxs-lookup"><span data-stu-id="1c1fb-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="1c1fb-110">Instalar Project Operations em um novo ambiente CDS</span><span class="sxs-lookup"><span data-stu-id="1c1fb-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="1c1fb-111">Como o [Global ou administrador do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, crie um novo ambiente do CDS na [Central administrativa do PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="1c1fb-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="1c1fb-112">Certifique-se de que **Banco de dados CDS** e **Aplicativos Dynamics 365** estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="1c1fb-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="1c1fb-113">Para obter mais informações, consulte [Criar e gerenciar ambientes no centro de administração da Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="1c1fb-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="1c1fb-114">Selecione **Microsoft Dynamics 365 Project Operations** na lista de implantação de aplicativos do Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1c1fb-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="1c1fb-115">Instalar Project Operations em um ambiente CDS existente</span><span class="sxs-lookup"><span data-stu-id="1c1fb-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="1c1fb-116">Como o [Global ou administrador do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente na [Central de administração do PowerPlatform](https://admin.powerplatform.com) onde você deseja instalar Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1c1fb-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="1c1fb-117">Instale o **Microsoft Dynamics 365 Project Operations** a partir da lista de implantação de aplicativos do Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1c1fb-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="1c1fb-118">Para obter mais informações, consulte [Gerenciar aplicativos Dynamics 365](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="1c1fb-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]