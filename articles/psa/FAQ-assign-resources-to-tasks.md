---
title: Atribuir um recurso a uma tarefa
description: Este artigo fornece informações sobre como atribuir recursos a tarefas.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: dae5a81c51f34b9115ac8c267452b167a6d7bef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913468"
---
# <a name="assign-a-resource-to-a-task"></a>Atribuir um recurso a uma tarefa

[!include [banner](../includes/psa-now-project-operations.md)]

Há três maneiras de atribuir um recurso a uma tarefa no Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservar um recurso como um membro da equipe e atribuí-lo a uma tarefa

É possível adicionar um recurso à equipe do projeto e atribuí-lo a tarefas na agenda do projeto.

1. Na guia **Membro da Equipe**, adicione um novo membro da equipe selecionando **Novo**. 

2. O painel **Criação Rápida de Membro de Equipe** é aberto, onde você pode selecionar o nome do recurso reservável e definir uma função. 

    Selecione um dos seguintes métodos de alocação para a reserva do recurso:

    - **Capacidade completa** registra a capacidade completa de recursos das datas específicas de início e término.
    - **Capacidade de porcentagem** registra o recurso para a porcentagem da capacidade do recurso para as datas de início e término.
    - **Por Horas Distribuídas Igualmente** reserva o recurso por um número de horas específico, distribuindo-as igualmente por dia pelo intervalo de datas especificado.
    - **Por horas de distribuição inicial** registra o recurso de um número de horas específico, com distribuição inicial das horas por dia nas datas de início e término especificadas.
    - **Nenhum** adiciona o recurso à equipe, mas não cria quaisquer registros que absorvem sua capacidade.

3. Na grade **Agendar** de uma tarefa, selecione o ícone **Recurso** na célula do recurso e, em **Membros da Equipe**, selecione o membro da equipe que acabou de adicionar. 

> [!NOTE]
> Nas guias **Membro da Equipe** e **Reconciliação**, o recurso mostra as horas reservadas e atribuídas. As horas devem ser as mesmas, mas não é obrigatório, pois as reservas e atribuições não são rigidamente combinadas. A guia **Reconciliação** fornece detalhes quando elas são diferentes, como quando você atribui a um recurso mais horas do que as que foram reservadas. Se necessário, você pode corrigir as informações estendendo as reservas ou alterando a atribuição do recurso.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Criar um membro da equipe genérico por meio da atribuição de tarefa

Ao criar um membro da equipe genérico por meio da atribuição de tarefa, você cria um espaço reservado ou recurso genérico que descreve as características do recurso nomeado que deseja usar nas tarefas. Em seguida, você gera um requisito (ou envia uma solicitação usando o requisito) que é usado para procurar e reservar o recurso nomeado.

1. Na grade **Agendar** de uma tarefa, selecione o ícone **Recurso** na célula do recurso.

2. Digite um nome para servir como o nome do recurso do espaço reservado. Por exemplo, Gerente de Programa.

3. Selecione **Criar** e, no campo **Criação Rápida: Membro da Equipe do Projeto**, defina a função para o recurso genérico.

4. Você pode continuar atribuindo tarefas a esse recurso de espaço reservado selecionando o recurso no **Seletor de Recursos** da tarefa. Eles são listado em **Membros da Equipe**.

5. Quando terminar de atribuir o recurso genérico, selecione o recurso genérico na guia **Equipe** e, em seguida, selecione **Gerar Requisito** de modo a criar um requisito de recurso para o recurso genérico.

6. Selecione **Registrar** para o recurso genérico. É possível usar o Quadro de Agendamento para encontrar e reservar um recurso real. Você também pode enviar o requisito para preenchimento por um gerente de recurso.

7. Quando o recurso genérico é preenchido com um recurso nomeado, o recurso genérico é removido da equipe e as atribuições de tarefa do recurso genérico são atribuídas ao recurso nomeado que preencheu o requisito de recurso do recurso genérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuir um recurso nomeado usando a lista de todos os recursos reserváveis

Você pode usar uma caixa de pesquisa no **Seletor de Recursos** para procurar todos os recursos reserváveis e atribui-los à uma tarefa.

Os recursos atribuídos dessa maneira são adicionados à equipe sem nenhuma reserva. É como adicionar um membro da equipe e selecionar Nenhum como o método de alocação. O recurso é exibido nas guias **Equipe** e **Reconciliação** como recursos apenas com atribuições e um déficit de reserva. Registre-os se quiser usar sua disponibilidade.

1. Na grade **Agendar** de uma tarefa, selecione o ícone **Recurso** na célula do recurso.

2. Comece a digitar um nome. Os resultados da pesquisa para o nome são exibidos no **Seletor de Recursos** em **Outros Recursos**.

3. Selecione o recurso que deseja atribuir à tarefa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
