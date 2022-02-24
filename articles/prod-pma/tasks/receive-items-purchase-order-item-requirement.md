---
title: Receber itens no pedido de compra a partir da solicitação
description: Este tópico explica como receber itens em um pedido de compra de um requisito de item.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071595"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Receber itens no pedido de compra a partir da solicitação

[!include [banner](../../includes/banner.md)]

Este tópico explica como receber itens em um pedido de compra de um requisito de item.

Ao usar uma necessidade de item em vez de uma transação de item, você pode planejar a entrega pouco antes de o item ser realmente usado, criar um pedido de compra, incluir o item na estrutura do contrato comercial e incluir a necessidade do item no planejamento da produção. 

Esta tarefa usa o conjunto de dados USSI.

1. No painel de navegação, vá para **Módulos > Gerenciamento e contabilidade de projetos > Projetos > Todos os projetos**.
2. Na lista, selecione o link na linha desejada.
3. No Painel de Ação, selecione **Plano**.
4. Selecione **Requisitos do item**.
5. Selecione **Novo**.
6. Na nova linha, insira ou selecione um valor no campo **Número de item**.
7. No campo **Quantidade**, insira um número.
8. Selecione **Salvar**.
9. No Painel de Ação, selecione **Gerenciar**.
10. Selecione **Funções**.
11. Selecione **Criar uma ordem de compra**.
12. Marque a caixa de seleção **Incluir todos**.
13. No campo **Conta do vendedor**, digite ou selecione um valor.
14. Selecione **OK**.
15. No painel de navegação, vá para **Módulos > Contas a pagar > Pedidos de compra > Todos os pedidos de compra**.
16. Na lista, selecione o link na linha desejada.
17. No Painel de Ação, selecione **Compra**.
18. Selecione **Confirmar**.
19. No Painel de Ação, selecione **Receber**.
20. Selecione **Recibo do produto**.
21. No campo **Recibo de produto**, digite um valor.
22. Selecione **OK**.

