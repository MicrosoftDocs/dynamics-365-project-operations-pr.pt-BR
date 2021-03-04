---
title: Alterações no Gerenciamento de recursos (Project Service Automation 3.x)
description: Este tópico fornece informações sobre as alterações na área de Gerenciamento de recursos.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148629"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Alterações no Gerenciamento de recursos (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

As seções deste tópico fornecem informações sobre as alterações feitas na área de Gerenciamento de recursos do Dynamics 365 Project Service Automation versão 3.x.

## <a name="project-estimates"></a>Estimativas de projeto

Em vez de se basearem na entidade **msdyn\_projecttask** (**Tarefa do Projeto**), as estimativas de projeto se baseiam na entidade **msdyn\_resourceassignment** (**Atribuição de Recurso**). As atribuições de recursos se tornaram a "fonte de referência" para preços e agendamento de tarefas.

## <a name="line-tasks"></a>Tarefas de linha

No PSA 3.x, as tarefas de linha são obsoletas (preteridas). As atribuições agora apontam para a tarefa inteira em vez das tarefas de linha.

O exemplo a seguir mostra como uma tarefa chamada "Tarefa de teste" é atribuída aos membros da equipe A e B em versões anteriores do PSA e no PSA 3.x.

- **Antes do PSA 3.x:**

    - Tarefa de teste

        - Tarefa de teste – Tarefa de linha 1

            - Atribuição a A

        - Tarefa de teste – Tarefa de linha 2

            - Atribuição a B

- **PSA 3.x:**

    - Tarefa de teste

        - Atribuição a A
        - Atribuição a B

## <a name="unassigned-assignment"></a>Atribuição não atribuída

No PSA 3.x, uma atribuição não atribuída é aquela que é atribuída a um membro da equipe **NULO** e a um recurso **NULO**. As atribuições não atribuídas podem ocorrer em alguns cenários:

- Se uma tarefa tiver sido criada, mas ainda não tiver sido atribuída a nenhum membro da equipe, uma atribuição não atribuída é sempre criada. 
- Se todos os destinatários em uma tarefa forem removidos, uma atribuição não atribuída é recriada para essa tarefa.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Campos de agendamento na entidade Tarefa do Projeto

Os campos na entidade **msdyn\_projecttask** foram preteridos, movidos para a entidade **msdyn\_resourceassignment** ou agora são referenciados da entidade **msdyn\_projectteam** (**Membro da Equipe do Projeto**).

| Campo preterido em msdyn\_projecttask (Tarefa do Projeto) | Novo campo em msdyn\_resourceassignment (Atribuição de Recurso) | Comentário |
|---|---|---|
| msdyn\_assignedresources | Nenhum(a) | |
| msdyn\_assignedteammembers | Nenhum(a) | |
| msdyn\_numberofresources | Nenhum(a) | |
| msdyn\_scheduledhours | Nenhum(a) | |
| msdyn\_effortcontour | msdyn\_plannedwork | O formato da estrutura de dados JavaScript Object Notation (JSON) que é armazenada no campo foi alterado. |

## <a name="schedule-contour"></a>Contorno de agenda

O contorno de agenda é armazenado no campo **Trabalho Planejado** (**msdyn\_plannedwork**) de cada entidade **Atribuição de Recurso** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Estrutura

A nova estrutura do contorno de agenda consiste em intervalos de tempo flexíveis que são definidos para cada dia da agenda. Cada intervalo de tempo tem as seguintes propriedades:

- **Início** – O início das horas de trabalho do dia, de acordo com o calendário do projeto.
- **Término** – O término das horas de trabalho do dia, de acordo com o calendário do projeto.
- **Horas** – O número de horas atribuídas no dia.

**Exemplo**

Esse exemplo usa um calendário de projeto em que o dia de trabalho é das 9h às 17h no fuso horário UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Agendamento automático e manual

Se uma tarefa é agendada de forma automática, as horas são decrescentes e a duração da tarefa pode ser reduzida.

**Exemplo**

A tarefa a seguir foi agendada automaticamente para 18 horas ao longo de três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Se uma tarefa é agendada de forma manual, as horas são igualmente distribuídas entre todas as datas.

**Exemplo**

A tarefa a seguir foi agendada manualmente para 18 horas ao longo de três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unidade de atribuição

A unidade de atribuição foi preterida no PSA 3.x. As horas de esforço da tarefa agora são igualmente divididas, por dia, entre todos os recursos atribuídos.

**Exemplo**

Nesse exemplo, a tarefa foi atribuída a dois recursos e agendada automaticamente para 36 horas ao longo de três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).

- Atribuição 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Atribuição 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensões de precificação

No PSA 3.x, campos de dimensões de precificação específicos aos recursos (como **Função** e **Unidade Organizacional**) foram removidos da entidade **msdyn\_projecttask**. Esses campos agora podem ser recuperados do membro da equipe do projeto correspondente (**msdyn\_projectteam**) da atribuição de recursos (**msdyn\_resourceassignment**) quando as estimativas do projeto forem geradas. Um novo campo, **msdyn\_organizationalunit**, foi adicionado à entidade **msdyn\_projectteam**.

| Campo preterido em msdyn\_projecttask (Tarefa do Projeto) | Campo de msdyn\_projectteam (Membro da Equipe do Projeto) que é usado no lugar |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Contornos

Os campos de contornos de estimativas e preços foram preteridos na entidade **msdyn\_projecttask**. Eles foram movidos para a entidade **msdyn\_resourceassignment**.

| Campo preterido em msdyn\_projecttask (Tarefa do Projeto) | Novo campo em msdyn\_resourceassignment (Atribuição de Recurso) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Os campos a seguir foram adicionados à entidade **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Os campos a seguir de custo e vendas planejados, reais e restantes não foram alterados na entidade **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]