---
title: Tipos de período
description: Este tópico fornece informações sobre como configurar tipos de período para estimativa de receita.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531353"
---
# <a name="period-types"></a><span data-ttu-id="56a34-103">Tipos de período</span><span class="sxs-lookup"><span data-stu-id="56a34-103">Period types</span></span>

<span data-ttu-id="56a34-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="56a34-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="56a34-105">Um tipo de período define a frequência com que a receita de um projeto é estimada.</span><span class="sxs-lookup"><span data-stu-id="56a34-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="56a34-106">Este tópico fornece informações sobre como configurar tipos de período para estimativa de receita.</span><span class="sxs-lookup"><span data-stu-id="56a34-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="56a34-107">Criar e trabalhar com tipos de período</span><span class="sxs-lookup"><span data-stu-id="56a34-107">Create and work with period types</span></span>
<span data-ttu-id="56a34-108">Para criar e trabalhar com tipos de período, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="56a34-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="56a34-109">em seu ambiente do Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projeto** > **Configuração** > **Estimativas** > **Tipos de período**.</span><span class="sxs-lookup"><span data-stu-id="56a34-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="56a34-110">Selecione **Novo** para criar um tipo de período.</span><span class="sxs-lookup"><span data-stu-id="56a34-110">Select **New** to create new period type.</span></span> <span data-ttu-id="56a34-111">Insira um nome e uma descrição.</span><span class="sxs-lookup"><span data-stu-id="56a34-111">Enter a name and description.</span></span>
3. <span data-ttu-id="56a34-112">No campo **Frequência**, selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="56a34-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="56a34-113">Se você selecionar **Semana**, **Por quinzena**, **Quinzenal**, **Mês**, **Dia**, **Trimestre**, ou **Ano**, o calendário será usado para gerar os períodos.</span><span class="sxs-lookup"><span data-stu-id="56a34-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="56a34-114">Se você selecionar **Período contábil**, os períodos contábeis da configuração da Contabilidade serão usados para gerar os períodos.</span><span class="sxs-lookup"><span data-stu-id="56a34-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="56a34-115">Se selecionar **Ilimitado**, você poderá especificar períodos personalizados.</span><span class="sxs-lookup"><span data-stu-id="56a34-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="56a34-116">Selecione o registro do tipo de período e selecione **Gerar períodos** para criar períodos para o tipo de período.</span><span class="sxs-lookup"><span data-stu-id="56a34-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="56a34-117">Com base na frequência do período selecionado, você pode ter a opção de especificar uma data de início ou o número de períodos a serem gerados.</span><span class="sxs-lookup"><span data-stu-id="56a34-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="56a34-118">Selecione **Períodos** para revisar os períodos gerados.</span><span class="sxs-lookup"><span data-stu-id="56a34-118">Select **Periods** to review generated periods.</span></span>

