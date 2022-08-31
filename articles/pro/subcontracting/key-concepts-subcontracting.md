---
title: Principais conceitos na subcontratação
description: Este artigo explica alguns conceitos-chave que se aplicam à subcontratação no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e75f2cf9c1092604e43e5cb60dda0e2a1b7dcd64
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262155"
---
# <a name="key-concepts-in-subcontracting"></a>Principais conceitos na subcontratação


_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

O artigo explica alguns conceitos-chave que você deve conhecer antes de começar a usar a funcionalidade de subcontratação no Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unidade de contratação no subcontrato

A unidade de contratação representa a divisão ou prática que possui a entrega do eventual projeto. A unidade de contratação é também a divisão que estabelece a relação contratual com o fornecedor.

## <a name="purchase-currency"></a>Moeda de compra

No Project Operations, a moeda de compra é a moeda na qual o subcontrato é criado. É também a moeda na qual os custos do subcontratado em um projeto são registrados. A moeda de compra pode ser diferente da moeda do projeto e a moeda do projeto pode, por sua vez, ser diferente da moeda de venda.

## <a name="billing-methods-on-subcontract-lines"></a>Métodos de faturamento em linhas de subcontrato

Para projetos, normalmente existem modelos de contratação com base em taxas fixas e consumo. O Project Operations oferece suporte a esses métodos de cobrança nos contextos de vendas e compras. Para uma compra, os métodos de faturamento funcionam da seguinte maneira:

- **Tempo e Material** - Quando uma linha de subcontrato usa o método de faturamento **Tempo e Material**, o custo do tempo é registrado no projeto à medida que os subcontratados trabalham nesse projeto e o tempo é registrado. Essas transações de custo de subcontratados são então combinadas com os itens de linha nas faturas do fornecedor. Nesse modelo, os gerentes de projeto que usam o Project Operations podem combinar e verificar as linhas da fatura do fornecedor com o tempo do subcontratado que é registrado e aprovado. Após a verificação ser concluída, os dados efetivos de custo anteriores registrados após a aprovação são revertidos e novos dados efetivos de custo baseados na fatura do fornecedor são criados no projeto.
- **Preço fixo** - Nesse modelo de contratação de taxa fixa, as faturas do fornecedor são baseadas em marcos fixos. No entanto, os recursos do subcontratado também podem relatar o tempo. O tempo é então revisado e aprovado pelo gerente de projeto. Quando é aprovado, o Project Operations cria dados efetivos de custo temporários no projeto. Depois que o fornecedor envia uma fatura para um marco, o gerente de projeto pode comparar os dados efetivos de custo registrados anteriormente com o marco. Quando a verificação é concluída, os dados efetivos de custo são revertidos e o custo baseado em marco é registrado.

## <a name="project-price-lists-on-subcontracts"></a>Listas de preços de projeto em subcontratos

As listas de preços do projeto são listas de preços usadas para definir os preços de compra para tempo, despesas e outros componentes relacionados ao projeto. Pode haver várias listas de preços, cada uma das quais pode ter seu próprio subcontrato com data efetiva no Project Operations. O Project Operations não permite a sobreposição de datas efetivas nas listas de preços do projeto para um subcontrato.

## <a name="transaction-classes-on-subcontracts"></a>Classes de transação em subcontratos

O Project Operations é compatível com quatro tipos de classes de transação:

- Hora
- Despesa
- Material
- Taxa

Os custos de compra podem ser estimados e incorridos apenas nas classes de transação **Tempo**, **Despesa** e **Material**. **Taxa** é uma classe de transação somente para receita e não está disponível no conteúdo de compra.

## <a name="purchase-pricing-dimensions"></a>Dimensões de preço de compra

As dimensões de preço permitem que você decida quais atributos são usados para configurar o preço de compra e padronizar as transações no tempo. Em relação à compra, o Project Operations oferece suporte apenas a conjuntos de dimensões fixas para a configuração e padronização do preço de compra. Para configuração do preço de compra e padronização de linhas de subcontratos e transações de tempo de subcontratos, os atributos são **Função** e **Recurso Reservável**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
