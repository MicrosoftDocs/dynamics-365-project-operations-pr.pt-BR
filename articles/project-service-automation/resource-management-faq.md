---
title: Perguntas frequentes sobre gerenciamento de recursos
description: Este tópico fornece respostas às perguntas frequentes sobre gerenciamento de recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749126"
---
# <a name="resource-management-faq"></a>Perguntas frequentes sobre gerenciamento de recursos

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
