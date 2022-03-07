---
title: Visão geral de aprovações
description: Este tópico fornece informações sobre como trabalhar com aprovações em Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071288"
---
# <a name="approvals-overview"></a>Visão geral de aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Os envios de Tempo e Despesa passam por um fluxo de trabalho de aprovação. Depois que as entradas forem aprovadas, as transações serão registradas em dados reais ou as horas serão reservadas na agenda.

## <a name="approvals-workflow"></a>Fluxo de trabalho de aprovações
Ao criar e enviar uma entrada de hora ou de despesa, é criada uma entrada de aprovação. O Aprovador do projeto ou o gerente revisa e aprova a entrada. Se a entrada estiver relacionada a um projeto, após a aprovação, os dados reais serão criados. Isso permite que o custo e a cobrança sejam rastreados. 

## <a name="approve-an-entry"></a>Aprovar uma entrada
O formulário **Aprovações** permite alternar entre diferentes exibições para que você possa exibir os diferentes tipos de aprovações.
  
1. Vá para o formulário **Aprovações** e selecione **Despesas**, **Hora** ou **Recuperações**.
2. Revise cada aprovação e selecione aquelas que deseja aprovar.
3. Selecione **Aprovar** para aprovar as entradas selecionadas.
O sistema processará essas entradas e criará dados reais ou uma reserva.

## <a name="reject-an-entry"></a>Rejeitar uma entrada
Como Aprovador do projeto, talvez seja necessário enviar uma entrada de volta para um usuário para correção.
  
1. Vá para o formulário **Aprovações** e selecione a entrada que deseja rejeitar. 
2. Selecione **Rejeitar**.
3. Opcional – Adicione um comentário na caixa de diálogo **Rejeitar Comentários** para informar o usuário o motivo pelo qual a entrada está sendo rejeitada.
4. Selecione **OK**. A entrada será devolvida para o usuário.
  
## <a name="recall-entries"></a>Recuperar entradas
Em algum momento, talvez seja necessário recuperar uma entrada enviada. Se a entrada não tiver sido aprovada, ela será devolvida imediatamente. No entanto, uma entrada aprovada poderá ter um impacto material. O Aprovador do projeto deve aprovar a recuperação para reverter a transação em Dados reais.

## <a name="specify-project-approvers"></a>Especificar Aprovadores de projeto
Cada projeto tem vários membros da equipe do projeto. Você pode especificar quais membros da equipe também são Aprovadores de projeto.

1. Vá para o formulário **Projetos** e abra o projeto da lista.
2. Na guia **Equipe**, selecione o membro da equipe que será um Aprovador do projeto e selecione **Editar**.
3. Defina o campo **Aprovador do projeto** como **Sim**.
4. Selecione **Salvar**.
5. Repita as etapas 2 e 4 para adicionar Aprovadores de projeto.

## <a name="configure-the-users-manager"></a>Configurar o gerente do usuário

1. Vá para **Configurações** > **Segurança** > **Usuários**.
2. Selecione o usuário ao qual você está atribuindo um gerente e, na área **Informações da Organização**, selecione o gerente na lista. 
3. Selecione **Salvar**.


