---
title: Comportamento da interface do usuário de entrada de hora
description: Este tópico fornece informações sobre o comportamento da interface do usuário para Entrada de Hora.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: fd62fb1d8e0b2d859cb7da8b99cb725af587ff2f
ms.sourcegitcommit: 639ec8a41fda15dedfd6918702d33ea406999ba6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304287"
---
# <a name="time-entry-ui-behavior"></a>Comportamento da interface do usuário de entrada de hora

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


A grade **Entrada de hora semanal** é um controle personalizado que possui duas seções principais: **Dimensões** e **Duração**.

## <a name="keyboard-shortcuts"></a>Atalhos do teclado
| Ação        | Atalho                  |
|------------   |------------------------   |
| Criar           | Alt + Shift + n           |
| Copiar linha      | Alt + Shift + c           |
| Editar entrada    | Alt + Shift + e           |
| Editar linha      | Alt + Shift + Ctrl + e    |
| Abrir entrada    | Alt + Shift + o           |
| Enviar        | Alt + Shift + s           |
| Recuperar        | Alt + Shift + r           |
| Delete        | Alt + Shift + d           |
| Copiar semana     | Alt + Shift + w           |

## <a name="dimensions"></a>Dimensões
A seção **Dimensões** mostra as dimensões em que as horas podem ser inseridas. As seguintes dimensões têm suporte imediato:

  - Project
  - Tarefa do Projeto
  - Função
  - Digitar
  - Status da Entrada

A seção **Dimensões** não permite a edição em linha. Esta seção é apoiada por uma exibição que permite que campos personalizados sejam adicionados à grade de entrada de hora semanal.

## <a name="duration"></a>Duração
A seção Duração mostra os dias da semana como cabeçalhos de colunas. Esta seção permite edição em linha. Após a criação de uma linha de entrada de hora com dimensões apropriadas, os usuários podem inserir rapidamente a quantidade de horas que passaram nessas dimensões.

## <a name="create-a-new-time-entry"></a>Criar uma entrada de hora

1. Na grade de entrada de hora, selecione **Nova**. 
2. Na caixa de diálogo **Criação de Entrada de Hora**, selecione a data da entrada de hora.
3. Insira os dados para as dimensões **Projeto**, **Tarefa do Projeto**, **Função** e **Duração**. Essas informações devem ser adicionadas em minutos, horas ou dias digitando **h**, **m** ou **d** junto com o número. 
4. Insira uma descrição para a entrada e comentários que podem ser compartilhados externamente relacionados à entrada de hora. 

Quando você salva a entrada, os valores inseridos aparecem na seção **Dimensões**. As informações inseridas no campo **Duração** aparecem na data em que a entrada de hora foi criada.

Os campos de pesquisa são apoiados por exibições do sistema. Por exemplo, depois que um usuário entra em um projeto, o campo **Tarefa do Projeto** é definido como **Copiar** por padrão. Para criar entradas de hora para tarefas que não são atribuídas a um usuário, selecione **Alterar Exibição** na caixa de diálogo de pesquisa e selecione a exibição **Todas as Tarefas de Projeto Ativas**.

## <a name="edit-a-time-entry"></a>Editar uma entrada de hora 
Os detalhes de alguns campos na página de entrada de hora, como **Descrição** e **Comentários Externos**, não são mostrados na grade de entrada de hora semanal. Em vez disso, um pequeno indicador triangular aparece nas células **Duração** que possuem esses detalhes adicionais. 

1. Para editar uma entrada de hora, selecione a célula que deseja atualizar na entrada de hora.
2. Selecione **Editar Detalhes** para atualizar os dados no painel **Formulário Principal de Entrada de Hora**. 

## <a name="copy-a-time-entry-row"></a>Copiar uma linha de entrada de hora
Após a criação da linha, você pode selecionar **Copiar Linha** para copiar a linha inteira para uma nova linha. Quando uma linha é copiada dessa maneira, as dimensões e as durações também são copiadas. Você também pode selecionar **Editar Linha** para atualizar valores e durações de dimensão em linha na seção **Duração**.

## <a name="open-a-time-entry-behavior"></a>Abrir um comportamento de entrada de hora
Para oferecer suporte à entrada ideal e rápida nos campos mais importantes, a grade de entrada de hora semanal mostra um subconjunto de dimensões e durações de tempo selecionadas. Para exibir todos os detalhes de uma entrada de hora única, em **Editar entrada**, selecione **Abrir**.

## <a name="submit-a-time-entry"></a>Enviar uma entrada de hora
Você pode enviar uma entrada de hora única ou um grupo de entradas de hora selecionando um bloco de células ou uma linha de entrada de hora inteira e, em seguida, selecionando **Enviar**. As entradas de hora enviadas são exibidas como pendentes de aprovação na página **Aprovação** dos aprovadores. Depois que as entradas de hora são enviadas com êxito, elas não podem ser editadas.

## <a name="recall-a-time-entry"></a>Recuperar uma entrada de hora
Você pode recuperar entradas de hora que você enviou. Você pode recuperar uma única entrada de hora, um bloco de entradas de hora ou uma linha inteira de entradas de hora. As entradas de hora recuperadas podem ser editadas.

## <a name="time-entry-status"></a>Status da entrada de hora

- **Rascunho**: novas entradas de hora recebem automaticamente um status de **Rascunho**. Somente as entradas de hora com status de **Rascunho** podem ser excluídas.
- **Enviada**: quando uma entrada de hora é enviada, o status é atualizado para **Enviada**. 
- **Aprovada**: quando uma entrada de hora enviada é aprovada, o status é atualizado para **Aprovada**. 
- **Devolvida**: se uma entrada de hora for rejeitada, o status será atualizado para **Devolvida**, e a entrada ficará disponível para correção e reenvio. 

## <a name="view-rejection-comments"></a>Exibir comentários de rejeição
Quando uma entrada de hora é rejeitada por um aprovador, este pode adicionar comentários para ajudar o recurso a entender o motivo da rejeição. Para exibir os comentários de rejeição para uma entrada de hora, selecione **Abrir entrada**. Os comentários de rejeição serão mostrados na linha do tempo. O usuário pode responder aos comentários de rejeição antes de reenviar a entrada.

## <a name="copy-week"></a>Copiar semana
Após a criação de algumas entradas de hora, os usuários podem criar várias entradas de hora ao mesmo tempo.

1. No formulário **Entradas de Hora**, selecione **Copiar Semana** para criar entradas de hora adicionais em massa. 
2. Na caixa de diálogo **Copiar**, na seção **Do período**, use os campos **Data de Início** e **Data de Término** para definir o intervalo de datas que será usado para copiar as entradas. 
3. Na seção **Até o período** no campo **Data de início**, especifique a data usada para criar as entradas de hora. 
4. Selecione **Copiar**. Para a data especificada em **Período De**, é criada uma cópia das entradas de hora para o dia da semana correspondente em **Do período**. Por exemplo, a entrada de hora de segunda-feira da semana passada é copiada na segunda-feira da semana especificada como o **Período De**.

## <a name="import"></a>Importar
O mesmo processo básico é usado para importar reservas, atribuições e trocas. Você pode especificar o intervalo de datas das reservas a ser importado e, em seguida, explicitamente selecionar as reservas que devem ser copiadas para as entradas de hora de rascunho. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
