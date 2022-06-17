---
title: Fazer uma reserva flexível de um recurso
description: Este artigo fornece informações sobre como agendar provisoriamente ou reservar de maneira flexível membros da equipe do projeto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c666e5c0a83a3d1b440144a62cbd58a58c5db81
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929108"
---
# <a name="soft-book-a-resource"></a>Fazer uma reserva flexível de um recurso

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Você pode tentar agendar ou fazer uma reserva flexível de um recurso em uma equipe de projeto para mostrar que planeja atribuir o recurso ao projeto. As reservas flexíveis não consomem a capacidade disponível de um recurso, e é possível atribuir membros da equipe com reserva flexível a tarefas do projeto. Entretanto, como a reserva flexível não consome a capacidade de um recurso, você ainda pode fazer a reserva fixa do recurso para outras tarefas no mesmo período. Não é possível fazer uma reserva flexível de recursos genéricos, e uma reserva flexível não pode atender a um recurso genérico.

Os membros da equipe do projeto com reserva flexível são listados na guia **Equipe** da página **Projeto**, com suas horas com reserva flexível mostradas na coluna **Horas com Reserva Flexível** da exibição **Membros da Equipe Nomeados**. Os membros da equipe com reserva flexível também são listados no Quadro de Agendamento. Como eles têm reservas flexíveis, o Quadro de Agendamento não mostra nenhum consumo da capacidade desses recursos. O tempo com reserva flexível não é exibido na guia **Reconciliação**, nem no campo **Estender Reservas** na guia **Reconciliação** do Quadro de Agendamento. 

Há duas maneiras de fazer uma reserva flexível de um membro da equipe em um projeto: diretamente no Quadro de Agendamento ou ao adicionar o membro da equipe na guia **Equipe**. 

## <a name="soft-book-from-the-schedule-board"></a>Fazer reserva flexível no Quadro de Agendamento
Conclua as etapas a seguir para fazer a reserva flexível de um recurso no Quadro de Agendamento. 

1. Abra o Quadro de Agendamento e, no painel **Requisitos de Reserva**, selecione a guia **Projeto**.
2. Localize o projeto para o qual deseja fazer a reserva flexível de um recurso. Se houver um grande úmero de projetos na lista, selecione o cabeçalho da coluna **Projeto** e use o filtro para procurar um ou mais projetos.
3. Selecione o projeto e arraste-o e solte-o na grade de tempo do recurso.
5. No painel **Criar Reserva de Recursos**, ajuste a data de início e de término, defina **Status da Reserva** como **Flexível** e defina as horas. 
6. Clique em **Reservar**. Agora o recurso é mostrado na guia **Equipe** como um recurso para o projeto. Na exibição **Membro da Equipe Nomeado**, você verá as horas com reserva flexível na coluna **Horas com Reserva Flexível**.

> [!NOTE]
> Agora é possível atribuir os recursos com reserva flexível a tarefas na guia **Agendar**. Na guia **Reconciliação**, o recurso mostra um déficit de reserva relacionado à atribuição de tarefa, pois a guia **Reconciliação** considera apenas as reservas fixas. Você pode usar o recurso **Estender Reservas** para fazer uma reserva fixa do recurso a fim de eliminar o déficit de reservas fixas em relação às atribuições de recursos. Será necessário cancelar manualmente a reserva flexível do recurso usando **Manter Reservas**.

## <a name="soft-book-on-the-team-tab"></a>Fazer reserva flexível na guia Equipe

Você pode adicionar membros da equipe diretamente na guia **Equipe** e alterar o status da reserva de **Fixa** para **Flexível** com **Manter Reservas**. Quando você adicionar um membro da equipe dessa maneira, isso sempre resultará em uma reserva fixa, a não ser que você selecione o método de alocação como **Nenhum**.

Para usar esse método, conclua as etapas a seguir.

1. Na página **Projetos**, na guia **Equipe**, clique em **Novo**.
2. Selecione o recurso reservável, a função, bem como as datas de início e de término.
3. Selecione um método de alocação diferente de **Nenhum**.
4. Selecione **Salvar**. O recurso será exibido na grade e suas horas serão exibidas na coluna **Horas com Reserva Fixa**.
5. Mantenha as reservas do recurso selecionando **Manter Reservas**.
6. Quando o Quadro de Agendamento abrir, expanda o recurso para mostrar suas reservas. Você verá a reserva mostrada como **Fixa**.
7. Clique com o botão direito na reserva e, em **Alterar Status**, selecione **Reserva Flexível** \> **Flexível**. O status da reserva agora é **Flexível**.
8. Depois de fechar o Quadro de Agendamento, você verá que as horas para o recurso foram movidas da coluna **Horas com Reserva Fixa** para **Horas com Reserva Flexível** na grade da guia **Equipe**, na exibição **Membros da Equipe Nomeados**.

> [!NOTE]
> Ao usar **Manter Reservas** para alterar o status de **Fixa** para **Flexível**, se você fizer uma reserva fixa de um recurso na equipe e, em seguida, atribuir tarefas ao recurso, as atribuições de tarefa para o recuso serão mantidas. Entretanto, na guia **Reconciliação**, o recurso terá uma deficiência de reserva, pois somente reservas fixas são consideradas ao reconciliar reservas e atribuições. Você pode usar o recurso **Estender Reservas** na guia **Reconciliação** para fazer uma reserva fixa do recurso a fim de eliminar o déficit de reservas fixas em relação às atribuições de recursos. Será necessário cancelar a reserva flexível do recurso usando **Manter Reservas**.

Quando estiver pronto para alterar um recurso de membro da equipe com reserva flexível para um com reserva fixa, faça o seguinte:

1. No Quadro de Agendamento, expanda o recurso para mostrar as reservas. Você verá a reserva mostrada como **Flexível**.
2. Clique com o botão direito na reserva e, em **Alterar Status**, selecione **Reserva Fixa** \> **Fixa**. O status da reserva agora é **Fixa**.
3. Depois de fechar o Quadro de Agendamento, voltar para o projeto e abrir a guia **Equipe**, você verá que as horas para o recurso foram movidas da coluna **Horas com Reserva Flexível** para **Horas com Reserva Fixa** na guia **Equipe** quando na exibição **Membros da Equipe Nomeados**. Se o recurso for atribuído a tarefas, elas não mostrarão mais um déficit de reservas na guia **Reconciliação**, pois sua reservas agora são fixas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
