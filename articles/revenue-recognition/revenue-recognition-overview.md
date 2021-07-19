---
title: Visão geral do reconhecimento de receita
description: Este tópico fornece informações sobre o reconhecimento de receita no Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368012"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="7baba-103">Visão geral do reconhecimento de receita</span><span class="sxs-lookup"><span data-stu-id="7baba-103">Revenue recognition overview</span></span>

<span data-ttu-id="7baba-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="7baba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7baba-105">No Dynamics 365 Project Operations, os princípios de reconhecimento de receita variam com base no método de faturamento selecionado para um projeto ou parte do projeto.</span><span class="sxs-lookup"><span data-stu-id="7baba-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="7baba-106">Este tópico fornece informações sobre o reconhecimento de receita no Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7baba-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="7baba-107">Transações contabilizadas usando o método de cobrança de hora e material</span><span class="sxs-lookup"><span data-stu-id="7baba-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="7baba-108">O custo e o reconhecimento da receita estão conectados.</span><span class="sxs-lookup"><span data-stu-id="7baba-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="7baba-109">O custo das transações e as vendas não cobradas são lançados usando o [Diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="7baba-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="7baba-110">O custo do projeto e o perfil de receita determinam se as transações de vendas não cobradas são lançadas na contabilidade.</span><span class="sxs-lookup"><span data-stu-id="7baba-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="7baba-111">Se a opção **Acumular receita** estiver selecionada, o sistema usa as contas **Valor de vendas de WIP** e **Valor de vendas da receita acumulada** durante o lançamento.</span><span class="sxs-lookup"><span data-stu-id="7baba-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="7baba-112">Veja a seguir um exemplo deste método.</span><span class="sxs-lookup"><span data-stu-id="7baba-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="7baba-113">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="7baba-113">Transaction type</span></span> | <span data-ttu-id="7baba-114">Débito/crédito</span><span class="sxs-lookup"><span data-stu-id="7baba-114">Debit/Credit</span></span> | <span data-ttu-id="7baba-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7baba-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="7baba-116">Valor de venda de WIP</span><span class="sxs-lookup"><span data-stu-id="7baba-116">WIP Sales value</span></span> | <span data-ttu-id="7baba-117">Débito</span><span class="sxs-lookup"><span data-stu-id="7baba-117">Debit</span></span> | <span data-ttu-id="7baba-118">100</span><span class="sxs-lookup"><span data-stu-id="7baba-118">100</span></span> |
  | <span data-ttu-id="7baba-119">Valor de venda da receita acumulada</span><span class="sxs-lookup"><span data-stu-id="7baba-119">Accrued revenue sales value</span></span> | <span data-ttu-id="7baba-120">Crédito</span><span class="sxs-lookup"><span data-stu-id="7baba-120">Credit</span></span> | <span data-ttu-id="7baba-121">100</span><span class="sxs-lookup"><span data-stu-id="7baba-121">100</span></span> |

- <span data-ttu-id="7baba-122">A receita é reconhecida durante o faturamento.</span><span class="sxs-lookup"><span data-stu-id="7baba-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="7baba-123">O sistema usa a conta **Receita faturada** durante o lançamento.</span><span class="sxs-lookup"><span data-stu-id="7baba-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="7baba-124">Veja a seguir um exemplo deste método.</span><span class="sxs-lookup"><span data-stu-id="7baba-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="7baba-125">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="7baba-125">Transaction type</span></span> | <span data-ttu-id="7baba-126">Débito/crédito</span><span class="sxs-lookup"><span data-stu-id="7baba-126">Debit/Credit</span></span> | <span data-ttu-id="7baba-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7baba-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="7baba-128">Saldo do cliente</span><span class="sxs-lookup"><span data-stu-id="7baba-128">Customer balance</span></span> | <span data-ttu-id="7baba-129">Débito</span><span class="sxs-lookup"><span data-stu-id="7baba-129">Debit</span></span> | <span data-ttu-id="7baba-130">120</span><span class="sxs-lookup"><span data-stu-id="7baba-130">120</span></span> |
  | <span data-ttu-id="7baba-131">Imposto a pagar</span><span class="sxs-lookup"><span data-stu-id="7baba-131">Sales tax payable</span></span> | <span data-ttu-id="7baba-132">Crédito</span><span class="sxs-lookup"><span data-stu-id="7baba-132">Credit</span></span> | <span data-ttu-id="7baba-133">20</span><span class="sxs-lookup"><span data-stu-id="7baba-133">20</span></span> |
  | <span data-ttu-id="7baba-134">Receita Faturada</span><span class="sxs-lookup"><span data-stu-id="7baba-134">Invoiced Revenue</span></span> | <span data-ttu-id="7baba-135">Crédito</span><span class="sxs-lookup"><span data-stu-id="7baba-135">Credit</span></span> | <span data-ttu-id="7baba-136">100</span><span class="sxs-lookup"><span data-stu-id="7baba-136">100</span></span> |

- <span data-ttu-id="7baba-137">Se a receita foi acumulada quando as vendas não cobradas foram lançadas, o sistema reverterá a receita acumulada no faturamento.</span><span class="sxs-lookup"><span data-stu-id="7baba-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="7baba-138">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="7baba-138">Transaction type</span></span> | <span data-ttu-id="7baba-139">Débito/crédito</span><span class="sxs-lookup"><span data-stu-id="7baba-139">Debit/Credit</span></span> | <span data-ttu-id="7baba-140">Valor</span><span class="sxs-lookup"><span data-stu-id="7baba-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="7baba-141">Valor de venda de WIP</span><span class="sxs-lookup"><span data-stu-id="7baba-141">WIP Sales value</span></span> | <span data-ttu-id="7baba-142">Crédito</span><span class="sxs-lookup"><span data-stu-id="7baba-142">Credit</span></span> | <span data-ttu-id="7baba-143">100</span><span class="sxs-lookup"><span data-stu-id="7baba-143">100</span></span> |
  | <span data-ttu-id="7baba-144">Valor de venda da receita acumulada</span><span class="sxs-lookup"><span data-stu-id="7baba-144">Accrued revenue sales value</span></span> | <span data-ttu-id="7baba-145">Débito</span><span class="sxs-lookup"><span data-stu-id="7baba-145">Debit</span></span> | <span data-ttu-id="7baba-146">100</span><span class="sxs-lookup"><span data-stu-id="7baba-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="7baba-147">Transações contabilizadas usando o método de cobrança de preço fixo</span><span class="sxs-lookup"><span data-stu-id="7baba-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="7baba-148">O custo e o reconhecimento da receita são separados.</span><span class="sxs-lookup"><span data-stu-id="7baba-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="7baba-149">O custo das transações é lançado usando o [Diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="7baba-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="7baba-150">As transações de vendas não cobradas não são criadas.</span><span class="sxs-lookup"><span data-stu-id="7baba-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="7baba-151">A receita pode ser reconhecida durante o faturamento se o custo do projeto e o perfil de receita tiver a opção **Princípio usado para cálculos de conclusão do projeto** definida como **Sem WIP**.</span><span class="sxs-lookup"><span data-stu-id="7baba-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="7baba-152">Use este método somente para projetos simples de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="7baba-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="7baba-153">A receita pode ser reconhecida usando estimativas de receita de preço fixo, com os métodos **Contrato concluído** ou **Reconhecimento de receita da porcentagem de conclusão**.</span><span class="sxs-lookup"><span data-stu-id="7baba-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7baba-154">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7baba-154">Additional resources</span></span>
[<span data-ttu-id="7baba-155">Artigo Configurar contabilidade para projetos faturáveis</span><span class="sxs-lookup"><span data-stu-id="7baba-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="7baba-156">Projetos de estimativa de receita de preço fixo</span><span class="sxs-lookup"><span data-stu-id="7baba-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="7baba-157">Gerenciar estimativas de receita</span><span class="sxs-lookup"><span data-stu-id="7baba-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="7baba-158">Custo para concluir os métodos</span><span class="sxs-lookup"><span data-stu-id="7baba-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]