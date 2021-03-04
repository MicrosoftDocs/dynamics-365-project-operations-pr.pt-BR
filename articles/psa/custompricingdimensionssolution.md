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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144624"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="29b2f-103">Criar soluções personalizadas para dimensões de preço</span><span class="sxs-lookup"><span data-stu-id="29b2f-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="29b2f-104">Todas as alterações de dimensão de preço personalizada devem ficar em uma solução separada.</span><span class="sxs-lookup"><span data-stu-id="29b2f-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="29b2f-105">Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="29b2f-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="29b2f-106">Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a para outras instâncias para reutilizar sua configuração de preço.</span><span class="sxs-lookup"><span data-stu-id="29b2f-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="29b2f-107">Selecione **Configurações** > **Soluções** e selecione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="29b2f-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="29b2f-108">Nomeie a solução, **dimensões de preço da \<your organization name>**, insira as informações necessárias restantes e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="29b2f-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Criando uma solução personalizada para dimensões de preço](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="29b2f-110">Adicionar todas as entidades necessárias e componentes relacionados à Solução de dimensão de preço</span><span class="sxs-lookup"><span data-stu-id="29b2f-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="29b2f-111">Você precisará adicionar as entidades a seguir do Project Service à sua solução de precificação.</span><span class="sxs-lookup"><span data-stu-id="29b2f-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="29b2f-112">Conclua as etapas deste procedimento para fazer algumas alterações importantes de esquema na solução de precificação para que as entidades se tornem conscientes das novas dimensões de preço.</span><span class="sxs-lookup"><span data-stu-id="29b2f-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="29b2f-113">Selecione **Configurações** > **Soluções** e clique duas vezes em **\<your organization name> dimensões de preço**.</span><span class="sxs-lookup"><span data-stu-id="29b2f-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="29b2f-114">No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="29b2f-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="29b2f-115">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="29b2f-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="29b2f-116">Real</span><span class="sxs-lookup"><span data-stu-id="29b2f-116">Actual</span></span>
- <span data-ttu-id="29b2f-117">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="29b2f-117">Bookable Resource</span></span>
- <span data-ttu-id="29b2f-118">Linha de Estimativa</span><span class="sxs-lookup"><span data-stu-id="29b2f-118">Estimate Line</span></span>
- <span data-ttu-id="29b2f-119">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="29b2f-119">Project Task</span></span>
- <span data-ttu-id="29b2f-120">Detalhe da Linha da Fatura</span><span class="sxs-lookup"><span data-stu-id="29b2f-120">Invoice Line Detail</span></span>
- <span data-ttu-id="29b2f-121">Linha do Diário</span><span class="sxs-lookup"><span data-stu-id="29b2f-121">Journal Line</span></span>
- <span data-ttu-id="29b2f-122">Detalhe da Linha de Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="29b2f-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="29b2f-123">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="29b2f-123">Project Team Member</span></span>
- <span data-ttu-id="29b2f-124">Detalhes da Linha de Cotação</span><span class="sxs-lookup"><span data-stu-id="29b2f-124">Quote Line Detail</span></span>
- <span data-ttu-id="29b2f-125">Markup de Preço da Função</span><span class="sxs-lookup"><span data-stu-id="29b2f-125">Role Price Markup</span></span>
- <span data-ttu-id="29b2f-126">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="29b2f-126">Role Price</span></span> 
- <span data-ttu-id="29b2f-127">Entrada de Horas</span><span class="sxs-lookup"><span data-stu-id="29b2f-127">Time Entry</span></span> 

> ![Adicionar entidades existentes à solução de dimensões de preço](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="29b2f-130">Certifique-se de incluir todos os formulários e exibições para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="29b2f-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="29b2f-131">Quando solicitado a incluir entidades dependentes para as entidades selecionadas, selecione **Não**.</span><span class="sxs-lookup"><span data-stu-id="29b2f-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Não inclua todos os componentes selecionados](media/Do-not-include-required.png)


