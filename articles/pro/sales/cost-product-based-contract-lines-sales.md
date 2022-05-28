---
title: Linhas de contrato de custos baseadas em produto - lite
description: Este tópico fornece informações sobre criação
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3def4c330dc9aadbf5ff806ef7682fbfd1072e4b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599256"
---
# <a name="cost-product-based-contract-lines---lite"></a>Linhas de contrato de custos baseadas em produto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_


As linhas de contrato baseadas em produto no Dynamics 365 Project Operations incluem o campo **Preço de custo**, que armazena o preço de custo do produto para cálculos de lucratividade posteriores.

Quando uma linha de contrato baseada em produto for criada para um produto do catálogo, o custo da linha é padronizado a partir do campo **Custo padrão** no catálogo de produtos. O campo **Custo Padrão** no catálogo de produtos é configurado na moeda base da Organização. Quando o custo unitário é padronizado na linha do contrato, ele é convertido para a moeda de venda no contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Custo unitário em uma linha de contrato baseada em produto

Ter um custo unitário em uma linha de contrato baseada em produto permite custos diferentes para um produto em cada venda de uma unidade. Embora nem sempre seja necessário, há certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor. Considere este cenário:

A Fabrikam Robotics está instalando braços robóticos nas linhas de montagem da Adatum Corporation. A Fabrikam fornece serviços de instalação, mas os braços robóticos são da Trey Research. Se a instalação de braços robóticos na Adatum Corporation abrir uma nova vertical de setor para a Trey Research, a Trey poderá oferecer um desconto especial referente a esse negócio à Fabrikam. Nesse caso, a Fabrikam cria uma linha de contrato baseada em produto para Braços robóticos. Um custo por unidade é inserido para este contrato. O custo é diferente do custo dos braços robóticos da Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]