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
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122374"
---
# <a name="corrected-invoices"></a><span data-ttu-id="fddab-103">Faturas corrigidas</span><span class="sxs-lookup"><span data-stu-id="fddab-103">Corrected invoices</span></span>

<span data-ttu-id="fddab-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="fddab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fddab-105">As faturas confirmadas podem ser editadas.</span><span class="sxs-lookup"><span data-stu-id="fddab-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="fddab-106">Quando você edita uma fatura confirmada, um rascunho da fatura corrigida é criado.</span><span class="sxs-lookup"><span data-stu-id="fddab-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="fddab-107">Como a suposição é de que você deseja reverter todas as transações e quantidades da fatura original, a fatura corrigida inclui todas as transações da fatura original e todas as quantidades nela são 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="fddab-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="fddab-108">Quando transações não exigem correção, você pode removê-las do rascunho de fatura corrigida.</span><span class="sxs-lookup"><span data-stu-id="fddab-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="fddab-109">Para reverter ou retornar apenas uma quantidade parcial, você pode editar o campo Quantidade nos detalhes da linha.</span><span class="sxs-lookup"><span data-stu-id="fddab-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="fddab-110">Se você abrir os detalhes da linha da fatura, será possível ver a quantidade da fatura original.</span><span class="sxs-lookup"><span data-stu-id="fddab-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="fddab-111">É possível editar a quantidade da fatura atual para que seja menor ou maior que a quantidade da fatura original.</span><span class="sxs-lookup"><span data-stu-id="fddab-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="fddab-112">Quando você confirma uma fatura corretiva, os dados reais de vendas cobradas originais são revertidos e novos dados reais de vendas cobradas são criados.</span><span class="sxs-lookup"><span data-stu-id="fddab-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="fddab-113">Se a quantidade foi reduzida, a diferença também fará com que novos dados reais de vendas não cobradas sejam criados.</span><span class="sxs-lookup"><span data-stu-id="fddab-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="fddab-114">Por exemplo, se a venda cobrada original for por oito horas e os detalhes da linha da fatura corrigida tiverem uma quantidade reduzida de seis horas, a linha de vendas cobradas original será revertida e dois novos dados efetivos serão criados:</span><span class="sxs-lookup"><span data-stu-id="fddab-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="fddab-115">Dados reais de vendas cobradas por seis horas.</span><span class="sxs-lookup"><span data-stu-id="fddab-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="fddab-116">Dados reais de vendas não cobradas pelas duas horas restantes.</span><span class="sxs-lookup"><span data-stu-id="fddab-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="fddab-117">Essa transação pode ser cobrada posteriormente ou marcada como não passível de cobrança, dependendo das negociações com o cliente.</span><span class="sxs-lookup"><span data-stu-id="fddab-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
