---
title: Linhas de contrato de custos baseadas em produto - lite
description: Este artigo fornece informações sobre como criar
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922898"
---
# <a name="cost-product-based-contract-lines---lite"></a>Linhas de contrato de custos baseadas em produto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_


As linhas de contrato baseadas em produto no Dynamics 365 Project Operations incluem o campo **Preço de custo**, que armazena o preço de custo do produto para cálculos de lucratividade posteriores.

Quando uma linha de contrato baseada em produto for criada para um produto do catálogo, o custo da linha é padronizado a partir do campo **Custo padrão** no catálogo de produtos. O campo **Custo Padrão** no catálogo de produtos é configurado na moeda base da Organização. Quando o custo unitário é padronizado na linha do contrato, ele é convertido para a moeda de venda no contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Custo unitário em uma linha de contrato baseada em produto

Ter um custo unitário em uma linha de contrato baseada em produto permite custos diferentes para um produto em cada venda de uma unidade. Embora nem sempre seja necessário, há certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor. Considere este cenário:

A Fabrikam Robotics está instalando braços robóticos nas linhas de montagem da Adatum Corporation. A Fabrikam fornece serviços de instalação, mas os braços robóticos são da Trey Research. Se a instalação de braços robóticos na Adatum Corporation abrir uma nova vertical de setor para a Trey Research, a Trey poderá oferecer um desconto especial referente a esse negócio à Fabrikam. Nesse caso, a Fabrikam cria uma linha de contrato baseada em produto para Braços robóticos. Um custo por unidade é inserido para este contrato. O custo é diferente do custo dos braços robóticos da Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]