---
title: Como posso fazer uma reserva flexível de recursos na versão 2.x do aplicativo?
description: Este artigo descreve como fazer uma reserva flexível de membros da equipe de projeto com o Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 472529c146fbb5e7a4540676c880cabd4ab1a32b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585180"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Como posso fazer uma reserva flexível de recursos no aplicativo Web (aplicativo Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Você pode tentar agendar ou fazer uma reserva flexível de um recurso em uma equipe de projeto para mostrar que planeja atribuir o recurso a um projeto. As reservas flexíveis não consomem a capacidade disponível de um recurso. Os membros da equipe com reserva flexível não podem ser atribuídos a tarefas do projeto. Somente recursos com o status Com reserva fixa e o tipo de confirmação Confirmado podem ser atribuídos a tarefas (supondo que tenham horas com reserva fixa suficientes para cobrir o esforço da atribuição).

Os membros da equipe de projeto com reserva flexível na grade Membro da equipe com suas horas com reserva flexível mostradas na coluna Reserva flexível. Eles também são exibidos no painel de agendamento. Além disso, eles não indicam nenhum consumo de capacidade, pois a reserva flexível não consome a capacidade de um recurso.

Há três maneiras de fazer uma reserva flexível de um membro da equipe em um projeto com a versão. 2.x do Project Service. Para fazer uma reserva flexível com o painel de agendamento, use o recurso Manter Reservas ou crie um recurso genérico. Esse métodos são descritos abaixo.

## <a name="soft-book-with-the-schedule-board"></a>Fazer reserva flexível com o painel de agendamento

Para fazer uma reserva flexível com o painel de agendamento, siga este procedimento: 
1. Abra o painel de agendamento.
2. Selecione a guia Projeto no painel inferior Requisitos da reserva do painel de agendamento.
3. Localize o projeto no qual você deseja fazer a reserva flexível de um recurso. Se você tiver muitos projetos, clique no cabeçalho da coluna Projeto e use o filtro.
4. Clique no projeto, arraste-o, solte-o na grade de tempo do recurso.
5. Isso abrirá o painel Criar reserva de recursos à direita. Ajuste as datas de início e de término, selecione Status de reserva como Flexível e defina as horas. 
6. Clique em Reservar.
7. Novamente no projeto, o recurso agora será exibido como um membro da equipe com as horas com reserva flexível na coluna Reserva flexível.

Observe que não é possível atribuir tarefas a ele na estrutura de detalhamento de trabalho (WBS), pois os recursos devem ter uma reserva fixa na equipe para serem atribuídos.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Fazer reserva flexível com o recurso Manter Reservas

Para fazer uma reserva flexível com Manter Reservas, siga este procedimento:
1. Na grade de membros da equipe, clique em Novo.
2. Selecione o recurso reservável, a função e datas de início e de término.
3. Selecione um método de alocação que não seja Nenhum:
- Capacidade total
- Capacidade percentual
- Por horas distribuídas igualmente
- Por horas de distribuição inicial
4. Clique em Salvar. O recurso será exibido na grade da equipe e suas horas indicadas como Fixas.
5. Mantenha as reservas do recurso clicando em Manter Reservas.
6. Quando o painel de agendamento abrir, expanda o recurso para mostrar suas reservas. Você verá a reserva indicada como Fixa.
7. Clique com o botão direito na reserva e, em Alterar Status, selecione Reserva Flexível e Flexível. O status da reserva agora é Flexível.
8. Depois de fechar o painel de agendamento, você verá que as horas para o recurso mudaram de Fixas para Flexíveis na grade de membro da equipe.
Observe que se você fizer uma reserva fixa de um recurso em uma equipe e atribuir tarefas a ele na WBS, ao usar Manter Reservas para alterar o status de Fixa para Flexível, as atribuições serão removidas das tarefas para esse recurso, pois apenas recursos com reservas fixas podem ser atribuídos a tarefas.

## <a name="soft-book-by-creating-a-generic-resource"></a>Fazer reserva flexível criando um recurso genérico

É possível criar uma reserva flexível gerando um membro da equipe de recurso genérico, atendendo ao painel de agendamento ou requisito de recursos e alterando o tipo durante a reserva.
Para fazer isso, siga o seguinte procedimento:

1. Na WBS do projeto, atribua funções às tarefas para as quais você deseja gerar membros da equipe genéricos.
2. Clique em Gerar Equipe de Projeto.
3. Na grade de membros da equipe de projeto, selecione o recurso genérico e clique em Reservar.
4. No painel de agendamento, selecione o recurso que você deseja reservar.
5. No painel Criar reserva de recursos do painel de agendamento, altere Status de reserva para Flexível.
6. Clique em Reservar ou Reservar e Sair.

Depois de fechar o painel de agendamento, será possível ver que o recurso selecionado foi adicionado à equipe com horas de reserva flexível e horas atribuídas. Você também verá que o recurso genérico permanece na equipe como um indicador de que as tarefas foram atribuídas a um membro da equipe com reserva flexível.

Quando estiver pronto para alterar um recurso de membro da equipe com reserva flexível para um membro com reserva fixa para que você possa atribuí-lo a tarefas, faça o seguinte:

1. Selecione esse recurso e clique em Manter Reservas.
2. Quando o painel de agendamento abrir, expanda o recurso para mostrar suas reservas. Você verá a reserva marcada como Flexível.
3. Clique com o botão direito na reserva e, em Alterar Status, selecione Reserva Fixa e Fixa. O status da reserva agora é Fixa.
4. Depois de fechar o painel de agendamento, você verá que as horas para o recurso mudaram de Flexíveis para Fixas na grade de membros da equipe. Agora é possível atribuir recursos a tarefas (contanto que haja um alinhamento entre as horas com reserva fixa e as horas de esforço da tarefa para a atribuição). Observe que se você seguiu as etapas de atendimento ao recurso genérico no item 3 acima, ao alterar o status do recurso reservável com reserva flexível para fixa, o membro da equipe genérico será removido da equipe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
