---
title: Desativar uma dimensão de precificação
description: Este tópico mostra como configurar dimensões de precificação na solução Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f308104246efe671d2001e660aa8c0ab9ef44c7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581684"
---
# <a name="turn-off-a-pricing-dimension"></a>Desativar uma dimensão de precificação

[!include [banner](../includes/psa-now-project-operations.md)]

Pode ser necessário analisar e atualizar sua estratégia de precificação de tempos a tempos. Quaisquer atualizações que você fizer podem exigir que você desative uma dimensão de precificação existente e crie uma outra. Por exemplo, você pode ter precificado anteriormente por **Função**, mas agora optou por **Experiência de trabalho**. Isso pode exigir que você desative **Função** como uma dimensão de precificação e crie **Experiência de trabalho** como uma nova dimensão de precificação. 

É possível desativar uma dimensão de precificação, independentemente de ser predefinida ou personalizada, definindo os campos **Aplicável ao custo** e **Aplicável a vendas** da dimensão de precificação como **Não**.

Contudo, ao fazer isso, você receberá a mensagem de erro a seguir.

![É provável que haja um erro no processo empresarial ao desativar uma dimensão de preço.](media/Business-Process-Error.png)


Essa mensagem de erro indica que existem registros de preços configurados anteriormente para a dimensão que está sendo desativada. Todos os registros **Preço da Função** e **Markup de Preço da Função** que se referem a uma dimensão devem ser excluídos antes que a aplicabilidade da dimensão possa ser definida como **Não**. Esta regra se aplica às dimensões de precificação predefinidas e a quaisquer dimensões de precificação personalizadas que você possa ter criado. O motivo dessa validação é porque o Project Service tem uma restrição de que cada registro **Preço da Função** deve ter uma combinação exclusiva de dimensões. Por exemplo, em uma lista de preços chamada **US Cost Rates 2018**, você tem a seguinte linha **Preço da função**. 

| Título padrão         | Unidades Organizacionais    |Unidade   |Preço  |Moeda  |
| -----------------------|-------------|-------|-------|----------|
| Engenheiro de sistemas|Cabral EUA|Hour| 100|USD|
| Engenheiro de sistemas sênior|Cabral EUA|Hour| 150| USD|


Quando você desativa o **Título padrão** como a dimensão de precificação e o mecanismo de precificação do Project Service procura um preço, ele usa apenas o valor **Unidade Organizacional** no contexto de entrada. Se a **Unidade Organizacional** do contexto de entrada for “Cabral US”, o resultado será não determinado porque as duas linhas corresponderão. Para evitar esse cenário, ao criar registros **Preço da Função**, o Project Service valida que a combinação de dimensões é exclusiva. Se a dimensão for desativada após a criação dos registros **Preço da Função**, essa restrição poderá ser violada. Portanto, é necessário que, antes de desativar uma dimensão, você exclua todas as linhas **Preço da Função** e **Markup de Preço da Função** que tenham esse valor de dimensão preenchido.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
