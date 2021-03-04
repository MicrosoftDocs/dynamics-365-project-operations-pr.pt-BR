---
title: Criar atribuições de recursos
description: Este tópico fornece informações sobre como criar atribuições de recursos genéricos e nomeados.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 829c1d1de7270e7cafbb98ef80235ae6404f77f7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131734"
---
# <a name="create-resource-assignments"></a>Criar atribuições de recursos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


Uma atribuição de recurso é a associação direta de um membro da equipe do projeto a uma tarefa de nó folha. Este tópico fornece informações sobre as formas diferentes para atribuir recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Criar um membro da equipe genérico por meio da atribuição de tarefa


Ao criar um membro da equipe genérico por meio da atribuição de tarefas, você cria um espaço reservado ou recurso genérico. Esse recurso genérico descreve as características do recurso nomeado que você deseja usar nas tarefas. Em seguida, você gera um requisito, ou envia uma solicitação usando o requisito, que é usado para procurar e reservar o recurso nomeado.

1. Na grade Agendar de uma tarefa, selecione o ícone Recurso na célula **Recurso**.
2. Digite um nome para servir como o nome do recurso do espaço reservado. Por exemplo, Gerente de Programa.
3. Selecione **Criar** e, no campo **Criação Rápida: Membro da Equipe do Projeto**, defina a função para o recurso genérico.
4. Atribua tarefas conforme necessário a esse recurso de espaço reservado selecionando o recurso no **Seletor de Recursos** da tarefa. Os recursos listados em **Membros da Equipe**.
5. Quando terminar de atribuir o recurso genérico, selecione o recurso genérico na guia **Equipe**, selecione o recurso genérico e depois selecione **Gerar Requisito** de modo a criar um requisito de recurso para o recurso genérico.
6. Selecione **Reservar** para o recurso genérico, e depois você pode usar o painel de Agendamento para encontrar e registrar um recurso real. Você também pode enviar o requisito para preenchimento por um gerente de recurso.
7. Quando o recurso genérico for totalmente atendido (o cumprimento parcial do requisito de recurso não resultará em uma atribuição de recurso) com um recurso nomeado, o recurso genérico será removido da equipe. As atribuições de tarefas para o recurso genérico são atribuídas ao recurso nomeado que atendeu ao requisito de recurso do recurso genérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuir um recurso nomeado usando a lista de todos os recursos reserváveis

Você pode usar uma caixa de pesquisa no **Seletor de Recursos** para procurar todos os recursos reserváveis ativos e atribui-los à uma tarefa de nó folha. Os recursos atribuídos dessa maneira são adicionados à equipe sem nenhuma reserva. É como adicionar um membro da equipe e selecionar **Nenhum** como o método de alocação. O recurso é exibido nas guias **Equipe**, **Atribuição de Recursos** e **Reconciliação** como recursos apenas com atribuições e um déficit de reserva. Registre-os se quiser usar sua disponibilidade.

1. Na grade de tarefas, no quadro ou na linha do tempo, navegue até a célula **Atribuído a**.
2. Na caixa de pesquisa, comece a digitar um nome. Os resultados da pesquisa para o nome são exibidos no **Seletor de Recursos** em **Outros Recursos**.
3. Selecione o recurso que deseja atribuir à tarefa ou selecione o nome do recurso em **Outros Recursos da Equipe**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]