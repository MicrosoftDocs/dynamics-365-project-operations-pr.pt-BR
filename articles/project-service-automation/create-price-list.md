---
title: Crie uma lista de preços
description: Como criar uma lista de preços no Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749164"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="52798-103">Criar uma lista de preços (Project Service)</span><span class="sxs-lookup"><span data-stu-id="52798-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="52798-104">As listas de preços fornecem um modelo que os gerentes de conta podem usar para criar cotações e projetos e para estabelecer os custos de um projeto.</span><span class="sxs-lookup"><span data-stu-id="52798-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="52798-105">Elas fornecem uma lista de itens de linha de funções e despesas, e o preço que será cobrado para cada um.</span><span class="sxs-lookup"><span data-stu-id="52798-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="52798-106">É possível criar várias listas de preços para que você possa manter estruturas de preços separadas para diferentes regiões que você vende seus produtos ou diferentes canais de vendas.</span><span class="sxs-lookup"><span data-stu-id="52798-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="52798-107">É uma boa ideia criar pelo menos uma lista de preços para cada moeda na qual você planeja cobrar os clientes.</span><span class="sxs-lookup"><span data-stu-id="52798-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="52798-108">Para criar estimativas financeiras para o trabalho a ser entregue, verifique se cada projeto tem um custo de suporte e uma lista de preços de venda.</span><span class="sxs-lookup"><span data-stu-id="52798-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="52798-109">Configure um custo e uma lista de preços de venda padrão que se apliquem a todos os projetos criados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="52798-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="52798-110">As listas de preços se baseiam em funções e em categorias de despesas, portanto, antes de criar uma lista de preços, verifique se você já configurou as funções e as categorias de despesas que deseja usar ao criar a lista de preços.</span><span class="sxs-lookup"><span data-stu-id="52798-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="52798-111">Vá para **Project Service > Listas de Preços**.</span><span class="sxs-lookup"><span data-stu-id="52798-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="52798-112">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="52798-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="52798-113">Em **Contexto**, selecione se a lista de preços é de **Custo**, de **Compra** ou de **Venda**.</span><span class="sxs-lookup"><span data-stu-id="52798-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="52798-114">Em **Nome**, insira um nome para a lista de preços.</span><span class="sxs-lookup"><span data-stu-id="52798-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="52798-115">Em **Moeda**, selecione a moeda que você usará para cobrança ou avaliação de custo.</span><span class="sxs-lookup"><span data-stu-id="52798-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="52798-116">Em **Unidade de Tempo**, especifique o período ao qual o preço se aplica, como dia ou hora.</span><span class="sxs-lookup"><span data-stu-id="52798-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="52798-117">Preencha a **Data de Início**, a **Data de término** e a **Descrição** conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="52798-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="52798-118">Clique em **Salvar** para criar o registro para poder continuar a editá-lo.</span><span class="sxs-lookup"><span data-stu-id="52798-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="52798-119">Para adicionar um preço da função à lista de preços, clique em **+** em **Preços da função**.</span><span class="sxs-lookup"><span data-stu-id="52798-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="52798-120">No painel **Preço de Função**, preencha os detalhes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="52798-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="52798-121">Continue a adicionar preços de função conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="52798-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="52798-122">Ao terminar, clique em **Salvar** no canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="52798-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="52798-123">Para adicionar um preço de categoria de despesas à lista de preços, clique em **+** em **Preços de categoria**.</span><span class="sxs-lookup"><span data-stu-id="52798-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="52798-124">No painel **Preço de Categoria de Transação**, preencha os detalhes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="52798-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="52798-125">Continue a adicionar preços de categorias conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="52798-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="52798-126">Ao terminar, clique em **Salvar** no canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="52798-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="52798-127">Para adicionar itens da lista de preços à lista de preços, clique em **+** em **Itens da Lista de Preços**.</span><span class="sxs-lookup"><span data-stu-id="52798-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="52798-128">No painel **Item da Lista de Preços**, preencha os detalhes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="52798-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="52798-129">Continue a adicionar itens da lista de preços conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="52798-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="52798-130">Ao terminar, clique em **Salvar** no canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="52798-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="52798-131">Para adicionar relacionamentos de regiões à lista de preços, clique em **+** **Relacionamentos de Regiões**.</span><span class="sxs-lookup"><span data-stu-id="52798-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="52798-132">Na janela **Nova Conexão**, preencha os detalhes e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="52798-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="52798-133">Continue a adicionar relacionamentos de regiões conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="52798-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="52798-134">Ao terminar, clique em **Salvar** no canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="52798-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="52798-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="52798-135">See Also</span></span>  
 [<span data-ttu-id="52798-136">Configurar Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="52798-136">Configure Project Service Automation</span></span>](../project-service/configure.md)
