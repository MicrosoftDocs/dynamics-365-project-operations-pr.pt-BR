---
title: Reservar recursos nomeados usando requisitos do recurso
description: Este tópico fornece informações sobre como reservar recursos nomeados para um requisito de recurso genérico.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145074"
---
# <a name="book-named-resources-from-resource-requirements"></a>Reservar recursos nomeados usando requisitos do recurso

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

É possível reservar um recurso nomeado para substituir recurso genérico que tenha um requisito de recurso.

1. No PSA (Project Service Automation), na página **Projetos**, clique na guia **Equipe**.
2. Selecione na lista o recurso genérico com um requisito de recurso e clique em **Reservar**. Ou abra o requisito de recurso e clique em **Reservar**.


![Reservando um membro de equipe genérico](media/RM-how-to-14.png)


3. Na página **Assistente de Agendamento**, selecione um recurso nomeado para reservar na equipe do seu projeto e clique em **Reservar**.

![Reservando um membro de equipe genérico usando o assistente de agendamento](media/RM-how-to-15.png)

Quando a reserva é concluída e preenchida por um recurso nomeado, o recurso genérico é substituído pelo recurso nomeado.

![Membro da equipe nomeado substituindo um membro da equipe genérico](media/RM-how-to-16.png)

As atribuições na agenda também são atualizadas com o recurso nomeado.

![Membro da equipe nomeado atribuído a tarefas do projeto](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Preencher um recurso genérico com vários recursos nomeados
Atender a um requisito para um recurso genérico com vários recursos nomeados é semelhante a atribuir um único recurso nomeado. Por exemplo, há uma tarefa com uma duração de cinco dias e 120 horas de esforço. Essa tarefa não pode ser concluída por um recurso que trabalha um dia comum de oito horas em uma semana de cinco dias. 

![Uma tarefa que precisa de 120 horas de esforço em cinco dias](media/RM-how-to-21.png)

O requisito é de 120 horas de engenharia robótica por cinco dias, o que significa 24 horas por dia.

![Requisito por dia](media/RM-how-to-22.png)

Este é um exemplo de quando vários recursos nomeados são necessários para atender a uma solicitação de recurso genérico. Você precisará reservar vários recursos para atender ao requisito.

![Reservando vários recursos para atender ao requisito](media/RM-how-to-23.png)

A principal diferença neste cenário é que o recurso genérico permanece na equipe atribuída à tarefa e os membros da equipe de recurso nomeados reservados não são atribuídos como parte da posição. O gerente de projeto pode atribuir o trabalho conforme apropriado aos recursos nomeados. A exibição **Reconciliação** pode ajudar um gerente de projeto na divisão de reservas entre vários recursos para atribuições de tarefa. Isso não é feito automaticamente porque em qualquer cenário mais complicado do que o exemplo simples acima, em que você tem um pacote de tarefas, por exemplo, compondo o requisito, a intenção de como o gerente de projeto quer atribuir, precisa ser pressuposta pelo sistema. Como o sistema não pode entender a intenção, as chances são de que as suposições sejam diferentes das intencionadas e de que o resultado seja incorreto ou imprevisível. O resultado previsível é que o recurso genérico permaneça atribuído até que o gerente de projeto crie atribuições deliberadamente, com a ajuda da exibição **Reconciliação**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]