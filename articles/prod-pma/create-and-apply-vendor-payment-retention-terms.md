---
title: Criar e aplicar termos de retenção de pagamento de fornecedor
description: Este tópico fornece informações sobre como configurar e manter os termos de retenção para pagamentos de fornecedores.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071565"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="9dd71-103">Criar e aplicar termos de retenção de pagamento de fornecedor</span><span class="sxs-lookup"><span data-stu-id="9dd71-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="9dd71-104">Configurar os termos de retenção de pagamento do fornecedor para um projeto é útil quando sua organização deseja reter parte dos pagamentos feitos a um fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9dd71-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="9dd71-105">Por exemplo, quando você deseja reter o pagamento a um fornecedor até que os produtos entregues atendam às suas expectativas.</span><span class="sxs-lookup"><span data-stu-id="9dd71-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="9dd71-106">Os termos de retenção de pagamento do fornecedor podem ser especificados quando você negocia um contrato com o fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9dd71-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="9dd71-107">Criar termos de retenção de pagamento de fornecedor</span><span class="sxs-lookup"><span data-stu-id="9dd71-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="9dd71-108">Você pode inserir a porcentagem do pagamento do fornecedor para retenção e a porcentagem dos valores retidos anteriormente a serem liberados.</span><span class="sxs-lookup"><span data-stu-id="9dd71-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="9dd71-109">Os valores são retidos automaticamente nas faturas do fornecedor até que o contrato atinja o estado de conclusão especificado.</span><span class="sxs-lookup"><span data-stu-id="9dd71-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="9dd71-110">Depois de definir os termos de retenção, você poderá aplicá-los a qualquer projeto desse fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9dd71-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="9dd71-111">Use as etapas a seguir para configurar e manter os termos de retenção para pagamentos de fornecedores.</span><span class="sxs-lookup"><span data-stu-id="9dd71-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="9dd71-112">Vá para **Gerenciamento e contabilidade de projeto** > **Retenção** > **Termos de retenção de pagamento de fornecedor**.</span><span class="sxs-lookup"><span data-stu-id="9dd71-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="9dd71-113">Selecione **Novo** para adicionar um novo termo de retenção de fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9dd71-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="9dd71-114">O valor de **ID da Regra** para o novo termo é inserido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9dd71-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="9dd71-115">Insira uma breve descrição no campo **Descrição** e, na Guia Rápida **Termos** , selecione **Adicionar linha** para inserir valores de termo para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9dd71-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="9dd71-116">**Porcentagem de unidades entregues** : insira uma porcentagem de conclusão para o termo.</span><span class="sxs-lookup"><span data-stu-id="9dd71-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="9dd71-117">Os valores serão retidos automaticamente nas faturas do fornecedor até que o estágio do projeto de conclusão seja igual à porcentagem especificada.</span><span class="sxs-lookup"><span data-stu-id="9dd71-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="9dd71-118">Por exemplo, se você inserir 50,00, os valores serão retidos até que o projeto esteja 50% concluído.</span><span class="sxs-lookup"><span data-stu-id="9dd71-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="9dd71-119">**Porcentagem a reter** : insira uma porcentagem do valor da fatura do fornecedor a ser retida.</span><span class="sxs-lookup"><span data-stu-id="9dd71-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="9dd71-120">Por exemplo, se você inserir 10,00, então 10% do valor em uma fatura do fornecedor serão retidos até que o projeto alcance a porcentagem de conclusão, conforme definido no campo **Porcentagem de unidades entregues**.</span><span class="sxs-lookup"><span data-stu-id="9dd71-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="9dd71-121">**Porcentagem para liberação** : selecione **Adicionar linha** para inserir uma porcentagem de quaisquer valores anteriormente retidos a serem liberados para o nível selecionado de conclusão do projeto.</span><span class="sxs-lookup"><span data-stu-id="9dd71-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="9dd71-122">Se você tiver mais de um marco para diferentes níveis de conclusão do projeto, insira uma linha de prazo de retenção de fornecedor separada para cada regra de retenção.</span><span class="sxs-lookup"><span data-stu-id="9dd71-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="9dd71-123">Cada linha pode especificar uma porcentagem de retenção diferente e uma porcentagem de liberação diferente para cada nível designado de conclusão do projeto.</span><span class="sxs-lookup"><span data-stu-id="9dd71-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="9dd71-124">Depois de criar os termos de retenção de fornecedor para um fornecedor, você poderá aplicar os termos a um projeto.</span><span class="sxs-lookup"><span data-stu-id="9dd71-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="9dd71-125">Aplicar termos de retenção de fornecedor a um projeto</span><span class="sxs-lookup"><span data-stu-id="9dd71-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="9dd71-126">Vá para **Gerenciamento e contabilidade de projeto** > **Projetos** > **Todos os projetos** e abra um projeto na página de listagem de projetos.</span><span class="sxs-lookup"><span data-stu-id="9dd71-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="9dd71-127">Na FastTab **Contratos de fornecedores** , selecione **Adicionar linha**.</span><span class="sxs-lookup"><span data-stu-id="9dd71-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="9dd71-128">No campo **Código de conta** , selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="9dd71-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="9dd71-129">**Tabela** : os termos de retenção de fornecedor se aplicam a um único fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9dd71-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="9dd71-130">**Grupo** : os termos de retenção de fornecedor se aplicam a todos os fornecedores em um grupo de fornecedores.</span><span class="sxs-lookup"><span data-stu-id="9dd71-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="9dd71-131">**Todos** : os termos de retenção de fornecedor se aplicam a todos os fornecedores.</span><span class="sxs-lookup"><span data-stu-id="9dd71-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="9dd71-132">No campo **Fornecedor/Grupo de fornecedores** , selecione o fornecedor ou grupo de fornecedores ao qual os termos de retenção do fornecedor se aplicam.</span><span class="sxs-lookup"><span data-stu-id="9dd71-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="9dd71-133">Se você tiver selecionado **Todos** na etapa anterior, esse campo não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="9dd71-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="9dd71-134">No campo **Termos de retenção do fornecedor** , selecione os termos de retenção que você criou no procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="9dd71-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="9dd71-135">Se o projeto também tiver termos de pagamento quando pago (PWP) configurados para o fornecedor, insira a porcentagem limite para o projeto no campo **Porcentagem de limite PWP**.</span><span class="sxs-lookup"><span data-stu-id="9dd71-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="9dd71-136">Os termos de retenção do fornecedor também são exibidos nas ordens de compra que você cria para o fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9dd71-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
