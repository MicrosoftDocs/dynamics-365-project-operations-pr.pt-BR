---
title: Criar uma equipe de projeto
description: Este tópico fornece informações sobre como criar e gerenciar equipes de projeto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f134d7566954e640eea8ff8af98e184273ad570c
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683018"
---
# <a name="create-a-project-team"></a>Criar uma equipe de projeto

[!include [banner](../includes/banner.md)]

Para usar as funções que foram configuradas anteriormente em um projeto, um gerente de projeto deve associar as funções ao projeto. Várias funções podem ser atribuídas a um projeto. Para evitar confusão, essas funções são automaticamente rotuladas durante a reserva. Por exemplo, se o gerente de projeto precisa de três engenheiros de software, três funções de engenheiro de software com os rótulos **engenheiro de software 1**, **engenheiro de software 2** e **engenheiro de software 3** serão geradas automaticamente. Se as características da função foram definidas anteriormente para a função, elas são aplicadas como um filtro durante as pesquisas de um recurso. Características adicionais podem ser adicionadas conforme necessário para refinar ainda mais a pesquisa.

As configurações de exibição também podem ser personalizadas para exibir melhor a disponibilidade de recursos. Existem opções para mostrar a disponibilidade horária, diária, semanal, mensal, trimestral e anual. Também há uma opção para mostrar a capacidade disponível e restante dos recursos. Essa opção é útil para gerenciamento de horas, ao estimar o tempo disponível para atividades ou disponibilidade de recursos.

O gerente de projeto pode selecionar uma função na página e, em seguida, se houver um recurso disponível que atenda ao requisito, selecionar para reservar um recurso para preencher a função. Observe que os recursos não precisam ser reservados nesse ponto do estágio de planejamento. Ao criar uma WBS, você pode substituir funções por recursos de equipe para o projeto. Se as funções forem substituídas por recursos de equipe na WBS, a configuração do recurso atualiza automaticamente o agendamento e a lista da equipe do projeto.

[![Lista da equipe do projeto que inclui funções e recursos reais.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

O gerente de projeto tem várias opções para reservar um recurso para um projeto, como **Capacidade restante**, **Capacidade total**, **Porcentagem de capacidade** e **Especificar horas**. Essas opções de reserva podem ser canceladas a qualquer momento se as atribuições de recursos forem alteradas. Dois tipos de reserva são compatíveis:

- **Reserva fixa**: a reserva de recurso foi aprovada e confirmada para trabalhar no compromisso pelo período especificado.
- **Reserva flexível**: a reserva de recurso foi configurada para tentar trabalhar no compromisso pelo período especificado.

O seguinte procedimento explica como criar uma equipe de projeto.

## <a name="create-a-project-team"></a>Criar uma equipe de projeto

1. Na página de lista **Todos os projetos**, selecione um projeto e, em seguida, **Editar**.
2. Na guia **Equipe do projeto e agendamento**, no campo **Data de término do agendamento**, insira a data de início do agendamento mais um mês. Por exemplo, se a data de início do agendamento for 24 de junho de 2017 (24/06/2017), insira **24/07/2017**.
3. Selecione **Adicionar**.
4. No painel **Adicionar funções ao projeto**, no campo **Função**, selecione **Gerente de projeto sênior**.
5. Selecione **Competências necessárias**.
6. Na página **Escolher características**, as características que você configurou anteriormente para a função de gerente de projeto sênior são selecionadas por padrão. Selecione **OK**.
7. Na página **Adicionar funções ao projeto**, no campo **Número de recursos**, digite **1**.
8. No campo **Recurso**, a pesquisa mostra todos os recursos que possuem as competências necessárias. Selecione **Daniel Goldschmidt** e, em seguida, **Criar**.
9. Na página **Projeto**, selecione **Adicionar**.
10. No painel **Adicionar funções ao projeto**, no campo **Função**, selecione **Membro da equipe**. No campo **Número de recursos**, insira **5**.
11. Selecione **Criar**.
12. Na página **Projetos**, selecione **Preencher recurso**.

## <a name="monitor-project-teams"></a>Monitorar equipes de projeto
1. Na página **Todos os projetos**, selecione o link da **ID do projeto** para o projeto **Atualização do XYZ fase 2**.
2. Na FastTab **Equipe do projeto e agendamento**, verifique se os recursos do projeto listados estão corretos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]