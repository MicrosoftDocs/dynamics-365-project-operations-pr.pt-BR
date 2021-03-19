---
title: Configurar recursos do projeto
description: Este tópico fornece informações sobre como configurar ou solicitar recursos do projeto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288725"
---
# <a name="set-up-project-resources"></a>Configurar recursos do projeto

[!include [banner](../includes/banner.md)]

Você deve configurar um calendário e associá-lo a um funcionário ou colaborador. O calendário é usado para agendar o projeto e o horário de trabalho dos recursos reservados para o projeto. Durante a configuração do calendário, os gerentes de projeto podem fazer o nivelamento de recursos como parte da otimização de recursos. Com base na agenda do calendário, podem ser colocadas restrições aos recursos. Você pode configurar um calendário na página **Calendários**.

Ao configurar um funcionário como recurso do projeto, você pode selecionar entre os funcionários que trabalham na empresa para a qual você está configurando os recursos. Você também pode selecionar funcionários de outras empresas em sua organização. Esses funcionários são conhecidos como recursos intercompanhia.

Os procedimentos a seguir explicam como configurar um funcionário como um recurso de projeto na sua empresa e como configurar um recurso de projeto intercompanhia.

## <a name="set-up-a-worker-as-a-project-resource"></a>Configurar um funcionário como um recurso do projeto

1. Na página **Funcionários**, na lista **Funcionários**, selecione o funcionário que você está adicionando como um recurso de projeto e abra o registro dele.
2. No Painel de ação, selecione **Projeto** &gt; **Configuração** &gt; **Configuração do projeto**.
3. Selecione um calendário e feche a página.

Você também pode especificar projetos padrão para um recurso como um tipo de atribuição prévia. As atribuições prévias podem ser usadas quando o gerente de recursos ou de projeto sabe com antecedência em quais projetos o recurso estará trabalhando. As atribuições prévias também podem ser baseadas na solicitação de um patrocinador ou cliente do projeto. Para fazer a atribuição prévia de um projeto, na página **Atribuir projetos**, na guia **Projetos**, na lista **Projetos pendentes**, selecione o projeto apropriado.

## <a name="set-up-an-intercompany-resource"></a>Configurar um recurso intercompanhia

Ao configurar um funcionário como um recurso intercompanhia, você deve concluir a configuração na empresa que faz e na que toma o empréstimo.

### <a name="in-the-lending-company"></a>Na empresa que faz o empréstimo

1. No Finance, verifique se a empresa que faz o empréstimo está selecionada e conclua o procedimento da seção anterior, "Configurar um funcionário como um recurso do projeto".
2. Na página **Contabilidade intercompanhia**, selecione **Novo**.
3. No campo **ID de entidade legal**, selecione a empresa que faz o empréstimo. Preencha os campos restantes conforme apropriado e, em seguida, selecione **Salvar**.
4. Na página **Preço de transferência**, selecione **Novo**.
5. No campo **Entidade legal que toma o empréstimo**, selecione a empresa apropriada.
6. Para emprestar à empresa que toma o empréstimo apenas o recurso que você criou no início desta seção, no campo **Recurso**, selecione o nome do recurso que você criou. Para colocar todos os recursos da empresa que faz o empréstimo à disposição da empresa que o toma, deixe o campo **Recurso** em branco.
7. Na página **Parâmetros de gerenciamento e contabilidade de projeto**, na guia **Intercompanhia**, defina a opção **Habilitar quadro de horários e agendamento de recursos intercompanhia** como **Sim**.

### <a name="in-the-borrowing-company"></a>Na empresa que toma o empréstimo

- Na página **Lista de recursos**, no filtro de pesquisa, insira o nome do recurso que você criou para a empresa que faz o empréstimo para verificar se o nome está incluído na lista de recursos para a empresa que o toma.

## <a name="request-project-resources"></a>Solicitar recursos do projeto
A funcionalidade de agendamento de recursos do projeto permite apenas que os gerentes de recursos distribuam recursos de equipe em compromissos ou projetos. Para ativar essa funcionalidade, conclua as seguintes tarefas ou verifique se elas foram concluídas:

- Configurar sequências numéricas.
- Configurar fluxos de trabalho de gerenciamento e contabilidade de projeto.
- Habilite fluxos de trabalho de solicitação de recursos.

Após a conclusão das tarefas anteriores, você poderá concluir as seguintes tarefas conforme necessário:

- Criar uma solicitação de recurso a partir de um recurso em equipe com reserva flexível.
- Monitorar as solicitações de recursos.
- Preencher solicitações de recursos.
- Solicitar um recurso de equipe de uma WBS.
- Reservar recursos para um projeto sem ter uma solicitação de um recurso de equipe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]