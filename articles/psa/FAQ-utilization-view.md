---
title: Exibir horas trabalhadas passíveis de cobrança para recursos
description: Este tópico fornece informações sobre a exibição de horas trabalhadas do recurso.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992820"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="52f36-103">Exibir horas trabalhadas passíveis de cobrança para recursos</span><span class="sxs-lookup"><span data-stu-id="52f36-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="52f36-104">A **Exibição das Horas Trabalhadas** na página **Horas Trabalhadas do Recurso do Project Service** mostra as horas trabalhadas passíveis de cobrança de cada recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="52f36-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="52f36-105">Como a exibição é baseada no quadro de agendamento, você encontrará muitas funções iguais.</span><span class="sxs-lookup"><span data-stu-id="52f36-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Captura de tela da exibição Horas trabalhadas](media/FAQ-utilization-1.png)
 

<span data-ttu-id="52f36-107">O cálculo das horas trabalhadas passíveis de cobrança funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="52f36-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="52f36-108">Horas trabalhadas passíveis de cobrança = (horas de dados reais passíveis de cobrança) / (capacidade do recurso)</span><span class="sxs-lookup"><span data-stu-id="52f36-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="52f36-109">As células representam as horas trabalhadas passíveis de cobrança calculadas para o período selecionado (dias, semanas ou meses).</span><span class="sxs-lookup"><span data-stu-id="52f36-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="52f36-110">As cores em cada célula mostram as horas trabalhadas passíveis de cobrança para um recurso em comparação com as horas trabalhadas passíveis de cobrança de destino.</span><span class="sxs-lookup"><span data-stu-id="52f36-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="52f36-111">As horas trabalhadas de destino podem ser definidas na função padrão do recurso ou no recurso individual em si.</span><span class="sxs-lookup"><span data-stu-id="52f36-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="52f36-112">O cálculo analisa o individual para o destino primeiro e, em seguida, para a função padrão do recurso.</span><span class="sxs-lookup"><span data-stu-id="52f36-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="52f36-113">Definir destino em um recurso</span><span class="sxs-lookup"><span data-stu-id="52f36-113">Set target on a resource</span></span>

1. <span data-ttu-id="52f36-114">Vá para **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="52f36-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="52f36-115">Selecione um recurso para abrir o registro.</span><span class="sxs-lookup"><span data-stu-id="52f36-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="52f36-116">Na guia **Project Service**, você pode definir as horas trabalhadas de destino do recurso.</span><span class="sxs-lookup"><span data-stu-id="52f36-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Captura de tela do uso da guia Project Service para definir as horas trabalhadas de destino](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="52f36-118">Definir horas trabalhadas de destino em uma função</span><span class="sxs-lookup"><span data-stu-id="52f36-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="52f36-119">Vá para **Recursos** \> **Funções do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="52f36-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="52f36-120">Selecione uma função e abra o registro.</span><span class="sxs-lookup"><span data-stu-id="52f36-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="52f36-121">Defina as horas trabalhadas de destino para a função.</span><span class="sxs-lookup"><span data-stu-id="52f36-121">Set the target utilization for the role.</span></span>

> ![Captura de tela do uso de Funções de recursos para definir as horas trabalhadas de destino](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="52f36-123">Calcular horas trabalhadas passíveis de cobrança para um recurso</span><span class="sxs-lookup"><span data-stu-id="52f36-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="52f36-124">Para calcular as horas trabalhadas passíveis de cobrança para um recurso, é necessário preencher alguns pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="52f36-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="52f36-125">Definir função padrão para recurso individual</span><span class="sxs-lookup"><span data-stu-id="52f36-125">Set default role for individual resource</span></span>

<span data-ttu-id="52f36-126">Em primeiro lugar, as horas trabalhadas de destino devem ser definidas no recurso individual ou nas funções de recurso.</span><span class="sxs-lookup"><span data-stu-id="52f36-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="52f36-127">Se você estiver usando funções de recursos para destinos, cada recurso individual deve ter uma função padrão.</span><span class="sxs-lookup"><span data-stu-id="52f36-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="52f36-128">Para isso, vá para **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="52f36-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="52f36-129">Selecione um recurso, abra o registro e selecione a guia **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="52f36-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="52f36-130">Na grade **Função do Recurso**, verifique se há uma função para o recurso e se **É Padrão** está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="52f36-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="52f36-131">Alterar tipo de cobrança para função do recurso</span><span class="sxs-lookup"><span data-stu-id="52f36-131">Change billing type for resource role</span></span>

<span data-ttu-id="52f36-132">As funções do recurso devem estar definidas para ter um tipo de cobrança **Passível de Cobrança**.</span><span class="sxs-lookup"><span data-stu-id="52f36-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="52f36-133">Vá para **Recursos** \> **Funções do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="52f36-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="52f36-134">Abra o registro que deseja atualizar e defina o padrão do tipo de cobrança como **Passível de Cobrança**.</span><span class="sxs-lookup"><span data-stu-id="52f36-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="52f36-135">Definir horas de trabalho para a função do recurso</span><span class="sxs-lookup"><span data-stu-id="52f36-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="52f36-136">O recurso deve ter as horas de trabalho para o cálculo de capacidade.</span><span class="sxs-lookup"><span data-stu-id="52f36-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="52f36-137">Vá para **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="52f36-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="52f36-138">Selecione um recurso para abrir o registro e selecione **Mostrar Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="52f36-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="52f36-139">Você pode atualizar em massa a lista de recursos aplicando um **Modelo de Horas de Trabalho** na exibição **Lista de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="52f36-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="52f36-140">Solucionando problemas de horas reais passíveis de cobrança</span><span class="sxs-lookup"><span data-stu-id="52f36-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="52f36-141">As horas reais passíveis de cobrança são provenientes da entidade **Dados reais**.</span><span class="sxs-lookup"><span data-stu-id="52f36-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="52f36-142">Os dados reais com um tipo de cobrança **Passível de Cobrança** são incluídos no cálculo e, por isso, é necessário ter projetos em que os dados reais são passíveis de cobrança.</span><span class="sxs-lookup"><span data-stu-id="52f36-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="52f36-143">Se você não está vendo as horas trabalhadas passíveis de cobrança, veja a seguir alguns aspectos que você pode verificar:</span><span class="sxs-lookup"><span data-stu-id="52f36-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="52f36-144">O recurso tem horas de trabalho definidas para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="52f36-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="52f36-145">O recurso tem horas trabalhadas de destino definidas individualmente ou tem uma função padrão atribuída a ele.</span><span class="sxs-lookup"><span data-stu-id="52f36-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="52f36-146">A função tem horas trabalhadas de destino definidas para ela.</span><span class="sxs-lookup"><span data-stu-id="52f36-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="52f36-147">Os dados reais têm um tipo de cobrança de **Passível de Cobrança** para o período pelo qual você está aguardando o cálculo de horas trabalhadas.</span><span class="sxs-lookup"><span data-stu-id="52f36-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="52f36-148">Verifique o seguinte se você estiver vendo dados reais com tipos de cobrança diferentes de passível de cobrança:</span><span class="sxs-lookup"><span data-stu-id="52f36-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="52f36-149">A função usada nos dados reais tem em um tipo padrão de cobrança que não é passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="52f36-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="52f36-150">A função na linha de contrato de projeto dando suporte ao projeto foi definida como não passível de cobrança.</span><span class="sxs-lookup"><span data-stu-id="52f36-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="52f36-151">O projeto não tem uma linha de contrato associada.</span><span class="sxs-lookup"><span data-stu-id="52f36-151">The project does not have an associated contract line.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]