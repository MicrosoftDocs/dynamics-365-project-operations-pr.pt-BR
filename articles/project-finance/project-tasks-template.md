---
title: Sincronizar tarefas de projetos diretamente do Project Service Automation para o Finance and Operations
description: Este tópico descreve o modelo e a tarefa subjacente usada para sincronizar tarefas de projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749139"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizar tarefas de projetos diretamente do Project Service Automation para o Finance and Operations

[!include[banner](../includes/banner.md)]

Este tópico descreve o modelo e a tarefa subjacente usada para sincronizar tarefas de projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.

> [!NOTE]
> - A integração de tarefas de projeto, as categorias de transação de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.
> - Se você estiver usando a Enterprise Edition 7.3.0, após instalar o KB 4132657 e o KB 4132660, será possível usar os modelos para integrar as tarefas de projeto, as categorias de transação, as estimativas de horas, as estimativas de despesas e os dados reais, além de configurar o bloqueio de funcionalidades. Se você precisar redefinir as distribuições de contabilidade, recomendamos que você também instale o KB 4131710.
> - A integração dos valores reais está disponível na versão 8.0.1 ou posterior.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de dados do Project Service Automation para o Finance

A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Project Service Automation e do Finance. O modelo de integração disponível com o recurso de integração de dados permite transferir dados sobre tarefas de projeto do Project Service Automation para o Finance.

A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation ao Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Modelo e tarefa

Para acessar o modelo, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

O seguinte modelo e as tarefa subjacente são usados para sincronizar tarefas do projeto do Project Service Automation para o Finance:

- **Nome do modelo na integração de dados:** Tarefas do projeto (PSA para Fin and Ops)
- **Nome da tarefa no projeto:** Tarefas do projeto

Antes de que as tarefas de projeto possam ser realizadas, você deve sincronizar contratos de projeto e projetos.

## <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Financeiro                             |
|----------------------------|-------------------------------------|
| Tarefas do Projeto              | Entidade de integração para tarefa de projeto |

## <a name="entity-flow"></a>Fluxo da entidade

As tarefas de projeto são gerenciadas no Project Service Automation e são sincronizadas com o Finance como atividades de projeto.

## <a name="prerequisites-and-mapping-setup"></a>Pré-requisitos e configuração de mapeamento

Antes de que as tarefas de projeto possam ser realizadas, você deve sincronizar contratos de projeto e projetos.

## <a name="power-query"></a>Power Query

Você deverá usar o Microsoft Power Query para Excel para filtrar dados se essa condição for atendida:

- Você tem registros específicos de recursos em uma tarefa de projeto.

Se você precisar usar o Power Query, siga esta diretriz:

- O modelo de tarefas do projeto (PSA para Fin e Ops) tem um filtro padrão que exclui registros específicos de recursos de uma tarefa do projeto, definindo o filtro em **IsLineTask** como **Falso**. Se você criar seu próprio modelo, deverá adicionar esse filtro.

## <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na integração de dados

A ilustração a seguir mostra um exemplo de mapeamentos de tarefas do modelo na integração de dados. O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.

[![Mapeamento de modelo](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
