---
title: Criar soluções personalizadas para dimensões de preço
description: Este tópico explica como criar uma solução personalizada ao criar dimensões de preço personalizadas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071437"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="af876-103">Criar soluções personalizadas para dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="af876-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af876-104">Todas as alterações de dimensão de preço personalizada devem ficar em uma solução separada.</span><span class="sxs-lookup"><span data-stu-id="af876-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="af876-105">Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="af876-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="af876-106">Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a para outras instâncias para reutilizar sua configuração de preço.</span><span class="sxs-lookup"><span data-stu-id="af876-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="af876-107">Selecione **Configurações** > **Soluções** e selecione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="af876-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="af876-108">Nomeie a solução, **dimensões de preço da \<your organization name>** , insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="af876-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Criando uma solução personalizada para dimensões de preço](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="af876-110">Adicionar todas as entidades necessárias e componentes relacionados à Solução de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="af876-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="af876-111">Você precisará adicionar as entidades a seguir do Project Service à sua solução de precificação.</span><span class="sxs-lookup"><span data-stu-id="af876-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="af876-112">Conclua as etapas deste procedimento para fazer algumas alterações importantes de esquema na solução de precificação para que as entidades se tornem conscientes das novas dimensões de preço.</span><span class="sxs-lookup"><span data-stu-id="af876-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="af876-113">Selecione **Configurações** > **Soluções** e clique duas vezes em **\<your organization name> dimensões de preço**.</span><span class="sxs-lookup"><span data-stu-id="af876-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="af876-114">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="af876-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="af876-115">Na caixa de diálogo **Componentes da Solução** , selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="af876-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="af876-116">Real</span><span class="sxs-lookup"><span data-stu-id="af876-116">Actual</span></span>
- <span data-ttu-id="af876-117">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="af876-117">Bookable Resource</span></span>
- <span data-ttu-id="af876-118">Linha de Estimativa</span><span class="sxs-lookup"><span data-stu-id="af876-118">Estimate Line</span></span>
- <span data-ttu-id="af876-119">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="af876-119">Project Task</span></span>
- <span data-ttu-id="af876-120">Detalhe da Linha da Fatura</span><span class="sxs-lookup"><span data-stu-id="af876-120">Invoice Line Detail</span></span>
- <span data-ttu-id="af876-121">Linha do Diário</span><span class="sxs-lookup"><span data-stu-id="af876-121">Journal Line</span></span>
- <span data-ttu-id="af876-122">Detalhe da Linha de Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="af876-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="af876-123">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="af876-123">Project Team Member</span></span>
- <span data-ttu-id="af876-124">Detalhes da Linha de Cotação</span><span class="sxs-lookup"><span data-stu-id="af876-124">Quote Line Detail</span></span>
- <span data-ttu-id="af876-125">Markup de Preço da Função</span><span class="sxs-lookup"><span data-stu-id="af876-125">Role Price Markup</span></span>
- <span data-ttu-id="af876-126">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="af876-126">Role Price</span></span> 
- <span data-ttu-id="af876-127">Entrada de Horas</span><span class="sxs-lookup"><span data-stu-id="af876-127">Time Entry</span></span> 

> ![Adicionar entidades existentes à solução de dimensões de preço](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="af876-130">Certifique-se de incluir todos os formulários e exibições para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="af876-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="af876-131">Quando solicitado a incluir entidades dependentes para as entidades selecionadas, selecione **Não**.</span><span class="sxs-lookup"><span data-stu-id="af876-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Não inclua todos os componentes selecionados](media/Do-not-include-required.png)


