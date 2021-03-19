---
title: Configurar gerenciamento de despesas
description: Este artigo descreve as considerações e as decisões que precisam ser tomadas durante o processo de planejamento antes de configurar o Gerenciamento de despesas no Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271339"
---
# <a name="configure-expense-management"></a><span data-ttu-id="ada03-103">Configurar gerenciamento de despesas</span><span class="sxs-lookup"><span data-stu-id="ada03-103">Configure expense management</span></span>

<span data-ttu-id="ada03-104">Este tópico descreve as considerações e as decisões que precisam ser tomadas durante o processo de planejamento antes de configurar o Gerenciamento de despesas.</span><span class="sxs-lookup"><span data-stu-id="ada03-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="ada03-105">No Gerenciamento de despesas é possível armazenar informações sobre formas de pagamento, requisições de viagem, relatórios de despesas, políticas, entre outros.</span><span class="sxs-lookup"><span data-stu-id="ada03-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="ada03-106">Como muitas decisões tomadas ao planejar a configuração do Gerenciamento de despesas são baseadas na hierarquia e na estrutura financeira da organização, você deve consultar os documentos de planejamento dessas áreas.</span><span class="sxs-lookup"><span data-stu-id="ada03-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="ada03-107">Despesas intercompanhia</span><span class="sxs-lookup"><span data-stu-id="ada03-107">Intercompany expenses</span></span>

<span data-ttu-id="ada03-108">Ao habilitar as despesas intercompanhia, você permite que as entidades legais e os funcionários incorram em despesas em nome de outra entidade legal e recebam o pagamento da entidade legal empregadora em sua organização.</span><span class="sxs-lookup"><span data-stu-id="ada03-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="ada03-109">Por exemplo, se um funcionário na entidade legal A conclui um projeto para a entidade legal B e o projeto incorre em despesas relacionadas a viagens.</span><span class="sxs-lookup"><span data-stu-id="ada03-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="ada03-110">Se as despesas intercompanhia estiverem habilitadas, o funcionário poderá arquivar um relatório de despesas que lançará a despesa para a entidade legal B, e a despesa deverá ser paga pela entidade legal A. Se a sua organização não tiver várias entidades legais, não será necessário habilitar as despesas intercompanhia.</span><span class="sxs-lookup"><span data-stu-id="ada03-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="ada03-111">**Decisão:** Deseja habilitar despesas intercompanhia?</span><span class="sxs-lookup"><span data-stu-id="ada03-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="ada03-112">Gerenciamento financeiro</span><span class="sxs-lookup"><span data-stu-id="ada03-112">Financial management</span></span>

<span data-ttu-id="ada03-113">O Gerenciamento de despesas é totalmente integrado ao gerenciamento financeiro da organização.</span><span class="sxs-lookup"><span data-stu-id="ada03-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="ada03-114">Muitas de suas configurações do Gerenciamento de despesas serão baseadas nas decisões tomadas em relação às finanças da sua organização.</span><span class="sxs-lookup"><span data-stu-id="ada03-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="ada03-115">As seguintes seções descrevem as diversas áreas que requerem planejamento e decisões, com base nas decisões financeiras da organização e orientações de sua equipe de liderança.</span><span class="sxs-lookup"><span data-stu-id="ada03-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="ada03-116">Diárias</span><span class="sxs-lookup"><span data-stu-id="ada03-116">Per diems</span></span>

<span data-ttu-id="ada03-117">É necessário definir as diárias de funcionários fornecidas pela sua organização.</span><span class="sxs-lookup"><span data-stu-id="ada03-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="ada03-118">Como as diárias são geralmente usadas para cobrir despesas como refeições, hospedagens e outras despesas incidentais, é possível criar regras para as diárias oferecidas pela organização.</span><span class="sxs-lookup"><span data-stu-id="ada03-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="ada03-119">as taxas de diária podem ser baseadas na época do ano, no local da viagem ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="ada03-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="ada03-120">Ao definir uma regra de diária, você pode especificar que uma porcentagem da taxa da diária será retida se um trabalhador receber refeições ou serviços gratuitos.</span><span class="sxs-lookup"><span data-stu-id="ada03-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="ada03-121">Você também pode definir camadas de taxas de diária para estabelecer o número mínimo e máximo de horas que a taxa da diária pode ser aplicada à viagem de um trabalhador.</span><span class="sxs-lookup"><span data-stu-id="ada03-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="ada03-122">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="ada03-122">**Decisions:**</span></span>

- <span data-ttu-id="ada03-123">Regras padrão de diária para o primeiro e o último dia:</span><span class="sxs-lookup"><span data-stu-id="ada03-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="ada03-124">Qual é o número mínimo de horas que um funcionário pode declarar em um dia e ainda receber uma diária?</span><span class="sxs-lookup"><span data-stu-id="ada03-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="ada03-125">Há redução no valor oferecido para refeições no primeiro e no último dia?</span><span class="sxs-lookup"><span data-stu-id="ada03-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="ada03-126">Se houver uma redução, qual será a porcentagem?</span><span class="sxs-lookup"><span data-stu-id="ada03-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="ada03-127">Há redução no valor oferecido para hospedagem no primeiro e no último dia?</span><span class="sxs-lookup"><span data-stu-id="ada03-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="ada03-128">Se houver uma redução, qual será a porcentagem?</span><span class="sxs-lookup"><span data-stu-id="ada03-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="ada03-129">Há redução no valor oferecido para outras despesas incorridas no primeiro e no último dia?</span><span class="sxs-lookup"><span data-stu-id="ada03-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="ada03-130">Se houver uma redução, qual será a porcentagem?</span><span class="sxs-lookup"><span data-stu-id="ada03-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="ada03-131">Regras padrão de diária:</span><span class="sxs-lookup"><span data-stu-id="ada03-131">Default per diem rules:</span></span>

    - <span data-ttu-id="ada03-132">Existe uma redução percentual na diária por refeição se, por exemplo, a refeição for gratuita?</span><span class="sxs-lookup"><span data-stu-id="ada03-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="ada03-133">Se houver uma redução, qual será a porcentagem para cada refeição?</span><span class="sxs-lookup"><span data-stu-id="ada03-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="ada03-134">A redução da refeição é calculada por dia, por viagem ou pelo número de refeições por dia?</span><span class="sxs-lookup"><span data-stu-id="ada03-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="ada03-135">Os valores de diárias devem ser arredondados da maneira regular ou para cima?</span><span class="sxs-lookup"><span data-stu-id="ada03-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="ada03-136">As diárias são calculadas em um período de 24 horas ou em um dia do calendário?</span><span class="sxs-lookup"><span data-stu-id="ada03-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="ada03-137">Regras de diária baseadas no local:</span><span class="sxs-lookup"><span data-stu-id="ada03-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="ada03-138">As taxas de diárias variam de acordo com o local?</span><span class="sxs-lookup"><span data-stu-id="ada03-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="ada03-139">Quais locais estão incluídos?</span><span class="sxs-lookup"><span data-stu-id="ada03-139">What locations are included?</span></span>
    - <span data-ttu-id="ada03-140">Se as taxas de diárias variam de acordo com o local, para cada local, qual porcentagem é fornecida para os seguintes tipos de despesas:</span><span class="sxs-lookup"><span data-stu-id="ada03-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="ada03-141">Refeições</span><span class="sxs-lookup"><span data-stu-id="ada03-141">Meals</span></span>
        - <span data-ttu-id="ada03-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="ada03-142">Hotel</span></span>
        - <span data-ttu-id="ada03-143">Outras despesas</span><span class="sxs-lookup"><span data-stu-id="ada03-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="ada03-144">Diários e contas de Gerenciamento de despesas</span><span class="sxs-lookup"><span data-stu-id="ada03-144">Expense management journals and accounts</span></span>

<span data-ttu-id="ada03-145">O Gerenciamento de despesas requer o uso de vários diários e contas.</span><span class="sxs-lookup"><span data-stu-id="ada03-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="ada03-146">É necessário decidir, por exemplo, se a mesma conta é usada para adiantamentos de dinheiro e contestações de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="ada03-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="ada03-147">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="ada03-147">**Decisions:**</span></span>

- <span data-ttu-id="ada03-148">Em qual diário-razão os relatórios de despesas aprovados são lançados?</span><span class="sxs-lookup"><span data-stu-id="ada03-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="ada03-149">Qual conta é usada para adiantamentos de dinheiro?</span><span class="sxs-lookup"><span data-stu-id="ada03-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="ada03-150">Os adiantamentos de dinheiro devem ser lançados imediatamente?</span><span class="sxs-lookup"><span data-stu-id="ada03-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="ada03-151">Formas de pagamento</span><span class="sxs-lookup"><span data-stu-id="ada03-151">Payment methods</span></span>

<span data-ttu-id="ada03-152">Ao permitir que os funcionários incorram em despesas em nome de sua empresa, é necessário definir as formas de pagamento que os funcionários podem usar.</span><span class="sxs-lookup"><span data-stu-id="ada03-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="ada03-153">Por exemplo, você pode permitir que os funcionários usem dinheiro ou um cartão de crédito corporativo.</span><span class="sxs-lookup"><span data-stu-id="ada03-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="ada03-154">Você também pode permitir que os funcionários usem cartões de crédito pessoais e depois reembolsá-los.</span><span class="sxs-lookup"><span data-stu-id="ada03-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="ada03-155">É necessário tomar as seguintes decisões para cada forma de pagamento permitida.</span><span class="sxs-lookup"><span data-stu-id="ada03-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="ada03-156">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="ada03-156">**Decisions:**</span></span>

- <span data-ttu-id="ada03-157">Quais formas de pagamento são permitidas?</span><span class="sxs-lookup"><span data-stu-id="ada03-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="ada03-158">Quem é o responsável pelas despesas incorridas na forma de pagamento?</span><span class="sxs-lookup"><span data-stu-id="ada03-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="ada03-159">Há um tipo de contrapartida?</span><span class="sxs-lookup"><span data-stu-id="ada03-159">Is there an offset account type?</span></span> <span data-ttu-id="ada03-160">Caso haja um tipo de contrapartida, qual será?</span><span class="sxs-lookup"><span data-stu-id="ada03-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="ada03-161">Caso haja um tipo de contrapartida, qual será a conta?</span><span class="sxs-lookup"><span data-stu-id="ada03-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="ada03-162">Se a forma de pagamento for um cartão de crédito, ela deverá ser usada somente com transações importadas?</span><span class="sxs-lookup"><span data-stu-id="ada03-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="ada03-163">Categorias de despesas e categorias compartilhadas</span><span class="sxs-lookup"><span data-stu-id="ada03-163">Expense categories and shared categories</span></span>

<span data-ttu-id="ada03-164">Quando os funcionários criam um relatório de despesas, cada despesa que eles registram deve ser associada a uma categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="ada03-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="ada03-165">As categorias de despesas são derivadas de categorias compartilhadas que podem ser compartilhadas entre as entidades legais em sua organização.</span><span class="sxs-lookup"><span data-stu-id="ada03-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="ada03-166">Essas categorias podem ser compartilhadas no Gerenciamento e contabilidade de projeto, dependendo da forma como a organização está definida.</span><span class="sxs-lookup"><span data-stu-id="ada03-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="ada03-167">Com base na definição da sua organização e orientação da equipe de implementação, determine se as categorias que são usadas no Gerenciamento de despesas serão usadas apenas no Gerenciamento de despesas ou se deverão ser compartilhadas entre o Gerenciamento e contabilidade de projeto e o Gerenciamento de despesas.</span><span class="sxs-lookup"><span data-stu-id="ada03-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="ada03-168">Observe que essas categorias podem ser compartilhadas entre Projeto e Despesa ou Projeto e Produção, mas não entre Despesa e Produção.</span><span class="sxs-lookup"><span data-stu-id="ada03-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="ada03-169">É necessário tomar as seguintes decisões para cada categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="ada03-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="ada03-170">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="ada03-170">**Decisions:**</span></span>

- <span data-ttu-id="ada03-171">Qual é a categoria da despesa?</span><span class="sxs-lookup"><span data-stu-id="ada03-171">What is the expense category?</span></span> <span data-ttu-id="ada03-172">Os exemplos incluem categorias para voos, hotel ou milhagem.</span><span class="sxs-lookup"><span data-stu-id="ada03-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="ada03-173">A categoria de despesas também pode ser usada no Gerenciamento e contabilidade de projeto?</span><span class="sxs-lookup"><span data-stu-id="ada03-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="ada03-174">Qual é o tipo de despesa?</span><span class="sxs-lookup"><span data-stu-id="ada03-174">What is the expense type?</span></span>
- <span data-ttu-id="ada03-175">Qual é a forma de pagamento padrão para a categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="ada03-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="ada03-176">As despesas na categoria de despesas devem ser discriminadas?</span><span class="sxs-lookup"><span data-stu-id="ada03-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="ada03-177">Qual é a conta principal padrão para a categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="ada03-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="ada03-178">Qual é o grupo de impostos do item padrão para a categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="ada03-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="ada03-179">São permitidas formas de pagamento adicionais para a categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="ada03-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="ada03-180">Se forem permitidas formas de pagamento adicionais, quais serão elas?</span><span class="sxs-lookup"><span data-stu-id="ada03-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="ada03-181">Existem subcategorias nesta categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="ada03-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="ada03-182">Se houver subcategorias, você também precisará tomar as seguintes decisões:</span><span class="sxs-lookup"><span data-stu-id="ada03-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="ada03-183">Alguma das subcategorias foi excluída da recuperação de impostos?</span><span class="sxs-lookup"><span data-stu-id="ada03-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="ada03-184">Qual é o grupo de impostos do item das subcategorias?</span><span class="sxs-lookup"><span data-stu-id="ada03-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="ada03-185">Se a categoria de despesa também for usada no Gerenciamento e contabilidade de projeto, responda às perguntas restantes.</span><span class="sxs-lookup"><span data-stu-id="ada03-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="ada03-186">Caso contrário, vá para a próxima seção.</span><span class="sxs-lookup"><span data-stu-id="ada03-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="ada03-187">Quais contas de custo serão usadas para as despesas a seguir?</span><span class="sxs-lookup"><span data-stu-id="ada03-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="ada03-188">Custo</span><span class="sxs-lookup"><span data-stu-id="ada03-188">Cost</span></span>
    - <span data-ttu-id="ada03-189">Alocação de folha de pagamento</span><span class="sxs-lookup"><span data-stu-id="ada03-189">Payroll allocation</span></span>
    - <span data-ttu-id="ada03-190">WIP – Valor de custo</span><span class="sxs-lookup"><span data-stu-id="ada03-190">WIP-cost value</span></span>
    - <span data-ttu-id="ada03-191">Custo – Item</span><span class="sxs-lookup"><span data-stu-id="ada03-191">Cost-item</span></span>
    - <span data-ttu-id="ada03-192">WIP – Valor de custo – Item</span><span class="sxs-lookup"><span data-stu-id="ada03-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="ada03-193">Perda acumulada</span><span class="sxs-lookup"><span data-stu-id="ada03-193">Accrued loss</span></span>
    - <span data-ttu-id="ada03-194">WIP – Perda acumulada</span><span class="sxs-lookup"><span data-stu-id="ada03-194">WIP-accrued loss</span></span>

- <span data-ttu-id="ada03-195">Quais contas de receita serão usadas para os itens a seguir?</span><span class="sxs-lookup"><span data-stu-id="ada03-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="ada03-196">Receita faturada</span><span class="sxs-lookup"><span data-stu-id="ada03-196">Invoiced revenue</span></span>
    - <span data-ttu-id="ada03-197">Receita acumulada - Valor de venda</span><span class="sxs-lookup"><span data-stu-id="ada03-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="ada03-198">WIP – Valor de venda</span><span class="sxs-lookup"><span data-stu-id="ada03-198">WIP-sales value</span></span>
    - <span data-ttu-id="ada03-199">Receita acumulada – Produção</span><span class="sxs-lookup"><span data-stu-id="ada03-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="ada03-200">WIP – Produção</span><span class="sxs-lookup"><span data-stu-id="ada03-200">WIP-production</span></span>
    - <span data-ttu-id="ada03-201">Receita acumulada – Lucro</span><span class="sxs-lookup"><span data-stu-id="ada03-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="ada03-202">WIP – Lucro</span><span class="sxs-lookup"><span data-stu-id="ada03-202">WIP-profit</span></span>
    - <span data-ttu-id="ada03-203">Receita acumulada – Subscrição</span><span class="sxs-lookup"><span data-stu-id="ada03-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="ada03-204">WIP – Subscrição</span><span class="sxs-lookup"><span data-stu-id="ada03-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="ada03-205">Impostos</span><span class="sxs-lookup"><span data-stu-id="ada03-205">Taxes</span></span>

<span data-ttu-id="ada03-206">Para impostos relacionados às despesas, é necessário determinar o que está incluído ou habilitado nos relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="ada03-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="ada03-207">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="ada03-207">**Decisions:**</span></span>

- <span data-ttu-id="ada03-208">O imposto sobre vendas está incluído nos valores das despesas?</span><span class="sxs-lookup"><span data-stu-id="ada03-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="ada03-209">A restituição de imposto deve ser habilitada nas despesas?</span><span class="sxs-lookup"><span data-stu-id="ada03-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="ada03-210">Quando estiver planejando a contabilidade, se decidiu aplicar regras de imposto sobre vendas e sobre o uso dos EUA, não será possível habilitar a restituição de imposto nas despesas.</span><span class="sxs-lookup"><span data-stu-id="ada03-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="ada03-211">(Para aplicar regras de imposto sobre vendas e sobre o uso dos EUA, defina a opção **Aplicar regras tributação do imposto sobre vendas** como **Sim**.)</span><span class="sxs-lookup"><span data-stu-id="ada03-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="ada03-212">Políticas</span><span class="sxs-lookup"><span data-stu-id="ada03-212">Policies</span></span>

<span data-ttu-id="ada03-213">Ao criar políticas de relatório de despesas, você pode ajudar a organização a economizar tempo e dinheiro quando os funcionários incorrerem em despesas em nome da empresa.</span><span class="sxs-lookup"><span data-stu-id="ada03-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="ada03-214">As políticas ajudam a garantir que os funcionários permaneçam dentro do orçamento, forneçam todas as informações necessárias e usem o dinheiro somente quando precisarem.</span><span class="sxs-lookup"><span data-stu-id="ada03-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="ada03-215">É necessário tomar as seguintes decisões para cada política de relatório de despesas e cada política de aprovação de relatório de despesas criada.</span><span class="sxs-lookup"><span data-stu-id="ada03-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="ada03-216">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="ada03-216">**Decisions:**</span></span>

- <span data-ttu-id="ada03-217">Qual é o nome da política?</span><span class="sxs-lookup"><span data-stu-id="ada03-217">What is the name of the policy?</span></span>
- <span data-ttu-id="ada03-218">Para que serve a política de despesas?</span><span class="sxs-lookup"><span data-stu-id="ada03-218">What is the expense policy for?</span></span>
- <span data-ttu-id="ada03-219">Se você decidiu habilitar as despesas intercompanhia, a quais empresas em sua organização essa política se aplica?</span><span class="sxs-lookup"><span data-stu-id="ada03-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="ada03-220">Quando a política entrará em vigor?</span><span class="sxs-lookup"><span data-stu-id="ada03-220">When does the policy become effective?</span></span>
- <span data-ttu-id="ada03-221">Quando a política expirará?</span><span class="sxs-lookup"><span data-stu-id="ada03-221">When does the policy expire?</span></span>
- <span data-ttu-id="ada03-222">Qual é a regra da política?</span><span class="sxs-lookup"><span data-stu-id="ada03-222">What is the policy rule?</span></span>
- <span data-ttu-id="ada03-223">Qual é o resultado da regra da política?</span><span class="sxs-lookup"><span data-stu-id="ada03-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]