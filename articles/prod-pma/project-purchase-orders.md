---
title: Pedidos de compra de um projeto
description: Este artigo descreve os vários métodos que você pode usar para criar pedidos de compra para um projeto. O método que você utiliza depende da finalidade do pedido de compra e de quando os itens adquiridos são consumidos e cobrados de um projeto.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999342"
---
# <a name="purchase-orders-for-a-project"></a>Pedidos de compra de um projeto

[!include [banner](../includes/banner.md)]

Este artigo descreve os vários métodos que você pode usar para criar pedidos de compra para um projeto. O método que você utiliza depende da finalidade do pedido de compra e de quando os itens adquiridos são consumidos e cobrados de um projeto.

### <a name="methods-for-creating-a-purchase-order"></a>Métodos para criar um pedido de compra

Você pode usar um dos métodos a seguir para criar um pedido de compra no gerenciamento e contabilidade de projeto. A finalidade do pedido de compra determina quando o pedido de compra é consumido e, portanto, quando os itens são cobrados de um projeto.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Finalidade</th>
<th>Consumo de itens</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crie um pedido de compra diretamente em um projeto.</td>
<td>Use esse método para comprar itens de um fornecedor externo para consumo em um projeto. Você pode criar o pedido de compra de duas maneiras:
<ul>
<li>No próprio projeto. Nesse caso, o projeto já está definido para o pedido de compra.</li>
<li>Navegando até o pedido de compra do projeto. Você deve selecionar o fornecedor e o projeto para o qual criar o pedido de compra.</li>
</ul></td>
<td>Os itens são consumidos quando a fatura do fornecedor é atualizada.</td>
</tr>
<tr class="even">
<td>Crie um pedido de compra em um pedido de venda.</td>
<td>Use esse método para comprar itens ao criar um pedido de venda em um projeto.</td>
<td>Os itens são consumidos quando o pedido de venda é faturado ao cliente.</td>
</tr>
<tr class="odd">
<td>Crie um pedido de compra em uma solicitação de item.</td>
<td>Use esse método para comprar itens ao criar uma solicitação de item em um projeto.</td>
<td>Os itens são consumidos quando a guia de remessa da solicitação do item é atualizada.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Quando você atualiza a fatura do fornecedor ou a guia de remessa, é solicitado que atualize a guia de remessa na solicitação do item.

Para obter mais informações, consulte [Receber itens no pedido de compra em uma solicitação de item](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]