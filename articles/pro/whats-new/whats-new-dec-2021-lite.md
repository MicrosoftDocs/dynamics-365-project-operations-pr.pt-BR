---
title: Novidades de dezembro de 2021 – implantação do Project Operations lite
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de dezembro de 2021 da implantação do Project Operations lite.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942963"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novidades de dezembro de 2021 – implantação do Project Operations lite

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em uma versão 4.27.0.195, 4.27.0.242 do ambiente do Dataverse


## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

### <a name="subcontract-management"></a>Gerenciamento de subcontratos 

- [Subcontratação de membros da equipe do projeto](../subcontracting/subcontracting-project-team-members.md): um gerente de projeto pode criar membros de equipe nomeados ou genéricos com subcontratos e linhas de subcontrato para impactar a equipe e a estimativa.
- [Opções de subcontratação de membros da equipe do projeto](../subcontracting/subcon-options.md): ao fazer escolhas de pessoal para membros nomeados ou genéricos da equipe do projeto, o gerente do projeto pode revisar subcontratos existentes ou criar subcontratos para um ou mais membros da equipe do projeto. 
- [Estimativa de custo de atribuições de recursos subcontratados](../subcontracting/costing-subcon-ra.md): a estimativa de custo do projeto levará em conta as atribuições de recursos subcontratados e os custeará usando as listas de preços de compra associadas aos subcontratos. 
- [Configurar o Quadro de Agendamento para mostrar os trabalhadores contratados e a capacidade subcontratada](../subcontracting/configure-sb-subcon.md): o painel de agendamento no Project Operations agora pode ser configurado para pesquisar e sugerir o tipo de trabalhador contratado de recursos reserváveis e capacidade subcontratada juntamente com funcionários. Essa configuração pode ser aplicada ao pesquisar recursos no contexto de equipe para um requisito de projeto específico ou ao pesquisar fora do contexto de um requisito de projeto.
- [Recrutando trabalhadores contratados e capacidade subcontratada para um projeto](../subcontracting/staffing-cw.md): os trabalhadores contratados agora podem ser contratados em projetos aproveitando as experiências do painel de agendamento.
- [Registro de tempo, despesas e uso de material em projetos para componentes subcontratados](../subcontracting/recording-subcon-actuals.md): os trabalhadores contratados podem registrar o tempo e as despesas, e os membros da equipe do projeto também podem registrar o uso de materiais adquiridos usando um subcontrato em um projeto. Isso resultará no registro de custos precisos em projetos que usam capacidade ou materiais adquiridos.
- [Transições de estado em um subcontrato](../subcontracting/subcon-states.md): os subcontratos podem ser confirmados para concluir a negociação com o fornecedor, fechados para indicar a conclusão da entrega ou cancelados para indicar a rescisão do contrato com o fornecedor antes da conclusão da entrega.

### <a name="task-planning"></a>Planejamento de tarefas
- Solução de problemas aprimorada para administradores de sistema. Quando um usuário não pode abrir um projeto, o administrador pode revisar os erros não relacionados à licença que são gerados do Project for the Web nos [Logs de agendamento do projeto](../../project-management/schedule-api-logs.md).
- [Usar listas de verificação de tarefas no Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). No Microsoft Project for the Web, você pode adicionar uma lista de verificação a uma tarefa para acompanhar itens específicos.

## <a name="quality-updates"></a>Atualizações de qualidade

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Planejamento e acompanhamento | 2392596 | APIs de agendamento agora permitem atualizações nos campos **Esforço restante**, **Esforço concluído** e **% concluído**. |
| Planejamento e acompanhamento | 2478497 | Os campos **Número da Atividade** e **ID da Tarefa** de APIs de agendamento podem ficar em branco na entrada porque o sistema os preencherá usando numeração automatizada.|
| Tempo e Despesa | 2468135 | O número de novas tentativas de aprovação é reduzido de cinco para três. |
| Tempo e Despesa | 2468188 | Corrigido o problema com o texto de registro excedendo o comprimento máximo no atributo **notetext** da entidade **Anotação**. |
