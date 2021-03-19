---
title: Copiar um projeto
description: Este tópico fornece informações sobre copiar projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479505"
---
# <a name="copy-a-project"></a>Copiar um projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Com o Dynamics 365 Project Operations, você pode criar projetos rapidamente selecionando **Copiar Projeto** no formulário **Projetos**. Para copiar um projeto, abra o projeto que deseja copiar e selecione **Copiar projeto**. A ação copiará:

- Propriedades do projeto (a data de início estimada é copiada do projeto de origem)
- A Estrutura de detalhamento de trabalho
- Membros da equipe de projeto
- Estimativas do projeto
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

Para obter informações sobre como acessar programaticamente Copiar Projeto, consulte [Desenvolver modelos de projeto com Copiar Projeto](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
