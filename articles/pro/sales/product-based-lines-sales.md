---
title: Linhas de oportunidade baseadas em produto
description: Este tópico fornece informações sobre itens de linha de oportunidade baseados em produto no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071354"
---
# <a name="product-based-opportunity-lines"></a>Linhas de oportunidade baseadas em produto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_

As linhas de oportunidade baseadas em produto são itens de linha na Oportunidade. Essas linhas são entregues ao cliente como itens de linha distintos na fatura eventual, sem quaisquer outros serviços de valor agregado. O gasto e o consumo associados não são controlados nas tarefas de qualquer projeto relacionado.

As linhas baseadas em produtos podem ser itens de catálogo ou produtos escritos. A maior parte da funcionalidade nas linhas baseadas no produto de uma Oportunidade segue a funcionalidade fornecida pelo aplicativo Dynamics 365 Sales. Para obter mais informações sobre linhas de oportunidade baseadas em produtos, consulte [Adicione produtos a uma oportunidade](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

As linhas de oportunidade baseadas em produto utilizam um conceito que é específico de oportunidades baseadas em projeto, que é o **Orçamento do cliente**. Use este campo para controlar o valor que o cliente está disposto a pagar pelo item de linha.

Se o método de receita do resumo da oportunidade for definido como **Calculado pelo sistema** , os valores do orçamento do cliente nas linhas baseadas em produto e projeto são resumidos para calcular a receita estimada.
