---
title: Recall de entradas aprovadas anteriormente
description: Este tópico explica como um membro da equipe do projeto pode solicitar o recall de registros de hora, despesas e uso de material enviados e aprovados anteriormente e como um gerente de projeto pode aprovar ou rejeitar solicitações de recall.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586560"
---
# <a name="recall-previously-approved-entries"></a>Recall de entradas aprovadas anteriormente

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Um membro da equipe do projeto que enviar uma entrada de hora, despesa ou uso de material pode fazer recall dessa entrada depois que ela foi aprovada. O processo de recall tem duas etapas principais:

1. Um remetente solicita uma recuperação.
2. Um aprovador aprova a solicitação de recall.

## <a name="request-a-recall"></a>Solicitar uma recuperação

Siga estas etapas para solicitar um recall de entradas de hora, despesa ou uso de material aprovadas.

1. Siga uma destas etapas, dependendo do tipo de entrada da qual você deseja fazer recall:

    - Para entradas de hora, vá para **Projetos** \> **Meu Trabalho** \> **Entrada de Hora** e selecione todas as entradas de hora para uma combinação específica de projeto e tarefa. Como alternativa, na grade, selecione as células individuais de hora em uma data específica para um projeto específico.
    - Para entradas de despesa, vá para **Projetos** \> **Meu Trabalho** \> **Despesas** e selecione a linha da entrada de despesa da qual deve ser feito recall.
    - Para entradas de uso de materiais, vá para **Projetos** \> **Meu Trabalho** \> **Log de Uso de Material** e selecione a linha da entrada de uso de material da qual deve ser feito recall.

2. Selecione **Recuperar**. Uma caixa de diálogo de confirmação é exibida. Se as entradas de hora, despesa ou uso de material já tiverem sido aprovadas, será solicitado que você insira um motivo para o recall.
3. Insira um motivo para a recuperação e, em seguida, selecione **OK** para confirmar a operação. O sistema enviará para a pessoa que aprovou as entradas uma solicitação para aprovar a recuperação.

> [!IMPORTANT]
> Não é possível criar uma solicitação de recall para uma entrada de hora, despesa ou uso de material aprovada que já foi faturada para o cliente. Se você tentar, receberá uma mensagem informando que não é possível fazer recall da entrada de hora, despesa ou uso de material porque ela já foi faturada. Nesse caso, você poderá solicitar recall da entrada somente se uma fatura corretiva for usada para emitir um crédito ou reembolso total para o cliente na fatura original.

## <a name="approve-or-reject-a-recall-request"></a>Aprovar ou rejeitar uma solicitação de recuperação

Siga estas etapas para aprovar ou rejeitar uma solicitação de recuperação.

1. Vá para **Projetos** \> **Meu Trabalho** \> **Aprovações**.
2. Na página da lista **Aprovações**, altere a exibição para **Solicitações de recuperação para aprovação**. Uma lista das solicitações de recuperação enviadas é exibida.
3. Selecione uma ou mais entradas e, em seguida, selecione **Aprovar** ou **Rejeitar**.
4. Se você selecionou **Aprovar**, receberá uma mensagem de aviso que explica o impacto da aprovação. Selecione **OK** para confirmar a operação. A solicitação de recuperação foi aprovada.

    –ou–

    Se você selecionou **Rejeitar**, a solicitação de recuperação foi rejeitada.

> [!IMPORTANT]
> Quando um recall é aprovado, da mesma forma que quando é solicitado, o sistema verifica se há atividade de faturamento nas entradas de hora, despesa ou uso de material. Se uma entrada já tiver sido faturada ou se estiver em uma fatura de rascunho, o aprovador receberá uma mensagem de erro informando que não é possível aprovar a hora ou despesa para recall porque ela já foi faturada. Nesse caso, o aprovador poderá aprovar o recall somente se uma fatura corretiva for usada para emitir um crédito ou reembolso total para o cliente na fatura original.

## <a name="impact-of-a-recall-request"></a>Impacto de uma solicitação de recuperação

Quando uma aprovação é recuperada, há impactos operacionais e financeiros.

### <a name="operational-impact"></a>Impacto operacional

Se uma solicitação de recuperação for aprovada, o registro de aprovação será marcado como **Rejeitado**. O status da entrada será alterado para **Devolvido** ou **Rejeitado**, dependendo da entrada ser de hora, despesa ou uso de material.

O membro da equipe do projeto pode visualizar entradas, editá-las e reenviá-las ou excluí-las completamente.

Se uma solicitação de recuperação for rejeitada, o status da entrada permanecerá **Aprovado** e ela não poderá ser editada pelo membro da equipe ou o aprovador do projeto.

### <a name="financial-impact"></a>Impacto financeiro

Se uma solicitação de recuperação for aprovada, os dados efetivos correspondentes de custo e vendas serão atualizados da seguinte maneira:

- O campo **Status do Ajuste** será atualizado para **Ajustado**.
- O campo **Status de Cobrança** será atualizado para **Cancelado**.

Em seguida, as entradas reversas são criadas na tabela Dados reais. Para criar entradas de reversão, o sistema dados reais originais nos valores de campo. Os únicos valores que não são copiados são os valores de quantidade. Esses valores são revertidos. Os dados reais revertidos são criados para dados reais de **Custo** e **Vendas Não Cobradas**. O campo **Status do Ajuste** nos dados efetivos revertidos será definido como **Não Ajustável**, e o campo **Status de Cobrança** será definido como **Cancelado**. Devido a essas alterações, o gasto registrado e a lista de pendências de receita no projeto não vão mais considerar os valores que esses dados efetivos representam.

Se uma solicitação de recuperação for rejeitada, não haverá impacto financeiro no projeto.

## <a name="changes-to-time-entry-records"></a>Alterações em registros de entradas de hora

A ilustração a seguir mostra as alterações que ocorrem em entradas de hora aprovadas e os registros de aprovação correspondentes quando é feito recall delas.

![Transições de estado de entradas de hora.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Alterações em registros de entrada de despesa e uso de material

A ilustração a seguir mostra as alterações que ocorrem em entradas de despesa e uso de material aprovadas e os registros de aprovação correspondentes quando é feito recall delas.

![Transições de estado de entradas de despesa.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
