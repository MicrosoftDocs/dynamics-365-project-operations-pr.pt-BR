---
title: Alterações de recursos para Project Service Automation para o Project Operations
description: Este artigo fornece uma visão geral das alterações de recursos do Project Service Automation para o Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621200"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Alterações de recursos para Project Service Automation para o Project Operations

Após um projeto ter sido atualizado com sucesso do Microsoft Dynamics 365 Project Service Automation 3.X para o Dynamics 365 Project Operations Lite, não é possível editar tarefas do projeto na estrutura de detalhamento de trabalho (WBS) da grade de tarefas. Os clientes poderão revisar as WBSs na grade de acompanhamento onde novos campos foram adicionados para fornecer todos os detalhes relacionados à tarefa. Para projetos em que são necessárias edições na WBS, você pode converter seletivamente projetos qualificados para a nova experiência de agendamento do Project for the Web.

## <a name="project-conversion-process"></a>Processo de conversão de projeto

Siga estas etapas para converter um projeto.

1. Abra a página principal do projeto e selecione **Converter** no Painel de Ação.
1. Na caixa de mensagem de confirmação, selecione **OK** para iniciar a conversão de projeto. As seguintes ações ocorrem:

    1. Uma barra de mensagens que aparece na página principal do projeto informa: "O agendamento do projeto está sendo convertido. Você não pode fazer alterações no projeto até que a conversão seja concluída."
    1. Você é redirecionado para a lista de projetos.

    Após a conclusão da conversão do projeto, ocorrem as seguintes ações:

    1. O gerente de projeto designado recebe uma notificação no lado direito do aplicativo.
    1. A barra de mensagens que informa que a conversão está em andamento é removida.
    1. A guia **Agendamento** mostra a nova experiência de agendamento com o Project for the web. Qualquer usuário que tenha as licenças e direitos de acesso apropriados pode editar a WBS.
    1. O campo **Mecanismo de agendamento** é atualizado para **Project for the web**.
    1. O botão **Converter** é removido do Painel de Ação.

> [!IMPORTANT]
> A conversão em massa de projetos não é permitida. Qualquer tentativa de atualizar um grande volume de projetos ao mesmo tempo terá o desempenho reduzido. Essa limitação ajuda a garantir alto desempenho para todos os clientes.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tarefas manuais versus tarefas automáticas

Quando um ambiente é atualizado do Project Service Automation para o Project Operations, todas as tarefas na WBS são consideradas agendadas automaticamente. O conceito de tarefas agendadas manualmente não está disponível no Project for the web. No entanto, você pode definir o comportamento de agendamento preferencial para seus projetos usando a configuração de [modo de agendamento](/project-management/scheduling-modes.md) ao criar novos projetos.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operações restritas para projetos de pré-conversão

Esta seção descreve as diferenças funcionais que você pode esperar quando os projetos não foram convertidos.

### <a name="copy-project"></a>Copiar projeto

A operação **Copiar** é suportada apenas em projetos convertidos. Os projetos atualizados não podem ser copiados antes da conversão.

### <a name="move-project"></a>Mover projeto

Uma alteração na data de início de um projeto não moverá proporcionalmente o início das tarefas, a menos que o projeto tenha sido convertido.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Quais são as diferenças entre projetos convertidos e novos projetos criados após a conclusão da atualização?

Para projetos convertidos após o upgrade do ambiente, será definido um sinalizador que instrui o agendamento a respeitar apenas o calendário do projeto. Esse comportamento corresponde ao comportamento no Project Service Automation. No entanto, o sinalizador não será definido para novos projetos criados após a atualização. Portanto, o agendamento respeitará as horas de trabalho dos recursos quando eles forem atribuídos a uma tarefa.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>O que devo fazer se meu projeto não for convertido?

Se seu projeto não for convertido, a primeira etapa é revisar os logs de erros para identificar quaisquer problemas comuns relacionados à sua WBS. Se os logs não indicarem um erro específico sobre o qual você possa agir, entre em contato com o Suporte ao cliente para que seu caso possa ser analisado mais detalhadamente.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Como os fechamentos de negócios são tratados no Project for the web?

O Project for the web não respeita os fechamentos de negócios que a empresa define no nível da organização. No entanto, isso respeitará outros tipos de dias de folga definidos em um determinado modelo de horário de trabalho.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Quais são as limitações do Project for the web?

Consulte [Criar uma estrutura de detalhamento de trabalho: Limitações do Project](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Posso esperar mudanças nas minhas estimativas de custo e vendas?

Em casos raros em que os contornos de atribuição de recursos são recalculados ou em um limite de data diferente do projeto de origem, você pode ver diferenças nas estimativas de vendas e custos. Como parte do processo de atualização, espera-se que os clientes testem um conjunto de amostra representativo de projetos, para que possam entender quaisquer possíveis alterações no cronograma.
