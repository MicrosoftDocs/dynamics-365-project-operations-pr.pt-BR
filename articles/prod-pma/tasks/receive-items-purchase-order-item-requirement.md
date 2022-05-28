---
title: Receber itens no pedido de compra a partir da solicitação
description: Este tópico explica como receber itens em um pedido de compra de um requisito de item.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab08dda6e81609595f54f3dd71c0154c12807270
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682513"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]