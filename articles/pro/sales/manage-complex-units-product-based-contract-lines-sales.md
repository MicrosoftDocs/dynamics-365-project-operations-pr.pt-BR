---
title: Gerenciar unidades complexas para linhas de contrato baseadas em produtos - lite
description: Este tópico fornece informações sobre o suporte à venda de produtos baseados em assinatura.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 214593c5b3fbfc5194031af3d3bef59d01750099
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593966"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Gerenciar unidades complexas para linhas de contrato baseadas em produtos - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

O Dynamics 365 Project Operations usa fatores de quantidade para dar suporte a produtos baseados em assinatura. Para produtos baseados em assinatura, a quantidade no contrato ou na linha de contrato do projeto é expressa como o número de meses do usuário.

O preço do software por assinatura é armazenado no catálogo como o preço mensal por usuário. Durante o processo de vendas, o preço na linha de contrato normalmente é o preço mensal por usuário que foi negociado e descontado pelo agente de vendas. Cada negociação tem um número diferente de usuários e um número diferente de meses de assinatura. A quantidade usada para calcular o valor da linha de contrato é um produto do número de usuários e do número de meses de assinatura.

Para dar suporte a esse tipo de venda, o Project Operations apoia o conceito de *fatores de quantidade*. Os fatores de quantidade dependem dos atributos de produto. Quando você configura propriedades específicas para um produto, é possível sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.

O Project Operations valida que apenas propriedades numéricas ou propriedades de produto que tenham um tipo de dados numérico sejam sinalizadas como fatores de quantidade. Quando um produto com fatores de quantidade configurados é adicionado a uma linha de contrato, o campo **Quantidade** torna-se somente leitura. Depois que você insere valores para propriedades do produto que são fatores de quantidade, o Project Operations calcula a quantidade da linha de contrato.

Por exemplo, o Dynamics 365 Sales pode ter as seguintes propriedades:

- **Número de usuários**: o número de usuários.
- **Número de Meses**: o número de meses de assinatura.
- **SKU do produto**: a unidade de manutenção de estoque (SKU) do produto.

As propriedades **Número de Usuários** e **Número de Meses** podem ser sinalizadas como fatores de quantidade editando as propriedades da linha de produtos.

Para criar fatores de quantidade a partir de propriedades do produto, conclua as etapas a seguir.

1. No **Project Operations**, selecione **Vendas-Produtos**.
2. Abra o produto para o qual você precisa configurar fatores de quantidade. Verifique se o produto tem propriedades já configuradas.
3. Na página **Informações do Projeto**, selecione a guia **Fatores de Quantidade**.
4. No painel subgrade, selecione **+ Nova computação de campo**.
5. Insira o nome do **Fator de Quantidade** e selecione o valor da propriedade que é mapeado para o cálculo do campo.
6. Salve e feche o formulário.
7. Repita as etapas 2 a 6 para todas as propriedades que juntas formarão a quantidade para a linha de contrato baseada em produto.

Com os fatores de quantidade configurados, quando o usuário cria uma linha de contrato para este produto, a quantidade da linha de contrato é bloqueada. A quantidade é calculada como um produto dos valores da propriedade para essa linha de contrato.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]