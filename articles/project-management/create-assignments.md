---
title: Criar atribuições de recursos
description: Este artigo fornece informações sobre como criar atribuições de recursos genéricos e nomeados.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811979"
---
# <a name="create-resource-assignments"></a>Criar atribuições de recursos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


Uma atribuição de recurso é a associação direta de um membro da equipe do projeto a uma tarefa de nó folha. Este artigo fornece informações sobre as diferentes formas de atribuir recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Criar um membro da equipe genérico por meio da atribuição de tarefa


Ao criar um membro da equipe genérico por meio da atribuição de tarefas, você cria um espaço reservado ou recurso genérico. Esse recurso genérico descreve as características do recurso nomeado que você deseja usar nas tarefas. Em seguida, você gera um requisito, ou envia uma solicitação usando o requisito, que é usado para procurar e reservar o recurso nomeado.

1. Na grade Agendar de uma tarefa, selecione o ícone Recurso na célula **Recurso**.
2. Digite um nome para servir como o nome do recurso do espaço reservado. Por exemplo, Gerente de Programa.
3. Selecione **Criar** e, no campo **Criação Rápida: Membro da Equipe do Projeto**, defina a função para o recurso genérico.
4. Atribua tarefas conforme necessário a esse recurso de espaço reservado selecionando o recurso no **Seletor de Recursos** da tarefa. Os recursos listados em **Membros da Equipe**.
5. Quando terminar de atribuir o recurso genérico, selecione o recurso genérico na guia **Equipe**, selecione o recurso genérico e depois selecione **Gerar Requisito** de modo a criar um requisito de recurso para o recurso genérico.
6. Selecione **Reservar** para o recurso genérico, e depois você pode usar o painel de Agendamento para encontrar e registrar um recurso real. Você também pode enviar o requisito para preenchimento por um gerente de recurso.
7. Quando o recurso genérico é totalmente preenchido com um recurso nomeado, o recurso genérico é removido da equipe. (O cumprimento parcial do requisito de recurso não resultará em uma atribuição de recurso.) As atribuições de tarefa para o recurso genérico são atribuídas ao recurso nomeado que atendeu ao requisito de recurso do recurso genérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuir um recurso nomeado usando a lista de todos os recursos reserváveis

Você pode usar uma caixa de pesquisa no **Seletor de Recursos** para procurar todos os recursos reserváveis ativos e atribui-los à uma tarefa de nó folha. Os recursos atribuídos dessa maneira são adicionados à equipe sem nenhuma reserva. É como adicionar um membro da equipe e selecionar **Nenhum** como o método de alocação. O recurso é exibido nas guias **Equipe**, **Atribuição de Recursos** e **Reconciliação** como recursos apenas com atribuições e um déficit de reserva. Registre-os se quiser usar sua disponibilidade.

1. Na grade de tarefas, no quadro ou na linha do tempo, navegue até a célula **Atribuído a**.
2. Na caixa de pesquisa, comece a digitar um nome. Os resultados da pesquisa para o nome são exibidos no **Seletor de Recursos** em **Outros Recursos**.
3. Selecione o recurso que deseja atribuir à tarefa ou selecione o nome do recurso em **Outros Recursos da Equipe**.

## <a name="editing-resource-assignment-contours"></a>Edição de contornos de atribuição de recursos

Por padrão, quando os recursos são atribuídos a uma tarefa no agendamento, seu esforço é distribuído linearmente para cada recurso, com base nas horas de trabalho desse recurso e no modo de agendamento do projeto. Um gerente de projeto pode usar a grade de atribuição de recursos para refinar as estimativas de esforço de cada recurso atribuído a uma ou várias tarefas nas diferentes escalas de tempo. Esse recurso ajuda os gerentes de projeto a produzir estimativas de custo e vendas mais precisas, que são orientadas pelos contornos de atribuição de recursos gerados quando um recurso é atribuído a uma tarefa. Além disso, os gerentes de projeto podem refletir mais facilmente a demanda de recursos necessária para criar a demanda em um requisito de recurso.

### <a name="navigation"></a>Navegação

Para acessar a grade de edição de contorno, o gerente de projeto primeiro seleciona a guia **Tarefas** na página principal do projeto e, em seguida, seleciona a guia **Atribuições**.

![Guia Atribuições na guia Tarefas da página principal do projeto.](media/AssignmentGrid.png)

A grade permite dois métodos de agrupamento: **grupo por recurso** e **grupo por tarefa**. Ao contrário da exibição de grade, as colunas não são configuráveis. As únicas colunas visíveis são **Atribuído a**, **Nome da Tarefa**, **Início da Atribuição**, **Término da Tarefa** e **Esforço de Atribuição**.

Quando a grade é renderizada inicialmente, ela começa no primeiro contorno de atribuição. Se seu agendamento não contiver nenhuma atribuição que tenha esforço, a grade ficará em branco e não renderizará nada.

![Grade de atribuição em branco.](media/emptyassignmentgrid.png)

Se você deseja visualizar seus contornos e diferentes escalas de tempo, a grade de atribuição de recursos somente leitura e a grade de reconciliação de recursos também estão disponíveis.

### <a name="resource-calendars"></a>Calendários de recursos

A capacidade de editar um contorno para um dia específico é regida pelos dias úteis do recurso, conforme refletido em seu calendário. Se uma célula estiver desativada para determinado recurso, esse recurso não tem dias úteis nesse período.

Os contornos de um recurso podem se estender além das datas de início e término atuais da tarefa atribuída. Se um contorno for atualizado para que seja após a última data de término de uma tarefa ou a primeira data de início de uma tarefa, a data de término ou a data de início da tarefa serão alteradas conforme apropriado. Contudo, se um contorno for atualizado para que seja anterior à data de início de uma tarefa vinculada a um predecessor, a atualização falhará porque a atribuição acionará o início da tarefa antes que seu predecessor seja concluído, e esse comportamento não recebe suporte atualmente.

### <a name="co-authoring"></a>Coautoria

As alterações na grade de atribuição de recursos são refletidas automaticamente em todas as exibições associadas, incluindo as exibições de gráfico, linha do tempo, quadro e grade. Se vários usuários estiverem revisando o projeto ao mesmo tempo, todas as alterações feitas por um usuário serão refletidas na grade. Por outro lado, quaisquer alterações feitas na grade de atribuição de recursos serão mostradas para todos os outros usuários que estiverem visualizando o projeto na mesma sessão.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
