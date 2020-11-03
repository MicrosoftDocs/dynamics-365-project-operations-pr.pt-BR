---
title: Conceitos básicos
description: Este tópico fornece informações sobre os conceitos básicos de gerenciamento de recursos no Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1e5e78bbeb1086fada799cf7ac66173e5a563e2d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071652"
---
# <a name="key-concepts"></a>Conceitos básicos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A tabela a seguir define os conceitos básicos usados no aplicativo Dynamics 365 Project Service Automation.

| Conceito                    | Definição |
|----------------------------|------------|
| Membro da equipe do projeto        | Como parte da equipe do projeto, um membro pode ser um recurso nomeado que possui reservas, um recurso nomeado que não possui reservas ou um recurso genérico. Os recursos genéricos não possuem reservas, são locais ao projeto e não possuem restrições de capacidade entre os projetos. |
| Recurso genérico de projeto   | Um espaço reservado de recurso que permite formar uma equipe e fornecer funcionários a um plano de projeto sem precisar conhecer o recurso nomeado. O calendário do projeto é usado como o calendário do recurso genérico. Os recursos genéricos podem ser adicionados a uma equipe de projeto e atribuídos a tarefas. |
| Horas reservadas               | As horas de recursos são reservadas de forma fixa para um projeto a fim de ajudar a garantir que o trabalho seja concluído. As horas reservadas são consumidas da capacidade geral do recurso. As reservas são feitas apenas para recursos nomeados, não para recursos genéricos. |
| Horas atribuídas             | As horas de recursos são atribuídas a tarefas na agenda do projeto. As atribuições podem ser relacionadas a recursos nomeados ou genéricos. As atribuições podem ser independentes das reservas. |
| Horas necessárias             | A capacidade que é necessária, mas que ainda não é atendida por um recurso nomeado. As horas necessárias são relevantes apenas para membros genéricos da equipe que tenham gerado requisitos de recursos. |
| Demanda                     | A carga de trabalho atual e de entrada. No Project Service Automation, a demanda é exibida como requisitos ou solicitações de recursos. |
| Requisito de Recurso       | Uma entidade que é usada para capturar horas necessárias, datas de início e de término, habilidades, geografia e outras dimensões de precificação para os requisitos necessários. Os requisitos de recursos são gerados com base em membros da equipe do projeto ou criados individualmente. |
| Solicitação de recurso           | Uma entidade que é usada como um "envelope" para carregar o requisito de recurso que deve ser atendido por um gerente de recursos. |
| Função padrão de recurso      | A função sob a qual um recurso é agrupado para o cálculo de horas trabalhadas. Presume-se que o recurso tenha as habilidades necessárias para a função e para atingir as horas trabalhadas de destino dessa função. |
| Unidade organizacional de recurso | A unidade organizacional à qual um recurso foi atribuído. |
| Contorno                    | Horas de tarefas, requisitos ou atribuições que são divididas em uma distribuição diária. Por exemplo, uma tarefa de 40 horas com duração de cinco dias pode ser dividida em oito horas por dia ao longo desse período. |
| Exibição Reconciliação        | Uma exibição que mostra as reservas e atribuições de cada membro da equipe do projeto. Essa exibição permite ao gerente de projetos procurar ocorrências de não correspondência entre reservas e atribuições, além de executar ações corretivas caso elas existam. |
| Horas de trabalho                 | Uma entidade que é usada para identificar a capacidade do recurso, além de horas de trabalho e de folga. Essa entidade também é conhecida como calendário de recursos. |
