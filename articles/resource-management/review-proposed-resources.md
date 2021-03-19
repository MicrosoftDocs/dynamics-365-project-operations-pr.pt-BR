---
title: Revisar recursos propostos
description: Este tópico fornece informações sobre como propor recursos de projeto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279259"
---
# <a name="review-proposed-resources"></a>Revisar recursos propostos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os gerentes de recursos podem propor um recurso ao gerente de projetos usando uma solicitação de recurso.

1. Na grade de solicitações ou na própria solicitação, selecione **Localizar Recursos**.
2. Na página **Assistente de Agendamento**, selecione o recurso e, em seguida, no painel **Criar Reserva de Recursos**, no campo **Status da Reserva**, selecione **Reservar**.

As seguintes atualizações de status ocorrem:

- Na página **Assistente de Agendamento**, os indicadores de status são atualizados para indicar que a reserva é proposta, não fixa.
- Na solicitação de recurso, o status é alterado para **Precisa de Revisão**.
- Na guia **Equipe** do projeto, o valor **Status de Solicitação** do membro genérico da equipe é alterado para **Precisa de Revisão**.

O gerente de projetos pode aceitar ou rejeitar a proposta.

Quando os gerentes de recursos processam solicitações de recursos, eles podem usar qualquer uma das seguintes abordagens:

- Propor vários recursos para satisfazer a demanda caso não haja um recurso único disponível para atender às horas necessárias. As horas propostas então serão divididas entre vários recursos que possam satisfazer as horas necessárias. Nesse cenário, não pode haver sobreposição de horas.
- Propor menos recursos do que o necessário. Nesse cenário, a capacidade do recurso proposta é menor do que as horas necessárias especificadas pelo solicitante. Portanto, quando o solicitante aceita os recursos propostos, um requisito de recurso não atendido é criado para capturar a demanda restante.
- Reservar vários recursos para satisfazer a demanda caso não haja um recurso único disponível para concluir o trabalho.
- Reservar menos recursos do que o necessário. Nesse cenário, o número de horas reservadas é inferior ao de horas necessárias. O sistema orienta você a propor recursos em vez de reservas, para que o solicitante possa verificar e acompanhar a demanda restante.

## <a name="resource-availability"></a>Disponibilidade do recurso

É essencial que os gerentes de recursos possam visualizar a disponibilidade de recursos e atualizar as reservas. Em alguns casos, não há demanda formal (solicitação de recurso), mas um gerente de recursos deve responder a uma demanda não planejada recebida por meio de canais como email, telefonema ou mensagem instantânea. Os gerentes de recursos usam o Painel de Agendamento para atualizar recursos e reservas.

As horas de trabalho do recurso são usadas como base para calcular a disponibilidade de um recurso. As reservas de recursos consomem a capacidade dos recursos.

O Painel de Agendamento usa cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, além do status das reservas. Uma das configurações do Painel de Agendamento permite mostrar uma legenda.

Se uma seta que aponta para a direita aparecer ao lado de um recurso reservável individual no Painel de Agendamento, o recurso poderá ser expandido para mostrar detalhes do trabalho no qual o recurso está reservado.

Como o Dynamics 365 Project Operations usa o mecanismo Universal Resource Scheduling, se você também tiver o Dynamics 365 Field Service instalado, poderá ver os detalhes das reservas de recursos para projetos, ordens de serviço e qualquer outra entidade à qual você tenha estendido o agendamento.

Para exibir mais detalhes sobre um recurso individual, clique com o botão direito do mouse nele para abrir o cartão de recurso.



[!INCLUDE[footer-include](../includes/footer-banner.md)]