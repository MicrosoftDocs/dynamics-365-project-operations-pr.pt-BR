---
title: Implantar o Project Operations - lite
description: Este artigo fornece informações sobre como instalar a implantação do Project Operations lite - gerenciar faturamento pro forma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930304"
---
# <a name="deploy-project-operations---lite"></a>Implantar o Project Operations - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_



O Project Operations oferece suporte a vários modelos de implantação. Para determinar o melhor modelo de implantação, consulte [Tipos de implantação](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implantação, implantação Lite - lidar com faturamento pro forma, resulta em uma implantação apenas de **Dataverse do Project Operations**.

- [Instalar o Project Operations em um novo ambiente do Dataverse](#new)
- [Instalar em um ambiente existente do Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Instalar o Project Operations em um novo ambiente do Dataverse

1. Como administrador [Global ou do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, crie um novo ambiente do Dataverse no [centro de administração do Power Platform](https://admin.powerplatform.com). As opções **Criar um banco de dados para este ambiente** e **Aplicativos do Dynamics 365** devem estar habilitadas. Para obter mais informações, consulte [Criar e gerenciar ambientes no centro de administração da Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Selecione **Microsoft Dynamics 365 Project Operations** na lista de implantação de aplicativos do Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalar o Project Operations em um ambiente existente do Dataverse
1. Certifique-se de que o ambiente não foi configurado com [gravação dupla](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), pois a instalação irá instalar os recursos do [Project Operations para cenários baseados em recursos/itens sem estoque](project-operations-integrated-deployment-overview.md).
2. Como o [Global ou administrador do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente na [Central de administração do PowerPlatform](https://admin.powerplatform.com) onde você deseja instalar Project Operations.
3. Instale o **Microsoft Dynamics 365 Project Operations** a partir da lista de implantação de aplicativos do Dynamics 365. Para obter mais informações, consulte [Gerenciar aplicativos Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
