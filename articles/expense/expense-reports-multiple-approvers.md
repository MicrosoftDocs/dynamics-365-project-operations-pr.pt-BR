---
title: Relatórios de despesas e vários aprovadores
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação de mais de uma pessoa.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071431"
---
# <a name="expense-reports-and-multiple-approvers"></a>Relatórios de despesas e vários aprovadores

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Dependendo das políticas de aprovação de despesas da organização, talvez seja necessária a aprovação por mais de uma pessoa de um relatório de despesas enviado. Ao configurar o processo de fluxo de trabalho para aprovação de relatório de despesas, você pode adicionar elementos de fluxo de trabalho que incluem tarefas ou etapas para um ou mais aprovadores de relatório de despesas. Por exemplo, você pode exigir que todos os relatórios de despesas sejam aprovados por duas pessoas diferentes, o gerente do funcionário que enviou o relatório e o coordenador de contas a pagar.

Se você decidir exigir vários aprovadores de relatórios de despesas, poderá adicionar os elementos do fluxo de trabalho de uma das seguintes maneiras:

- Adicione um elemento de aprovação com uma etapa. Por exemplo, a etapa pode exigir que um relatório de despesas seja atribuído a um grupo de usuários e que seja aprovado por 50% dos membros do grupo.
- Adicione um elemento de aprovação com várias etapas. Por exemplo, o elemento de aprovação pode ter as seguintes etapas:

    1. O gerente do funcionário que enviou o relatório de despesas o aprova.
    2. O administrador de contas a pagar verifica os recibos e os itens do relatório de despesas.
    3. O proprietário do orçamento aprova o relatório de despesas.

- Adicione vários elementos de aprovação, cada um com uma etapa. Por exemplo, você pode adicionar um elemento de aprovação separado para cada uma das seguintes etapas:

    1. O gerente do funcionário aprova o relatório de despesas.
    2. O proprietário do orçamento aprova o relatório de despesas.
