---
title: Reservar requisitos de forma flexível
description: Este tópico fornece informações sobre como reservar requisitos de forma flexível.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124084"
---
# <a name="soft-book-requirements"></a>Reservar requisitos de forma flexível

Um requisito de recurso pode ser reservado de forma fixa. Uma reserva fixa cria uma proposta que consome a capacidade de um recurso. A proposta então é enviada de volta ao solicitante para aprovação. Uma reserva flexível provisoriamente adiciona um recurso a uma equipe de projeto e tem um status diferente no Painel de Agendamento, mas não consome a capacidade do recurso. Para reservar um recurso de forma flexível no Painel de Agendamento, defina o campo **Status da Reserva** como **Flexível**.

![Status da reserva definido como Flexível](media/Resource-Management-image77.png)

Quando a guia **Equipe** estiver na exibição **Membros da Equipe Nomeados**, o recurso aparecerá lá. As horas com reserva flexível são relatadas na coluna **Horas com Reserva Flexível**.

![Horas com reserva flexível na exibição Membros da Equipe Nomeados](media/Resource-Management-image78.png)

Os membros da equipe com reserva flexível podem ser atribuídos a tarefas.

![Membro da equipe com reserva flexível atribuído a uma tarefa](media/Resource-Management-image79.png)

Na guia **Reconciliação**, nenhuma reserva é exibida para um recurso com reserva flexível, pois a guia **Reconciliação** considera apenas reservas fixas.

![Recurso com reserva flexível sem reservas na guia Reconciliação](media/Resource-Management-image80.png)

> [!NOTE]
> Não é possível reservar um recurso de forma flexível de um requisito que foi gerado com base em um membro genérico da equipe.

No Painel de Agendamento, uma coloração diferente é usada para reservas flexíveis de um recurso.

![Reservas flexíveis no Painel de Agendamento](media/Resource-Management-image81.png)

Para converter uma reserva flexível em uma reserva fixa, no Painel de Agendamento, clique com o botão direito do mouse na reserva flexível e, em seguida, selecione **Alterar Status** \> **Reserva Fixa** \> **Fixa**.

![Alterar o status da reserva para Fixa](media/Resource-Management-image82.png)

A reserva é alterada, e o status é alterado no Painel de Agendamento. Como o status da reserva agora é **Fixa**, o recurso é exibido como reservado e sua capacidade e disponibilidade são ajustadas.

Você pode usar o mesmo método para cancelar uma reserva fixa ou flexível no Painel de Agendamento.

Para converter um recurso com reserva flexível em um com reserva fixa na guia **Equipe** do projeto, selecione o recurso e, em seguida, selecione **Confirmar**.

![Confirmar comando](media/Resource-Management-image83.png)
