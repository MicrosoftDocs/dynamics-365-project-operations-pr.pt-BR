---
title: Desempenho de propostas de fatura do projeto
description: Este artigo fornece informações sobre melhorias de desempenho para propostas de fatura do projeto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927176"
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
> O desempenho da proposta de fatura não pode ser aplicado quando as regras de faturamento estão habilitadas.
> 
> Durante o processo em lote para criar propostas de fatura, o número de subtarefas dividirá as tarefas em um número máximo com base no número de contratos com transações faturáveis, independentemente do que você inseriu. Por exemplo, se você inserir **3** para o número de subtarefas para criação de proposta de fatura em lote, e houver apenas dois contratos com transações faturáveis, apenas duas subtarefas serão criadas.
