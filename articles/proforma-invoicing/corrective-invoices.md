---
title: Faturas corrigidas
description: Este tópico fornece informações sobre faturas corrigidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122374"
---
# <a name="corrected-invoices"></a>Faturas corrigidas

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

As faturas confirmadas podem ser editadas. Quando você edita uma fatura confirmada, um rascunho da fatura corrigida é criado. Como a suposição é de que você deseja reverter todas as transações e quantidades da fatura original, a fatura corrigida inclui todas as transações da fatura original e todas as quantidades nela são 0 (zero).

Quando transações não exigem correção, você pode removê-las do rascunho de fatura corrigida. Para reverter ou retornar apenas uma quantidade parcial, você pode editar o campo Quantidade nos detalhes da linha. Se você abrir os detalhes da linha da fatura, será possível ver a quantidade da fatura original. É possível editar a quantidade da fatura atual para que seja menor ou maior que a quantidade da fatura original.

Quando você confirma uma fatura corretiva, os dados reais de vendas cobradas originais são revertidos e novos dados reais de vendas cobradas são criados. Se a quantidade foi reduzida, a diferença também fará com que novos dados reais de vendas não cobradas sejam criados. Por exemplo, se a venda cobrada original for por oito horas e os detalhes da linha da fatura corrigida tiverem uma quantidade reduzida de seis horas, a linha de vendas cobradas original será revertida e dois novos dados efetivos serão criados:

- Dados reais de vendas cobradas por seis horas.
- Dados reais de vendas não cobradas pelas duas horas restantes. Essa transação pode ser cobrada posteriormente ou marcada como não passível de cobrança, dependendo das negociações com o cliente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]