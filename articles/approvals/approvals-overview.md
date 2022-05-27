---
title: Visão geral de aprovações
description: Este tópico fornece informações sobre como trabalhar com aprovações em Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 735cd820011a4badb83dbf6540ffe9c49f960ca1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576164"
---
# <a name="approvals-overview"></a>Visão geral de aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Tempo, despesas e uso de material são enviados por um fluxo de trabalho de aprovação. Depois que as entradas forem aprovadas, as transações serão registradas em dados reais ou as horas serão reservadas na agenda.

## <a name="approvals-workflow"></a>Fluxo de trabalho de aprovações
Ao criar e enviar uma entrada de tempo, despesa ou uso de material, é criado um registro de aprovação. O aprovador ou gerente do projeto avalia e aprova a entrada. Se a entrada estiver relacionada a um projeto, os dados reais serão criados quando ele for aprovado. Isso permite que o custo e a cobrança sejam rastreados.

## <a name="approve-an-entry"></a>Aprovar uma entrada
A página **Aprovações** permite alternar entre exibições diferentes para permitir a exibição de diferentes tipos de aprovações.
  
1. Acesse a página **Aprovações** e selecione **Despesas**, **Hora**, **Uso de Material** ou **Recalls**.
2. Revise cada aprovação e selecione aquelas que deseja aprovar.
3. Selecione **Aprovar** para aprovar as entradas selecionadas.
O sistema processa essas entradas e cria dados reais.

## <a name="reject-an-entry"></a>Rejeitar uma entrada
Como Aprovador do projeto, talvez seja necessário enviar uma entrada de volta para um usuário para correção.
  
1. Acesse a página **Aprovações** e selecione a entrada a ser rejeitada. 
2. Selecione **Rejeitar**.
3. Opcional, adicione um comentário na caixa de diálogo **Comentários de Rejeição** para informar ao usuário de que a entrada está sendo rejeitada.
4. Selecione **OK**. A entrada será devolvida para o usuário.
  
## <a name="cancel-approval"></a>Cancelar aprovação
Em alguns casos, pode ser necessário cancelar uma entrada aprovada anteriormente. O cancelamento de uma entrada aprovada anteriormente terá um impacto financeiro. 

## <a name="approving-recall-requests"></a>Aprovar solicitações de recuperação
Em alguns casos, um consultor pode precisar recuperar uma entrada aprovada anteriormente. O cancelamento de uma entrada aprovada anteriormente terá um impacto financeiro. O aprovador do projeto deve aprovar a recuperação para reverter a transação em Dados reais.

## <a name="specify-project-approvers"></a>Especificar Aprovadores de projeto
Cada projeto tem vários membros da equipe do projeto. Você pode especificar quais membros da equipe também são Aprovadores de projeto.

1. Acesse a página **Projetos** e abra o projeto da lista.
2. Na guia **Equipe**, selecione o membro da equipe que será um Aprovador do projeto e selecione **Editar**.
3. Defina o campo **Aprovador do projeto** como **Sim**.
4. Selecione **Salvar**.
5. Repita as etapas 2 e 4 para adicionar Aprovadores de projeto.

## <a name="configure-the-users-manager"></a>Configurar o gerente do usuário

1. Vá para **Configurações** > **Segurança** > **Usuários**.
2. Selecione o usuário ao qual você está atribuindo um gerente e, na área **Informações da Organização**, selecione o gerente na lista. 
3. Selecione **Salvar**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
