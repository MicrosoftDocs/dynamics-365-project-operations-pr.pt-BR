---
title: Configurar a conversão de moeda para calcular os preços de venda a partir das taxas de custo
description: Este artigo explica como configurar o comportamento de conversão de moeda que será usado no Microsoft Dynamics 365 Project Operations quando as transações de vendas forem geradas a partir de transações de custo.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816658"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Configurar a conversão de moeda para calcular os preços de venda a partir das taxas de custo

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

No Microsoft Dynamics 365 Project Operations, os preços de vendas para categorias de despesas podem ser configurados como valores numéricos ou podem ser configurados para que sejam calculados com base no custo incorrido.

Quando são configurados para serem calculados com base no custo incorrido, as seguintes opções estão disponíveis:

- A preço de custo
- Marcar a porcentagem sobre o custo

Em cenários em que o custo da despesa é incorrido em uma moeda diferente da moeda de venda do contrato do projeto, a conversão de moeda é necessária para calcular o preço de venda com base no custo.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Comportamento de conversão de moeda que usa taxas de câmbio nativas do Dataverse

Por padrão, o Project Operations usa as taxas de câmbio armazenadas na tabela Moeda no Dataverse. Para configurar o Project Operations para usar taxas de câmbio nativas para calcular os preços de venda do custo, siga estas etapas.

1. Vá para **Project Operations \> Configurações \> Parâmetros**.
1. Abra a página de detalhes **Parâmetro do Projeto**.
1. Defina o campo **Lógica de conversão de moeda** com um valor em branco.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Comportamento de conversão de moeda que usa taxas de câmbio de aplicativos de finanças e operações

As taxas de câmbio na tabela Moeda que está disponível nativamente no Dataverse não têm data efetiva. Portanto, elas podem nem sempre ser dimensionadas para os requisitos que você tem para o cálculo de preços de venda usando taxas de custo.

É possível usar as taxas de câmbio no ambiente financeiro e operacional para calcular o preço de venda na moeda de venda usando uma taxa de custo na moeda de custo. Para configurar esse comportamento de conversão de moeda, siga estas etapas.

1. Na página **Parâmetros do projeto**, adicione o campo **Lógica de conversão de moeda**. Depois, salve e publique a personalização.
1. Vá para **Project Operations \> Configurações \> Parâmetros**.
1. Abra a página de detalhes **Parâmetro do Projeto**. 
1. Defina o campo **Comportamento de conversão de moeda** como **Estendido com fallback para padrão**.
1. Conceda ao direito de acesso de **Usuário de aplicativo de gravação dupla** permissão de **Leitura global** para as seguintes tabelas:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. Em seu ambiente de finanças e operações, execute os seguintes mapas de gravação dupla com sincronização inicial:

    - Tipo de taxa de câmbio (msdyn\_exchangeratetypes)
    - Par de moedas de taxa de câmbio (msdyn\_currencyexchangeratepairs)
    - Taxas de câmbio do CDS (msdyn\_currencyexchangerates)

Depois que essas alterações forem concluídas, a gravação dupla disponibilizará as taxas de câmbio do ambiente de finanças e operações no Dataverse. O Project Operations usará essas taxas de câmbio para converter as taxas de custo na moeda de venda do contrato.

> [!NOTE]
> Esse comportamento de conversão de moeda se aplica somente ao cálculo de preços de venda a partir de taxas de custo. Não será usado para calcular genericamente os valores da moeda base. Os valores da moeda base sempre usarão as taxas de câmbio nativas do Dataverse, independentemente de você concluir ou não esse procedimento.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
