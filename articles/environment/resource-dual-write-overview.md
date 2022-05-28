---
title: Integração de gravação dupla do Project Operations
description: Este tópico fornece uma visão geral da integração de gravação dupla do Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582742"
---
# <a name="project-operations-dual-write-integration-overview"></a>Visão geral de integração de gravação dupla do Project Operations

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

O Project Operations usa [recursos de gravação dupla](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar dados entre o Microsoft Dataverse e o Dynamics 365 Finance.

A ilustração a seguir mostra como os dados são sincronizados como parte desta integração entre o Dataverse e o Finance.

![Visão geral de fluxos de dados do Project Operations.](./media/ProjectOperationsFlows.jpg)

O Project Operations no Dataverse fornece uma interface de usuário (IU) moderna e extensibilidade fácil sem código/com pouco código usando recursos do Power Platform. Gerentes de projeto, gerentes de recursos, membros da equipe do projeto e outras personas da linha de frente, realizam atividades no Project Operations no Dataverse.

O Project Operations no Finance fornece suporte para contabilidade de projetos e reconhecimento de receita. O Project Operations se conecta à estrutura financeira do Finance para cálculo de impostos, taxas de câmbio, relatórios de dimensão financeira e muito mais. As experiências do contador do projeto se baseiam principalmente no Finance.

A integração do Project Operations consiste na seguinte integração de componentes:


- [Configuração do Project Operations e integração de dados de configuração](resource-dual-write-setup-integration.md) 
- [Estimativas e dados reais do projeto](resource-dual-write-estimates-actuals.md)
- [Faturas do projeto](resource-dual-write-project-invoice.md)
- [Gerenciamento de despesas](resource-dual-write-expense.md)
- [Fatura de fornecedor](resource-dual-write-vendor-invoice.md)
