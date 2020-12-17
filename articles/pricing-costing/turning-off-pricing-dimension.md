---
title: Desativar uma dimensão de precificação
description: Este tópico fornece informações sobre como desativar dimensões de precificação.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650035"
---
# <a name="turning-off-a-pricing-dimension"></a>Desativar uma dimensão de precificação

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Pode ser necessário analisar e atualizar sua estratégia de precificação de tempos a tempos. Quaisquer atualizações que você fizer podem exigir que você desative uma dimensão de precificação existente e crie uma outra. Por exemplo, você pode ter precificado anteriormente por **Função**, mas agora optou por **Experiência de trabalho**. Isso pode exigir que você desative **Função** como uma dimensão de precificação e crie **Experiência Profissional** como uma nova dimensão de precificação. 

É possível desativar uma dimensão de precificação, independentemente de ser predefinida ou personalizada, definindo os campos **Aplicável ao custo** e **Aplicável a vendas** da dimensão de precificação como **Não**.

No entanto, ao fazer isso, você pode receber a mensagem de erro, **A dimensão de precificação não pode ser atualizada nem excluída se houver registros de preços associados.**

![É provável que haja um erro no processo de negócios ao desativar uma dimensão de precificação](media/Business-Process-Error.png)

Essa mensagem de erro indica que existem registros de preços configurados anteriormente para a dimensão que está sendo desativada. Todos os registros **Preço da Função** e **Markup de Preço da Função** que se referem a uma dimensão devem ser excluídos antes que a aplicabilidade da dimensão possa ser definida como **Não**. Esta regra se aplica às dimensões de precificação predefinidas e a quaisquer dimensões de precificação personalizadas que você possa ter criado. O motivo dessa validação é que cada registro **Preço da Função** deve ter uma combinação exclusiva de dimensões. Por exemplo, em uma lista de preços chamada **US Cost Rates 2018**, você tem a seguinte linha **Preço da função**. 

| Título padrão         | Unidades Organizacionais    |Unidade   |Preço  |Moeda  |
| -----------------------|-------------|-------|-------|----------|
| Engenheiro de sistemas|Cabral EUA|Hour| 100|USD|
| Engenheiro de sistemas sênior|Cabral EUA|Hour| 150| USD|


Quando você desativa **Cargo Padrão** como a dimensão de precificação e o mecanismo de precificação procura um preço, ele usa apenas o valor **Unidade Organizacional** do contexto de entrada. Se a **Unidade Organizacional** do contexto de entrada for “Cabral US”, o resultado será não determinado porque as duas linhas corresponderão. Para evitar esse cenário, ao criar registros **Preço da Função**, o sistema valida que a combinação de dimensões é exclusiva. Se a dimensão for desativada após a criação dos registros **Preço da Função**, essa restrição poderá ser violada. Portanto, é necessário que, antes de desativar uma dimensão, você exclua todas as linhas **Preço da Função** e **Markup de Preço da Função** que tenham esse valor de dimensão preenchido.
