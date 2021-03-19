---
title: Configurar uma lista de preços para vendas
description: Este tópico fornece informações sobre listas de preços de vendas para precificação de projetos.
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
ms.openlocfilehash: 05b1c13540e902975eee7379276cf394d9fc5743
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275434"
---
# <a name="set-up-a-sales-price-list"></a>Configurar uma lista de preços para vendas

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Em cotações e contratos do projeto, uma lista de preços de projeto tem um padrão de substituição de preço diferente de uma lista de preços de produto. Em uma linha de cotação baseada em catálogo de produtos, você pode substituir o preço de funções e categorias diretamente na linha de cotação, pois cada linha de cotação aponta exatamente para um item do catálogo. No entanto, em uma linha de cotação baseada em projeto, não é possível substituir o preço de funções e categorias diretamente na linha de cotação. Você pode usar a lista de preços de projeto para trabalhar com os dois padrões de substituição distintos.

> [!NOTE]
> É recomendável ter uma lista de preços separada para seus recursos de projeto e itens de catálogo devido às diferenças de comportamento entre as duas quando você substitui preços.

Cada uma das seguintes entidades pode ter uma ou mais listas de preços de vendas associadas para preço de projeto:

- Cliente (conta) 
- Oportunidade 
- Cotação 
- Contrato de Projeto

A associação dessas entidades a uma lista de preços é indicada pelas listas de preços de projeto. Você pode associar uma ou mais listas de preços às entidades de vendas Cliente, Oportunidade, Cotação e Contrato de Projeto.

Uma lista de preços de projeto padrão não é inserida automaticamente em um registro do cliente. No entanto, você pode anexar manualmente uma lista de preços de projeto ao registro do cliente. Todavia, você deve anexar manualmente uma lista de preço de projeto somente quando tiver um contrato de preço personalizado com o cliente. 

Quando uma lista de preços de projeto é anexada a uma entidade de vendas, as seguintes informações são validadas:

- A lista de preços tem um contexto de **Vendas**. 
- A moeda da lista de preços corresponde à moeda do cliente. 

Em um contrato de projeto, a seguinte ordem de precedência é usada para definir automaticamente as listas de preços de projetos relacionadas:

1. Cotação
2. Oportunidade
3. Cliente 
4. Configurações globais 

Quando uma lista de preços de projeto é inserida por padrão, o sistema valida que a moeda corresponde à moeda do cliente e que as listas de preços padrão que foram inseridas têm um contexto de **Vendas**.

Você pode associar várias listas de preços de projeto às entidades Cliente, Oportunidade, Cotação e Contrato de Projeto. Esse recurso aceita preços padrão específicos de data para um contrato de projeto de longa duração, onde você pode exigir mais de uma lista de preços para considerar atualizações de preço que ocorrem por conta da inflação. No entanto, se as listas de preços que você associa à entidade Cliente, Oportunidade, Cotação ou Contrato de Projeto tiverem sobreposição de data efetiva, os preços padrão poderão estar incorretos. Desse modo, é preciso ter certeza de que as listas de preços de projeto que tenham sobreposição de data efetiva não sejam associadas a essas entidades.


[!INCLUDE[footer-include](../includes/footer-banner.md)]