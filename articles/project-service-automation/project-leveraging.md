---
title: Estimativas e projetos de vendas
description: Este tópico fornece informações sobre como aproveitar a agenda e as estimativas no processo de vendas.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749053"
---
# <a name="sales-estimates-and-projects"></a>Estimativas e projetos de vendas

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durante o processo de vendas, você pode criar estimativas de vendas vinculando um projeto a uma cotação de vendas. Dessa forma, a estimativa determinista pode ocorrer durante o processo de vendas para aproveitar os recursos de estimativa e agendamento do projeto. Se as vendas se consumarem, a agenda que foi usada para fins de estimativa poderá ser usada como a base para mais refinamento do plano de projeto.

## <a name="linking-a-project-to-a-quote-line"></a>Vinculando um projeto a uma linha de cotação

Quando você cria uma linha de cotação baseada em projeto, é possível criar um novo projeto ou associar um projeto existente na página **Linha de Cotação**. 

> ![Formulário de linha de cotação](media/project-8.png)
 
Quando você cria um novo projeto com base nos detalhes da linha de cotação, é possível aproveitar os modelos do projeto. Os modelos do projeto são projetos modelo que representam planos de projeto padrão e estimativas financeiras que são típicas em uma organização. Eles também representam cópias de planos de projeto e estimativas de projetos passados.

> ![Detalhes da linha de cotação](media/project-9.png)
  
Quando você cria o projeto com base na cotação, o projeto é automaticamente associado à linha de cotação.

## <a name="components-of-estimates-in-a-project"></a>Componentes de estimativas em um projeto

Uma agenda permite dividir o trabalho em tarefas, manter uma hierarquia de tarefas, determinar quais recursos são exigidos para concluir uma tarefa e atribuir uma estimativas do esforço que é exigido para concluir a tarefa.

Você pode definir as estimativas de agenda e esforço de trabalho usando os campos na guia **Agendar** da página **Projeto**. Como uma lista de preços é associada ao projeto, as estimativas financeiras são calculadas usando preços de custo e vendas que são definidos na lista de preços.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importando estimativas de um projeto em uma cotação

Após definição de estimativas do projeto, você pode importá-las na linha de cotação. Na página **Detalhes da Linha de Cotação**, selecione na faixa de opções **Importar de estimativas** para resumir as estimativas do projeto por tipo de transação, função ou nível da tarefa.
