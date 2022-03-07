---
title: Criar e atualizar um projeto
description: Este tópico fornece informações sobre a atualização de projetos no Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d0847b5343cf3e353b91eae04c94509f14213ba5
ms.sourcegitcommit: 51224cb3bf7cdeae6614d39fc8d899c83dbad5f2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2021
ms.locfileid: "7678335"
---
# <a name="create-and-update-a-project"></a>Criar e atualizar um projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

A seguir, um resumo dos campos que podem ser atualizados em um projeto após sua criação. Isso também inclui quaisquer implicações aplicáveis com base nessas atualizações.

## <a name="project-detail-fields"></a>Campos de detalhes do projeto

- **Nome**: o título do projeto.
- **Descrição**: uma visão geral do projeto.
- **Cliente**: a empresa para a qual o projeto será entregue.
- **Modelo de calendário**: as horas de trabalho do projeto. Quando o campo é alterado, a agenda inteira é recalculada.
- **Moeda**: a moeda do projeto. O valor padrão para esse campo se baseia na moeda definida na unidade de contratação. Quando a unidade de contratação é atualizada, o campo também é atualizado.
- **Unidade de Contratação**: a unidade organizacional que representa o grupo ou a divisão da empresa que primariamente é responsável por efetuar vendas e gerenciar a prestação de trabalho e serviços ao cliente.  Quando a unidade organizacional do gerente de projeto não estiver definida, esse campo assumirá o valor padrão definido nos parâmetros do projeto.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
