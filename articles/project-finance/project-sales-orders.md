---
title: Pedidos de vendas de projetos para projetos de tempo e material
description: Este tópico explica como criar pedidos de venda com base em projeto para projetos de tempo e material.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749029"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Pedidos de vendas de projetos para projetos de tempo e material

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Este tópico descreve como criar uma ordem de vendas para um projeto. Pedidos de venda só podem ser criados para projetos do tipo **tempo e material**.

Se um projeto de tempo e material tem várias fontes de financiamento no contrato de projeto, você deve habilitar o parâmetro **Permitir pedidos de vendas para projetos com várias fontes de financiamento** na página **Parâmetros de gerenciamento e contabilidade de projeto**. 

> [!NOTE]
> - O suporte para pedidos de vendas de projetos com várias fontes de financiamento está disponível a partir do aplicativo versão 10.0.2 e superior.
> - O parâmetro para habilitar o suporte para pedidos de vendas de projetos com várias fontes de financiamento será removido na onda de lançamento de abril de 2020, após a qual a funcionalidade estará sempre habilitada.

Você pode criar pedidos de venda baseados em projeto de duas maneiras:

- Vá para o próprio projeto. No Painel de Ação, selecione **Gerenciar > Tarefas de item> Pedido de venda**. As informações do projeto serão padronizadas para o pedido de venda do projeto. Se o contrato do projeto tiver mais de uma fonte de financiamento, você precisará selecionar a fonte de financiamento para definir o cliente para o pedido de venda. Se houver apenas uma fonte de financiamento para o projeto, o cliente será definido automaticamente.
- Vá para a página de lista **Todos os pedidos de vendas** e crie um novo pedido de venda. Você precisará selecionar o projeto para o pedido de venda. Depois que o projeto for selecionado, o cliente será definido a partir da fonte de financiamento ou você precisará selecionar a fonte de financiamento se o contrato do projeto tiver várias fontes de financiamento.

