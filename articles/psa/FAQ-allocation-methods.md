---
title: Métodos de alocação de reserva em Project Service Automation
description: Este tópico fornece informações sobre as diferentes maneira de reservar alocações.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: a770a51c2bf05e227367efc834dbff2832a316f617ae4fe22a43572940f43cbe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000832"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Métodos de alocação de reserva em Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Independentemente de adicionar um membro da equipe diretamente a um projeto na guia **Equipe**, ou de reservar um recurso para um projeto ou requisito no Quadro de Agendamento, há alguns métodos diferentes para reservar a alocação que você pode usar. Este tópico explica como cada método funciona e quais métodos podem levar à reserva em excesso de recursos.

## <a name="full-capacity"></a>Capacidade Total 
O método Capacidade Total reserva toda a capacidade do recurso para o intervalo de datas especificado. Por exemplo, se um recurso tiver um calendário definido para trabalhar oito horas por dia, cinco dias da semana, definir uma data de início e de término que cubra cinco dias de trabalho reservará o recurso por 40 horas. O registro referente foi feito sem relação à capacidade restante dos recursos. Se um recurso já estiver reservado para outros projeto durante esse período, as 40 horas serão reservadas como horas adicionais, o que potencialmente levará ao excesso de reserva.

## <a name="remaining-capacity"></a>Capacidade Restante
O método Capacidade Restante só estará disponível quando você reservar diretamente em um projeto usando o Quadro de Agendamento. Esse método agenda a capacidade disponível de recuso dentro da variação de data especificada. Por exemplo, se um recurso tiver uma capacidade de 40 horas por semana e já tiver reservado 10 horas, a reserva para a mesma semana resultará na reserva das 30 horas restantes da capacidade para essa semana.

## <a name="percentage-capacity"></a>Capacidade Percentual
O método Capacidade Percentual reserva o recurso para uma porcentagem da capacidade no intervalo de datas especificado. Por exemplo, se o calendário de um recurso estiver definido para trabalhar oito horas por dia, cinco dias por semana, definir uma data de início e de término que cubra cinco dias de trabalho com 50% da capacidade reservaria o recurso por 20 horas. Neste exemplo, as reservas individuais por dia são distribuídas igualmente no período, quatro horas por dia. O registro referente foi feito sem relação à capacidade restante dos recursos. Se o recurso já estiver reservado durante esse período para outros projeto, as 20 horas serão reservadas como horas adicionais, o que potencialmente levará ao excesso de reserva.

## <a name="evenly-distribute-hours"></a>Distribuir Horas Uniformemente
O método Distribuir Horas Uniformemente reserva o recurso para um número de horas específico, distribuindo o tempo igualmente por dia pelas datas de início e término especificadas. Por exemplo, se você reservar um recurso por 20 horas em um período de cinco dias, esse método distribuirá as 20 horas igualmente em quatro horas por dia. O registro referente foi feito sem relação à capacidade restante dos recursos. Se o recurso já estiver reservado durante esse período para outros projeto, as 20 horas serão reservadas como horas adicionais, o que potencialmente levará ao excesso de reserva.

## <a name="front-load-hours"></a>Distribuição Inicial de Horas
O método Distribuição Inicial de Horas reserva o recurso para um número de horas específico, com distribuição inicial das horas por dia pelas datas de início e término especificadas. A distribuição inicial consome a capacidade disponível de recurso em uma ordem que privilegia o que acontece primeiro. Por exemplo, se a agenda de trabalho de um recurso for de oito horas por dia, cinco dias da semana, e não tiver reservas recentes, reservar o recurso por 20 horas por um período de cinco dias resultará no seguinte padrão de reserva diária: 

|         Reservas          |    Dia 1    |    Dia 2    |    Dia 3    |    Dia 4    |    Dia 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Reservas existentes    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nova Reserva          |    8        |    8        |    4        |    0        |    0        |    20       |

O método de distribuição inicial leva em consideração os registros existentes e a capacidade disponível. Por exemplo, se o mesmo recurso já tiver 20 horas de registros na semana de trabalho, os novos registros consomem a capacidade restante da forma a seguir:

|   Reservas          | Dia 1 | Dia 2 | Dia 3 | Dia 4 | Dia 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| Reservas existentes | 8     | 8     | 4     | 0     | 0     | 20    |
| Nova Reserva       | 0     | 0     | 4     | 8     | 8     | 20    |

Como a capacidade disponível é considerada, você pode receber uma mensagem de erro se o recurso não tiver capacidade restante que possa ser absorvida para o registro. Com esse método, não será possível registrar em excesso.

## <a name="none"></a>Nenhum(a)
O método Nenhum só estará disponível quando você fizer a reserva na guia **Equipe** de um projeto. Este método adiciona o recurso como um membro da equipe no projeto, mas não cria quaisquer registros que absorvem a capacidade do recurso. Este método é usado quando o membro da equipe de gerente de projeto padrão é adicionado quando um projeto é criado. O usuário gerente de projeto que cria o projeto é adicionado por padrão para o projeto, para que o registro da entidade do projeto tenha um dono e para que exista um aprovador no projeto. Como esse usuário não tem reservas, se você quiser reservar o recurso, será possível excluí-lo e adicioná-lo novamente usando um método de alocação diferente, ou adicionar o recurso a tarefas e usar **Estender Reservas** na guia **Reconciliação** a fim de criar reservas para as atribuições.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Métodos de alocação que levam a registros em excesso
Em resumo, os seguintes métodos de alocação levam a registro em excesso se o recurso já estiver comprometido em outros projetos (ou para outras ordens de serviço ou entidades agendáveis):

- Capacidade Total
- Capacidade Percentual
- Distribuir Horas Uniformemente

Ao usar um desses três métodos de alocação, você não será notificado que o recurso está com registros em excesso. Para corrigir a reserva em excesso, será preciso usar o Quadro de Agendamento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]