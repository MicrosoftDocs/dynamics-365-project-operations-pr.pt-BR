---
title: Desempenho de propostas de fatura do projeto
description: Este tópico fornece informações sobre melhorias de desempenho para propostas de fatura do projeto.
author: Yowelle
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999477"
---
# <a name="project-invoice-proposal-performance"></a>Desempenho de propostas de fatura do projeto

[!include [banner](../includes/banner.md)]

Ao criar uma nova proposta de fatura, você pode encontrar problemas de desempenho à medida que o número de projetos e subprojetos aumenta. Para melhorar o desempenho, está disponível um recurso que reduz o tempo necessário para criar uma nova proposta de fatura para transações de projeto publicadas.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Habilitar melhoria de desempenho da proposta de fatura do projeto
Para habilitar o recurso de aprimoramento de desempenho da proposta de fatura do projeto, conclua as etapas a seguir.

1.  Acesse **Gerenciamento de recursos** > **Todos**. Na lista de recursos, localize **Aprimoramento de desempenho da proposta de fatura do projeto**.
2.  Selecione **Habilitar agora**.
3.  Atualize o navegador e crie uma nova proposta de fatura.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Desative o aprimoramento de desempenho da proposta de fatura do projeto
Conclua as etapas a seguir para desativar o aprimoramento de desempenho da proposta de fatura do projeto.

1.  Acesse **Gerenciamento de recursos** > **Todos**. Na lista de recursos, localize **Aprimoramento de desempenho da proposta de fatura do projeto**.
2.  Selecione **Desabilitar**.
3.  Atualize seu navegador.

> [!NOTE]
> O desempenho da proposta de fatura não pode ser aplicado quando as regras de cobrança estão habilitadas ou os processos em lote estão em execução.
