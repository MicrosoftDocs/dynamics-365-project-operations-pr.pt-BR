---
title: Verificar a lista de pendências de faturamento em projetos e contratos de projetos
description: Esse tópico oferece informações sobre como revisar listas de pendências de horas, despesas e produtos, além de marcá-las como prontas para faturamento.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282769"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="dcaa4-103">Verificar a lista de pendências de faturamento em projetos e contratos de projetos</span><span class="sxs-lookup"><span data-stu-id="dcaa4-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dcaa4-104">Quando uma transação estiver pronta para ter uma fatura criada e processada, a transação deve ser marcada como **Pronta para faturamento**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="dcaa4-105">Esse tópico descreve os tipos de transações que podem ser criadas.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="dcaa4-106">Verificar a lista de pendências de cobrança de hora e material</span><span class="sxs-lookup"><span data-stu-id="dcaa4-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="dcaa4-107">Quando uma entrada de hora e despesa for enviada e aprovada para um projeto, o PSA criará um projeto real.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="dcaa4-108">Se a combinação do projeto e a classe de transação forem mapeadas para uma linha de contrato de um projeto de tempo e materiais, dois valores reais serão criados quando a entrada for aprovada:</span><span class="sxs-lookup"><span data-stu-id="dcaa4-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="dcaa4-109">Custo real</span><span class="sxs-lookup"><span data-stu-id="dcaa4-109">Cost actual</span></span> 
- <span data-ttu-id="dcaa4-110">Valores reais de vendas não cobrados</span><span class="sxs-lookup"><span data-stu-id="dcaa4-110">Unbilled sales actual</span></span>

<span data-ttu-id="dcaa4-111">Os valores de vendas não cobrados representam a lista de pendências de cobranças e o status da cobrança deve ser definido como **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="dcaa4-112">Quando uma fatura de projeto é criada, os valores reais de vendas não cobrados marcados como **Pronto para faturar** são copiados como detalhes das linhas de faturamento.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="dcaa4-113">Para verificar a lista de pendências de cobranças de hora e materiais, vá para **Vendas** \> **Cobrança** \> **Lista de pendências de cobrança de hora e materiais**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="dcaa4-114">Selecione todos os valores reais de vendas não cobrados que estão prontos para serem faturados e, em seguida, selecione **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="dcaa4-115">O status de cobrança desses valores reais é alterado para **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Lista de pendências de cobrança de hora e materiais](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="dcaa4-117">Revisar a lista de pendências de cobrança do produto</span><span class="sxs-lookup"><span data-stu-id="dcaa4-117">Review the product billing backlog</span></span>

<span data-ttu-id="dcaa4-118">No PSA, quando um contrato de projeto tem linhas de contrato baseadas no produto, essas linhas são consideradas para faturamento sempre que uma fatura for criada para o contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="dcaa4-119">Todos os produtos com linhas de contrato marcadas como **Pronto para faturar** são copiados para a fatura do projeto como linhas de faturamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="dcaa4-120">Para analisar a lista de pendências de cobrança dos produtos, vá para **Vendas** \> **Cobrança** \> **Lista de pendências de cobrança do produto**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="dcaa4-121">Selecione todas as linhas de contrato baseadas no produto que estão prontas para serem faturadas e, em seguida, selecione **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="dcaa4-122">O status de cobrança dessas linhas é alterado para **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Lista de pendências de cobrança do produto](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="dcaa4-124">Revisar as etapas de cobrança em contratos de preço fixo</span><span class="sxs-lookup"><span data-stu-id="dcaa4-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="dcaa4-125">Todas as linhas de contrato do projeto com um método de cobrança de preço fixo devem definir as etapas do contrato.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="dcaa4-126">Essas etapas do contrato podem ser faturadas somente se estiverem marcadas como **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="dcaa4-127">Para revisar as etapas de cobrança, vá para **Vendas** \> **Cobrança** \> **Etapas com preço fixo**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="dcaa4-128">Selecione as etapas prontas para faturamento e, em seguida, selecione **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="dcaa4-129">O status de cobrança dessas etapas foi alterado para **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="dcaa4-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Etapas de preço fixo](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]