---
title: Gerenciar fusos horários
description: Quando um projeto é criado, seu fuso horário é baseado no fuso horário definido no modelo de hora de trabalho aplicado.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d3fc0453e3038839107a98c4179e6bd4aede95cf4a5fcfe2d52f823b83029485
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988682"
---
# <a name="manage-time-zones"></a>Gerenciar fusos horários

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


## <a name="projects"></a>Projetos

Quando um projeto é criado, o fuso horário é baseado no fuso horário definido no modelo de hora de trabalho aplicado. No **Projeto**, as datas são sempre relativas ao fuso horário do usuário que está conectado em cada guia, exceto a guia **Tarefa**. Quando você visualiza a estrutura de detalhamento de trabalho, as datas sempre serão exibidas no fuso horário do projeto.

## <a name="tasks"></a>Tarefas

Quando uma tarefa é criada, a hora de início, hora de término e horas/dia são controlados pelas horas de trabalho do projeto. Por exemplo, se uma tarefa for criada com um projeto cujo fuso horário é -8 PST e tem as seguintes horas de trabalho: 9h00 às 17h00 de segunda a sexta-feira, qualquer tarefa criada sem uma atribuição respeitará a hora de início e hora de término do calendário do projeto.

## <a name="manage-resources-with-time-zones"></a>Gerenciar recursos com fusos horários

Para obter resultados precisos e previsíveis ao usar **Estender reserva**, há dois pré-requisitos principais que devem ser atendidos:  

- O usuário deve configurar o fuso horário de seu dispositivo para corresponder ao fuso horário definido nas **Configurações de personalização** do sistema.
 
  ![Configurações de fuso horário no Windows 10.](media/reconcile-assignments-03.png)

  ![Configurações de fuso horário nas configurações de personalização.](media/reconcile-assignments-04.png)
 
- O recurso reservável deve ter pelo menos um minuto de tempo de trabalho que se sobreponha aos contornos usados para definir a extensão solicitada. Por exemplo, os seguintes recursos com horários de trabalho entre 9h00 e 19h00. 

  ![Comparação de contornos de recursos.](media/reconcile-assignments-05.png)

As listas de tabela a seguir mostra:

- Um modelo de calendário de projeto
- Recurso A: este recurso tem o mesmo calendário e está no mesmo fuso horário do projeto. O horário de início das reservas será 9:00.
- Recurso B: este recurso está localizado em um fuso horário diferente do projeto e começa às 7h00 em seu fuso horário. No entanto, as reservas começarão às 9h, já que é o horário de início mais cedo do contorno da tarefa.
- Recursos C e D: os recursos estão localizados em fusos horários diferentes, ambos diferentes uns dos outros e do projeto, e suas reservas não começam antes de seus respectivos horários de início disponíveis.

|Entity  |Calendário  |
|-|-|
|Modelo de calendário de projeto   | ![calendário de projeto.](media/reconcile-assignments-06.png) |
|Recurso A  | ![Calendário do Recurso A.](media/reconcile-assignments-06.png) |
|Recurso B  |  ![Calendário do Recurso B.](media/reconcile-assignments-07.png) |
|Recurso C  |  ![Calendário do Recurso C.](media/reconcile-assignments-08.png) |
|Recurso D  | ![Calendário do Recurso D.](media/reconcile-assignments-09.png)  |
 
Quando você navegar até a exibição **Reconciliação**, as atribuições de recursos e as faltas de reserva associadas são exibidas.

![Exibição de reconciliação antes da extensão.](media/reconcile-assignments-10.png)

Depois que a funcionalidade de reserva estendida tiver sido usada para cada recurso, as reservas são estendidas com êxito para cada recurso porque as horas de trabalho de cada recurso corresponderam aos contornos da falta.

![Exibição de reconciliação após a extensão da reserva.](media/reconcile-assignments-11.png) 

Observe que uma análise mais detalhada dos detalhes das reservas mostra diferenças na hora de início das reservas. As reservas não começam antes da hora de início do contorno da atribuição nem antes da hora de início disponível do recurso.

![Novas reservas de recursos no quadro de horários.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]