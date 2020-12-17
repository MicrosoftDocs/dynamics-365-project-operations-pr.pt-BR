---
title: Atualizar atributos de plug-in com novas dimensões de preço
description: Este tópico fornece informações sobre como atualizar atributos de plug-in para dimensões de preço.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643204"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="56923-103">Atualizar atributos de plug-in com novas dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="56923-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="56923-104">Este tópico fornece informações sobre como atualizar atributos de plug-in para dimensões de preço.</span><span class="sxs-lookup"><span data-stu-id="56923-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="56923-105">Este tópico se aplica apenas aos recursos de cotação e contrato no Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="56923-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="56923-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="56923-106">Prerequisites</span></span>
<span data-ttu-id="56923-107">Antes de concluir as etapas neste tópico, você concluir os procedimentos nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="56923-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="56923-108">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="56923-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="56923-109">Adicionar campos personalizados a entidades transacionais e de configuração de preço </span><span class="sxs-lookup"><span data-stu-id="56923-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="56923-110">[Configurar campos personalizados como dimensões de preço](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="56923-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="56923-111">Se você não concluiu esses procedimentos, conclua-os e retorne a este tópico.</span><span class="sxs-lookup"><span data-stu-id="56923-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="56923-112">Registrar um plug-in</span><span class="sxs-lookup"><span data-stu-id="56923-112">Register a plug-in</span></span>
<span data-ttu-id="56923-113">Quando um detalhe de linha de cotação é criado na página **Linha de Cotação** para uma linha de cotação de projeto, o sistema cria duas linhas de estimativa.</span><span class="sxs-lookup"><span data-stu-id="56923-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="56923-114">Uma linha é para o custo da estimativa e a outra linha é para as vendas.</span><span class="sxs-lookup"><span data-stu-id="56923-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="56923-115">O mesmo se aplica às linhas de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="56923-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="56923-116">Quando você altera para a quantidade ou um campo no custo, essa alteração também é feita nas vendas.</span><span class="sxs-lookup"><span data-stu-id="56923-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="56923-117">Isso é possível porque os plug-ins PreOperation em Quotelinedetail e as entidades de detalhes de linha de contrato conectam atributos específicos do custo às vendas da transação.</span><span class="sxs-lookup"><span data-stu-id="56923-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="56923-118">Se você precisar que as mudanças feitas nos valores de dimensão de preço nas vendas também sejam feitas no custo, os plug-ins a seguir deverão ser registrados novamente após fazer alterações em uma dimensão de preço.</span><span class="sxs-lookup"><span data-stu-id="56923-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="56923-119">Estes são os plug-ins para atualizar e registrar novamente:</span><span class="sxs-lookup"><span data-stu-id="56923-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="56923-120">PreOperationContractLineDetailUpdate - **Atualizar msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="56923-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="56923-121">PreOperationQuoteLineDetailUpdate - **Atualiza msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="56923-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="56923-122">Conclua as etapas a seguir para atualizar e registrar novamente os plug-ins.</span><span class="sxs-lookup"><span data-stu-id="56923-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="56923-123">Abra **PluginRegistrationTool** e se conecte ao ambiente Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="56923-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="56923-124">Selecione **Pesquisa** e digite as primeiras letras do plug-in a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="56923-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="56923-125">Após encontrar o plug-in for, selecione-o e marque **Selecionar no Formulário Principal**.</span><span class="sxs-lookup"><span data-stu-id="56923-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="56923-126">Selecione a etapa **Atualizar msdyn_orderlinetransaction**, clique com o botão direito do mouse e selecione **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="56923-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="56923-127">Na página de diálogo **Atualizar**, selecione as reticências (**...**) nos atributos de filtragem.</span><span class="sxs-lookup"><span data-stu-id="56923-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="56923-128">A janela de atributos de filtragem é aberta e fornece uma lista de todos os atributos na entidade e as dimensões de preço.</span><span class="sxs-lookup"><span data-stu-id="56923-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="56923-129">Marque as caixas de seleção para os atributos de dimensão de preço.</span><span class="sxs-lookup"><span data-stu-id="56923-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="56923-130">Selecione **OK** para fechar a página e selecione **Atualizar Etapa**.</span><span class="sxs-lookup"><span data-stu-id="56923-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="56923-131">Repita as etapas de 2 a 7 para o segundo plug-in, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="56923-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="56923-132">Para este plug-in, você precisa atualizar a etapa **Atualização de msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="56923-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="56923-133">Feche **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="56923-133">Close **PluginRegistrationTool**.</span></span>
