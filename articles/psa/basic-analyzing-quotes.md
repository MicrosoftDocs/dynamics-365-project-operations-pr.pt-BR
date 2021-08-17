---
title: Análise de cotações de projeto
description: Este tópico fornece informações sobre a análise das cotações do projeto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b50f419d2c13cff4914f4b589c8d7ad9099c8734834d75f8d17104d2db40049b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002812"
---
# <a name="analysis-of-project-quotes"></a>Análise de cotações de projeto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Dynamics 365 Project Service Automation analisa cotações do projeto para estimar a lucratividade. Ele também analisa o quanto a cotação se alinha às expectativas do cliente quanto à data de entrega ou à data de conclusão e quanto ao orçamento.

## <a name="profitability-analysis"></a>Análise de lucratividade

O Project Service Automation analisa a lucratividade usando a margem bruta e a margem bruta ajustada.

- As margens brutas são calculadas usando a seguinte fórmula:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- A margem bruta ajustada é calculada usando a seguinte fórmula:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Se os valores da margem bruta ou da margem bruta ajustada tiverem uma grande margem de diferença, grande parte do trabalho na cotação será classificada como não cobrável.

## <a name="analysis-of-customer-expectations"></a>Análise das expectativas do cliente

Você pode analisar cotações e gerar gráficos para expectativas do cliente quanto ao agendamento e orçamento se inserir valores para os seguintes campos:

- O campo **Data de entrega solicitada** no cabeçalho da cotação.
- O campo **Orçamento do cliente** para cada linha de cotação (para linhas baseadas no projeto e linhas baseadas no produto).

A análise das expectativas do cliente quanto ao agendamento é realizada pela comparação da data de término mais recente dos detalhes da linha da cotação com a data de entrega solicitada em todas as linhas na cotação.

A análise das expectativas do cliente quanto ao orçamento é realizada pela comparação da soma do orçamento total do cliente com o valor cotado em todas as linhas da cotação.


[!INCLUDE[footer-include](../includes/footer-banner.md)]