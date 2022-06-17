---
title: Manter membros da equipe
description: Este artigo fornece informações sobre como reservar recursos nomeados para equipes de projeto e atribuí-los a tarefas.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 6ab1541cc79870fcab9dbce45073e6b5a7bb0133
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933432"
---
# <a name="maintain-team-members"></a>Manter membros da equipe

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Você pode adicionar um recurso nomeado à equipe do projeto reservando-o diretamente na equipe.

1. No Dynamics 365 Project Operations, vá para **Projetos** e abra o projeto para o qual está fazendo a reserva.
2. Na página **Projetos**, na guia **Equipe**, selecione **Novo**. 
3. Na caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto**, selecione o recurso reservável. O campo **Função** será preenchido com a função padrão do recurso, caso tenha uma atribuída. Você pode alterar a função. 
4. Selecione o intervalo de datas em que o recurso será necessário e o método de alocação da capacidade do recurso. 
5. Se quiser que o membro da equipe seja um aprovador de projeto, selecione **Sim** no campo **Aprovador do Projeto**. O membro da equipe pode aprovar as entradas de despesa e tempo enviadas para esse projeto. 
6. Selecione **Salvar**.

Agora é possível atribuir o recurso reservado a tarefas no projeto. Na página **Projeto**, na guia **Agendar**, atribua tarefas ao novo recurso. O seletor de recurso que é iniciado no campo **Recursos** na grade da tarefa mostrará os membros da equipe que podem ser selecionados.


Em Project Operations, as reservas de recursos e as atribuições de tarefas não estão estreitamente associadas. Quando você usar o seletor de recurso na agenda, será possível atribuir tarefas aos membros da equipe para mais horas do que as cobertas na reserva do projeto.

As diferenças entre as reservas e atribuições dos membros da equipe são mostradas nas guias **Equipe** e **Reconciliação de Recursos**. Você também pode reconciliar as diferenças entre reservas e atribuições de recursos em um nível mais detalhado.

Use o seletor de recurso na guia **Agendar** para pesquisar e selecionar recursos reserváveis que não fazem parte da equipe do projeto. Esses recursos são mostrado no seletor de recurso como **Outros Recursos**.

Quando você faz uma seleção, o recurso é adicionado à equipe do projeto e atribuído à tarefa, mas não são geradas reservas.

É possível usar o recurso de extensão da guia **Reconciliação** ou **Quadro de Agendamento** para reservar a capacidade do recurso para o projeto.

Depois que um membro da equipe é reservado no projeto, você pode usar o recurso **Manter reservas** ou o **Quadro de agendamento** diretamente para gerenciar as reservas dele.


[!INCLUDE[footer-include](../includes/footer-banner.md)]