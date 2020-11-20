---
title: Atualizar um projeto
description: Este tópico fornece informações sobre a atualização de projetos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131419"
---
# <a name="update-a-project"></a>Atualizar um projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Veja a seguir um resumo dos campos que podem ser atualizados em um projeto após sua criação e todas as implicações aplicáveis das atualizações.

## <a name="project-detail-fields"></a>Campos de detalhes do projeto

- **Nome**: o título do projeto.
- **Descrição**: uma visão geral do projeto.
- **Cliente**: a empresa para a qual o projeto será entregue.
- **Modelo de calendário**: as horas de trabalho do projeto. Quando o campo é alterado, toda a agenda é recalculada.
- **Moeda**: a moeda do projeto. Este campo é padronizado com base na moeda definida na unidade de contratação. Quando a unidade de contratação é atualizada, o campo também é atualizado.
- **Unidade de Contratação**: a unidade organizacional que representa o grupo ou a divisão da empresa que primariamente é responsável por efetuar vendas e gerenciar a prestação de trabalho e serviços ao cliente. 
- **Gerente de Projeto**: o membro da equipe do projeto que tem autoridade para revisar e aprovar entradas de horas e despesas.

## <a name="estimate-fields"></a>Campos de estimativa

- **Data de Início Estimada**: a data de início do projeto. Quando este campo é atualizado, todas as tarefas no projeto são movidas proporcionalmente com a nova data de início.
- **Data de Término**: a data em que o projeto está programado para terminar.
- **Esforço**: o esforço estimado do projeto. Quando as tarefas são adicionadas ao projeto, este campo não é mais editável.
- **Custo Estimado de Mão de Obra**: o custo estimado da mão de obra do projeto. Quando os custos de mão de obra são adicionadas ao projeto, este campo não é mais editável.
- **Despesas Estimadas**: as despesas estimadas do projeto. Quando as despesas são adicionadas ao projeto, este campo não é mais editável.

## <a name="project-actual-fields"></a>Campos reais do projeto
- **Início Real**: a data de início do projeto.
- **Término Real**: a ser atualizado quando um projeto for concluído.

## <a name="project-status-fields"></a>Campos de status de projetos

- **Status Geral do Projeto**: a integridade geral do projeto fornecida pelo gerente de projeto.
- **Comentários**: uma narrativa sobre a integridade atual do projeto fornecida pelo gerente de projeto.

