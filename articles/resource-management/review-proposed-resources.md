---
title: Revisar recursos propostos
description: Este artigo fornece informações sobre como propor recursos de projeto.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f20dda2b7b384608b8f4b548c18ac21d07fee07
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924830"
---
# <a name="review-proposed-resources"></a>Revisar recursos propostos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os gerentes de recursos podem propor um recurso ao gerente de projetos usando uma solicitação de recurso.

Para revisar os recursos propostos, siga estas etapas:

1. Na grade **Solicitação**, ou na própria solicitação, selecione **Localizar Recursos**.
2. Na página **Assistente de Agenda**, selecione o recurso e, em seguida, confirme se todas as horas propostas estão incluídas na reserva proposta.
3. No painel **Criar Reserva de Recursos**, defina o campo **Status da Reserva** como **Proposta** e, em seguida, selecione **Reservar**.

    > [!NOTE]
    > A configuração do **Status da Reserva** para **Proposta** não reserva definitivamente o recurso e não substitui o recurso genérico pelo membro da equipe nomeado.

    As seguintes atualizações de status ocorrem:

    - Na página **Assistente de Agendamento**, os indicadores de status são atualizados para indicar que a reserva é proposta, não fixa.
    - Na solicitação de recurso, o status é alterado para **Precisa de Revisão**.
    - Na guia **Equipe** do projeto, o valor **Status de Solicitação** do membro genérico da equipe é alterado para **Precisa de Revisão**.

O gerente de projetos pode aceitar ou rejeitar a proposta.

Quando os gerentes de recursos processam solicitações de recursos, eles podem usar qualquer uma das seguintes abordagens:

- Propor vários recursos para satisfazer a demanda caso não haja um recurso único disponível para atender às horas necessárias. As horas propostas então serão divididas entre vários recursos que possam satisfazer as horas necessárias. Nesse cenário, não pode haver sobreposição de horas.
- Propor menos recursos do que o necessário. Nesse cenário, a capacidade do recurso proposta é menor do que as horas necessárias especificadas pelo solicitante. Quando o solicitante aceita os recursos propostos, um requisito de recurso não atendido é criado para capturar a demanda restante.
- Reservar vários recursos para satisfazer a demanda caso não haja um recurso único disponível para concluir o trabalho.
- Reserve menos recursos do que o necessário. Nesse cenário, o número de horas reservadas é inferior ao de horas necessárias. O sistema orienta você a propor recursos em vez de reservas, para que o solicitante possa verificar e acompanhar a demanda restante.

## <a name="resource-availability"></a>Disponibilidade do recurso

Os gerentes de recursos devem exibir a disponibilidade de recursos e atualizar as reservas. Em alguns casos, não há demanda formal (solicitação de recursos). No entanto, um gerente de recursos deve responder a uma demanda não planejada que chega por meio de outros canais, como emails, chamadas telefônicas ou mensagens instantâneas. Os gerentes de recursos usam o **Painel de Agendamento** para atualizar recursos e reservas.

As horas de trabalho do recurso são usadas como base para calcular a disponibilidade de um recurso. As reservas de recursos consomem a capacidade dos recursos.

O **Painel de Agendamento** usa cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, além do status das reservas. Uma configuração no **Painel de Agendamento** permite exibir uma legenda.

Se uma seta que aponta para a direita aparecer ao lado de um recurso reservável individual no **Painel de Agendamento**, o recurso poderá ser expandido para mostrar detalhes do trabalho no qual o recurso está reservado.

Como o Dynamics 365 Project Operations usa o mecanismo Universal Resource Scheduling, se você também tiver o Dynamics 365 Field Service instalado, poderá ver os detalhes das reservas de recursos para projetos, ordens de serviço e qualquer outra entidade à qual você tenha estendido o agendamento.

Para exibir outros detalhes sobre um recurso individual, clique com o botão direito do mouse nele para abrir o cartão de recurso.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
