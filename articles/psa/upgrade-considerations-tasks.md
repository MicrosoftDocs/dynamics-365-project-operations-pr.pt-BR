---
title: Considerações sobre atualização para a estrutura de detalhamento de trabalho
description: Este tópico fornece informações sobre a atualização da estrutura de detalhamento de trabalho do Project Service Automation 2.x para 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951330"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Considerações sobre atualização para a estrutura de detalhamento de trabalho

[!include [banner](../includes/psa-now-project-operations.md)]

Este tópico fornece informações sobre a atualização da estrutura de detalhamento de trabalho do Project Service Automation 2.x para 3.x. Este tópico define o estado íntegro de um projeto no Project Service Automation (PSA) necessário para uma atualização bem-sucedida. Há também informações sobre as condições de bloqueio comuns que causarão falhas na atualização. Para obter mais informações sobre como definir tarefas do projeto e suas funções em uma agenda do projeto, consulte [Agendas de projeto](project-creating.md).

## <a name="key-entities"></a>Entidades principais
Para uma estrutura de detalhamento de trabalho precisa que já esteja carregada com recursos, são necessárias as seguintes entidades:

- [Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Equipe do Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Tarefa do Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Atribuições de Recursos](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dependência de Tarefa do Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Recursos Reserváveis](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Para definir uma estrutura de detalhamento de trabalho carregada por recurso, você deve concluir as seguintes etapas:

1. Crie um projeto. Para obter mais informações sobre como criar um projeto, consulte [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Crie uma ou mais tarefas. Para obter mais informações sobre como criar uma tarefa, consulte [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Defina as dependências da tarefa. Para mais informações, consulte [Dependência da tarefa do projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Atribua membros da equipe do projeto para o projeto. Para obter mais informações, consulte [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Atribua membros da equipe do projeto para as tarefas. Para obter mais informações, consulte [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relações da equipe do projeto

Para garantir uma atualização bem-sucedida, os seguintes relacionamentos devem ser mantidos corretamente:
- Todos os membros da equipe do projeto devem estar associados a um recurso que pode ser reservado.
- Todos os membros da equipe do projeto devem estar associados ao mesmo projeto. 

## <a name="project-task-relationships"></a>Relações de tarefas do projeto
Para garantir uma atualização bem-sucedida, os seguintes relacionamentos devem ser mantidos corretamente:

- Todas as tarefas relacionadas devem ser associadas ao mesmo projeto.
- Toda tarefa de linha deve ter uma tarefa pai.
- Toda tarefa deve ter um projeto pai.

### <a name="valid-conditions"></a>Condições válidas

- Todas as durações de tarefa devem ser maiores ou iguais a (>=) uma hora e inferiores a 1.800.000 minutos (1.250 dias).*
- Todas as tarefas devem ter uma data de início não anterior a 2000/01/01.*
- Todas as tarefas devem ter uma data de início, de no máximo 17 anos a partir do dia atual.*
- Todas as tarefas devem ter uma data de início anterior ou igual à data de término.
- Todos os tipos de transação nas classificações (despesa, material, imposto e hora) devem ter valores para **Unidade Padrão** e **Grupo de Unidades**.
- Os formatos de data com letras devem ser evitados.

### <a name="potential-mitigation-steps"></a>Etapas de mitigação potencial
- Use a Localização Avançada para identificar tarefas do Projeto que não contêm uma ID do Projeto.
- Use a Localização Avançada para identificar tarefas do Projeto em que a duração agendada é maior que 1.800.000.
- Antes de fazer alterações nos dados, você deve investigar personalizações associadas à entidade que possam ter levado os dados a um estado ruim. Essas personalizações devem ser abordadas antes de prosseguir com as atualizações relacionadas a dados.
- Para as tarefas identificadas que ficaram órfãs, considere excluí-las se não forem necessárias ou se devessem estar associadas ao projeto pai correto.
- Para tarefas cuja duração seja maior que 1.250 dias, considere adicionar várias tarefas para representar a duração total, se possível.

> [!NOTE]
> Os itens anotados com um asterisco (\*) têm limites porque o CRM oferece suporte a apenas a 7.320 expansões de recorrência. Você deve permanecer abaixo desse limite.

## <a name="resource-assignment-relationships"></a>Relações de atribuição de recursos
Para garantir uma atualização bem-sucedida, os seguintes relacionamentos devem ser mantidos corretamente:

- Todas as atribuições de recursos em uma estrutura de detalhamento de trabalho devem estar relacionadas ao mesmo projeto.
- Todas as atribuições de recursos em uma estrutura de detalhamento de trabalho devem ser associadas aos membros da equipe do projeto no mesmo projeto.

### <a name="potential-mitigation-steps"></a>Etapas de mitigação potencial
- Identifique todas as tarefas que estão fora das condições descritas acima.  
- As atribuições de recursos que não sejam mais válidas devem ser excluídas.

## <a name="project-task-dependency-relationships"></a>Relacionamentos de dependência de tarefas do projeto
Para garantir uma atualização bem-sucedida, os seguintes relacionamentos devem ser mantidos corretamente:

- Todas as dependências de tarefa do projeto devem estar relacionadas ao mesmo projeto.
- Uma tarefa não pode ter a mesma dependência referenciada mais de uma vez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]