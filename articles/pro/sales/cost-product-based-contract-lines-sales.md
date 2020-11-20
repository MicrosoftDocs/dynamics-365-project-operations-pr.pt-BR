---
title: Linhas de contrato de custos baseadas em produto - lite
description: Este tópico fornece informações sobre criação
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177227"
---
# <a name="cost-product-based-contract-lines---lite"></a>Linhas de contrato de custos baseadas em produto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_


As linhas de contrato com base em produto no Dynamics 365 Project Operations incluem o campo **Preço de Custo**, que armazena o preço de custo do produto para cálculos de lucratividade posteriores.

Quando uma linha de contrato baseada em produto é criada para um produto de catálogo, o custo da linha de contrato baseada em produto assume o padrão do campo **Custo Padrão** no catálogo de produtos. O campo **Custo Padrão** no catálogo de produtos é configurado na moeda base da Organização. Quando o custo unitário é padronizado na linha do contrato, ele é convertido para a moeda de venda no contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Custo unitário em uma linha de contrato baseada em produto

Ter um custo unitário em uma linha de contrato baseada em produto permite custos diferentes para um produto em cada venda de uma unidade. Embora nem sempre seja necessário, há certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor. Considere este cenário:

A Fabrikam Robotics está instalando braços robóticos nas linhas de montagem da Adatum Corporation. A Fabrikam fornece serviços de instalação, mas os braços robóticos são adquiridos da Trey Research. Se a instalação de braços robóticos na Adatum Corporation abrir uma nova vertical de setor para a Trey Research, a Trey poderá oferecer um desconto especial referente a esse negócio à Fabrikam. Nesse caso, a Fabrikam cria uma linha de contrato com base em produto para Braços Robóticos e insere um custo por unidade para esse contrato, que é diferente do custo padrão de braços robóticos da Trey Research.
