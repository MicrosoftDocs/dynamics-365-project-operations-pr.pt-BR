---
title: Implantar o Project Operations Lite
description: Este artigo fornece informações sobre como instalar a implantação do Project Operations lite - gerenciar faturamento pro forma.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810964"
---
# <a name="deploy-project-operations-lite"></a>Implantar o Project Operations Lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_



O Project Operations oferece suporte a vários modelos de implantação. Para determinar o melhor modelo de implantação, consulte [Tipos de implantação](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implantação, implantação Lite - lidar com faturamento pro forma, resulta em uma implantação apenas de **Dataverse do Project Operations**.

- [Instalar o Project Operations em um novo ambiente do Dataverse](#new)
- [Instalar em um ambiente existente do Dataverse](#existing)
- [Instalar em um ambiente do Dataverse existente que tenha componentes de gravação dupla](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Instalar o Project Operations Lite em um novo ambiente do Dataverse

1. Como administrador [Global ou do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, crie um novo ambiente do Dataverse no [centro de administração do Power Platform](https://admin.powerplatform.com). As opções **Criar um banco de dados para este ambiente** e **Aplicativos do Dynamics 365** devem estar habilitadas. Para obter mais informações, consulte [Criar e gerenciar ambientes no centro de administração da Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Selecione **Microsoft Dynamics 365 Project Operations** na lista de implantação de aplicativos do Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalar o Project Operations Lite em um ambiente existente do Dataverse 
1. Como o [Global ou administrador do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente na [Central de administração do PowerPlatform](https://admin.powerplatform.com) onde você deseja instalar Project Operations.
1. Instale o **Microsoft Dynamics 365 Project Operations** a partir da lista de implantação de aplicativos do Dynamics 365. Para obter mais informações, consulte [Gerenciar aplicativos Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Instalar o Project Operations Lite em um ambiente existente do Dataverse onde as soluções de gravação dupla já estão presentes

Se você quiser continuar executando o Project Operations no modo de implantação do Lite, siga estas etapas:

1. Como o [Global ou administrador do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente na [Central de administração do PowerPlatform](https://admin.powerplatform.com) onde você deseja instalar Project Operations.
1. Instale o **Microsoft Dynamics 365 Project Operations** a partir da lista de implantação de aplicativos do Dynamics 365. Para obter mais informações, consulte [Gerenciar aplicativos Dynamics 365](/power-platform/admin/manage-apps).
1. Como seu ambiente possui componentes de gravação dupla que ajudam na integração com aplicativos de finanças e operações instalados, a instalação do Project Operations também instalará os recursos e extensões necessários para integrar os dados relacionados ao Project aos aplicativos de finanças e operações. Como você deseja executar o Project Operations na implantação do Lite, esses componentes de integração devem ser removidos, pois criarão restrições e sobrecarga para os cenários de implantação do Lite. Desinstale manualmente as soluções **Gravação dupla do Dynamics 365 Project Operations** e **Mapas de entidades de gravação dupla do Dynamics 365 Project Operations** para remover esses componentes.
1. Vá para **Project Operations -> Configurações -> Parâmetros**. Abra a página de detalhes **Parâmetro do Projeto** e defina o campo **Comportamento da atualização da solução** como **Somente Lite**. Isso garante que quaisquer atualizações subsequentes do Project Operations não trarão de volta os componentes de integração para o Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
