---
title: Agendar um projeto com uma estrutura de detalhamento de trabalho
description: Como agendar um projeto com uma estrutura de detalhamento de trabalho no Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149799"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Agendar um projeto com uma estrutura de detalhamento de trabalho (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

O cronograma de um projeto comunica o trabalho que precisa ser executado, os recursos que executarão o trabalho e o período de tempo em que o trabalho precisa ser concluído. O cronograma de um projeto reflete qualquer trabalho associado à entrega do projeto dentro do prazo. Uma das primeiras etapas de fase de iniciação do projeto é apresentar um cronograma do projeto. Para estabelecer um cronograma de projeto, é necessário criar uma estrutura de detalhamento de trabalho.  
  
 Criar uma estrutura de projeto com uma estrutura de detalhamento de trabalho ajuda você a:  
  
- Dividir o trabalho em tarefas gerenciáveis  
  
- Estimar o tempo necessário para concluir uma tarefa  
  
- Definir dependências e a duração da tarefa  
  
- Determinar as funções necessárias para concluir cada tarefa  
  
  O cronograma do projeto na estrutura de detalhamento de trabalho tem um aspecto familiar, finalizado com um gráfico de Gantt interativo.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Criar uma estrutura de detalhamento de trabalho de um projeto  
 Crie uma estrutura da detalhamento de trabalho para representar a sequência de tarefas em um projeto. A estrutura de detalhamento de trabalho inclui tarefas, requisitos para cada tarefa e informações de receita e custo. Na estrutura da detalhamento de trabalho, você pode adicionar:  
  
-   A sequência das tarefas em uma hierarquia  
  
-   Outras tarefas, se existirem, que devem ser concluídas antes que uma tarefa seja iniciada  
  
-   A data de início, a data de término e a duração de uma tarefa  
  
-   O número de horas necessárias para uma tarefa  
  
-   As habilidades e qualificações necessárias do trabalhador  
  
-   Os trabalhadores atribuídos a uma tarefa  
  
-   A receita e os custos estimados  
  
## <a name="task-types"></a>Tipos de tarefa  
Você usará os seguintes tipos de tarefa para criar a estrutura de detalhamento de trabalho:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nó raiz do projeto** | A tarefa resumo de nível superior do projeto. Todas as outras tarefas do projeto são criadas nele. O nome da tarefa raiz é o nome do projeto. O esforço, as datas e a duração do nó raiz são baseados nos valores da hierarquia abaixo deles. Você não pode editar as propriedades do nó raiz ou excluir o nó raiz. | 
| **Tarefas de contêiner ou resumo** | A tarefa resumo é uma tarefa que contém subtarefas abaixo nela. Uma tarefa resumo não tem nenhum esforço de trabalho nem custo próprio. Seus esforços e custo de trabalho são o valor acumulado de suas subtarefas. Você pode alterar o nome de uma tarefa resumo, mas não pode alterar o esforço, as datas ou a duração, pois esses valores são calculados automaticamente. A exclusão de uma tarefa resumo excluirá a tarefa e todas as suas subtarefas.|  
| **Tarefas do nó folha** | Uma tarefa de nó folha representa o trabalho mais detalhado do projeto. Ela tem um esforço estimado, um número planejado de recursos, datas de início e de término e uma a duração.|

  
## <a name="task-hierarchy"></a>Hierarquia da tarefa  
 Você tem as opções a seguir na criação de uma hierarquia de tarefas:  
  
- **Adicionar uma tarefa**.   Você pode adicionar uma tarefa a uma posição escolhida na hierarquia de tarefas. Se você não selecionar uma posição, a nova tarefa aparecerá no fim.  
  
- **Recuar tarefa**.   Recuar uma tarefa para torná-la secundária em relação a uma tarefa imediatamente acima dela.  
  
- **Recuar tarefa para a esquerda**   Recuar uma tarefa para a esquerda para que ela não seja mais uma subtarefa da tarefa principal original.  
  
- **Mover para cima e mover para baixo**.   Mover tarefas para cima e para baixo na hierarquia da tarefa principal. Mover uma tarefa para cima ou para baixo não afeta seu esforço, custo, datas ou duração.  
  
## <a name="task-attributes"></a>Atributos da tarefa  
 O nome de uma tarefa descreve o trabalho que precisa ser concluído. Você usa vários atributos de tarefa para descrever o cronograma e as necessidades de pessoal para a tarefa.  
  
### <a name="schedule-attributes"></a>Atributos da agenda

 - Atribua valores a **Horas de esforço**, **Número de recursos**, **Data inicial**, **Data final** e **Duração** para determinar a agenda da tarefa. 
 - O **Esforço** é uma estimativa das horas necessárias para concluir a tarefa.
 - O **Número de recursos** é uma estimativa que o gerente de projetos atribui à tarefa para ajudar a apresentar o melhor cronograma possível. 
 - A **Duração** (em dias) indica o número de dias úteis necessário para concluir a tarefa.  
  
### <a name="staffing-attributes"></a>Atributos de pessoal

 - Os valores **Função**, **Unidade organizacional do recurso**, **Número de recursos** e **Recursos** descrevem as necessidades de pessoal para a realização da tarefa. 
 - A **Função** descreve o tipo de recurso necessário executar a tarefa. 
 - A **Unidade organizacional do recurso** indica a unidade organizacional à qual os recursos devem ser fornecidos para a realização da tarefa; isso também afeta a estimativa de vendas e custos da tarefa, pois ela é registrada no momento em que o preço unitário de venda é determinado para o recurso. 
 - Os **Recursos** retêm um recurso genérico ou um recurso nomeado quando um dele é localizado.  
  
## <a name="task-dependencies"></a>Dependências da tarefa  
 Você pode criar relacionamentos predecessores entre uma ou mais tarefas na estrutura de detalhamento de trabalho. Você pode definir um ou mais valores no campo para tarefas predecessoras para indicar as tarefas das quais ela será dependente. Quando você atribuir um valor predecessor a uma tarefa, a tarefa só poderá ser iniciada quando todas as tarefas predecessoras forem concluídas. A definição dessa dependência desta tarefa resultará no recálculo da data de início prevista para a tarefa como a última data de término de todas as suas predecessoras. Os impactos relacionados às predecessoras em um cronograma não são limitados pelo modo de tarefa definido na tarefa.  
  
## <a name="task-mode"></a>Modo de tarefa  
 O modo de tarefa é um dos fatores importantes que determinam o agendamento de tarefas de nó folha. Há dois modos para cada tarefa: modo de agendamento automático e modo de agendamento manual.  
  
-   **Agendamento automático**.   Ao definir o modo da tarefa para Agendado Automaticamente, o mecanismo de agendamento da tarefa usa as regras de agendamento nos seguintes atributos da tarefa para determinar a agenda para a tarefa:  
  
    -   Antecessoras  
  
    -   Esforço  
  
    -   Número de recursos  
  
    -   Datas de início e término  
  
-   **Regras de agendamento**.   A data de início de uma tarefa de nó folha que não possui predecessoras assume como padrão a data de início do agendamento do projeto. A duração de uma tarefa de nó folha é sempre calculada como o número de dias úteis entre as datas de início e término. Quando uma tarefa é agendada automaticamente, o mecanismo de agendamento segue as regras abaixo:  
  
    -   As datas de início e término de uma tarefa devem ser sempre dias úteis de acordo com o calendário de agendamento do projeto  
  
    -   A data de início de uma tarefa que tem predecessoras assume como padrão a data de término mais recente de suas predecessoras  
  
    -   Esforço = Número de pessoas * Duração * horas em um dia útil padrão do calendário do projeto  
  
-   **Agendamento manual**.   Em alguns casos, talvez você queira desconsiderar essas regras. Nesses casos, você pode definir o modo de tarefa para que seja agendado manualmente. Isso faz com que o mecanismo de agendamento pare de calcular os valores para outros atributos de agendamento. A definição de tarefas predecessoras sempre afeta a data de início da tarefa dependente.  
  
## <a name="create-a-work-breakdown-structure"></a>Criar uma estrutura de detalhamento de trabalho  
  
1.  Vá para **Project Service > Projetos**.  
  
2.  Clique no projeto no qual você deseja trabalhar.  
  
3.  Na barra da parte superior da tela, selecione a seta para baixo ao lado do nome do projeto e, em seguida, clique em Estrutura de detalhamento de trabalho.  
  
4.  Para adicionar uma tarefa, clique em **Adicionar Tarefa**. Preencha os campos da tarefa e clique em **Salvar**.  
  
5.  Continue adicionando tarefas até que sua estrutura de detalhamento de trabalho esteja completa. Ao criar a estrutura de detalhamento de trabalho, é possível fazer o seguinte para organizar suas tarefas:  
  
    -   Selecione uma tarefa e clique em **Recuar** para movê-la para baixo de outra tarefa ou clique em Recuar para a esquerda para movê-la um nível.  
  
    -   Selecione uma tarefa e clique em **Mover para Cima** ou **Mover para Baixo** para movê-la para cima ou para baixo na lista.  
  
    -   Clique em **Ocultar Gantt** para ocultar o gráfico de Gantt e clique em **Mostrar Gantt** para exibi-lo novamente.  
  
    -   Selecione um período diferente para o gráfico de Gantt em **Escala de Tempo**.  
  
6.  Para adicionar as funções especificadas na estrutura de detalhamento de trabalho aos membros da equipe do projeto, clique em **Gerenciar Equipe do Projeto**.  
  
7.  Ao terminar de fazer as alterações, clique no botão **Salvar** no canto inferior direito da tela.  
  
### <a name="see-also"></a>Consulte também  
 [Guia do gerente de projeto](../psa/project-manager-guide.md)
