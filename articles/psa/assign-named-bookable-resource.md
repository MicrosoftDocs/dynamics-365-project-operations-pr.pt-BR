---
title: Reservar recursos reserváveis nomeados a uma equipe de projeto e atribuir tarefas
description: Este artigo fornece informações sobre como reservar recursos nomeados para equipes de projeto e atribuí-los a tarefas.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 61c9b47088e836c0a9c78477adf891df3d14853b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919310"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Reservar recursos reserváveis nomeados a uma equipe de projeto e atribuir tarefas 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Você pode adicionar um recurso nomeado à equipe do projeto reservando-o diretamente na equipe. Para fazer isso, execute estas etapas.

1. No Project Service Automation, vá para **Projetos** e abra o projeto para o qual está fazendo a reserva.
2. Na página **Projetos**, na guia **Equipe**, clique em **Novo**. 

![Adicionando um membro da equipe pela guia de equipe.](media/RM-how-to-1.png)

3. Na caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto**, selecione o recurso reservável. O campo **Função** será preenchido com a função padrão do recurso, caso tenha uma atribuída. Você pode alterar a função, se necessário. 
4. Selecione o intervalo de datas em que o recurso será necessário e o método de alocação da capacidade do recurso. 
5. Se quiser que o membro da equipe seja um aprovador de projeto, selecione **Sim** no campo **Aprovador do Projeto**. Isso significa que o membro da equipe pode aprovar as entradas de despesa e tempo enviadas para esse projeto. 
6. Clique em **Salvar**.

![Adicionando um membro da equipe no formulário de criação rápida.](media/RM-how-to-2.png)


Agora é possível atribuir o recurso reservado a tarefas no projeto. Na página **Projeto**, clique na guia **Agendar** para atribuir atarefas ao novo recurso. O seletor de recurso que é iniciado no campo **Recursos** na grade da tarefa mostrará os membros da equipe que podem ser selecionados.

![Atribuindo um membro da equipe a uma tarefa na guia de agendamento.](media/RM-how-to-3.png)

Na versão 3 do PSA (Project Service Automation), reservas de recurso e atribuições de tarefa não são rigidamente acopladas. Isso significa que quando você usar o seletor de recurso na agenda, será possível atribuir tarefas aos membros da equipe para mais horas do que as cobertas na reserva do projeto.
É possível ver as diferenças entre atribuições e reservas do membro da equipe na guia **Equipe** ou na guia **Reconciliação de Recursos**. Você também pode reconciliar as diferenças entre reservas e atribuições para recursos em um nível mais detalhado.

![Guia Reconciliação de recursos.](media/RM-how-to-4.png)

Você também pode usar o seletor de recurso na guia **Agendar** para pesquisar e selecionar recursos reserváveis que não fazem parte da equipe do projeto. Eles são mostrado no seletor de recurso como **Outros Recursos**.

![Atribuindo um recurso de membro que não faz parte da equipe a uma tarefa.](media/RM-how-to-5.png)

Ao fazer isso, o recurso é adicionado à equipe do projeto e atribuído à tarefa, mas não são geradas reservas.

![Membro da equipe com atribuições e sem reservas.](media/RM-how-to-6.png)

É possível usar o recurso de extensão da guia **Reconciliação** ou **Quadro de Agendamento** para reservar a capacidade do recurso para o projeto.

![Estendendo reservas para um membro da equipe na guia de reconciliação de recursos.](media/RM-how-to-7.png)

Depois que um membro da equipe é reservado no projeto, você pode usar o recurso de manter reservas ou o Quadro de Agendamento diretamente para gerenciar as reservas dele.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
