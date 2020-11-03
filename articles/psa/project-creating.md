---
title: Agendas de projeto
description: Esse tópico fornece informações sobre como criar uma agenda.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071463"
---
# <a name="project-schedules"></a>Agendas de projeto 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Uma agenda de projeto comunica qual trabalho deve ser concluído, quais recursos farão o trabalho e o período em que o trabalho deve ser concluído. Ela reflete todo o trabalho que é associado à entrega do projeto no prazo. No Dynamics 365 Project Service Automation, você cria uma agenda de projeto dividindo o trabalho em tarefas gerenciáveis, estimando o tempo que é necessário para cada tarefa, configurando as dependências da tarefa, configurando durações das tarefas e estimando os recursos genéricos que executarão as tarefas. A agenda de projeto é criada na guia **Agendar** da página do projeto.
 
## <a name="tasks"></a>Tarefas

A primeira etapa na criação de uma agenda de projeto é dividir o trabalho em partes gerenciáveis. A agenda no PSA permite os seguintes recursos:

- Nó raiz do projeto
- Tarefas de contêiner ou resumo
- Tarefas do nó folha

### <a name="project-root-node"></a>Nó raiz do projeto

O nó raiz do projeto é a tarefa de resumo de nível superior do projeto. Todas as outras tarefas do projeto são criadas nele. O nome do nó raiz sempre é definido para o nome do projeto. O esforço, as datas e a duração do nó raiz são resumidos com base nos valores da hierarquia abaixo deles. Você não pode editar as propriedades do nó raiz. Você também não pode excluir o nó raiz.

### <a name="summary-or-container-tasks"></a>Tarefas de contêiner ou resumo 

As tarefas de resumo têm subtarefas ou tarefas de contêiner abaixo delas. Elas não têm esforço de trabalho nem custo próprio. Em vez disso, o esforço de trabalho e custo dessas tarefas são acúmulos do esforço de trabalho e custo das suas tarefas de contêiner. A data de início da tarefa de resumo é a data de início das tarefas de contêiner, e a data de término é a data de término das tarefas de contêiner. O nome de uma tarefa de resumo pode ser editado, mas as propriedades de agendamento (esforço, datas e duração) não podem ser editadas. Se você excluir uma tarefa de resumo, todas as respectivas tarefas de contêiner também serão excluídas.

### <a name="leaf-node-tasks"></a>Tarefas do nó folha

As tarefas de nó folha representam o trabalho mais granular no projeto. Elas têm um esforço estimado, recursos, datas de início e de término planejadas e uma duração.
 
## <a name="creating-a-task-hierarchy"></a>Criando uma hierarquia de tarefa

Você pode criar uma hierarquia de tarefas usando as seguintes opções:

- Botão **Adicionar tarefa**
- Botão **Recuar tarefa**
- Botão **Recuar tarefa para a esquerda**
- Botões **Mover para cima** e **Mover para baixo**
- Acessibilidade e atalhos de teclado

### <a name="add-task"></a>Adicionar tarefa

O botão **Adicionar tarefa** permite criar uma nova tarefa na hierarquia. Se você não selecionar uma posição, a tarefa será inserida no final. 

A ID da agenda é atribuída a cada tarefa. A ID da agenda representa a profundidade e a posição da tarefa na hierarquia. Ela usa numeração de estrutura de tópicos. Para tarefas no primeiro nível sob o nó raiz do projeto, um esquema de numeração 1, 2, 3... é usado. Para tarefas sob o primeiro nível, um esquema de numeração 1.1, 1.2, 1.3... é usado.

### <a name="indent-task"></a>Recuar tarefa

Quando uma tarefa é recuada, ela se torna um filho da tarefa que está diretamente acima dela. A ID da agenda da tarefa é recalculada para que seja baseada na ID da agenda de seu novo pai e segue o esquema de numeração de estrutura de tópicos. A tarefa pai agora é uma tarefa de resumo ou uma tarefa de contêiner. Portanto, ela se torna um valor acumulado de suas tarefas filho.

### <a name="outdent-task"></a>Recuar tarefa para a esquerda 

Quando uma tarefa é recuada para a esquerda, ela não é mais filho da tarefa que foi seu pai. A ID da agenda é então recalculada para que reflita a profundidade e a posição atualizada da tarefa na hierarquia. O esforço, o custo e as datas da tarefa pai anterior são recalculados para que não incluam essa tarefa.

### <a name="move-up-and-move-down"></a>Mover para cima e mover para baixo 

Os botões **Mover para cima** e **Mover para baixo** mudam a posição de uma tarefa em sua hierarquia pai. As alterações desse tipo não afetam o esforço, o custo, as datas ou a duração da tarefa. Somente a ID da agenda da tarefa é afetada. A ID da agenda é recalculada para que reflita a nova posição da tarefa na lista de tarefas filho do pai.

### <a name="accessibility-and-keyboard-shortcuts"></a>Acessibilidade e atalhos de teclado

A grade **Agendar** é totalmente acessível e pode ser usada com leitores de tela como o Narrator, JAWS ou NVDA. Você pode se mover pela área da grade usando as teclas de seta (como no Microsoft Excel), pode usar a tecla Tab para avançar pelos elementos da interface de usuário interativa, bem como pode usar a tecla de Seta para baixo, a tecla Enter ou a barra de espaços para selecionar e invocar os menus suspensos. Os cabeçalhos de coluna também são interativos. É possível ocultar e mostrar colunas, usar a tecla Tab e teclas de direção para se mover pelos cabeçalhos de coluna e usar os botões de ação na barra de ferramentas. Além disso, você pode usar os seguintes atalhos de teclado:

- **Atualizar** : ALT+SHIFT+F5
- **Adicionar** : ALT+SHIFT+Insert
- **Excluir** : ALT+SHIFT+Delete
- **Mover para cima/baixo** : ALT+SHIFT+Setas para Cima/Baixo
- **Recuar/Recuar para a esquerda** : ALT_SHIFT+Setas para a Esquerda/Direita
- **Expandir/Recolher Hierarquias** : ALT+SHIFT+Teclas de Mais/Menos

## <a name="task-attributes"></a>Atributos da tarefa

O nome de uma tarefa descreve o trabalho que deve ser concluído. No PSA, os atributos associados a uma tarefa descrevem a agenda da tarefa e seus requisitos de equipe.

> ![Atributos da tarefa](media/project-2.png)
 
### <a name="schedule-attributes"></a>Atributos da agenda

Os atributos **Esforço** , **Data de início** , **Data de término** e **Duração** definem a agenda para a tarefa.

Os atributos de agenda adicionais incluem:

- **Horas de esforço** : insira uma estimativa das hora que são necessárias para concluir a tarefa. 
- **Duração** : especifique o número de dias de trabalho que são necessários para concluir a tarefa.
- **ID da Agenda** : essa ID gerada automaticamente é usada para ordenar tarefas na hierarquia. As dependências entre as tarefas gerenciam a ordem real na qual as tarefas são trabalhadas.
 
### <a name="staffing-attributes"></a>Atributos de pessoal

Os atributos de equipe são acessados pelo campo **Recursos** na agenda. Você pode procurar um recurso existente ou clicar em **Criar** e, no painel **Criação Rápida** , adicionar um membro da equipe do projeto como um novo recurso.

Os campos **Função** , **Unidade de Recursos** e **Nome da Posição** são usados para descrever os requisitos de equipe para a tarefa. Esses atributos de equipe em conjunto com a agenda da tarefa são usados para encontrar recursos disponíveis para realização da tarefa.

**Função** – especifique o tipo de recurso que é exigido para realização da tarefa.

**Unidade de recursos** – especifique a unidade de onde os recursos para a tarefa devem ser atribuídos. Esse atributo afeta a estimativa de custo e vendas para a tarefa se o custo e a taxa de cobrança para o recurso forem definidos com base nas unidades de recursos.

**Nome da posição** – insira um nome amigável para o recurso genérico que sirva como um espaço reservado para o recurso que no fim das contas fará o trabalho.

O campo **Recursos** mantém o nome da posição do recurso genérico ou recurso nomeado quando um é encontrado.

O campo **Categoria** mantém os valores que indicam um tipo mais amplo de trabalho em que a tarefa pode ser agrupada. Esse campo não afeta o agendamento ou a equipe. Ele é usado apenas para relatório.

### <a name="task-dependencies"></a>Dependências da tarefa 

Você pode usar a agenda no PSA para criar relacionamentos antecessores entre as tarefas. O campo **Predecessor** em **Tarefas** usa um ou mais valores para indicar as tarefas das quais uma tarefa depende. Quando os valores predecessores são atribuídos a uma tarefa, a tarefa pode ser iniciada apenas depois que todas as tarefas predecessoras tiverem sido concluídas. Devido à dependência, a data de início planejada da tarefa é redefinida para a data quando as tarefas predecessoras são concluídas.

O modo de tarefa não tem efeito em atualizações que são feitas nas datas de início e término das tarefas predecessoras/dependentes.

## <a name="task-mode"></a>Modo de tarefa 

O modo da tarefa determina o agendamento de tarefas do nó folha. O PSA dá suporte a dois modos de tarefa para cada tarefa: agendamento automático e agendamento manual.

### <a name="auto-scheduling"></a>Agendamento automático 
 
Quando o modo da tarefa é definido para **Agendado Automaticamente** para uma tarefa, o mecanismo de agendamento da tarefa usa as regras de agendamento em atributos de tarefa para determinar a agenda da tarefa.

#### <a name="scheduling-rules"></a>Regras de agendamento

Por padrão, se uma tarefa de nó folha não tiver predecessores, sua data de início é definida para a data de início agendada do projeto. A duração de uma tarefa de nó folha é sempre calculada como o número de dias úteis entre as datas de início e término. Quando uma tarefa é agendada automaticamente, o mecanismo de agendamento segue estas regras:

- As datas de início e término da tarefa devem ser dias úteis, de acordo com o calendário de agendamento do projeto. 
- Para qualquer tarefa que tenha tarefas predecessoras, a data de início é definida automaticamente para a data final mais recente de suas predecessoras.
- O esforço é calculado usando esta fórmula: número de pessoas × duração × horas em um dia de trabalho padrão no calendário do projeto.

### <a name="manual-scheduling"></a>Agendamento manual

Se as regras de agendamento automático não atenderem aos seus requisitos, você poderá definir o modo de tarefa como **Agendado Manualmente**. Essa configuração faz com que o mecanismo de agendamento pare de calcular os valores de outros atributos de agendamento. Independentemente do modo da tarefa, se você definir predecessoras em tarefas, você sempre afetará a data de início da tarefa dependente.
