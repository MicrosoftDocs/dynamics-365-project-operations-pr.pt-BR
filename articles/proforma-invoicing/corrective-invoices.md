---
title: Faturas corrigidas
description: Este tópico fornece informações sobre faturas corrigidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287809"
---
# <a name="corrected-invoices"></a><span data-ttu-id="f31cc-103">Faturas corrigidas</span><span class="sxs-lookup"><span data-stu-id="f31cc-103">Corrected invoices</span></span>

<span data-ttu-id="f31cc-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="f31cc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f31cc-105">As faturas confirmadas podem ser editadas.</span><span class="sxs-lookup"><span data-stu-id="f31cc-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="f31cc-106">Quando você edita uma fatura confirmada, um rascunho da fatura corrigida é criado.</span><span class="sxs-lookup"><span data-stu-id="f31cc-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="f31cc-107">Como a suposição é de que você deseja reverter todas as transações e quantidades da fatura original, a fatura corrigida inclui todas as transações da fatura original e todas as quantidades nela são 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f31cc-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="f31cc-108">Quando transações não exigem correção, você pode removê-las do rascunho de fatura corrigida.</span><span class="sxs-lookup"><span data-stu-id="f31cc-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="f31cc-109">Para reverter ou retornar apenas uma quantidade parcial, você pode editar o campo Quantidade nos detalhes da linha.</span><span class="sxs-lookup"><span data-stu-id="f31cc-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="f31cc-110">Se você abrir os detalhes da linha da fatura, será possível ver a quantidade da fatura original.</span><span class="sxs-lookup"><span data-stu-id="f31cc-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="f31cc-111">É possível editar a quantidade da fatura atual para que seja menor ou maior que a quantidade da fatura original.</span><span class="sxs-lookup"><span data-stu-id="f31cc-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="f31cc-112">Quando você confirma uma fatura corretiva, os dados reais de vendas cobradas originais são revertidos e novos dados reais de vendas cobradas são criados.</span><span class="sxs-lookup"><span data-stu-id="f31cc-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="f31cc-113">Se a quantidade foi reduzida, a diferença também fará com que novos dados reais de vendas não cobradas sejam criados.</span><span class="sxs-lookup"><span data-stu-id="f31cc-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="f31cc-114">Por exemplo, se a venda cobrada original for por oito horas e os detalhes da linha da fatura corrigida tiverem uma quantidade reduzida de seis horas, a linha de vendas cobradas original será revertida e dois novos dados efetivos serão criados:</span><span class="sxs-lookup"><span data-stu-id="f31cc-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="f31cc-115">Dados reais de vendas cobradas por seis horas.</span><span class="sxs-lookup"><span data-stu-id="f31cc-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="f31cc-116">Dados reais de vendas não cobradas pelas duas horas restantes.</span><span class="sxs-lookup"><span data-stu-id="f31cc-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="f31cc-117">Essa transação pode ser cobrada posteriormente ou marcada como não passível de cobrança, dependendo das negociações com o cliente.</span><span class="sxs-lookup"><span data-stu-id="f31cc-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]