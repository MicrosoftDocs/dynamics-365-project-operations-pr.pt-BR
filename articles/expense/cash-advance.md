---
title: Adiantamento em dinheiro
description: Este tópico oferece informações sobre adiantamentos de dinheiro.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071311"
---
# <a name="cash-advance"></a>Adiantamento em dinheiro

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Um adiantamento de dinheiro permite que os funcionários peçam dinheiro emprestado à empresa antes de incorrer em quaisquer despesas. Quando um adiantamento de dinheiro solicitado é aprovado e pago, o funcionário pode usar o dinheiro para as despesas de negócios em que possa incorrer. 

## <a name="create-and-submit-a-cash-advance-request"></a>Criar e enviar uma solicitação de adiantamento de dinheiro

1. Em **Minhas Despesas** , selecione **Adiantamentos de dinheiro** > **Novo** para criar um adiantamento de dinheiro. 
2. Na página **Nova solicitação de adiantamento de dinheiro** , insira a finalidade da despesa e selecione o local onde a despesa será incorrida.
3. Insira o valor e a moeda solicitados e selecione **Salvar**. 
4. Quando estiver pronto para enviar a solicitação de adiantamento de dinheiro na página **Solicitação de adiantamento de dinheiro** , selecione **Fluxo de trabalho** > **Enviar**.

## <a name="modify-a-cash-advance-request"></a>Modificar uma solicitação de adiantamento de dinheiro

Você pode modificar uma solicitação de adiantamento de dinheiro se ela não tiver sido enviada para aprovação.

1. Em **Minhas Despesas: Adiantamentos de Dinheiro** , localize e selecione o adiantamento de dinheiro que deseja editar.
2. Selecione **Editar** e faça as alterações necessárias na solicitação de adiantamento de dinheiro. 
3. Selecione **Salvar e fechar**.


## <a name="view-cash-advance-requests"></a>Exibir solicitações de adiantamento de dinheiro
Você pode revisar a lista de todos os adiantamentos de dinheiro em rascunho, enviados, em análise ou pagos em **Minhas despesas: Adiantamentos de dinheiro**. 

## <a name="approve-cash-advance-requests"></a>Aprovar solicitações de adiantamento de dinheiro

Os gerentes ou usuários configurados como aprovadores no fluxo de trabalho poderão aprovar os adiantamentos de dinheiro enviados a eles para revisão. 

1. Para aprovar um adiantamento de dinheiro, em **Processar adiantamentos de dinheiro** , selecione **Adiantamentos de dinheiro para minha revisão**.
2. Selecione o adiantamento de dinheiro que precisa revisar e selecione **Aprovar**.  

## <a name="pay-cash-advances"></a>Pagar adiantamentos de dinheiro 
O procedimento a seguir é normalmente concluído por um contador ou um usuário com permissões de contabilidade.

1. Para lançar adiantamentos de dinheiro aprovados, selecione **Adiantamentos de dinheiro aprovados** e depois **Pagar e transferir**.  
2. Forneça os detalhes do diário para os adiantamentos de dinheiro e selecione **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Enviar um relatório de despesas referente a um adiantamento de dinheiro pago 

Ao criar e enviar um relatório de despesas para o adiantamento de dinheiro recebido, as despesas serão automaticamente ajustadas em relação a esse adiantamento. Se o adiantamento de dinheiro for maior que o valor gasto, será necessário devolver o saldo à empresa usando a categoria de despesas **Devolver dinheiro**. Se o adiantamento de dinheiro pago pela empresa for inferior ao valor gasto, a empresa reembolsará o saldo. 

### <a name="example"></a>Exemplo
Você planeja viajar para uma conferência de Seattle para Nova York. Você cria uma solicitação de adiantamento de dinheiro para US$3.000,00 de acordo com o valor previsto para as despesas com ingresso da conferência, passagens aéreas, hotel, refeições e táxi. Você não será pago a menos que o gerente aprove essa solicitação. Após a aprovação do gerente, o adiantamento de dinheiro solicitado é pago no valor de US$3.000,00 em sua conta bancária. Posteriormente, você participa da conferência. Depois de voltar da viagem, você descobre que a despesa total foi de apenas US$2.790,00. Selecione **Dinheiro** no campo **Forma de pagamento** e envie a despesa no valor de US$2.790,00. O valor da despesa enviada é ajustado automaticamente de acordo com o adiantamento de dinheiro em US$ 3.000,00 emprestado a você. Agora você deve um saldo de US$210,00 (3.000-2.790) à empresa, e esse valor pode ser devolvido usando a categoria de despesa **Devolver dinheiro**. 
