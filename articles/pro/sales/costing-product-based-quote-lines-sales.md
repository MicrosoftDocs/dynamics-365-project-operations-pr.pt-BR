---
title: Linhas de custos de cotação baseadas em produto
description: Este artigo fornece informações sobre como aplicar um preço de custo a uma linha de cotação baseada em produto.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 23eb3d29081769347d62098534a9863fd28fa90c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932558"
---
# <a name="costing-product-based-quote-lines"></a>Linhas de custos de cotação baseadas em produto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


Linhas de cotação com base em produto no Dynamics 365 Project Operations também têm um campo **Preço de Custo**. Esse campo é usado para rastrear o preço de custo do produto na linha de cotação e para cálculos de lucratividade posteriores.

Quando uma linha de cotação baseada em produto é criada para um produto de catálogo, o custo da linha de cotação baseada em produto assume o padrão do campo **Custo padrão** no catálogo de produtos. O campo de custo padrão no catálogo de produtos é configurado na moeda base da Organização. O custo unitário padrão na linha de cotação baseada em produto é convertido para a moeda de venda na cotação.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Custo unitário em uma linha de cotação baseada em produto

O objetivo de ter um custo unitário em uma linha de cotação baseada em produto é permitir custos diferentes para um produto em cada venda. Este não é um cenário comum, mas às vezes o custo do produto pode ser descontado pelo fornecedor dependendo do cliente da venda final.

Por exemplo:

A Fabrikam Robotics está instalando braços robóticos nas linhas de montagem da A Datum Corporation. A Fabrikam fornece serviços de instalação, mas os braços robóticos são adquiridos da robótica da Trey. Se a instalação de braços robóticos na A Datum Corporation abrir uma nova vertical de indústria para os braços robóticos da Trey, a Trey poderá oferecer um desconto especial referente a esse negócio à Fabrikam.

Nesse caso, a Fabrikam criará uma linha de cotação baseada em produto para Braços Robóticos e inserirá um custo especial por unidade para essa cotação. Esse custo é diferente do custo padrão de Braços Robóticos da Trey.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]