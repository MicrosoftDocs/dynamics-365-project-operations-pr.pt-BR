---
title: Copiar um projeto
description: Este tópico fornece informações sobre como copiar projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907857"
---
# <a name="copy-a-project"></a>Copiar um projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Com o Dynamics 365 Project Operations é possível criar projetos rapidamente usando a ação **Copiar Projeto** no formulário **Projetos**. Para copiar um projeto, selecione um projeto e depois **Copiar**. A ação copiará:

- Propriedades do projeto
- A Estrutura de detalhamento de trabalho
- Membros da equipe de projeto
- Estimativas de projeto
- Estimativas de despesas do projeto

## <a name="project-properties"></a>Propriedades do projeto

Quando o projeto é copiado, os valores nos seguintes campos são copiados:

- Nome
- Descrição
- Cliente
- Modelo de Calendário
- Moeda
- Unidade de Contratação
- Gerente de Projeto
- Status
- Status Geral do Projeto
- Comentários
- Estimativas
- Data de Início Estimada
- Data de Término
- Esforço (Horas)
- Custo Estimado da Mão de Obra
- Custo Estimado da Despesa

## <a name="work-breakdown-structure"></a>Estrutura de detalhamento de trabalho

Quando o projeto é copiado, toda a estrutura de detalhamento de trabalho carregada por recurso é copiada. Os recursos nomeados são substituídos por recursos genéricos. Se os recursos nomeados não tiverem as mesmas horas de trabalho que o recurso genérico, a agenda será recalculada e as durações das tarefas poderão mudar.

## <a name="project-team-members"></a>Membros da equipe de projeto

Quando uma equipe de projeto for copiada do projeto de origem, os recursos genéricos são copiados. As atribuições de recursos genéricos também são mantidas, pois estavam no projeto de origem. Os recursos nomeados serão convertidos em membros da equipe genéricos.

## <a name="estimates"></a>Estimativas

Quando o projeto é copiado, as linhas de estimativa de recursos e de despesas são copiadas do projeto de origem.