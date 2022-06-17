---
title: Dados reais
description: Este artigo fornece informações sobre como trabalhar com dados reais no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924784"
---
# <a name="actuals"></a>Dados reais

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os dados reais representam o progresso financeiro revisado e aprovado e da agenda em um projeto. Eles são criados quando entradas de hora, despesa e uso de material, entradas de diário e faturas são aprovadas.

> [!IMPORTANT]
> Os dados reais não devem ser editados nem excluídos do sistema. Do contrário, a integridade financeira e a integração com outros sistemas financeiros e contábeis podem ser afetadas negativamente. O Microsoft Dynamics 365 Project Operations permite que você use a reversão e a substituição de dados reais para editar esses dados em vários pontos do ciclo de vida do processo empresarial de seus projetos.

## <a name="recording-actuals-based-on-project-events"></a>Registrando dados reais baseados em eventos do projeto

O Project Operations registra as transações financeiras que ocorrem durante o ciclo de vida de um compromisso de projeto como dados reais. A criação de dados reais em vários eventos no ciclo de vida varia, dependendo se o compromisso do projeto usa o modelo de cobrança de tempo e material ou o modelo de cobrança de preço fixo e se está na fase de pré-venda ou se é um projeto interno.

Os seguintes artigos explicam o impacto na tabela Dados reais em vários eventos para diferentes variações:

- [Impacto dos dados reais em um compromisso de tempo e material](ActualsonTM.md)
- [Impacto dos dados reais em um compromisso de preço fixo](ActualonFP.md)
- [Impacto dos dados reais durante a fase de pré-venda de um compromisso](ActualonPreSales.md)
- [Impacto dos dados reais de um projeto interno](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
