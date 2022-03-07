---
title: Copiar um projeto
description: Este tópico fornece informações sobre copiar projetos no Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007177"
---
# <a name="copy-a-project"></a>Copiar um projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Com o Dynamics 365 Project Operations, você pode criar projetos rapidamente selecionando **Copiar Projeto** no formulário **Projetos**. Para copiar um projeto, abra o projeto que deseja copiar e selecione **Copiar projeto**. A ação copiará o seguinte:

- Propriedades do projeto 
- Estrutura de detalhamento de trabalho
- Membros da equipe de projeto
- Estimativas do projeto
- Estimativas de despesas do projeto
- Estimativas de material do projeto

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
- Data de Início Estimada: é a data em que o projeto é criado a partir da cópia.
- Data de Término Estimada: esta data é ajustada com base na data de início do novo projeto que foi feito a partir da cópia.
- Esforço (Horas)
- Custo Estimado da Mão de Obra
- Custo Estimado da Despesa
- Custo Estimado dos Materiais

> [!NOTE]
> Copiar projeto é uma operação de execução prolongada. Os registros do projeto, seus atributos relevantes e muitas entidades relacionadas também são copiados. Devido à natureza de execução prolongada da operação, após o início da cópia, a página do projeto de destino é bloqueada para edição até que a operação de cópia seja concluída.

## <a name="work-breakdown-structure"></a>Estrutura de detalhamento de trabalho

Quando o projeto é copiado, toda a estrutura de detalhamento de trabalho carregada por recurso é copiada. Os recursos nomeados são substituídos por recursos genéricos. Se os recursos nomeados não tiverem as mesmas horas de trabalho que o recurso genérico, a agenda será recalculada e as durações das tarefas poderão mudar.

## <a name="project-team-members"></a>Membros da equipe de projeto

Quando uma equipe de projeto for copiada do projeto de origem, os recursos genéricos são copiados. As atribuições de recursos genéricos também são mantidas, pois estavam no projeto de origem. Os recursos nomeados serão convertidos em membros da equipe genéricos.

## <a name="estimates"></a>Estimativas

Quando o projeto é copiado, as linhas de estimativa de recursos, despesas e materiais são copiadas do projeto de origem. 

Para obter informações sobre como acessar programaticamente Copiar Projeto, consulte [Desenvolver modelos de projeto com Copiar Projeto](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
