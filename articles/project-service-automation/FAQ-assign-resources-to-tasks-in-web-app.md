---
title: Como atribuir um recurso reservável a uma tarefa no aplicativo Web
description: Uma visão geral de como é possível atribuir recursos reserváveis.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749171"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Como eu atribuo um recurso agendável a uma tarefa no aplicativo Web (aplicativo Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Há duas maneiras de atribuir um recurso a uma tarefa no Project Service. Você pode registrar um recurso como um membro de equipe e depois atribui-lo a tarefa. Ou, você pode criar um membro de equipe genérico por meio de atribuição de função em tarefas, gerar uma equipe e depois preencher os requisitos de de backup com um recurso nomeado.

Observe que, se você quiser atribuir um recurso agendável a uma tarefa, o membro da equipe de recurso agendável deve ter registros disponíveis o suficiente. O status do registro deve ser Reserva fixa do tipo de comprometimento e Status comprometido. Se não houver registros suficientes para o recurso, Project Service remove a atribuição e exibe a mensagem de erro a seguir:

*Impossível atribuir recursos a tarefa - Os recursos a seguir não têm horas suficientes registradas para o projeto*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Registre um recurso como um membro de equipe e depois atribua o recurso a uma tarefa

Com esse método você adiciona um recurso a equipe de projeto e depois atribui tarefas ao recurso no agendamento do projeto. Veja como você faz isso:
1.  Na grade de membro de equipe, adicione um novo membro da equipe selecionando **Novo**.
2.  Na tela Criação rápida de membro de equipe, selecione o nome de recurso agendável e definir uma função.
3.  Selecione as datas **De** e **Para**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de tela da inclusão de membro da equipe](media/FAQ-Resources-to-Tasks2-1.png "Captura de tela da inclusão de membro da equipe")
 
4.  Selecione um dos métodos de alocação a seguir para o registrar o recurso:
    - **Capacidade completa** registra a capacidade completa de recursos das datas específicas de início e término.
    - **Capacidade de porcentagem** registra o recurso para a porcentagem da capacidade do recurso para as datas de início e término.
    - **Por horas distribuídas igualmente** registra o recurso de um número de horas específico, distribuindo-os por tempo igualmente por dia nas datas de início e término especificadas.
    - **Por horas de distribuição inicial** registra o recurso de um número de horas específico, com distribuição inicial das horas por dia nas datas de início e término especificadas.

    Não selecione **Nenhum** porque ele adiciona o recurso à equipe, mas não cria quaisquer registros que absorvem a capacidade do recurso.
5.  Selecione **Salvar**.

    Observe que as horas de registro devem ser suficientes para cobrir as horas de esforço e faixas de data das tarefas as quais você atribui o recurso. Se eles não tiverem alinha dos, você não pode atribuir o recurso à tarefa.

6.  Na estrutura de detalhamento de trabalho (WBS) da tarefa, clique na célula em suspenso. Depois: 

    1. Selecione **Adicionar**.
    2. Selecione os **Recursos** suspensos e selecione o membro de equipe adicionado acima.
    3. Selecione **OK**. O membro de equipe agora é atribuído à tarefa.

    > [!div class="mx-imgBorder"] 
    > ![Captura de tela da inclusão de recursos com a WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de tela da inclusão de recursos com a WBS")
 
Na grade de membro de equipe, você verá o agregado das horas de recurso atribuídos nas Horas atribuídas. Será menor ou igual às horas registradas para o recurso. 

> [!div class="mx-imgBorder"] 
> ![Captura de tela das horas atribuídas a um recurso](media/FAQ-Resources-to-Tasks2-3.png "Captura de tela das horas atribuídas a um recurso")
 
Se a tarefa que você está tentando atribuir ao recurso começa depois da data de término dos registros de recurso, o recurso não aparecerá no menu suspenso.

Observe que é possível atribuir um recurso para mais horas que suas horas registradas se o recurso tiver alguma capacidade restante não atribuída. Nesse caso, o recurso será parcialmente atribuído para seus registros. Você pode encontrar essas horas de tarefa não atribuídas adicionando a coluna Horas sem recursos à estrutura de detalhamento de trabalho.

Se os recursos forem atribuídos a suas horas registradas (suas horas registradas é igual a suas horas atribuídas), você verá a mensagem de erro a seguir quando tentar atribui-los mais tarefas:

*Impossível atribuir recursos a tarefa - Os recursos a seguir não têm horas suficientes registradas para o projeto.*

Além disso, o membro da equipe de gerente de projeto adicionado à equipe quando você cria o projeto é adicionado sem quaisquer registros e não pode ser atribuído a qualquer tarefa. Eles não aparecerão no menu suspenso de recurso das tarefas.

Se você quiser atribuir esse recurso, é preciso removê-los da equipe e depois readicioná-los com um método de alocação diferente de Nenhum. Eles são adicionados à equipe quando o projeto é criado para que o projeto tenha, pelo menos, um aprovador de projeto por padrão.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Crie um membro de equipe genérico por meio da atribuição de função nas tarefas

Este método assegura que que os recursos possuem registros suficientes para tarefas. Primeiro, você cria um recurso de espaço reservado ou genérico que descreve as características do recurso nomeado que você deseja usar nas tarefas gerando uma equipe após atribuir funções às tarefas. Veja como você faz isso:

1. Na estrutura de detalhamento de trabalho, selecione uma tarefa.
2. Selecione o ícone suspenso **Função atribuída** na célula de recurso.
3. Selecione o menu suspenso **Função** e selecione a função do recurso genérico.
4. Selecione **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de tela do uso da WBS para incluir recurso](media/FAQ-Resources-to-Tasks2-4.png "Captura de tela do uso da WBS para incluir recurso")
 
Depois de ter concluído a atribuição de tarefas na WBS, selecione **Gerar equipe de projeto**. O Project Service cria o número mínimo de membros de equipe genérico baseado nas funções, unidades de organização de recurso, e calendário de projeto agregando as atribuições de tarefa.

> [!div class="mx-imgBorder"] 
> ![Captura de tela da geração da equipe de projeto](media/FAQ-Resources-to-Tasks2-5.png "Captura de tela da geração da equipe de projeto")
 
Na grade Membro de equipe, você verá recursos do tipo Recurso genético com a função e nome da posição. Se dois recursos são necessários para uma função completar o trabalho, o recurso Gerar equipe cria dois membros de equipe e usa o nome de posição para defini-los separadamente.

> [!div class="mx-imgBorder"] 
> ![Captura de tela da inclusão de dois recursos genéricos](media/FAQ-Resources-to-Tasks2-6.png "Captura de tela da inclusão de dois recursos genéricos")
 
Você pode abrir o requisito de recurso de backup para o membro de equipe genérico selecionando o link em Requisito de recurso.

> [!div class="mx-imgBorder"] 
> ![Captura de tela da abertura do requisito de recurso de backup](media/FAQ-Resources-to-Tasks2-7.png "Captura de tela da abertura do requisito de recurso de backup")

Selecione **Livro** para o recurso genérico, e depois você pode usar o painel de agendamento para encontrar e registrar um recurso real. Você também pode enviar o requisito para preenchimento por um gerente de recurso selecionando **Enviar solicitação**.

Quando o recurso genérico é preenchido com um recurso nomeado, o recurso genérico é removido da equipe e as atribuições de tarefa do recurso genérico são atribuídas ao recurso nomeado que preencheu o requisito de recurso do recurso genérico.
 

