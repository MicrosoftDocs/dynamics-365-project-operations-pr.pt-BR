---
title: Linhas de oportunidade baseadas em produto - lite
description: Este tópico fornece informações sobre itens de linha de oportunidade baseados em produto no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176302"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="46c11-103">Linhas de oportunidade baseadas em produto - lite</span><span class="sxs-lookup"><span data-stu-id="46c11-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="46c11-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="46c11-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46c11-105">As linhas de oportunidade baseadas em produto são itens de linha na Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="46c11-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="46c11-106">Essas linhas são entregues ao cliente como itens de linha distintos na fatura eventual, sem quaisquer outros serviços de valor agregado.</span><span class="sxs-lookup"><span data-stu-id="46c11-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="46c11-107">O gasto e o consumo associados não são controlados nas tarefas de qualquer projeto relacionado.</span><span class="sxs-lookup"><span data-stu-id="46c11-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="46c11-108">As linhas baseadas em produtos podem ser itens de catálogo ou produtos escritos.</span><span class="sxs-lookup"><span data-stu-id="46c11-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="46c11-109">A maior parte da funcionalidade nas linhas baseadas no produto de uma Oportunidade segue a funcionalidade fornecida pelo aplicativo Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="46c11-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="46c11-110">Para obter mais informações sobre linhas de oportunidade baseadas em produtos, consulte [Adicione produtos a uma oportunidade](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="46c11-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="46c11-111">As linhas de oportunidade baseadas em produto utilizam um conceito que é específico de oportunidades baseadas em projeto, que é o **Orçamento do cliente**.</span><span class="sxs-lookup"><span data-stu-id="46c11-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="46c11-112">Use este campo para controlar o valor que o cliente está disposto a pagar pelo item de linha.</span><span class="sxs-lookup"><span data-stu-id="46c11-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="46c11-113">Se o método de receita do resumo da oportunidade for definido como **Calculado pelo sistema**, os valores do orçamento do cliente nas linhas baseadas em produto e projeto são resumidos para calcular a receita estimada.</span><span class="sxs-lookup"><span data-stu-id="46c11-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
