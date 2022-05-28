---
title: Fluxo de trabalho de gerenciamento de despesas
description: Este tópico explica como usar o sistema de fluxo de trabalho do Microsoft Dynamics 365 Finance para configurar um processo de revisão de relatórios de despesas no Gerenciamento de despesas.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eb4d57194ce2dd7f80d75c2c765f1cfa48b0348
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684235"
---
# <a name="expense-management-workflow"></a>Fluxo de trabalho de gerenciamento de despesas

Você pode usar o sistema de fluxo de trabalho para configurar um processo de revisão para relatórios de despesas no gerenciamento de despesas. Você pode configurar um fluxo de trabalho que usa os seguintes critérios para determinar quem aprova os relatórios de despesas:

- A hierarquia de relatórios de funcionários e limites de aprovação predefinidos
- Aprovação em vários níveis que dá suporte a aprovadores provisórios e um aprovador final
- Dimensões financeiras e responsabilidade do projeto
- Atribuição a usuários ou grupos de usuários específicos

As aprovações de fluxo de trabalho podem ser criadas para relatórios de despesas, requisições de viagem, adiantamentos de dinheiro e recuperação de imposto de valor agregado (IVA).

**Exemplo**

O processo a seguir é um exemplo do fluxo de trabalho de gerenciamento de despesas para um relatório de despesas.

1. Um funcionário cria e salva um relatório de despesas.
2. O funcionário envia o relatório de despesas para aprovação. O aprovador é identificado com base nas regras definidas quando o fluxo de trabalho foi configurado.
3. O aprovador recebe uma notificação de que um relatório de despesas está pronto para aprovação. O aprovador analisa o relatório de despesas e verifica se as seguintes condições foram atendidas:

    - As despesas não violam políticas de despesas. Se uma despesa violar uma política, o aprovador verificará se o relatório de despesas inclui uma justificativa comercial válida.
    - Os recibos eletrônicos são anexados ao relatório de despesas.

4. O aprovador aprova o relatório de despesas.
5. O relatório de despesas é atribuído ao coordenador de contas a pagar para postagem.
6. Uma das seguintes etapas ocorre, dependendo se a postagem automática está configurada:

    - Se a postagem automática estiver configurado, o relatório de despesas será processado para pagamento e o status do relatório de despesas será atualizado.
    - Se a postagem automática não estiver configurada, o coordenador de contas a pagar verificará se todos os recibos originais foram enviados e se os recibos estão alinhados com as despesas no relatório de despesas. Todos os códigos de imposto inseridos no relatório de despesas também devem ser verificados como corretos.

Após a verificação desses requisitos, o relatório de despesas é postado.

Depois que o relatório de despesas é postado, o pagamento é autorizado para o relatório de despesas e o funcionário é reembolsado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]