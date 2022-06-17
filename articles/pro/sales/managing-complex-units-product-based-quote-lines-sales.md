---
title: Gerenciar unidades complexas, como por usuário, por mês para linhas de cotação baseadas em produto - lite
description: Este artigo fornece informações sobre como gerenciar unidades complexas para linhas de cotação baseadas em produto.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929890"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Gerenciar unidades complexas, como por usuário, por mês para linhas de cotação baseadas em produto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

O Dynamics 365 Project Operations usa fatores de quantidade para dar suporte a produtos baseados em assinatura. Para produtos baseados em assinatura, a quantidade na linha de contrato do projeto ou da cotação é expressada como o número de meses do usuário.

Geralmente, o preço do software por assinatura é armazenado no catálogo como o preço mensal por usuário. Durante o processo de vendas, o preço na linha de cotação normalmente é o preço mensal por usuário que foi negociado e descontado pelo agente de vendas de TI. Cada negociação tem um número diferente de usuários e um número diferente de meses de assinatura. A quantidade usada para calcular a linha de cotação é um produto do número de usuários e do número de meses de assinatura.

Para dar suporte a esse tipo de vendas, o Project Operations introduziu o conceito de fatores de quantidade. Os fatores de quantidade dependem dos atributos de produto no Dynamics 365. Quando você configura propriedades específicas para um produto, o Project Operations permite sinalizar um subconjunto ou todas as propriedades como fatores de quantidade.

O Project Operations valida que apenas propriedades numéricas ou propriedades de produto que tenham um tipo de dados numérico sejam sinalizadas como fatores de quantidade. Quando você adiciona um produto com fatores de quantidade a uma linha de cotação, o campo **Quantidade** torna-se somente leitura. Depois que você insere valores para propriedades do produto que são fatores de quantidade, o Project Operations calcula a quantidade da linha de cotação.

Por exemplo, o Dynamics 365 Sales pode ter as seguintes propriedades:

- **Número de Usuários**: o número de usuários
- **Número de Meses**: o número de meses de assinatura
- **SKU do Produto**

É possível sinalizar as propriedades **Número de Usuários** e **Número de Meses** como fatores de quantidade editando as propriedades da linha de produtos.

Para criar fatores de quantidade a partir das propriedades do produto, siga estas etapas:

1. No painel de navegação esquerdo do Project Operations, vá para **Vendas** > **Produtos**.
2. Abra o produto para o qual você precisa configurar fatores de quantidade. Certifique-se de que o produto já tenha propriedades configuradas.
3. Na página **Informações do projeto** do produto, selecione o guia **Fatores de quantidade**.
4. No painel subgrade, selecione **+ Nova computação de campo**.
5. Digite o nome do fator de quantidade e selecione o valor da propriedade que mapeia para o cálculo do campo.
6. Salve e feche o formulário. Repita essas etapas para todas as propriedades a serem usadas para calcular a quantidade da linha de cotação baseada no produto.

Quando você criar uma linha de cotação baseada em produto para um produto, a quantidade da linha de cotação será bloqueada. A quantidade será calculada como um produto dos valores de propriedade que você inseriu para essa linha de cotação.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]