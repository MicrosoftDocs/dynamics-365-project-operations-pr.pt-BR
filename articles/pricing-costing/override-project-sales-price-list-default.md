---
title: Substituir listas de preços de vendas do projeto
description: Este tópico fornece informações sobre a criação de listas de preços de venda personalizadas.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275524"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="fbff3-103">Substituir listas de preços de vendas do projeto</span><span class="sxs-lookup"><span data-stu-id="fbff3-103">Override project sales price lists</span></span>

<span data-ttu-id="fbff3-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="fbff3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="fbff3-105">Listas de preços de projetos específicas do cliente</span><span class="sxs-lookup"><span data-stu-id="fbff3-105">Customer-specific project price lists</span></span>

<span data-ttu-id="fbff3-106">Os contratos de preços específicos do cliente podem ser configurados como listas de preços do projeto em um registro da conta no Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fbff3-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="fbff3-107">Para configurar uma lista de preços de projeto específica do cliente, na área **Vendas**, navegue até o registro da conta.</span><span class="sxs-lookup"><span data-stu-id="fbff3-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="fbff3-108">Abra a página de lista **Contas**.</span><span class="sxs-lookup"><span data-stu-id="fbff3-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="fbff3-109">Localize e clique duas vezes em um registro de cliente para abrir a página de detalhes da **Conta**.</span><span class="sxs-lookup"><span data-stu-id="fbff3-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="fbff3-110">Na guia **Listas de Preços do projeto**, selecione **+ Nova Lista de Preços do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="fbff3-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="fbff3-111">Na página **Nova Lista de Preços do Projeto**, selecione uma lista de preços da lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="fbff3-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="fbff3-112">Apenas listas de preços que têm o contexto definido como **Vendas** e cuja moeda corresponda à moeda da conta estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="fbff3-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="fbff3-113">Nomeie a associação e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="fbff3-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="fbff3-114">Uma lista de preços de projetos específicas do cliente será criada.</span><span class="sxs-lookup"><span data-stu-id="fbff3-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="fbff3-115">Esta lista de preços será usada para definir preços de projeto padrão em cotações de projeto ou contratos criados para este cliente, onde a data de criação da cotação ou do contrato do projeto está dentro da data efetiva da lista de preços.</span><span class="sxs-lookup"><span data-stu-id="fbff3-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="fbff3-116">Preços personalizados nas cotações do projeto</span><span class="sxs-lookup"><span data-stu-id="fbff3-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="fbff3-117">Nas cotações do projeto, você pode ter o preço do projeto que começa com uma lista de preços padrão do cliente ou dos parâmetros do projeto.</span><span class="sxs-lookup"><span data-stu-id="fbff3-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="fbff3-118">Quando você precisar de preços personalizados para o trabalho relacionado ao projeto em uma cotação específica, poderá obtê-los na entidade associada às listas de preços do projeto.</span><span class="sxs-lookup"><span data-stu-id="fbff3-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="fbff3-119">Conclua as etapas a seguir para configurar o preço de projeto específico da cotação.</span><span class="sxs-lookup"><span data-stu-id="fbff3-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="fbff3-120">Abra a cotação do projeto e selecione a guia **Listas de Preços do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="fbff3-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="fbff3-121">Na subgrade, selecione **Criar precificação personalizada**.</span><span class="sxs-lookup"><span data-stu-id="fbff3-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="fbff3-122">Todas as listas de preços do projeto anexadas à cotação são copiadas para novas listas de preços.</span><span class="sxs-lookup"><span data-stu-id="fbff3-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="fbff3-123">Os nomes das novas listas de preços refletem o nome da cotação com um carimbo de data e hora para quando essas listas de preços foram criadas.</span><span class="sxs-lookup"><span data-stu-id="fbff3-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="fbff3-124">Você pode usar cada uma dessas listas de preços e fazer atualizações nos preços de mão de obra (preço da função) e despesas (preço da categoria).</span><span class="sxs-lookup"><span data-stu-id="fbff3-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="fbff3-125">Esses preços serão aplicáveis apenas a esta cotação de projeto.</span><span class="sxs-lookup"><span data-stu-id="fbff3-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="fbff3-126">Listas de preços em um contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="fbff3-126">Price lists on a project contract</span></span>

<span data-ttu-id="fbff3-127">Em um contrato do projeto, o preço do projeto sempre é padronizado como uma lista de preços personalizada com o nome do contrato e o carimbo de data/hora de criação anexado ao nome.</span><span class="sxs-lookup"><span data-stu-id="fbff3-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="fbff3-128">Isso ocorre se o contrato foi criado quando a cotação foi ganha ou se o contrato foi criado do zero.</span><span class="sxs-lookup"><span data-stu-id="fbff3-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="fbff3-129">Se necessário, você pode remover essa associação à lista de preços personalizada e associar uma lista de preços padrão ao contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="fbff3-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="fbff3-130">Quando você associa uma lista de preços padrão às listas de preços do projeto na cotação ou contrato, quaisquer alterações feitas nos preços na lista de preços afetarão todas as cotações e contratos que usam a lista de preços.</span><span class="sxs-lookup"><span data-stu-id="fbff3-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]