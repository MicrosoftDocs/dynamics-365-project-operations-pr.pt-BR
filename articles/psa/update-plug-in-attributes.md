---
title: Atualizar os atributos de plug-in para incluir novas dimensões de precificação
description: Este tópico fornece informações sobre a atualização de atributos de plug-in para dimensões de precificação.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c42e5fda79d51430f4dedf46037e11c86a38c474
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121834"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="abf1c-103">Atualizar os atributos de plug-in para incluir novas dimensões de precificação</span><span class="sxs-lookup"><span data-stu-id="abf1c-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="abf1c-104">Se você não estiver usando os recursos de cotação e contratação do Project Service Automation (PSA), poderá ignorar este tópico.</span><span class="sxs-lookup"><span data-stu-id="abf1c-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="abf1c-105">Este tópico presume que os procedimentos nos tópicos foram concluídos, [Criar campos personalizados e entidades](create-custom-fields-entities.md), [Adicionar campos personalizados para configuração de preço e entidades transacionais](field-references.md) e [Configurar campos personalizados como dimensões de preço](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="abf1c-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="abf1c-106">Se você não concluiu esses procedimentos, volte e conclua-os e retorne a este tópico.</span><span class="sxs-lookup"><span data-stu-id="abf1c-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="abf1c-107">Quando um detalhe da linha de cotação é criado na página **Linha de Cotação** para uma linha de cotação do projeto, o sistema cria duas linhas de estimativa em segundo plano – uma linha para o lado do custo da estimativa e outra para o lado das vendas.</span><span class="sxs-lookup"><span data-stu-id="abf1c-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="abf1c-108">O mesmo se aplica às linhas de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="abf1c-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="abf1c-109">Quando você altera uma quantidade ou um campo no lado do custo, essa alteração é propagada para o lado das vendas.</span><span class="sxs-lookup"><span data-stu-id="abf1c-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="abf1c-110">Isso é possível por causa dos plug-ins a seguir que devem ser registrados novamente após uma alteração nas dimensões de precificação.</span><span class="sxs-lookup"><span data-stu-id="abf1c-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="abf1c-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="abf1c-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="abf1c-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="abf1c-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="abf1c-113">As etapas a seguir orientam você no processo de registro dos plug-ins.</span><span class="sxs-lookup"><span data-stu-id="abf1c-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="abf1c-114">Abra **PluginRegistrationTool** e conecte-se à sua instância online</span><span class="sxs-lookup"><span data-stu-id="abf1c-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="abf1c-115">Clique em **Pesquisar** e procure o plug-in a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="abf1c-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Captura de tela da árvore de pesquisa](media/PRT-1.png)

3. <span data-ttu-id="abf1c-117">Depois que o plug-in for encontrado, selecione-o e clique em **Selecionar no Formulário Principal**.</span><span class="sxs-lookup"><span data-stu-id="abf1c-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="abf1c-118">Selecione a etapa do plug-in a ser atualizado, clique com o botão direito do mouse e selecione **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="abf1c-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Captura de tela do plug-in a ser atualizado](media/PRT-2.png)
 
5. <span data-ttu-id="abf1c-120">Na janela de atualização, clique nas reticências (**...**) nos atributos de filtragem.</span><span class="sxs-lookup"><span data-stu-id="abf1c-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Captura de tela das informações de configuração Atualizar etapa existente](media/PRT-3.png)
 
6. <span data-ttu-id="abf1c-122">Marque as caixas de seleção do atributo de precificação.</span><span class="sxs-lookup"><span data-stu-id="abf1c-122">Select the pricing attribute check boxes.</span></span>

 ![Captura de tela mostrando a marcação da caixa de seleção de atributos de precificação](media/PRT-4.png)

7. <span data-ttu-id="abf1c-124">Clique em **OK** para fechar a página e selecione **Atualizar Etapa**.</span><span class="sxs-lookup"><span data-stu-id="abf1c-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Captura de tela mostrando o botão “Atualizar Etapa”](media/PRT-5.png)
 
8. <span data-ttu-id="abf1c-126">Repita esse processo para o segundo plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="abf1c-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="abf1c-127">Feche a ferramenta de registro de plug-in.</span><span class="sxs-lookup"><span data-stu-id="abf1c-127">Close the plug-in registration tool.</span></span>

