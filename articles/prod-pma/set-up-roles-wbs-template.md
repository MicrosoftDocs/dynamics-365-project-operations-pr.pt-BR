---
title: Configurar funções em modelos de estrutura de detalhamento de trabalho
description: Este tópico fornece informações sobre como configurar informações de função em modelos de estrutura de detalhamento de trabalho.
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
ms.openlocfilehash: 35ab88d61c9b1e9d9aebeb776d6a7783b96c62f6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682834"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Configurar funções em modelos de estrutura de detalhamento de trabalho

[!include [banner](../includes/banner.md)]

Os gerentes de projeto podem configurar modelos de estrutura de detalhamento de trabalho (WBS) que podem ser aplicados ao criar uma WBS para novos projetos. Os gerentes de projeto podem adicionar funções ao criar um modelo. Use o procedimento a seguir para atribuir uma função a um modelo de WBS.

1. Selecione **Gerenciamento e contabilidade de projetos** > **Configuração** > **Projetos** > **Modelos de estrutura de detalhamento de trabalho**.
2. Selecione **Detalhes** para um modelo de WBS selecionado.
3. Selecione uma tarefa na lista e, em seguida, no campo **Função**, selecione uma função para atribuir à tarefa.

## <a name="work-with-a-wbs"></a>Trabalhar com uma WBS

Você pode criar uma nova WBS ou copiar uma WBS de um modelo de WBS existente. Um gerente de projeto pode gerenciar facilmente os recursos atribuindo funções a novas tarefas na WBS. As funções podem ser substituídas após a aquisição de um recurso ou após a identificação de um recurso confirmado para trabalhar na tarefa. Essa flexibilidade permite que os gerentes de projeto realizem as seguintes tarefas:

- Identificar o número de recursos necessários para os pacotes de trabalho da WBS.
- Estimar os custos do projeto.
- Determinar um orçamento preliminar.
- Estimar a duração da atividade, com base em funções e recursos.
- Desenvolver alguns planos de gerenciamento de projeto, com base nas informações de projeto disponíveis.

Outras opções foram adicionadas à WBS para usar melhor a funcionalidade de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Atribuições de recursos</td>
<td>Visualize os recursos atribuídos, as datas, o número de horas e tipo de reserva para tarefas na WBS.</td>
</tr>
<tr class="even">
<td>Gerar equipe automaticamente</td>
<td>Adicione recursos planejados automaticamente usando funções associadas a uma tarefa. O Finance sugere automaticamente recursos planejados usando análise de decisão de vários critérios baseada em funções. Depois que as funções e o esforço (horas) forem definidos para as tarefas em uma WBS, e depois que a estrutura for liberada, selecione <strong>Gerar equipe automaticamente</strong>. O número necessário de recursos planejados é adicionado à WBS e à guia <strong>Equipe do projeto e agendamento</strong>.</td>
</tr>
<tr class="odd">
<td>Recurso (lista suspensa)</td>
<td>Na página <strong>Abrir formulário de atribuição de recursos</strong>, você pode selecionar recursos para reserva fixa ou flexível, com base na duração especificada. Você pode ajustar as configurações de exibição para ver e definir a duração das atividades dos recursos. Você pode selecionar e atribuir recursos no nível do pacote de trabalho usando as seguintes opções:
<ul>
<li><strong>Aceitar</strong>: confirmar as alterações no recurso atribuído a uma tarefa.</li>
<li><strong>Cancelar</strong>: cancelar as alterações no recurso atribuído a uma tarefa.</li>
<li><strong>Atribuir automaticamente</strong>: um recurso da equipe disponível que possui uma função correspondente é automaticamente selecionado e atribuído à tarefa selecionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na página **Todos os projetos**, selecione o projeto **Atualização do XYZ fase 2**.
2. Selecione **Planejar** > **Atividades** > **Estrutura de detalhamento de trabalho**.
3. Selecione **Nova** para adicionar as seguintes atividades de nível um à WBS:

    - Iniciando
    - Planejamento
    - Executando
    - Monitoramento e controle
    - Fechar

4. Defina as datas e o esforço (horas), conforme mostrado na ilustração a seguir.

    [![Definindo as datas e o esforço.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selecione a linha de tarefa **Iniciando** e, em seguida, no campo **Função**, selecione **Gerente de projeto sênior**.
6. Selecione **Publicar**.
7. Na mesma linha, no campo **Recurso**, selecione **Daniel Goldschmidt** e, em seguida, **Aceitar**.
8. Selecione a linha de tarefa **Planejamento** e, em seguida, no campo **Função**, selecione **Analista de negócios**.
9. Selecione **Publicar** e, em seguida, **Gerar equipe automaticamente**.
10. Na caixa de mensagem que é exibida, selecione **Sim**.
11. No campo **Recurso**, verifique se o valor é **Analista de negócios 1**.
12. Para o recurso **Analista de negócios 1**, abra a pesquisa e selecione **Iniciar atribuições de recursos**. Em seguida, selecione um funcionário para a tarefa.
13. Selecione **Atribuição flexível** &gt; **Capacidade total**.

    > [!NOTE] 
    > Você não recebe um aviso de que o recurso especificado agora é o 2, porque o número de recursos permanece 1.

14. Na página **Estrutura de detalhamento de trabalho**, valide a atribuição de recursos na WBS e selecione **Salvar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]