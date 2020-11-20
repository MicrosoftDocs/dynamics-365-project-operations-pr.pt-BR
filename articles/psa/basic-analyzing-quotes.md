---
title: Análise de cotações de projeto
description: Este tópico fornece informações sobre a análise das cotações do projeto.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127009"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="a522c-103">Análise de cotações de projeto</span><span class="sxs-lookup"><span data-stu-id="a522c-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a522c-104">O Dynamics 365 Project Service Automation analisa cotações do projeto para estimar a lucratividade.</span><span class="sxs-lookup"><span data-stu-id="a522c-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="a522c-105">Ele também analisa o quanto a cotação se alinha às expectativas do cliente quanto à data de entrega ou à data de conclusão e quanto ao orçamento.</span><span class="sxs-lookup"><span data-stu-id="a522c-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="a522c-106">Análise de lucratividade</span><span class="sxs-lookup"><span data-stu-id="a522c-106">Profitability analysis</span></span>

<span data-ttu-id="a522c-107">O Project Service Automation analisa a lucratividade usando a margem bruta e a margem bruta ajustada.</span><span class="sxs-lookup"><span data-stu-id="a522c-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="a522c-108">As margens brutas são calculadas usando a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="a522c-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="a522c-109">A margem bruta ajustada é calculada usando a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="a522c-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="a522c-110">Se os valores da margem bruta ou da margem bruta ajustada tiverem uma grande margem de diferença, grande parte do trabalho na cotação será classificada como não cobrável.</span><span class="sxs-lookup"><span data-stu-id="a522c-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="a522c-111">Análise das expectativas do cliente</span><span class="sxs-lookup"><span data-stu-id="a522c-111">Analysis of customer expectations</span></span>

<span data-ttu-id="a522c-112">Você pode analisar cotações e gerar gráficos para expectativas do cliente quanto ao agendamento e orçamento se inserir valores para os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="a522c-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="a522c-113">O campo **Data de entrega solicitada** no cabeçalho da cotação.</span><span class="sxs-lookup"><span data-stu-id="a522c-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="a522c-114">O campo **Orçamento do cliente** para cada linha de cotação (para linhas baseadas no projeto e linhas baseadas no produto).</span><span class="sxs-lookup"><span data-stu-id="a522c-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="a522c-115">A análise das expectativas do cliente quanto ao agendamento é realizada pela comparação da data de término mais recente dos detalhes da linha da cotação com a data de entrega solicitada em todas as linhas na cotação.</span><span class="sxs-lookup"><span data-stu-id="a522c-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="a522c-116">A análise das expectativas do cliente quanto ao orçamento é realizada pela comparação da soma do orçamento total do cliente com o valor cotado em todas as linhas da cotação.</span><span class="sxs-lookup"><span data-stu-id="a522c-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
