---
title: Visão geral do assistente de agendamento
description: Este tópico fornece informações sobre como trabalhar com o assistente de Agenda para reservar recursos.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014102"
---
# <a name="schedule-assistant-overview"></a>Visão geral do assistente de agendamento

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O assistente de Agenda é usado para reservar recursos com base nos requisitos definidos pelo gerente de projeto. O assistente de Agenda depende dos parâmetros fornecidos no requisito de recursos para localizar o recurso. O assistente de Agenda recomenda recursos que atendam aos requisitos relevantes, como janelas de tempo ou habilidades necessárias.

Depois que os recursos adequados são identificados, o gerente de recursos ou de projeto pode reservar o recurso para o trabalho.

## <a name="prerequisites"></a>Pré-requisitos

O assistente de Agenda faz parte da solução Universal Resource Scheduling. Esta solução está incluída e instalada com o Dynamics 365 Project Operations, o Dynamics 365 Field Service e o Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Correspondência entre requisitos e recursos

Um requisito de recurso gerado é baseado em detalhes como:

-   Características
-   Direitos
-   Unidades de negócios
-   Preferências de recurso
-   Contornos de esforço
-   Fuso horário

O assistente de Agenda usa esses detalhes para filtrar recursos.

## <a name="launch-the-schedule-assistant"></a>Iniciar o assistente de Agenda

Existem duas maneiras de iniciar o assistente de Agenda. Se você estiver usando o modo híbrido, na grade de membros da equipe, selecione qualquer membro da equipe com um requisito de recurso não atendido e, em seguida, **Reservar**. Se você estiver usando o modo central, o gerente de recursos encontra e seleciona o recurso.

## <a name="schedule-assistant-filters"></a>Filtros do assistente de agendamento

Depois que o assistente de Agenda é executado, os detalhes do requisito de recurso são exibidos como valores filtrados no painel à esquerda. O gerente de recursos ou o gerente de projeto podem ajustar os resultados alterando os filtros para atender às necessidades de agendamento.

O painel de filtro mostra opções relacionadas ao trabalho, incluindo:

-   Início e término do trabalho
-   Características
-   Direitos
-   Unidades organizacionais
-   Empresa de recursos
-   Tipos de recurso
-   Recursos preferenciais


[!INCLUDE[footer-include](../includes/footer-banner.md)]