---
title: Diárias
description: Este tópico fornece informações sobre as regras de diária usadas no gerenciamento de despesas.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995247"
---
# <a name="per-diems"></a><span data-ttu-id="328cb-103">Diárias</span><span class="sxs-lookup"><span data-stu-id="328cb-103">Per diems</span></span>

<span data-ttu-id="328cb-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="328cb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="328cb-105">Uma diária é um subsídio pago a um funcionário que viaja a trabalho.</span><span class="sxs-lookup"><span data-stu-id="328cb-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="328cb-106">No gerenciamento de despesas, você pode criar regras de diária para várias situações de viagem.</span><span class="sxs-lookup"><span data-stu-id="328cb-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="328cb-107">As taxas de diária podem ser baseadas na época do ano, no local da viagem ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="328cb-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="328cb-108">Ao criar uma regra de diária, você pode especificar que uma porcentagem da taxa da diária será retida se um funcionário receber refeições ou serviços gratuitos.</span><span class="sxs-lookup"><span data-stu-id="328cb-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="328cb-109">Você também pode definir um número mínimo e máximo de horas que a taxa da diária pode aplicar à viagem de um funcionário.</span><span class="sxs-lookup"><span data-stu-id="328cb-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="328cb-110">Configuração</span><span class="sxs-lookup"><span data-stu-id="328cb-110">Configuration</span></span> 

1. <span data-ttu-id="328cb-111">Para adicionar locais de diária, vá para **Configurar** > **Cálculos e códigos** > **Locais de diária**.</span><span class="sxs-lookup"><span data-stu-id="328cb-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="328cb-112">Para cada um dos locais adicionados acima, selecione uma taxa de diária e uma moeda que seja válida entre uma data de início e término específica para hotel, refeições e outras despesas.</span><span class="sxs-lookup"><span data-stu-id="328cb-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="328cb-113">As taxas e moedas diárias são configuradas em **Configurar** > **Cálculos e códigos** > **Diárias**.</span><span class="sxs-lookup"><span data-stu-id="328cb-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="328cb-114">No página **Locais de diária**, configure os níveis da taxa de diária.</span><span class="sxs-lookup"><span data-stu-id="328cb-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="328cb-115">Os níveis da taxa de diária permitem definir a divisão percentual de uma diária para hotel, refeições e outras despesas.</span><span class="sxs-lookup"><span data-stu-id="328cb-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="328cb-116">Para especificar a redução percentual de refeição para o café da manhã, almoço ou jantar, atualize os campos na página **Parâmetros de gerenciamento de despesas** na guia **Diárias**.</span><span class="sxs-lookup"><span data-stu-id="328cb-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="328cb-117">Enviar despesas usando diária</span><span class="sxs-lookup"><span data-stu-id="328cb-117">Submit expenses using per diem</span></span>
<span data-ttu-id="328cb-118">Para enviar despesas usando diárias, use a categoria de despesas **Diárias** ao criar um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="328cb-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="328cb-119">Digite o **Data inicial de diária**, **Data final de diária** e o **Local da diária**.</span><span class="sxs-lookup"><span data-stu-id="328cb-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="328cb-120">O valor será calculado com base nas taxas de diária para o local selecionado e a redução de refeição será calculada com base nos níveis de taxas de diárias.</span><span class="sxs-lookup"><span data-stu-id="328cb-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]