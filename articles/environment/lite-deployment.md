---
title: Implantar o Project Operations - lite
description: Este tópico fornece informações sobre como instalar a implantação simplificada do Project Operations - transação para faturamento pro forma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642169"
---
# <a name="deploy-project-operations---lite"></a>Implantar o Project Operations - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

O Project Operations oferece suporte a vários modelos de implantação. Para determinar o melhor modelo de implantação, consulte [Tipos de implantação](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implantação, implantação Lite - lidar com faturamento pro forma, resulta em uma implantação apenas de **Common Data Service do Project Operations**.

- [Instalar Project Operations em um novo ambiente CDS](#new)
- [Instale em um ambiente CDS existente](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Instalar Project Operations em um novo ambiente CDS

1. Como o [Global ou administrador do Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, crie um novo ambiente do CDS na [Central administrativa do PowerPlatform](https://admin.powerplatform.com). Certifique-se de que **Banco de dados CDS** e **Aplicativos Dynamics 365** estão habilitados. Para obter mais informações, consulte [Criar e gerenciar ambientes no centro de administração da Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Selecione **Microsoft Dynamics 365 Project Operations** na lista de implantação de aplicativos do Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Instalar Project Operations em um ambiente CDS existente

1. Como o [Global ou administrador do Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente na [Central de administração do PowerPlatform](https://admin.powerplatform.com) onde você deseja instalar Project Operations.
2. Instale o **Microsoft Dynamics 365 Project Operations** a partir da lista de implantação de aplicativos do Dynamics 365. Para obter mais informações, consulte [Gerenciar aplicativos Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).


