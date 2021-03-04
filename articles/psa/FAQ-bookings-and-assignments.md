---
title: Reservas de recursos e como elas se relacionam com as atribuições de tarefa
description: Este tópico fornece informações sobre como gerenciar recursos nomeados, reservas de recurso e atribuições de tarefa, e como se relacionam entre si.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 0e4eea87bfb059a3c0be8ccbd2914a4d6c3cf46b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149934"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Reservas de recursos e como elas se relacionam com as atribuições de tarefa

[!include [banner](../includes/psa-now-project-operations.md)]

Há duas maneiras de reservar recursos nomeados para uma equipe do projeto e atribuí-los a tarefas do projeto:

- O recurso pode ser reservado diretamente em um projeto e, em seguida, atribuído às tarefas do projeto.
- As tarefas podem ser atribuídas a um recurso genérico, que é usado para encontrar e substituir o genético por um recurso nomeado. 

Nos dois casos, o ato de registrar o recurso reserva a capacidade do recurso.

O gerente de projeto que está planejando o projeto é proprietário do plano e da agenda do projeto. Ao usar o recurso genérico para a atribuição e gerar uma solicitação de recurso com base nele, o gerente de projeto pode reservar recursos no projeto com contornos especificados no plano do projeto. Eles podem reservar recursos para um projeto e atribui-los às tarefas. No entanto, não há uma forma de alinhar os contornos de reserva com os contornos das tarefas. As reservas não afetam a agenda do projeto.

Considere um projeto complexo com várias tarefas de sobreposição onde vários recursos do mesmo tipo precisam trabalhar juntamente. Se um recurso receber um contorno diferente do agregado de suas atribuições, é difícil modificar as tarefas para se encaixar ao contorno dos registros a suas tarefas discretas e seus contornos originais.

No exemplo abaixo, o esforço total necessário pelo mesmo recurso de um conjunto de quatro tarefas é 62 horas durante um período de duas semanas e há um contorno específico. Se o recurso Bob é registrado para 62 horas durante as mesmas duas semanas, mas com um contorno diferente, o requisito e registros estão em alinhamento.

| **Contornos de tarefa**    | **Horas totais** | Seg 4/6 | Ter 5/6 | Qua 6/6 | Qui 7/6 | Sex 8/6 | Sáb 9/6 | Dom 10/6 | Seg 11/6 | Ter 12/6 | Qua 13/6 | Qui 14/6 | Sex 15/6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tarefa 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tarefa 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tarefa 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tarefa 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totais**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Disponibilidade do Bob
| **Reserva de recursos** | **Horas totais** | Seg 4/6 | Ter 5/6 | Qua 6/6 | Qui 7/6 | Sex 8/6 | Sáb 9/6 | Dom 10/6 | Seg 11/6 | Ter 12/6 | Qua 13/6 | Qui 14/6 | Sex 15/6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Entretanto, não existe uma forma sistemática de atribuir o contorno de horas registradas a tarefas por dia. Se o gerente de projeto quiser mudar a agenda do projeto para estar de acordo com a disponibilidade do recurso, então ele terá de remover a atribuição e revisar todas as tarefas para que elas combinem com os contornos registrados.

No caso onde uma organização deu a tarefa de planejamento de projeto para o gerente de projeto ou um gerente de recurso, o gerente de projeto define a agenda, e isso inclui contornar o trabalho necessário. O gerente de recurso não pode afetar a agenda sem o conhecimento do gerente de projeto alterando os contornos de esforço enquanto registra recursos reais. Se o gerenciador do recurso estiver cumprindo algo diferente do que o gerente de projeto solicitou, eles precisam entrar em acordo sobre quais alterações são necessárias na agenda do projeto.

Como as reservas e atribuições não são rigidamente combinadas, é possível reservar contornos que sejam diferentes dos contornos da tarefa ou alterar as atribuições para resultar em circunstâncias onde reservas e atribuições estejam fora de alinhamento.

A **Exibição de Reconciliação** permite que o gerente de projeto veja as reservas e atribuições para cada membro da equipe do projeto. A exibição usa cores e sombreamento para exibir onde há uma má combinação entre registros e atribuições dos membros da equipe. Com base nessas informações, o gerente de projeto pode tomar a ação corretiva para estender os registros de recurso para casos onde há atribuições a nenhum registro, ou cancelar registros onde recursos são registrados, mas onde não há atribuições.

> [!NOTE]
> Se você mover uma tarefa que você mesmo contornou, esses contornos não serão mantidos. Os contornos são registrados de acordo com o calendário do projeto para contar as alterações em horas de trabalho e feriados. Isso é proposital, pois o sistema não sabe da intenção do contorno original e não pode determinar se faz sentido manter esse contorno em um novo período. Como as reservas e atribuições estão desconectadas, as reservas retêm os contornos de reserva originais. Nesse caso, será necessário cancelar e registrar novamente o novo contorno da atribuição.



[!INCLUDE[footer-include](../includes/footer-banner.md)]