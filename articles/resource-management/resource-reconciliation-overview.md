---
title: Visão geral da reconciliação de recurso
description: Este tópico fornece informações que ajudarão você a garantir que as reservas de recursos e atribuições para projetos estejam alinhadas.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1542e97955902486d22ca637514e4e121fae70e2b227cafc7020c031061b5f98
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994757"
---
# <a name="resource-reconciliation-overview"></a>Visão geral da reconciliação de recurso

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Para membros da equipe, reservas e atribuições são livremente combinadas. Em outras palavras, os recursos podem ter atribuições, mas nenhuma reserva, ou podem ter reservas, mas nenhuma atribuição. De maneira ideal, reservas e atribuições devem ser alinhadas para que os recursos tenham capacidade confirmada para executar as atribuições de tarefa. No entanto, as reservas podem ser baseadas na disponibilidade e as durações das tarefas podem ser alteradas conforme o projeto continua. Portanto, a livre combinação de reservas e atribuições proporciona flexibilidade.

A guia **Reconciliação** na página **Projetos** permite aos gerentes de projeto reconciliar reservas dos membros da equipe e suas atribuições para equipes de projeto.

A guia **Reconciliação** mostra reservas e atribuições até o nível da atribuição de tarefas individual para cada membro da equipe. As horas são exibidas células que podem representar períodos, desde meses até dias. A guia também mostra um total líquido geral para o projeto com uma coluna **Total**.

Para cada recurso, a guia **Reconciliação** calcula a diferença entre as reservas do membro da equipe e um valor acumulado das atribuições de tarefas do membro da equipe. O ideal é que essa diferença seja 0 (zero). Em outras palavras, não deve haver diferença entre as reservas e as atribuições. As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:

- **Falta de reserva** – a falta de reserva ocorre quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, o gerente de projeto pode querer corrigir essa condição estendendo as reservas do recurso para cobrir o déficit.
- **Reservas em excesso** – ocorrem quando um recurso é reservado para o projeto, mas não é atribuído a tarefas. Essa condição pode ser aceitável nos casos em que o recurso foi reservado para o projeto antes da atribuição da tarefa. No entanto, em outros casos, em que não há um plano para atribuir o recurso às tarefas, o gerente de projetos deve considerar o cancelamento das reservas do recurso. Dessa forma, a capacidade pode ser usada para outro projeto.

Em alguns casos, quando você exibe tempo em um nível mais alto do que o nível de dia (por exemplo, o nível de mês), é possível ver uma diferença líquida de zero para um recurso (em outras palavras, reservas = atribuições). No entanto, se você exibir a hora no nível de semana, será possível ver que há atribuições de zero horas e reservas de 40 horas na primeira semana, mas as atribuições de 40 horas e reservas de zero horas na segunda semana. De modo geral, as reservas e atribuições são reconciliadas, mas elas diferem de uma semana para a outra.

Ao exibir tempo em níveis mais altos, as células na guia **Reconciliação** têm um indicador para informar que há diferenças em níveis mais baixos. Ao tocar duas vezes em uma célula, você pode ampliar para exibir a diferença. É possível clicar e manter selecionado (ou clicar com o botão direito do mouse) para reduzir. Ao selecionar um recurso e usar o controle **Próxima diferença** na barra de ferramentas da grade, você pode ir para a próxima diferença entre reservas e atribuições para esse recurso. Você pode usar o controle **Diferença anterior** para voltar. Também é possível desativar o indicador de diferença e o comportamento da navegação em **Configurações**.

Se você tiver atribuições de tarefa para um recurso, mas nenhuma reserva, na página **Projetos**, na guia **Reconciliação**, selecione a falta de reserva e, em seguida, **Estender Reserva**. A caixa de diálogo **Estender Reserva** que aparece mostra a reserva que é necessária para suprir a falta do recurso. A caixa de diálogo também mostra as reservas existentes do recurso em todos os projetos ou outras entidades que podem ser agendadas. Se você selecionar **OK** a fim de criar a reserva para o recurso, independentemente da disponibilidade desse recurso, é possível haver reservas em excesso.

Reservas que são criadas por meio da ação **Estender reserva** são associadas ao requisito principal do projeto. Quando uma extensão é iniciada, o requisito específico que deve ser estendido não pode ser determinado, porque o recurso pode estar associado a mais de um requisito para o projeto.

O gerente de projeto ou o gerente de recursos pode usar o quadro de agendamento para gerenciar situações em que um recurso é reservado em excesso além de sua capacidade.


[!INCLUDE[footer-include](../includes/footer-banner.md)]