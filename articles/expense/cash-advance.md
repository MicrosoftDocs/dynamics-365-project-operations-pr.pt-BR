---
title: Adiantamento em dinheiro
description: Este tópico oferece informações sobre adiantamentos de dinheiro.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8151ecfb83f0d6da32451d509364b8f63dffdb4d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585686"
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

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Selecione adiantamentos de dinheiro que se aplicam às suas despesas
Antes de enviar um relatório de despesas, é possível selecionar o adiantamento de dinheiro que se alinhe às transações de despesas no relatório. Para usar essa funcionalidade, os dois seguintes recursos devem estar habilitados no espaço de trabalho **Gerenciamento de recursos**:

  - Relatórios de despesas reinventados
  - Capacidade de mapear adiantamentos de dinheiro para linhas de despesas
 
 Quando esses recursos estiverem habilitados:
 
  - Você pode adicionar um ou mais adiantamentos em dinheiro para cada linha de despesa.
  - O saldo disponível de um adiantamento de dinheiro está visível em tempo real quando um relatório de despesa é salvo. Isso permite processar transações de despesa e retornar transações de pagamento ao mesmo tempo.
  - Você pode selecionar vários adiantamentos de dinheiro para uma transação de despesa.
  - Os dados de reconciliação de adiantamento de dinheiro estão disponíveis usando uma consulta. 
 
Se você não usar esses recursos, a funcionalidade permanecerá a mesma, com adiantamentos de dinheiro existentes automaticamente reduzidos após uma despesa ter sido enviada.

### <a name="example"></a>Exemplo 
Você planeja viajar de Seattle a Nova York para uma conferência. Você cria uma solicitação de adiantamento em dinheiro de USD 3.000,00 com base no custo estimado do ingresso da conferência, voos, hotel, refeições e táxi. Você não será pago a menos que seu gerente aprove esta solicitação. Após a aprovação do gerente, o adiantamento de dinheiro solicitado é pago no valor de US$ 3.000,00 em sua conta bancária. Posteriormente, você participa da conferência. Depois de voltar da viagem, você descobre que a despesa total foi de apenas US$ 2.790,00. Selecione **Dinheiro** no campo **Forma de pagamento** e envie sua despesa de USD 2.790,00. O valor da despesa enviada é ajustado automaticamente de acordo com o adiantamento de dinheiro em US$ 3.000,00 emprestado a você. Agora você deve um saldo de USD 210,00 (3.000,00 - 2.790,00), que pode ser devolvido à empresa usando a categoria de despesas **Devolver dinheiro**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
