---
title: Visão geral do Project Service Automation
description: Este tópico fornece informações sobre o Dynamics 365 Project Service Automation para a solução de integração do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749097"
---
# <a name="project-service-automation-overview"></a>Visão geral do Project Service Automation

[!include[banner](../includes/banner.md)]

A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Dynamics 365 Finance e do Dynamics 365 Project Service Automation por meio do Common Data Service. Os modelos de integração disponíveis com o recurso de integração de dados permitem transferir fluxo de projeto, contratos de projetos, linhas de contrato de projetos, etapas da linha de contrato de projeto, tarefas de projeto, categorias de transação de despesas, estimativa de horas e estimativa de despesas do Project Service Automation para o Finance.

> [!NOTE]
> - Se estiver usando a versão 7.3.0, você precisará instalar o KB 4074835. Você poderá então integrar projetos de preço fixo.
> - Se você estiver usando a versão 7.3.0 e estiver transferindo as transações de taxa do Project Service Automation, instale o KB 4345320 para incluir essas taxas na fatura do projeto.
> - Se você estiver usando a versão 8.0, você será capaz de usar a integração de tarefas de projeto, as categorias de transação de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades.
> - Se estiver usando a versão 8.0.1 ou posterior, você poderá sincronizar dados reais.

Antes de poder integrar o Project Service Automation Finance, você deve configurar os parâmetros de integração do Project Service Automation. Para obter mais informações, consulte [Parâmetros de integração do Project Service Automation](PSA-parameters.md).

Esta solução de integração permite a sincronização direta nos seguintes cenários:

- Manter contratos de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.
- Criar projetos no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.
- Manter linhas de contrato de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.
- Manter etapas de linhas de contrato de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.
- Manter tarefas de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.
- Manter categorias de transação de despesas no Finance e sincronizá-los diretamente do Finance para o Project Service Automation.
- Criar estimativas de hora de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.
- Criar estimativas de despesas de projeto no Project Service Automation e sincronizá-los diretamente do Project Service Automation para o Financeiro.
- Criar horas do projeto, despesas e taxas efetivas no Project Service Automation e criar transações do projeto no diário de integração do Project Service Automation para que possam ser postadas em Finance.

## <a name="data-synchronization"></a>Sincronização de dados

A ilustração a seguir mostra como os dados são sincronizados como parte da integração entre o Project Service Automation e o Finance.

> [!NOTE]
> Nem todos os modelos estão disponíveis atualmente. Os modelos serão lançados assim que forem concluídos.

[![Integração do Project Service Automation ao Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Requisitos de sistema para finanças

Para usar a solução de integração Project Service Automation to Finance, você deve instalar Enterprise Edition 7.3 com atualização 12 da plataforma ou posterior.

## <a name="system-requirements-for-project-service-automation"></a>Requisitos do sistema para Project Service Automation

Para usar a solução de integração Project Service Automation to Finance, você deve instalar os seguintes componentes:

- Dynamics 365 Project Service Automation versão 9.0.0.0 ou posterior
- Solução de perspectiva de caixa para o Dynamics 365 Sales, versão 1.14.0.0 (v14) ou posterior
- Automação de serviços de projeto para solução de finanças para Dynamics 365 Project Service Automation versão 1.0.0.0 ou posterior

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instale a solução de integração do Project Service Automation para o Finance em sua instância do Project Service Automation

Baixe a solução de integração de Project Service Automation to Finance em [Centro de Download da Microsoft ](https://www.microsoft.com/download/details.aspx?id=57016) e siga as instruções que acompanham a solução.
