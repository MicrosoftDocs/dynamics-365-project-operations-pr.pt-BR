---
title: Criar cotações de projetos a partir de oportunidades
description: Este tópico fornece informações sobre como criar uma cotação de projeto a partir de uma projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898518"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="f6185-103">Criar cotações de projetos a partir de oportunidades</span><span class="sxs-lookup"><span data-stu-id="f6185-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="f6185-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="f6185-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f6185-105">As cotações podem ser criadas a partir de oportunidades de projeto das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="f6185-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="f6185-106">Na guia **Cotações** na página **Oportunidade de projeto**</span><span class="sxs-lookup"><span data-stu-id="f6185-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="f6185-107">A partir do fluxo de processo de vendas de oportunidade</span><span class="sxs-lookup"><span data-stu-id="f6185-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="f6185-108">Ao atualizar a referência de oportunidade em uma cotação existente</span><span class="sxs-lookup"><span data-stu-id="f6185-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="f6185-109">Na guia Cotações da página Oportunidade de projeto</span><span class="sxs-lookup"><span data-stu-id="f6185-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="f6185-110">Para criar uma cotação de projeto a partir de uma oportunidade, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6185-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="f6185-111">Abra a página **Oportunidade de projeto** e selecione a guia **Cotações**.</span><span class="sxs-lookup"><span data-stu-id="f6185-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="f6185-112">Na sub-grade **Cotações**, selecione o **+** para criar uma nova cotação de projeto com base na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f6185-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="f6185-113">Todas as linhas de oportunidade e listas de preços do projeto relacionadas são copiadas para a nova cotação da oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f6185-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="f6185-114">A partir do fluxo de processo de vendas de oportunidade</span><span class="sxs-lookup"><span data-stu-id="f6185-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="f6185-115">Para criar uma cotação a partir do fluxo de processo de vendas de Oportunidade, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6185-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="f6185-116">No fluxo do processo de vendas da Oportunidade, abra a Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f6185-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="f6185-117">Selecione o estágio **Qualificar**.</span><span class="sxs-lookup"><span data-stu-id="f6185-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="f6185-118">Selecione **Próximo** e então selecione **+ Criar** para criar uma nova cotação.</span><span class="sxs-lookup"><span data-stu-id="f6185-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="f6185-119">A maioria das informações na guia **Resumo** para esta nova cotação terá a oportunidade como padrão.</span><span class="sxs-lookup"><span data-stu-id="f6185-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="f6185-120">Insira qualquer informação necessária que esteja faltando ou atualize os valores padrão conforme necessário na aba **Resumo**,</span><span class="sxs-lookup"><span data-stu-id="f6185-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="f6185-121">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="f6185-121">Select **Save**.</span></span> <span data-ttu-id="f6185-122">A nova cotação é criada e associada à oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f6185-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="f6185-123">Agora você pode ver as informações de cotação na guia **Cotações** da página **Oportunidade**.</span><span class="sxs-lookup"><span data-stu-id="f6185-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="f6185-124">O processo de vendas de oportunidades passa para a próxima etapa, **Propor**.</span><span class="sxs-lookup"><span data-stu-id="f6185-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="f6185-125">Ao atualizar a referência de oportunidade em uma cotação existente</span><span class="sxs-lookup"><span data-stu-id="f6185-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="f6185-126">Uma cotação existente pode ser vinculada a uma Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f6185-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="f6185-127">Conclua as etapas a seguir para atualizar as informações da oportunidade em uma cotação existente.</span><span class="sxs-lookup"><span data-stu-id="f6185-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="f6185-128">Abra a página **Cotação** e selecione a guia **Resumo**.</span><span class="sxs-lookup"><span data-stu-id="f6185-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="f6185-129">No campo **Oportunidade**, selecione a oportunidade que deseja vincular à cotação.</span><span class="sxs-lookup"><span data-stu-id="f6185-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="f6185-130">Você pode ver a cotação na grade **Cotações** da Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f6185-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="f6185-131">Usando o processo de vendas de oportunidade, a oportunidade pode ser movida para a próxima fase, **Propor**.</span><span class="sxs-lookup"><span data-stu-id="f6185-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="f6185-132">Ao mover uma oportunidade para este estágio, você pode selecionar esta cotação em uma lista de cotações associadas a esta oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f6185-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="f6185-133">Selecionar esta cotação indica que você está avançando com ela.</span><span class="sxs-lookup"><span data-stu-id="f6185-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="f6185-134">Todas as outras cotações associadas à Oportunidade ainda estarão disponíveis e ativas até que uma delas seja ganha.</span><span class="sxs-lookup"><span data-stu-id="f6185-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="f6185-135">Você pode mover o processo de vendas de volta para o estágio anterior **Qualificar** e escolha outra citação para seguir em frente.</span><span class="sxs-lookup"><span data-stu-id="f6185-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
