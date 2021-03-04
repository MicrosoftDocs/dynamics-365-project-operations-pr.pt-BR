---
title: Adiantamento em dinheiro
description: Este tópico oferece informações sobre adiantamentos de dinheiro.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098870"
---
# <a name="cash-advance"></a>Adiantamento em dinheiro

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Um adiantamento de dinheiro permite que os funcionários peçam dinheiro emprestado à empresa antes de incorrer em quaisquer despesas. Quando um adiantamento de dinheiro solicitado é aprovado e pago, o funcionário pode usar o dinheiro para as despesas de negócios em que possa incorrer. 

## <a name="create-and-submit-a-cash-advance-request"></a>Criar e enviar uma solicitação de adiantamento de dinheiro
Para criar um novo adiantamento em dinheiro e enviar uma solicitação de adiantamento em dinheiro, faça o seguinte: 

1. Em **Minhas despesas**, selecione **Adiantamentos em dinheiro** > **Novo**. 
2. Na página **Nova solicitação de adiantamento de dinheiro**, insira a finalidade da despesa e selecione o local onde a despesa será incorrida.
3. Insira o valor e a moeda solicitados e selecione **Salvar**. 
4. Quando estiver pronto para enviar a solicitação de adiantamento de dinheiro na página **Solicitação de adiantamento de dinheiro**, selecione **Fluxo de trabalho** > **Enviar**.

## <a name="modify-a-cash-advance-request"></a>Modificar uma solicitação de adiantamento de dinheiro

Você pode modificar uma solicitação de adiantamento de dinheiro se ela não tiver sido enviada para aprovação.

1. Em **Minhas despesas: adiantamentos em dinheiro**, localize e selecione o adiantamento em dinheiro que deseja editar.
2. Selecione **Editar** e faça as alterações necessárias na solicitação de adiantamento de dinheiro. 
3. Selecione **Salvar e fechar**.


## <a name="view-cash-advance-requests"></a>Exibir solicitações de adiantamento de dinheiro
Você pode revisar a lista de todos os adiantamentos de dinheiro em rascunho, enviados, em análise ou pagos em **Minhas despesas: Adiantamentos de dinheiro**. 

## <a name="approve-cash-advance-requests"></a>Aprovar solicitações de adiantamento de dinheiro

Os gerentes ou usuários configurados como aprovadores no fluxo de trabalho poderão aprovar os adiantamentos de dinheiro enviados a eles para revisão. 

1. Para aprovar um adiantamento de dinheiro, em **Processar adiantamentos de dinheiro**, selecione **Adiantamentos de dinheiro para minha revisão**.
2. Selecione o adiantamento de dinheiro que precisa revisar e selecione **Aprovar**.  

## <a name="pay-cash-advances"></a>Pagar adiantamentos de dinheiro 
O procedimento a seguir é normalmente concluído por um contador ou um usuário com permissões de contabilidade.

1. Para lançar adiantamentos de dinheiro aprovados, selecione **Adiantamentos de dinheiro aprovados** e depois **Pagar e transferir**.  
2. Forneça os detalhes do diário para os adiantamentos de dinheiro e selecione **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Enviar um relatório de despesas referente a um adiantamento de dinheiro pago 

Quando você cria e envia um relatório de despesas para o adiantamento em dinheiro que já recebeu, as despesas serão automaticamente ajustadas em relação a esse adiantamento. Se o adiantamento de dinheiro for maior que o valor gasto, será necessário devolver o saldo à empresa usando a categoria de despesas **Devolver dinheiro**. Se o adiantamento em dinheiro pago pela empresa for menor do que o valor que você gastou, a empresa deve reembolsar o restante. 

### <a name="example"></a>Exemplo
Você planeja viajar de Seattle a Nova York para uma conferência. Você cria uma solicitação de adiantamento em dinheiro de USD 3.000,00 com base no custo estimado do ingresso da conferência, voos, hotel, refeições e táxi. Você não será pago a menos que seu gerente aprove esta solicitação. Após a aprovação do gerente, o adiantamento de dinheiro solicitado é pago no valor de US$ 3.000,00 em sua conta bancária. Posteriormente, você participa da conferência. Depois de voltar da viagem, você descobre que a despesa total foi de apenas US$ 2.790,00. Selecione **Dinheiro** no campo **Forma de pagamento** e envie sua despesa de USD 2.790,00. O valor da despesa enviada é ajustado automaticamente de acordo com o adiantamento de dinheiro em US$ 3.000,00 emprestado a você. Agora você deve um saldo de USD 210,00 (3.000,00 - 2.790,00), que pode ser devolvido à empresa usando a categoria de despesas **Devolver dinheiro**.

