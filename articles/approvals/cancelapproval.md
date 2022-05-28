---
title: Cancelar a aprovação de entradas aprovadas anteriormente
description: Este tópico explica como um gerente de projeto pode cancelar a aprovação de entradas de hora, despesa ou uso de material aprovadas anteriormente.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584766"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Cancelar a aprovação de entradas aprovadas anteriormente

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Um gerente de projeto ou aprovador que já tenha aprovado entradas de hora, despesa ou uso de material pode cancelar a aprovação dessas entradas. 

Siga estas etapas para cancelar a aprovação de uma entrada de hora, despesa ou uso de material aprovada anteriormente.

1. Vá para **Projetos** \> **Meu Trabalho** \> **Aprovações**.
2. A página de listagem **Aprovações** mostra todas as entradas de hora que estão aguardando aprovação. Altere a exibição para **Minhas aprovações anteriores**.
3. Selecione as aprovações de horas, despesas ou material a serem canceladas. Em seguida, no Painel de Ações, selecione **Cancelar Aprovação**.
4. Na caixa de mensagem de confirmação que aparece, selecione **OK** para confirmar a operação.

> [!IMPORTANT]
> Não é possível cancelar a aprovação de uma entrada de hora, despesa e uso de material aprovada anteriormente que já tenha sido faturada para o cliente. Se tentar, você receberá uma mensagem informando que a aprovação não pode ser cancelada porque já foi faturada. Nesse caso, você poderá cancelar a aprovação somente se uma fatura corretiva for usada para emitir um crédito completo ou reembolso ao cliente na fatura original.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impacto de cancelar a aprovação de uma entrada aprovada anteriormente

Quando uma aprovação é cancelada, há impactos operacionais e financeiros.

### <a name="operational-impact"></a>Impacto operacional

Se a aprovação de uma entrada for cancelada, o registro da aprovação será marcado como **Enviado**. O status da entrada é alterado para **Enviada**. Nesse estágio, um membro da equipe do projeto pode recuperar a entrada sem enviar uma solicitação de recuperação.

O aprovador pode alterar os valores **Quantidade faturável** e **Tipo de cobrança** e, em seguida, aprovar a entrada mais uma vez.

### <a name="financial-impact"></a>Impacto financeiro

Se a aprovação de uma entrada for cancelada, os dados reais correspondentes de custo e vendas serão atualizados da seguinte maneira:

- O campo **Status do Ajuste** será atualizado para **Ajustado**.
- O campo **Status de Cobrança** será atualizado para **Cancelado**.

Em seguida, as entradas reversas são criadas na tabela Dados reais. Para criar entradas de reversão, o sistema dados reais originais nos valores de campo. Os únicos valores que não são copiados são os valores de quantidade. Esses valores são revertidos. Os dados reais revertidos são criados para dados reais de **Custo** e **Vendas Não Cobradas**. O campo **Status do Ajuste** nos dados efetivos revertidos será definido como **Não Ajustável**, e o campo **Status de Cobrança** será definido como **Cancelado**. Devido a essas alterações, o gasto registrado e a lista de pendências de receita no projeto não vão mais considerar os valores que esses dados efetivos representam.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
