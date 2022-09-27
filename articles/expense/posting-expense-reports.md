---
title: Postar relatórios de despesas
description: Este artigo explica como postar relatórios de despesas.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524855"
---
# <a name="post-expense-reports"></a>Postar relatórios de despesas

Depois que um relatório de despesas tiver sido aprovado e transferido para o diário geral, ele pode ser postado. Quando você posta um relatório de despesas, as despesas elegíveis para recuperação do imposto sobre valor agregado (IVA) são identificadas. A tarefa de verificar e recuperar pagamentos de IVA é atribuída ao funcionário que é responsável por verificar o relatório de despesas.

Se as despesas em um relatório de despesas forem cobradas de uma empresa que não seja a empresa que emprega o funcionário, você deve verificar a empresa que deve as despesas e a empresa à qual se devem as despesas. Por exemplo, o funcionário que enviou um relatório de despesas trabalha para a empresa DAT, mas cobrou uma despesa da empresa DIR. Nesse caso, DAT é a empresa que deve a despesa e DIR é a empresa à qual a despesa é devida. Depois de verificar essas linhas do diário, você pode postar as linhas de despesas na contabilidade.

Para postar um relatório de despesas, na página **Relatórios de despesas aprovados**, selecione o relatório de despesas e, em seguida, no Painel de Ações, selecione **Postar**.

Você também pode postar todos os relatórios de despesas na lista ao mesmo tempo. Selecione todos os relatórios de despesas e, em seguida, selecione **Postar**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Habilitar o recurso Possibilidade de lançar o passivo de despesas na moeda do fornecedor para a forma de pagamento à vista

O recurso **Possibilidade de lançar o passivo de despesas na moeda do fornecedor para a forma de pagamento à vista** permite que os relatórios de despesas sejam lançados na moeda do fornecedor para a forma de pagamento à vista.

Atualmente, quando você envia despesas em dinheiro, os relatórios de despesas são lançados na moeda contábil. Devido à conversão de valor entre a moeda da transação, a moeda contábil e a moeda do fornecedor, um valor incorreto será pago aos fornecedores se a data da transação da despesa e a data do pagamento real tiverem taxas de câmbio diferentes.

Esse recurso garantirá que o saldo do fornecedor seja registrado na moeda do fornecedor quando o relatório de despesas for lançado.

1. Acesse **Workspaces** \> **Gerenciamento de Recursos**.
2. Na lista, encontre e selecione **Possibilidade de lançar o passivo de despesas na moeda do fornecedor para a forma de pagamento à vista** e, em seguida, selecione **Habilitar agora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
