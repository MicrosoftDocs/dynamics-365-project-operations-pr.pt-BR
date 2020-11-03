---
title: Fazer implantação do Project Operations Lite – gerenciar faturamento pro forma
description: Este tópico fornece informações sobre como instalar a implantação simplificada do Project Operations - transação para faturamento pró-forma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071292"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a>Fazer implantação do Project Operations Lite – gerenciar faturamento pro forma

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_

O Project Operations oferece suporte a vários modelos de implantação. Para determinar o melhor modelo de implantação, consulte [Tipos de implantação](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implantação, implantação Lite - lidar com faturamento pró-forma, resulta em uma implantação apenas de **Common Data Service do Project Operations**.

- [Instalar Project Operations em um novo ambiente CDS](#new)
- [Instale em um ambiente CDS existente](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Instalar Project Operations em um novo ambiente CDS

1. Como o [Global ou administrador do Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, crie um novo ambiente do CDS na [Central administrativa do PowerPlatform](https://admin.powerplatform.com). Certifique-se de que **Banco de dados CDS** e **Aplicativos Dynamics 365** estão habilitados. Para obter mais informações, consulte [Criar e gerenciar ambientes no centro de administração da Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Selecione **Microsoft Dynamics 365 Project Operations** da lista de implantação de aplicativos Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Instalar Project Operations em um ambiente CDS existente

1. Como o [Global ou administrador do Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente na [Central de administração do PowerPlatform](https://admin.powerplatform.com) onde você deseja instalar Project Operations.
2. Instale **Microsoft Dynamics 365 Project Operations** da lista de implantação de aplicativos Dynamics 365. Para obter mais informações, consulte [Gerenciar aplicativos Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).


