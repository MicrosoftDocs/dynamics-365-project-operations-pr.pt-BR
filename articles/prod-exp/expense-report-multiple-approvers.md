---
title: Vários aprovadores em um relatório de despesas
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação de várias pessoas.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960593"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Vários aprovadores em um relatório de despesas

Dependendo das políticas de aprovação de despesas da organização, talvez seja necessária a aprovação por mais de uma pessoa de um relatório de despesas enviado por um funcionário. Ao configurar o processo de fluxo de trabalho para aprovação de relatório de despesas, você pode adicionar elementos de fluxo de trabalho que incluem tarefas ou etapas para um ou mais aprovadores de relatório de despesas. Por exemplo, você pode exigir que todos os relatórios de despesas sejam aprovados primeiro pelo gerente do funcionário que enviou o relatório e, depois, pelo coordenador de contas a pagar.

Se você decidir exigir vários aprovadores de relatórios de despesas, poderá adicionar os elementos do fluxo de trabalho de uma das seguintes maneiras:

- Adicione um elemento de aprovação com uma etapa. Por exemplo, a etapa pode exigir que um relatório de despesas seja atribuído a um grupo de usuários e que seja aprovado por 50% dos membros do grupo.
- Adicione um elemento de aprovação com várias etapas. Por exemplo, o elemento de aprovação pode ter as seguintes etapas:

    1. O gerente do funcionário que enviou o relatório de despesas o aprova.
    2. O administrador de contas a pagar verifica os recibos e os itens do relatório de despesas.
    3. O proprietário do orçamento aprova o relatório de despesas.

- Adicione vários elementos de aprovação, cada um com uma etapa. Por exemplo, você pode adicionar um elemento de aprovação separado para cada uma das seguintes etapas:

    1. O gerente do funcionário aprova o relatório de despesas.
    2. O proprietário do orçamento aprova o relatório de despesas.
