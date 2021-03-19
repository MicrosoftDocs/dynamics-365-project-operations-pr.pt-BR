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
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287269"
---
# <a name="period-types"></a><span data-ttu-id="fbfbc-103">Tipos de período</span><span class="sxs-lookup"><span data-stu-id="fbfbc-103">Period types</span></span>

<span data-ttu-id="fbfbc-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="fbfbc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fbfbc-105">Um tipo de período define a frequência com que a receita de um projeto é estimada.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="fbfbc-106">Este tópico fornece informações sobre como configurar tipos de período para estimativa de receita.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="fbfbc-107">Criar e trabalhar com tipos de período</span><span class="sxs-lookup"><span data-stu-id="fbfbc-107">Create and work with period types</span></span>
<span data-ttu-id="fbfbc-108">Para criar e trabalhar com tipos de período, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fbfbc-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="fbfbc-109">em seu ambiente do Dynamics 365 Finance, acesse **Gerenciamento e contabilidade de projeto** > **Configuração** > **Estimativas** > **Tipos de período**.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="fbfbc-110">Selecione **Novo** para criar um tipo de período.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-110">Select **New** to create new period type.</span></span> <span data-ttu-id="fbfbc-111">Insira um nome e uma descrição.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-111">Enter a name and description.</span></span>
3. <span data-ttu-id="fbfbc-112">No campo **Frequência**, selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="fbfbc-113">Se você selecionar **Semana**, **Por quinzena**, **Quinzenal**, **Mês**, **Dia**, **Trimestre**, ou **Ano**, o calendário será usado para gerar os períodos.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="fbfbc-114">Se você selecionar **Período contábil**, os períodos contábeis da configuração da Contabilidade serão usados para gerar os períodos.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="fbfbc-115">Se selecionar **Ilimitado**, você poderá especificar períodos personalizados.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="fbfbc-116">Selecione o registro do tipo de período e selecione **Gerar períodos** para criar períodos para o tipo de período.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="fbfbc-117">Com base na frequência do período selecionado, você pode ter a opção de especificar uma data de início ou o número de períodos a serem gerados.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="fbfbc-118">Selecione **Períodos** para revisar os períodos gerados.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]