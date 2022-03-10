---
title: Modos de agendamento
description: Este tópico fornece informações sobre os modos de agendamento.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 41e56d01c3cfa62558b10e178085a4408a0aadb023f3f7347a61d121f542bb08
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987737"
---
# <a name="scheduling-modes"></a>Modos de agendamento

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


O Dynamics 365 Project Operations oferece às organizações a possibilidade de definir como elas gerenciam mudanças nas principais variáveis em tarefas dentro da estrutura de detalhamento de trabalho. Com base nas necessidades específicas da organização, os gerentes de projeto podem fazer alterações no modo de agendamento quando um projeto é criado.

Existem três modos de agendamento disponíveis no Project Operations:

  - Duração fixa (este é o modo padrão)
  - Esforço fixo (*Trabalho*)
  - Unidades fixas

Os valores afetados pela definição de um modo de agendamento específico são determinados pela seguinte fórmula:

  Esforço = Duração x Unidades

Ao definir o modo de agendamento de um projeto, você está definindo um desses valores, que não poderá ser alterado. Manter esse valor como uma constante coloca uma prioridade sobre esse valor, o que notifica o sistema para não alterá-lo quando os outros dois valores mudarem. A tabela a seguir fornece informações sobre os impactos da seleção de um modo específico.

| **Nesta tarefa**             | **Se você revisar as unidades**   | **Se você revisar a duração** | **Se você revisar o esforço**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Tarefa de unidades fixas     | A duração é recalculada. | O esforço é recalculado.    | A duração é recalculada. |
| Tarefa de esforço fixo    | A duração é recalculada. | As unidades são recalculadas.    | A duração é recalculada. |
| Tarefa de duração fixa  | O esforço é recalculado.   | O esforço é recalculado.    | As unidades são recalculadas.   |

Para obter mais informações sobre as implicações de um determinado modo, consulte [Alterar o tipo de tarefa para um agendamento mais preciso](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). No tópico, o termo **Trabalho** é usado em vez de **Esforço**.

## <a name="change-the-organizations-scheduling-mode"></a>Alterar o modo de agendamento da organização

Conclua as etapas a seguir para definir o modo de agendamento de uma organização.

1. Acesse **Configurações** \> **Geral** \> **Parâmetros** e, a seguir, selecione o parâmetro do projeto. 
2. Na página **Parâmetros do Projeto**, selecione o modo de agendamento padrão para a organização e defina a capacidade do gerente de projeto de substituir a configuração ao criar um novo projeto.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Alterar a configuração do modo de agendamento em um projeto

Se uma organização permitir que o gerente de projeto substitua o modo de agendamento padrão, o gerente de projeto poderá fazer essa alteração ao criar um novo projeto. No entanto, depois que o projeto for salvo, o modo de agendamento não poderá ser alterado.

## <a name="copied-projects"></a>Projetos copiados

Como um projeto é criado quando a ação de cópia do projeto é executada, o gerente de projeto não pode definir o modo de agendamento. O projeto de destino sempre será padronizado para o modo definido no nível organizacional.

## <a name="copied-tasks"></a>Tarefas copiadas

Quando uma tarefa é copiada de um projeto para outro, a tarefa herda o modo de agendamento do projeto de destino.
