---
title: Custo para concluir métodos
description: Este tópico fornece informações sobre os métodos usados para calcular o custo para concluir um projeto.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fe42ea0e1a5c562ec648fbf2a2924648af80381b9db8ffe0c209cb5247bb2ba2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997952"
---
# <a name="cost-to-complete-methods"></a>Custo para concluir métodos

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico fornece informações sobre os métodos usados para calcular o custo para concluir um projeto. Existem vários métodos que você pode usar para calcular o custo para concluir um projeto. 

Ao criar uma estimativa para um projeto, na página **Criar estimativa**, no campo **Custo para concluir o método**, é possível selecionar um dos seguintes custos para concluir o método.

| Custo para concluir o método    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Custo total – real            | Insira os custos estimados manualmente nos campos **Custo total** ou **Quantidade total** usando o botão **Estimativa de custo** na **Página de estimativa**. O sistema subtrai os custos reais dos totais inseridos. O total é o custo para concluir o projeto. Este método não usa as estimativas de despesas e atribuições de recursos inseridos no Project Operations criados no Microsoft Dataverse. O custo total ou a quantidade total podem ser atualizados manualmente conforme necessário.  |
| Previsão total - real        | As atribuições de recursos e as estimativas de despesas são usadas para determinar o valor total da previsão do projeto. Os custos reais são comparados com esta previsão para calcular o custo para concluir.                                                                                                                                                                                                                                                                          |
| Conforme estimativa anterior         | Os mesmos métodos de estimativa que foram usados no período anterior são usados aqui. Este método exige um modelo de previsão se o período anterior exigir um modelo de previsão.                                                                                                                                                                                                                                                                                                                           |
| Definir custo a ser concluído como zero | Normalmente usado antes do projeto previsto ser eliminado, este método associa as estimativas totais às transações reais lançadas e limpa a coluna **Custo para concluir**. Quando concluído, o resultado é sempre 100%. Para cada linha de custo criada, a caixa de seleção **Previsão** é desmarcada e a estimativa total é copiada da estimativa de custo anterior. O consumo real para o período previsto é deduzido do custo para concluir o projeto.              |
| A partir do modelo de custo           | O custo para concluir o método configurado no modelo de custo associado ao projeto de estimativa selecionado.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]