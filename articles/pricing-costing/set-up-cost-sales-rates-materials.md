---
title: Configurar taxas de custo e de vendas para materiais
description: Este artigo fornece informações sobre como configurar as taxas de custo e vendas para materiais usados em projetos.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911766"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Configurar taxas de custo e de vendas para materiais

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Você pode configurar preços de custo e de vendas para produtos no Dynamics 365 Project Operations. Os preços de custo e de vendas de produtos só podem ser listados em uma moeda, que deve ser a moeda no cabeçalho da lista de preços.

Para configurar as taxas de custo e de vendas de produtos, conclua as etapas a seguir. 

1. Acesse **Vendas** > **Clientes** > **Listas de Preços** e selecione **Novo** para criar uma nova lista de preços. 
2. Em **Itens da lista de preços**, no menu de subgrade, selecione **Novo item da lista de preços**. 
3. Na página **Criação Rápida**, insira o produto e a unidade para os quais você está criando o novo preço.

Para obter mais informações sobre como definir preços para itens de catálogo, consulte [Definir preços de produtos com listas de preços e itens da lista de preços](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) e [Precisão decimal em moeda e preço](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> O Dynamics 365 Project Operations não oferece suporte a todos os métodos de precificação de produtos do Dynamics 365 Sales. O único método de precificação com suporte para produtos a serem usados em projetos é *Valor da moeda*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
