---
title: Criar uma estrutura de detalhamento de trabalho
description: Este tópico explica como criar uma estrutura de detalhamento de trabalho (WBS), incluindo os controles básicos na nova interface de agendamento.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841301"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Criar uma estrutura de detalhamento de trabalho (WBS)

Uma agenda de projeto comunica qual trabalho deve ser concluído, quais recursos farão o trabalho e o período em que o trabalho deve ser concluído. O cronograma reflete qualquer trabalho associado à entrega do projeto dentro do prazo. No Dynamics 365 Project Operations, você cria um cronograma de projeto:

  - Dividir o trabalho em tarefas gerenciáveis.
  - Estimar o tempo necessário para realizar cada tarefa.
  - Definir dependências de tarefa.
  - Definir durações de tarefas.
  - Estimar os recursos genéricos que farão as tarefas. 

O cronograma do projeto é criada na guia **Cronograma** da página **Projeto**.

## <a name="tasks"></a>Tarefas

A primeira etapa na criação de uma agenda de projeto é dividir o trabalho em partes gerenciáveis. O cronograma no Project Operations permite os seguintes recursos:

- Tarefas de contêiner ou resumo
- Tarefas do nó folha

### <a name="summary-tasks"></a>Tarefas de resumo

As tarefas de resumo podem armazenar outras tarefas de resumo ou tarefas de nó folha. Elas não têm esforço de trabalho nem custo próprio. Em vez disso, o esforço de trabalho e custo dessas tarefas são acúmulos do esforço de trabalho e custo das suas tarefas de contêiner. A data de início da tarefa de resumo é a data de início das tarefas de contêiner, e a data de término é a data de término das tarefas de contêiner. O nome de uma tarefa de resumo pode ser editado, mas as propriedades de agendamento, incluindo esforço, datas e duração, não podem ser editadas. Se você excluir uma tarefa de resumo, todas as respectivas tarefas de contêiner também serão excluídas.

### <a name="leaf-node-tasks"></a>Tarefas do nó folha

As tarefas de nó folha representam o trabalho mais granular no projeto. Elas têm um esforço estimado, recursos, datas de início e de término planejadas e uma duração.

## <a name="create-a-task-hierarchy"></a>Criar uma hierarquia de tarefa

### <a name="add-a-task"></a>Adicionar uma tarefa

Conclua as etapas a seguir para adicionar uma ou mais tarefas.

1. Vá para **Projetos** e selecione e abra o registro do projeto para o qual deseja criar um cronograma. 
2. Selecione a guia **Tarefas**. 
3. Selecione **Adicionar nova tarefa**, digite um nome para a tarefa e pressione Enter.
2. Digite outro nome de tarefa e pressione Enter novamente até obter uma lista completa de tarefas.

### <a name="manage-hierarchy-of-a-task"></a>Gerenciar a hierarquia de uma tarefa

Quando uma tarefa é recuada, ela se torna um filho da tarefa que está diretamente acima dela. A ID da agenda da tarefa é recalculada para que seja baseada na ID da agenda de seu novo pai e segue o esquema de numeração de estrutura de tópicos. A tarefa pai agora é uma tarefa de resumo. Portanto, ela se torna um valor acumulado de suas tarefas filho. Quando uma tarefa é promovida, ela não é mais filho da tarefa que foi seu pai. A ID da agenda é então recalculada para que reflita a profundidade e a posição atualizada da tarefa na hierarquia. O esforço, o custo e as datas da tarefa pai anterior são recalculados para que não incluam essa tarefa.

Conclua as etapas a seguir para recuar uma tarefa para a esquerda ou promovê-la.

1. Na página **Projeto**, na guia **Tarefas**, em **Tarefas de resumo**, selecione os três pontos verticais no nome da tarefa e, em seguida, selecione **Criar subtarefa**. 
2. Selecione a tarefa para recuar ou promover. Para selecionar mais de uma tarefa, selecione uma tarefa, pressione e segure Ctrl e selecione mais tarefas.
2. Selecione **Recuar** ou **Promover subtarefa** para mover tarefas abaixo ou acima de tarefas de resumo.

### <a name="move-tasks-up-and-down"></a>Mover tarefas para cima e para baixo

As tarefas podem ser movidas para qualquer nível na estrutura de detalhamento de trabalho de duas maneiras:

- Selecione uma ou mais tarefas e arraste-as para o local desejado.
- Selecione uma ou mais tarefas, clique com o botão direito e selecione **Recortar**, selecione a célula de destino no cronograma e, a seguir, clique com o botão direito e selecione **Colar**.

## <a name="task-attributes"></a>Atributos da tarefa

O nome de uma tarefa descreve o trabalho que deve ser concluído. No Project Operations, os atributos associados a uma tarefa descrevem o cronograma da tarefa e seus requisitos de equipe.

## <a name="schedule-attributes"></a>Atributos da agenda

Os atributos **Esforço**, **Data de início**, **Data de término** e **Duração** definem a agenda para a tarefa.

A tabela a seguir mostra atributos adicionais de cronograma.

| **Nome final de exibição** | **Descrição final** |
| --- | --- |
| Esforço Concluído (Horas) | Trabalho total da tarefa em horas. |
| Duração | Exibe a duração da tarefa em dias. |
| Esforço total | Trabalho total da tarefa em horas. |
| Encerrar | Hora e data de término. |
| % Concluído | A porcentagem de conclusão da tarefa. |
| Bucket do Projeto | O painel de tarefas pode ser agrupado por buckets para que cada um tenha sua própria coluna. |
| Esforço Restante (Horas) | Trabalho restante da tarefa em horas. |
| Iniciada | Hora e data de início. |
| Nome | Nome da tarefa. |
| ID | A ID da tarefa na estrutura de detalhamento de trabalho (WBS). |

## <a name="staffing-attributes"></a>Atributos de pessoal

Os atributos de equipe são acessados pelo campo **Recursos** na agenda. Você pode procurar um recurso existente ou selecionar **Criar** e, no painel **Criação Rápida**, adicionar um membro da equipe do projeto como um novo recurso.

Os campos **Função**, **Unidade de Recursos** e **Nome da Posição** são usados para descrever os requisitos de equipe para a tarefa. Esses atributos de equipe em conjunto com a agenda da tarefa são usados para encontrar recursos disponíveis para realização da tarefa.

   - **Função**: especifique o tipo de recurso que é exigido para realização da tarefa.
   - **Unidade de recursos**: especifique a unidade de onde os recursos para a tarefa devem ser atribuídos. Esse atributo afeta a estimativa de custo e vendas para a tarefa se o custo e a taxa de cobrança para o recurso forem definidos com base nas unidades de recursos.
   - **Nome da posição**: insira um nome amigável para o recurso genérico que sirva como um espaço reservado para o recurso que no fim das contas fará o trabalho.

O campo **Recursos** mantém o nome da posição do recurso genérico ou recurso nomeado quando um é encontrado.

O campo **Categoria** mantém os valores que indicam um tipo mais amplo de trabalho em que a tarefa pode ser agrupada. Esse campo não afeta o agendamento ou a equipe. Em vez disso, o campo é usado apenas para relatórios.

## <a name="task-dependencies"></a>Dependências da tarefa

Você pode usar a agenda no Project Operations para criar relacionamentos antecessores entre as tarefas. O campo **Antecessor** usa um ou mais valores para indicar as tarefas das quais uma tarefa depende. Quando os valores antecessores são atribuídos a uma tarefa, a tarefa pode ser iniciada apenas depois que todas as tarefas predecessoras tiverem sido concluídas. Devido à dependência, a data de início planejada da tarefa é redefinida para a data quando as tarefas predecessoras são concluídas.

O modo de tarefa não tem efeito em atualizações que são feitas nas datas de início e término das tarefas predecessoras/dependentes.

## <a name="accessibility-and-keyboard-shortcuts"></a>Acessibilidade e atalhos de teclado

A grade **Agendar** é totalmente acessível e pode ser usada com leitores de tela como o Narrator, JAWS ou NVDA. Você pode se mover pela área da grade usando as teclas de seta (como no Microsoft Excel), pode usar a tecla Tab para avançar pelos elementos da interface de usuário interativa, bem como usar a tecla de seta para baixo, a tecla Enter ou a barra de espaços para selecionar e abrir os menus suspensos.
