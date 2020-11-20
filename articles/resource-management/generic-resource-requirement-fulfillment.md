---
title: Atendimento a requisitos de recursos genéricos
description: Este tópico fornece informações sobre como reservar recursos nomeados para um requisito de recurso genérico.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130293"
---
# <a name="generic-resource-requirement-fulfillment"></a>Atendimento a requisitos de recursos genéricos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

É possível reservar um recurso nomeado para substituir recurso genérico que tenha um requisito de recurso.

1. Na página **Projetos**, selecione a guia **Equipe**.
2. Selecione o recurso genérico com um requisito de recurso na lista e selecione **Reservar**. Ou abra o requisito de recurso e selecione **Reservar**.
3. Na página **Assistente de Agendamento**, selecione um recurso nomeado para reservar na equipe do projeto e selecione **Reservar**.

Quando a reserva é concluída e preenchida por um recurso nomeado, o recurso genérico é substituído pelo recurso nomeado.

As atribuições na agenda também são atualizadas com o recurso nomeado.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Preencher um recurso genérico com vários recursos nomeados
Atender a um requisito para um recurso genérico com vários recursos nomeados é semelhante a atribuir um único recurso nomeado. Por exemplo, há uma tarefa com uma duração de cinco dias e 120 horas de esforço. Essa tarefa não pode ser concluída por um recurso que trabalha em um dia comum de oito horas em uma semana de cinco dias. 

O requisito é de 120 horas de engenharia robótica por cinco dias, o que significa 24 horas por dia.

Este é um exemplo de quando vários recursos nomeados são necessários para atender a uma solicitação de recurso genérico. Você precisará reservar vários recursos para atender ao requisito.

A principal diferença neste cenário é que o recurso genérico permanece na equipe atribuída à tarefa e os membros da equipe de recurso nomeados reservados não são atribuídos como parte da posição. O gerente de projeto pode atribuir o trabalho conforme apropriado aos recursos nomeados. A exibição **Reconciliação** pode ajudar um gerente de projeto na divisão de reservas entre vários recursos para atribuições de tarefa. Isso não é feito automaticamente porque em qualquer cenário mais complicado do que o exemplo simples acima, como quando você tem um pacote de tarefas compondo o requisito ou a intenção de como o gerente de projeto deseja atribuir, isso precisa ser pressuposto pelo sistema. Como o sistema não pode entender a intenção, é provável que as suposições sejam diferentes das pretensões e um resultado incorreto ou imprevisível seja obtido. O resultado previsível é que o recurso genérico permaneça atribuído até que o gerente de projeto crie atribuições deliberadamente, com a ajuda da exibição **Reconciliação**.


