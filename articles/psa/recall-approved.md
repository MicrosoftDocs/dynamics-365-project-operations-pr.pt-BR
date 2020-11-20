---
title: Recuperar entradas de hora ou despesa aprovadas
description: Este tópico fornece informações sobre como recuperar uma transação de hora ou despesa aprovada anteriormente.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120529"
---
# <a name="recall-approved-time-or-expense-entries"></a>Recuperar entradas de hora ou despesa aprovadas

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Um membro da equipe do projeto ou outra pessoa que enviar uma entrada de hora ou despesa pode recuperar essa entrada após sua aprovação. O processo de recuperação de uma entrada de hora ou despesa aprovada tem duas etapas:

1. Um remetente solicita uma recuperação.
2. Um aprovador aprova a recuperação.

## <a name="request-a-recall"></a>Solicitar uma recuperação

Siga estas etapas para solicitar a recuperação de uma entrada de hora ou despesa aprovada.

1. Para entradas de hora, acesse **Projetos** \> **Minhas Atividades** \> **Entrada de Hora**.

    –ou–

    Para entradas de despesa, acesse **Projetos** \> **Minhas Atividades** \> **Despesas**.

2. Para entradas de hora, selecione todas as entradas de hora para uma combinação específica de um projeto e uma tarefa. Como alternativa, na grade, selecione as células individuais de hora em uma data específica para um projeto específico.

    –ou–

    Para entradas de despesa, selecione a linha para a entrada de despesa recuperar.

3. Selecione **Recuperar**. Uma caixa de diálogo de confirmação é exibida. Se as entradas de hora e despesa selecionadas já tiverem sido aprovadas, você será solicitado a inserir um motivo para a recuperação.
4. Insira um motivo para a recuperação e, em seguida, selecione **OK** para confirmar a operação. O sistema enviará para a pessoa que aprovou as entradas uma solicitação para aprovar a recuperação.

> [!NOTE]
> Embora as entradas de hora e despesa aprovadas possam ser recuperadas, se uma hora ou despesa aprovada já tiver sido faturada para o cliente, uma solicitação de recuperação não poderá ser criada. O usuário que tentar criar uma solicitação de recuperação receberá uma mensagem informando que a hora ou despesa não pode ser recuperada, pois já foi faturada.

## <a name="approve-or-reject-a-recall-request"></a>Aprovar ou rejeitar uma solicitação de recuperação

Siga estas etapas para aprovar ou rejeitar uma solicitação de recuperação.

1. Vá para **Projetos** \> **Meu Trabalho** \> **Aprovações**.
2. Na página da lista **Aprovações**, altere a exibição para **Solicitações de recuperação para aprovação**. Uma lista das solicitações de recuperação enviadas é exibida.
3. Selecione uma ou mais entradas e, em seguida, selecione **Aprovar** ou **Rejeitar**.
4. Se você selecionou **Aprovar**, receberá uma mensagem de aviso que explica o impacto da aprovação. Selecione **OK** para confirmar a operação. A solicitação de recuperação foi aprovada.

    –ou–

    Se você selecionou **Rejeitar**, a solicitação de recuperação foi rejeitada.

> [!NOTE]
> Assim como ocorre na solicitação de recuperação, quando uma recuperação é aprovada, o sistema verifica se há atividade de faturamento nas entradas de hora ou despesa. Se uma entrada já tiver sido faturada ou se estiver em uma fatura de rascunho, o aprovador receberá uma mensagem de erro informando que a hora ou despesa não pode ser aprovada para recuperação, pois já foi faturada.

## <a name="impact-of-a-recall-request"></a>Impacto de uma solicitação de recuperação

Quando uma aprovação é recuperada, há impactos operacionais e financeiros.

### <a name="operational-impact"></a>Impacto operacional

Se uma solicitação de recuperação for aprovada, o registro de aprovação será marcado como **Rejeitado**. O status da entrada será alterado para **Devolvido** ou **Rejeitado**, dependendo da entrada ser de hora ou despesa.

O membro da equipe do projeto pode visualizar entradas, editá-las e reenviá-las ou excluí-las totalmente.

Se uma solicitação de recuperação for rejeitada, o status da entrada permanecerá **Aprovado** e ela não poderá ser editada pelo membro da equipe ou o aprovador do projeto.

### <a name="financial-impact"></a>Impacto financeiro

Se uma solicitação de recuperação for aprovada, os dados efetivos correspondentes de custo e vendas serão atualizados da seguinte maneira:

- O campo **Status do Ajuste** será atualizado para **Ajustado**.
- O campo **Status de Cobrança** será atualizado para **Cancelado**.

Em seguida, as entradas reversas são criadas na tabela Dados reais. Para criar entradas de reversão, o sistema dados reais originais nos valores de campo. Os únicos valores que não são copiados são os valores de quantidade. Esses valores são revertidos. Os dados reais revertidos são criados para dados reais de **Custo** e **Vendas Não Cobradas**. O campo **Status do Ajuste** nos dados efetivos revertidos será definido como **Não Ajustável**, e o campo **Status de Cobrança** será definido como **Cancelado**. Devido a essas alterações, o gasto registrado e a lista de pendências de receita no projeto não vão mais considerar os valores que esses dados efetivos representam.

Se uma solicitação de recuperação for rejeitada, não haverá impacto financeiro no projeto.

## <a name="changes-to-time-entry-records"></a>Alterações em registros de entradas de hora

A ilustração a seguir mostra as alterações que ocorrem em entradas de hora aprovadas quando elas são recuperadas.

![Transições de estado de Entradas de Hora](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Alterações em registros de entradas de despesa

A ilustração a seguir mostra as alterações que ocorrem em entradas de despesa aprovadas quando elas são recuperadas.

![Transições de estado de Entradas de Despesa](media/ExpenseEntryStateTransitions.png)
