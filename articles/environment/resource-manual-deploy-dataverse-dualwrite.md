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
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Implantar manualmente o aplicativo Dataverse do Project Operations com suporte à gravação dupla

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico explica como implantar manualmente o Microsoft Dynamics 365 Project Operations no Microsoft Dataverse, de forma que ele suporte gravação dupla. O Project Operations detecta a configuração do ambiente e adiciona suporte adicional para gravação dupla, se os pré-requisitos forem atendidos.

Durante a implantação por meio do Microsoft Dynamics Lifecycle Services (LCS), se você seguiu as instruções neste tópico, poderá pular a implantação da integração do Microsoft Power Platform (anteriormente conhecido como o ambiente do Common Data Service).

O processo de implantação do Project Operations no Dataverse para que seja compatível com gravação dupla tem quatro etapas principais:

1. [Criar um novo ambiente no Dataverse que suporta gravação dupla](#create).
2. [Adicionar pré-requisitos de gravação dupla ao ambiente](#prerequisites).
3. [Adicionar o aplicativo Dataverse do Project Operations](#dataverse).
4. [Vincular seus ambientes](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Criar um novo ambiente no Dataverse que suporta gravação dupla

Para concluir este procedimento, você deve se conectar como administrador.

1. Abra o [centro de administração do Power Platform](https://admin.powerplatform.com) e entre como administrador.
2. Crie um novo ambiente e dê um nome a ele.
3. Selecione o tipo de ambiente. Se você se inscreveu para a oferta de avaliação, selecione **Avaliação (baseada em assinatura)**.
4. Confirme a região de implantação.
5. Ative a opção **Criar um banco de dados para este ambiente**. 
6. Confirme o idioma e, em seguida, confirme se a moeda corresponde à moeda de seu aplicativo Finance and Operations.
7. Ative a opção **Aplicativos Dynamics 365** e confirme se o campo **Implantar esses aplicativos automaticamente** está definido como **Nenhum**.
8. Adicione um grupo de segurança, se um grupo de segurança for necessário.
9. Selecione **Salvar** para criar o ambiente.
10. Espere até que a implantação seja concluída e o ambiente atinja o estado **Pronto**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Adicionar pré-requisitos de gravação dupla ao ambiente

O suporte de gravação dupla inclui campos adicionais que são adicionados às principais entidades, como a entidade **Empresa**. Se você estiver adicionando suporte de gravação dupla a um ambiente existente, pode ser necessário atualizar os dados para ativar o suporte. Para obter informações sobre como inicializar os dados, consulte [Dados da empresa de bootstrap](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Para obter mais informações sobre gravação dupla, consulte [Requisitos de sistema de gravação dupla](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Conclua este procedimento para adicionar os pré-requisitos de gravação dupla ao seu ambiente.

1. Abra o ambiente que você acabou de criar e vá para **Recurso** \> **Aplicativos do Dynamics 365**.
2. Selecione **Solução principal de gravação dupla** na lista de aplicativos e instale-a.
3. Aguarde até que a instalação seja concluída. Em seguida, selecione **Solução principal de gravação dupla** na lista de aplicativos e instale-a.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Adicionar o aplicativo Dataverse do Project Operations

Você pode concluir este procedimento apenas se tiver concluído os procedimentos anteriores antes de instalar o Project Operations. Durante a instalação, o sistema analisa a configuração do ambiente e adiciona suporte para gravação dupla, se necessário.

1. Abra o ambiente que você criou anteriormente e vá para **Recurso** \> **aplicativos Dynamics 365**.
2. Selecione **Microsoft Dynamics 365 Project Operations** na lista de aplicativos e instale-o.

## <a name="link-your-environments"></a><a name="link"></a>Vincular seus ambientes

Depois que o ambiente do Dataverse for implantado, você pode configurar o link em seu aplicativo do Finance and Operations. Siga as etapas em [Usar o assistente de gravação dupla para vincular seus ambientes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
