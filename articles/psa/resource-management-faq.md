---
title: Perguntas frequentes sobre gerenciamento de recursos
description: Este tópico fornece respostas às perguntas frequentes sobre gerenciamento de recursos.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8ce1edf7d7c535271fa8076befd26f092fbd495
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587480"
---
# <a name="resource-management-faq"></a>Perguntas frequentes sobre gerenciamento de recursos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Qual é a diferença entre um membro da equipe e um requisito de recurso?

Um membro da equipe do projeto pode ser atribuído a tarefas, reservado ou reservado em excesso e definido como um aprovador. Um requisito de recurso pode existir sem um membro da equipe do projeto, como uma anotação de rascunho da demanda. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Qual é a diferença entre horas com reserva flexível e propostas?

As horas propostas e as horas com reserva flexível diferem em visibilidade. As horas propostas são visíveis apenas para gerentes de recursos e o gerente de projetos que iniciou a demanda usando uma solicitação de recurso. As horas com reserva flexível são visíveis para qualquer pessoa que tenha acesso ao Painel de Agendamento.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Como posso ver as horas com reserva flexível para recursos em uma equipe?

As reservas flexíveis podem ser feitas ao reservar um requisito de recurso. Os recursos com reserva flexível em uma equipe do projeto aparecem como membros da equipe que possuem horas com reserva flexível. Eles também aparecem no Painel de Agendamento.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Como faço para alterar as horas necessárias e as datas de início e término de um recurso (genérico ou nomeado) que reservei?

Depois de reservar os recursos, selecione **Manter Reservas** para fazer quaisquer alterações necessárias.

## <a name="what-resources-types-does-project-service-automation-support"></a>A quais tipos de recursos o Project Service Automation oferece suporte?

**Usuário** e **Contato** são os únicos tipos de recursos com suporte no Dynamics 365 Project Service Automation. Embora seja possível criar outros tipos de recursos (por exemplo, **Equipamento** e **Grupo**), nenhum caso de uso completo terá suporte para eles.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Qual é a diferença entre uma atribuição e uma reserva?

As atribuições são a atribuição de recursos a tarefas do projeto na agenda do projeto. Os recursos podem ser reais ou genéricos. As reservas são a alocação fixa ou flexível de recursos para um projeto. As reservas fixas consomem a capacidade de um recurso. O ideal é que, para recursos reais, as reservas e atribuições sejam correspondentes, pois elas não diferem. No entanto, o PSA não impõe essa correspondência. A exibição Reconciliação mostra a um gerente de projetos os locais em que as reservas e atribuições de um recurso não correspondem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
