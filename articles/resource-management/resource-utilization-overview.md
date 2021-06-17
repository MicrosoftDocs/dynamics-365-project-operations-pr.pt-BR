---
title: Visão geral da utilização de recurso
description: Este tópico fornece informações sobre a utilização do recurso no Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000782"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="ee7c4-103">Visão geral da utilização de recurso</span><span class="sxs-lookup"><span data-stu-id="ee7c4-103">Resource utilization overview</span></span>

<span data-ttu-id="ee7c4-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="ee7c4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee7c4-105">Os recursos podem ter horas trabalhadas faturáveis de destino.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="ee7c4-106">Essas horas trabalhadas de destino são definidas como um atributo na função padrão de um recurso ou definidas no registro do recurso reservável individual.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="ee7c4-107">Os cálculos de horas trabalhadas se baseiam nas horas reais que os recursos relataram usando entradas de hora aprovadas.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="ee7c4-108">As fórmulas a seguir são usadas para calcular as horas trabalhadas:</span><span class="sxs-lookup"><span data-stu-id="ee7c4-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="ee7c4-109">Horas trabalhadas faturáveis = Horas reais passíveis de cobrança ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ee7c4-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="ee7c4-110">Horas trabalhadas não faturáveis = Tempo real com ID do tipo de cobrança = Não passível de cobrança, Complementar ou Não disponível ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ee7c4-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="ee7c4-111">Interno = Tempo real sem contrato de vendas ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ee7c4-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="ee7c4-112">Capacidade do recurso = Horas de trabalho do recurso – Ausência temporária – Dias de folga</span><span class="sxs-lookup"><span data-stu-id="ee7c4-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="ee7c4-113">Você pode encontrar a exibição **Horas Trabalhadas do Recurso** no painel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="ee7c4-114">Cada célula na grade representa o percentual de horas trabalhadas faturáveis do recurso em um período, como dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="ee7c4-115">As fórmulas a seguir são usadas para colorir as células:</span><span class="sxs-lookup"><span data-stu-id="ee7c4-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="ee7c4-116">**Verde**: horas trabalhadas faturáveis >= horas trabalhadas de destino do recurso</span><span class="sxs-lookup"><span data-stu-id="ee7c4-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="ee7c4-117">**Amarelo**: horas trabalhadas de destino – 20 <= horas trabalhadas faturáveis < horas trabalhadas de destino</span><span class="sxs-lookup"><span data-stu-id="ee7c4-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="ee7c4-118">**Vermelho**: horas trabalhadas faturáveis < horas trabalhadas de destino – 20</span><span class="sxs-lookup"><span data-stu-id="ee7c4-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="ee7c4-119">Como a exibição **Horas Trabalhadas do Recurso** é baseada no Painel de Agendamento, você pode usar as funcionalidades de filtragem dele para filtrar seus resultados.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="ee7c4-120">A grade exige que você defina as horas trabalhadas de destino na função ou no recurso individual.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="ee7c4-121">Para definir essa configuração, vá para **Recursos** > **Funções de recursos**.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="ee7c4-122">Além disso, uma função padrão deve ser atribuída a cada recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="ee7c4-123">Vá para **Recursos** > **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="ee7c4-124">Na guia **Project Service**, verifique se uma função do recurso está definida e se o campo **É Padrão** está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="ee7c4-125">É possível adicionar outras funções onde **É Padrão** = **Não**.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="ee7c4-126">A função onde **É Padrão** = **Sim** é usada para avaliar a utilização do recurso em relação ao destino dessa função.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="ee7c4-127">Na guia **Project Service**, você também pode definir horas trabalhadas de destino individuais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="ee7c4-128">O cálculo de horas trabalhadas então usa essas horas trabalhadas de destino para avaliar o destino do recurso em vez do destino da função padrão do recurso.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="ee7c4-129">As horas trabalhadas são mostradas para um recurso, somente se ele tiver tempo passível de cobrança, aprovado durante o período exibido na grade.</span><span class="sxs-lookup"><span data-stu-id="ee7c4-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]