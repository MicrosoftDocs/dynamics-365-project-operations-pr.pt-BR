---
title: Visão geral da reconciliação de recurso
description: Este tópico fornece informações sobre a garantia de que reservas de recursos e atribuições para projetos estejam alinhadas.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125704"
---
# <a name="resource-reconciliation-overview"></a>Visão geral da reconciliação de recurso

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Para membros da equipe, reservas e atribuições são livremente combinadas. Em outras palavras, os recursos podem ter atribuições, mas nenhuma reserva, ou podem ter reservas, mas nenhuma atribuição. De maneira ideal, reservas e atribuições devem ser alinhadas para que os recursos tenham capacidade confirmada para executar as atribuições de tarefa. No entanto, as reservas podem ser baseadas na disponibilidade e as durações das tarefas podem ser alteradas conforme o projeto continua. Portanto, a livre combinação de reservas e atribuições proporciona flexibilidade.

A guia **Reconciliação** no formulário **Projeto** permite aos gerentes de projeto reconciliar reservas dos membros da equipe e suas atribuições para equipes de projeto.

A guia **Reconciliação** também mostra reservas e atribuições até o nível da atribuição de tarefas individuais para cada membro da equipe. Horas são exibidas em células que representam períodos, desde meses até dias.

A guia também mostra um total líquido geral para o projeto com uma coluna **Total**.

Para cada recurso, a guia calcula a diferença entre as reservas do membro da equipe e um valor acumulado das atribuições de tarefas do membro da equipe. O ideal é que essa diferença seja 0 (zero). Em outras palavras, não deve haver diferença entre as reservas e as atribuições. As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:

- **Falta de reserva** – a falta de reserva ocorre quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, um gerente de projeto pode querer corrigir essa condição estendendo as reservas do recurso para cobrir o déficit.
- **Reservas em excesso** – ocorrem quando um recurso é reservado para o projeto, mas não é atribuído a tarefas. Essa condição pode ser aceitável nos casos onde o recurso foi reservado para o projeto antes da atribuição da tarefa. No entanto, em outros casos, o recurso não foi planejado para ser atribuído a tarefas. Nesses casos, o gerente de projetos deve considerar o cancelamento das reservas do recurso, para que a capacidade possa ser usada em outro projeto.

Em alguns casos, quando você exibe tempo em um nível mais alto do que o nível de dia (por exemplo, o nível de mês), é possível ver uma diferença líquida de zero para um recurso (em outras palavras, reservas = atribuições). No entanto, se você exibir o tempo no nível de semana, será possível ver que há atribuições de zero horas e reservas de 40 horas na primeira semana, mas as atribuições de 40 horas e reservas de zero horas na segunda semana. De modo geral, as reservas e atribuições são reconciliadas, mas elas diferem de uma semana para a outra.

Ao exibir tempo em níveis mais altos, as células na guia **Reconciliação** têm um indicador para informar que há diferenças em níveis mais baixos. Ao clicar duas vezes em uma célula, você pode ampliar para exibir a diferença. É possível clicar com o botão direito do mouse para reduzir. Ao selecionar um recurso e usar o controle **Próxima diferença** na barra de ferramentas da grade, você pode ir para a próxima diferença entre reservas e atribuições para esse recurso. Você pode usar o controle **Diferença anterior** para voltar. Também é possível desativar o indicador de diferença e o comportamento da navegação em **Configurações**.


Se você tiver atribuições de tarefa para um recurso, mas nenhuma reserva, na página **Projetos**, na guia **Reconciliação**, selecione a falta de reserva e, em seguida, **Estender Reserva**. A caixa de diálogo **Estender Reserva** aparece e mostra a reserva que é necessária para suprir a falta do recurso. Ela também mostra as reservas existentes do recurso em todos os projetos ou outras entidades que podem ser agendadas. Se você selecionar **OK** a fim de criar a reserva para o recurso, independentemente da disponibilidade desse recurso, é possível haver reservas em excesso.

O gerente de projeto ou o gerente de recursos pode usar o Quadro de Agendamento para gerenciar situações em que um recurso é reservado em excesso além de sua capacidade.

