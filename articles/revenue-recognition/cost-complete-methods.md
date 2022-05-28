---
title: Custo para concluir métodos
description: Este tópico fornece informações sobre os métodos usados para calcular o custo para concluir um projeto.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 244afa919e5fbc16be8f905acce2e2354c7da974
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601648"
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