---
title: Contratos baseados em adiantamentos e honorários
description: Este tópico fornece informações sobre modelos de contratação com base em honorários e adiantamentos no Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fcee7b818097c10f8f861c4de4898daacef60e4f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574784"
---
# <a name="advances-and-retainer-based-contracts"></a>Contratos baseados em adiantamentos e honorários


_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations dá suporte a contratos baseados em honorários. Um contrato com base em honorários é um conjunto negociado de pagamentos igualmente distribuídos pelo qual o cliente será faturado durante a duração de um projeto. Esse tipo de contrato é geralmente usado para modelos de cobrança com base em tempo e material ou consumo, em que é necessário fornecer ao cliente uma fatura e um agendamento de pagamento previsíveis. As receitas reais acumuladas em cada período são reconciliadas com o pagamento recebido do cliente no início do período. De acordo com o conceito do modelo de cobrança por tempo e material, os valores das receitas acumuladas em cada período podem variar com os custos incorridos. Se a receita acumulada for superior ao valor recebido no início do período, a empresa de entrega do projeto pode:

- Somente faturar o cliente pelo excesso 
- Adiar a reconciliação da receita para o próximo período de faturamento e faça uma cobrança final ao término do projeto para qualquer receita não reconciliada restante

A principal diferença entre um modelo de contratação baseado em honorário e um modelo de contrato de preço fixo no Project Operations é que, no modelo de contrato de preço fixo, o valor da fatura não está vinculado ou associado aos custos incorridos. O faturamento segue uma abordagem baseada em marcos que está alinhada com os custos incorridos nesse período. Em um contrato com base em honorários, a receita que pode ser faturada é registrada com base no método de cobrança na linha do contrato. Quando o método de cobrança é o tempo e o material, a receita faturável está vinculada aos custos incorridos em qualquer período e pode variar de período para período. No entanto, o cliente só é faturado pelo valor do honorário periódico. O sistema usa outra fatura no final do período para reconciliar a receita faturável registrada durante o período com o valor que o cliente foi faturado no início do período.

A vantagem desse método é que os custos do cliente se tornam previsíveis no agendamento de honorários, ao contrário de um modelo típico de tempo e material. A organização que entrega o projeto também tem algum espaço para cobrir o risco de recuperar os custos incorridos em razão de qualquer aumento no escopo que um modelo de preço fixo não teria permitido.

Além de um agendamento baseado em honorários periódicos, o Project Operations pode registrar um adiantamento único de um cliente e reconciliá-lo em relação aos diferentes componentes de custo do projeto.

O honorário no Project Operations não está disponível para uso até que seja faturado ao cliente. Isso é indicado pelos seguintes campos na subgrade para adiantamentos e honorários.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| Valor Disponível | O valor que está disponível para ser usado no registro de honorário ou adiantamento. | Até que o adiantamento ou honorário seja faturado, ele não estará disponível para uso, o que significa que o valor disponível será zero. |
| Valor Usado | O valor que já é utilizado no honorário ou adiantamento. | Um adiantamento ou honorário pode ser parcialmente reconciliado em uma fatura com os custos reais que terão alguma parte marcada como já usada ou consumida. O restante do valor do adiantamento ou honorário está disponível para reconciliação em uma fatura futura com os custos reais. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]