---
title: Configurar custos padrão para mão de obra e despesas
description: Este tópico explicar como configurar custos padrão para mão de obra e despesas de um projeto.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071485"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurar custos padrão para mão de obra e despesas

[!include [banner](../../includes/banner.md)]

Este tópico explicar como configurar custos padrão para mão de obra e despesas de um projeto. Esta tarefa usa o conjunto de dados USSI.

1. No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de custo (hora)**.
2. Selecione **Novo**.
3. No campo **Data de efetivação** , insira uma data.
4. No campo **Preço de custo** , insira um número. Você pode configurar um preço de custo padrão para a categoria de projeto ou pode configurar um preço de custo por número de trabalhador, número de projeto, categoria, data ou qualquer combinação dessas opções. O preço de custo aplicado é o preço de custo com o maior nível de detalhes.  
5. Selecione **Salvar**.
6. No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de venda (hora)**.
7. Selecione **Novo**.
8. No campo **Data de efetivação** , insira uma data.
9. No campo **Válido por** , selecione uma opção.
10. No campo **Preço** , insira um número. Você pode configurar um preço de venda padrão para transações por hora ou para uma categoria de projeto. Você também pode configurar preços de venda por número de trabalhador, número de projeto, categoria, data da transação ou qualquer combinação dessas opções. O preço de venda real, que é aplicado quando um trabalhador insere uma transação no Diário de horas é o preço de venda com o maior nível de detalhes. Por exemplo, se um preço de venda geral e um preço de venda específico de um trabalhador forem configurados, o preço de venda específico do trabalhador será usado.  
11. Selecione **Salvar**.
12. Feche a página.
13. No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de custo (despesa)**.
14. Selecione **Novo**.
15. No campo **Data de efetivação** , insira uma data.
16. No campo **Preço de custo** , insira um número. Vários campos podem ser preenchidos, mas isso é o mínimo necessário para salvar o registro.  
17. Selecione **Salvar**.
18. No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de venda (despesa)**.
19. Selecione **Novo**.
20. No campo **Data de efetivação** , insira uma data.
21. No campo **Válido por** , selecione uma opção.
22. No campo **Preço** , insira um número. O preço de venda real, que é aplicado quando um trabalhador insere transações em um diário de despesas é o preço de venda com o maior nível de detalhes. Por exemplo, se um preço de venda geral e um preço de venda específico de um trabalhador forem configurados, o preço de venda específico do trabalhador será usado.  
23. Selecione **Salvar**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]