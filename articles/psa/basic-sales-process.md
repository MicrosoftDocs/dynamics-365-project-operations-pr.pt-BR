---
title: Processos de vendas
description: Este tópico fornece informações sobre os processos de vendas básicos.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f09b30fe6d842faaf896cb97f44b060ec4049213
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071542"
---
# <a name="sales-processes"></a><span data-ttu-id="f285f-103">Processos de vendas</span><span class="sxs-lookup"><span data-stu-id="f285f-103">Sales processes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f285f-104">Os processos de vendas que são usados em uma organização baseada em projeto diferem dos processos de vendas que são usados em uma organização baseada em produto.</span><span class="sxs-lookup"><span data-stu-id="f285f-104">The sales processes that are used in a project-based organization differ from the sales processes that are used in a product-based organization.</span></span> <span data-ttu-id="f285f-105">Essa diferença ocorre porque os ciclos de vendas para organizações baseadas em projeto são mais longos e exigem técnicas de estimativa personalizadas para analisar e criar cotações para cada negociação.</span><span class="sxs-lookup"><span data-stu-id="f285f-105">This difference occurs because the sales cycles for project-based organizations are longer and require customized estimation techniques to analyze and create quotes for each deal.</span></span> <span data-ttu-id="f285f-106">O Dynamics 365 Project Service Automation usa algumas das mesmas funcionalidades que são usadas no processo de vendas do Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f285f-106">Dynamics 365 Project Service Automation uses some of the same functionality that is used in the sales process for Dynamics 365 Sales.</span></span> <span data-ttu-id="f285f-107">Veja alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="f285f-107">Here are some examples:</span></span>

- <span data-ttu-id="f285f-108">A entidade Cliente Potencial é usada par rastrear os processos de vendas.</span><span class="sxs-lookup"><span data-stu-id="f285f-108">A Lead entity is used to track the sales process.</span></span>
- <span data-ttu-id="f285f-109">Os clientes potenciais qualificados são rastreados como oportunidades.</span><span class="sxs-lookup"><span data-stu-id="f285f-109">Qualifying leads are tracked as opportunities.</span></span> <span data-ttu-id="f285f-110">O processo de vendas também pode iniciar com oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f285f-110">The sales process can also start with opportunity.</span></span>
- <span data-ttu-id="f285f-111">Todos os artefatos relacionados para uma oportunidade são acessados.</span><span class="sxs-lookup"><span data-stu-id="f285f-111">All related artifacts for an opportunity are accessed.</span></span> <span data-ttu-id="f285f-112">Esses artefatos incluem a equipe de vendas, participantes, probabilidade, classificação, estágios da venda e processos empresariais.</span><span class="sxs-lookup"><span data-stu-id="f285f-112">These artifacts include the sales team, stakeholders, probability, rating, sales stages, and business processes.</span></span>
- <span data-ttu-id="f285f-113">Várias cotações são criadas para uma oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f285f-113">Multiple quotes are created for an opportunity.</span></span>
- <span data-ttu-id="f285f-114">Uma cotação é marcada como **Fechada como Ganha** para criar um pedido de venda.</span><span class="sxs-lookup"><span data-stu-id="f285f-114">A quote is marked **Closed as Won** to create a sales order.</span></span> <span data-ttu-id="f285f-115">No PSA, o pedido de venda é personalizado e chamado de contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="f285f-115">In PSA, the sales order is customized and is called a project contract.</span></span>

<span data-ttu-id="f285f-116">A seguinte ilustração mostra um processo de vendas típico em uma organização baseada em projeto.</span><span class="sxs-lookup"><span data-stu-id="f285f-116">The following illustration shows a typical sales process in a project-based organization.</span></span>

> ![O processo de vendas em uma organização baseada em projeto](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a><span data-ttu-id="f285f-118">Estimando uma venda</span><span class="sxs-lookup"><span data-stu-id="f285f-118">Estimating a sale</span></span>
<span data-ttu-id="f285f-119">O valor de uma venda pode ser estimado com base em projetos que foram entregues anteriormente e na complexidade dos projetos.</span><span class="sxs-lookup"><span data-stu-id="f285f-119">The value of a sale can be estimated based on projects that have previously been delivered and the complexity of projects.</span></span> <span data-ttu-id="f285f-120">Em projetos que envolvem extensões para projetos anteriores, ou projetos em que a experiência do fornecedor é alta e em que modelos de trabalho reconhecidos são usados, você pode usar um processo de estimativa mais simples.</span><span class="sxs-lookup"><span data-stu-id="f285f-120">For projects that involve extensions to previous projects, or projects where the vendor's expertise is high and well-known work templates are used, you can use a simpler estimation process.</span></span> <span data-ttu-id="f285f-121">Os projetos mais complexos geralmente têm um processo de compra mais longo.</span><span class="sxs-lookup"><span data-stu-id="f285f-121">More complex projects usually have a longer purchase process.</span></span> <span data-ttu-id="f285f-122">Portanto, há mais estágios no processo de estimativa de vendas.</span><span class="sxs-lookup"><span data-stu-id="f285f-122">Therefore, there are more stages in the sales estimation process.</span></span> <span data-ttu-id="f285f-123">No início do processo, a equipe de vendas usa a entrada dos gerentes de conta e SMEs (especialistas no assunto) para iniciar a criação de uma estimativa de alto nível para cada componente distinto de trabalho que é cotado.</span><span class="sxs-lookup"><span data-stu-id="f285f-123">Early in the process, the sales team uses the input of account managers and subject matter experts (SMEs) to start to create a high-level estimate for each distinct component of work that is quoted.</span></span> <span data-ttu-id="f285f-124">Esses componentes de trabalho são representados pelas linhas de cotação.</span><span class="sxs-lookup"><span data-stu-id="f285f-124">These components of work are represented by quote lines.</span></span> 

<span data-ttu-id="f285f-125">Você pode criar uma estimativa de alto nível da cotação.</span><span class="sxs-lookup"><span data-stu-id="f285f-125">You can create a high-level estimate of the quote.</span></span> <span data-ttu-id="f285f-126">Por fim, essa estimativa de alto nível será substituída por uma estimativa mais detalhada que se baseia em um plano de projeto que você cria usando modelos de projeto padronizados.</span><span class="sxs-lookup"><span data-stu-id="f285f-126">Eventually, this high-level estimate will be replaced by a more detailed estimate that is based on a project plan that you create by using the standardized project templates.</span></span> <span data-ttu-id="f285f-127">Esses modelos ajudam você a criar uma agenda e determinar os valores monetários na cotação e seus componentes (linhas de cotação).</span><span class="sxs-lookup"><span data-stu-id="f285f-127">These templates help you build a schedule and determine monetary values on the quote and its components (quote lines).</span></span> 

<span data-ttu-id="f285f-128">É possível criar várias cotações para um projeto e agrupá-las sob um único tipo de entidade de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f285f-128">You can create multiple quotes for a project and group them under a single opportunity entity type.</span></span> <span data-ttu-id="f285f-129">Por fim, uma dessas cotações é marcada como **Fechada como Ganha** e um contrato de projeto ou SOW (declaração de trabalho) é criado.</span><span class="sxs-lookup"><span data-stu-id="f285f-129">Eventually, one of those quotes is marked **Closed as Won** , and a project contract or statement of work (SOW) is created.</span></span> <span data-ttu-id="f285f-130">Um contrato de projeto mantém o valor contratado para cada componente (linha de contrato) que é aceito pelo cliente para entrega.</span><span class="sxs-lookup"><span data-stu-id="f285f-130">A project contract holds the contracted value for each component (contract line) that is accepted by the customer for delivery.</span></span> <span data-ttu-id="f285f-131">Uma SOW geralmente é criada como um documento do Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="f285f-131">An SOW is usually created as a Microsoft Word document.</span></span> <span data-ttu-id="f285f-132">Todas as faturas que são enviadas ao cliente durante o curso da entrega do projeto fazem referência ao contrato de projeto ou à SOW.</span><span class="sxs-lookup"><span data-stu-id="f285f-132">All invoices that are sent to the customer over the course of the project's delivery reference the project contract or SOW.</span></span>

<span data-ttu-id="f285f-133">Também é possível criar cotações alternativas sob um tipo de entidade de oportunidade ou configurar o sistema para que um contrato de projeto seja criado quando uma cotação é ganha.</span><span class="sxs-lookup"><span data-stu-id="f285f-133">You can also create alternate quotes under one opportunity entity type or set up the system so that a project contract is created when a quote is won.</span></span> <span data-ttu-id="f285f-134">Nesse caso, você pode anexar um documento do Word que represente a SOW ao registro do contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="f285f-134">In this case, you can attach a Word document that represents the SOW to the project contract record.</span></span>

![Fechando uma cotação para criar um contrato de projeto](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a><span data-ttu-id="f285f-136">Configurando o processo de vendas</span><span class="sxs-lookup"><span data-stu-id="f285f-136">Configuring the sales process</span></span>
<span data-ttu-id="f285f-137">Você pode usar BPFs (fluxos de processo empresarial) no Microsoft Dynamics 365 para configurar seu processo de vendas.</span><span class="sxs-lookup"><span data-stu-id="f285f-137">You can use business process flows (BPFs) in Microsoft Dynamics 365 to configure your sales process.</span></span> <span data-ttu-id="f285f-138">Os BPFs proporcionam aos seus funcionários de vendas uma interface visual guiada que eles podem usar para avançar as negociações pelas fases que são típicas da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="f285f-138">BPFs give your sales staff a guided visual interface that they can use to move deals forward through the stages that are typical for your company.</span></span>

<span data-ttu-id="f285f-139">Por exemplo, sua empresa pode ter os seis seguintes estágios no processo de vendas:</span><span class="sxs-lookup"><span data-stu-id="f285f-139">For example, your company might have the following six stages in the sales process:</span></span>

1. <span data-ttu-id="f285f-140">Qualificar</span><span class="sxs-lookup"><span data-stu-id="f285f-140">Qualify</span></span>
2. <span data-ttu-id="f285f-141">Estimativa</span><span class="sxs-lookup"><span data-stu-id="f285f-141">Estimate</span></span>
3. <span data-ttu-id="f285f-142">Revisão interna</span><span class="sxs-lookup"><span data-stu-id="f285f-142">Internal review</span></span>
4. <span data-ttu-id="f285f-143">Contrato</span><span class="sxs-lookup"><span data-stu-id="f285f-143">Contract</span></span>
5. <span data-ttu-id="f285f-144">Entrega</span><span class="sxs-lookup"><span data-stu-id="f285f-144">Deliver</span></span>
6. <span data-ttu-id="f285f-145">Fechar</span><span class="sxs-lookup"><span data-stu-id="f285f-145">Close</span></span>

<span data-ttu-id="f285f-146">Esses seis estágios são representados por setas (\>) que você seleciona para expandir em cada tipo de entidade de oportunidade que cria.</span><span class="sxs-lookup"><span data-stu-id="f285f-146">These six stages are represented by chevrons (\>) that you select to expand in each opportunity entity type that you create.</span></span>

![Configuração do processo empresarial no Dynamics 365](media/basic-guide-3.png)
 
<span data-ttu-id="f285f-148">Sua organização pode usar entidades diferentes para representar a mesma negociação conforme evolui.</span><span class="sxs-lookup"><span data-stu-id="f285f-148">Your organization might use different entities to represent the same deal as it evolves.</span></span> <span data-ttu-id="f285f-149">No início do processo de vendas, uma negociação é representada pela entidade Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f285f-149">Early in the sales process, a deal is represented by the Opportunity entity.</span></span> <span data-ttu-id="f285f-150">Conforme o tempo passa e mais detalhes surgem, é possível usar estimativas de alto nível para criar uma ou mais cotações.</span><span class="sxs-lookup"><span data-stu-id="f285f-150">As time passes and more details emerge, you might use high-level estimates to create one or more quotes.</span></span> <span data-ttu-id="f285f-151">Se uma dessas cotações for revisada pelos participantes internos ou do cliente, a entidade Cotação representará a negociação.</span><span class="sxs-lookup"><span data-stu-id="f285f-151">If one of these quotes is reviewed by internal and customer stakeholders, the Quote entity represents the deal.</span></span> <span data-ttu-id="f285f-152">Depois que o cliente aceita a cotação, um contrato de projeto ou SOW representa a negociação.</span><span class="sxs-lookup"><span data-stu-id="f285f-152">After the customer accepts the quote, a project contract or SOW represents the deal.</span></span> <span data-ttu-id="f285f-153">Para dar suporte a esse comportamento, os BPFs são estruturados para que cada estágio no processo seja vinculado a uma tabela de banco de dados diferente.</span><span class="sxs-lookup"><span data-stu-id="f285f-153">To support this behavior, BPFs are structured so that each stage in the process is linked to a different database table.</span></span>

<span data-ttu-id="f285f-154">O estágio **Qualificar** no processo de vendas pode ser rastreado por uma entidade Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f285f-154">The **Qualify** stage in the sales process can be backed by an Opportunity entity.</span></span> <span data-ttu-id="f285f-155">Os estágios **Estimativa** e **Revisão Interna** podem ser apoiados por uma entidade Cotação.</span><span class="sxs-lookup"><span data-stu-id="f285f-155">The **Estimate** and **Internal Review** stages can be backed by a Quote entity.</span></span> <span data-ttu-id="f285f-156">Os estágios **Contrato** , **Entrega** e **Fechamento** podem ser apoiados por uma entidade Contrato de Projeto.</span><span class="sxs-lookup"><span data-stu-id="f285f-156">The **Contract** , **Delivery** , and **Close** stages can be backed by a Project Contract entity.</span></span>

<span data-ttu-id="f285f-157">À medida que as negociações avançam pelos estágios, é solicitada a criação do registro da entidade apropriado para ajudar e guiar você pelo processo.</span><span class="sxs-lookup"><span data-stu-id="f285f-157">As you move deals through the stages, you're prompted to create the appropriate entity record to help and guide you through the process.</span></span> <span data-ttu-id="f285f-158">Os estágios podem ser condicionais.</span><span class="sxs-lookup"><span data-stu-id="f285f-158">The stages can be conditional.</span></span> <span data-ttu-id="f285f-159">Por exemplo, se você exigir uma revisão interna de uma cotação apenas se a cotação usar uma lista de preços personalizada, será possível configurar essa condição no estágio apropriado do processo empresarial.</span><span class="sxs-lookup"><span data-stu-id="f285f-159">For example, if you require an internal review of a quote only if the quote uses a custom price list, you can configure that condition in the appropriate stage of the business process.</span></span> <span data-ttu-id="f285f-160">O estágio **Revisão Interna** será mostrada somente para cotações que usam uma lista de preços personalizada.</span><span class="sxs-lookup"><span data-stu-id="f285f-160">The **Internal Review** stage is then shown only for quotes that use a custom price list.</span></span> <span data-ttu-id="f285f-161">Para todas as outras negociações e cotações, o estágio **Estimativa** é seguido pelo estágio **Contrato**.</span><span class="sxs-lookup"><span data-stu-id="f285f-161">For all other deals and quotes, the **Estimate** stage is followed by the **Contract** stage.</span></span>

> [!NOTE]
> <span data-ttu-id="f285f-162">O PSA tem páginas específicas para as entidades Oportunidade, Cotação, Ordem e Fatura.</span><span class="sxs-lookup"><span data-stu-id="f285f-162">PSA has specific pages for the Opportunity, Quote, Order, and Invoice entities.</span></span> <span data-ttu-id="f285f-163">Você deve criar oportunidades, cotações, ordens e faturas de serviço de projeto usando as páginas de informações do projeto para essas entidades.</span><span class="sxs-lookup"><span data-stu-id="f285f-163">You must create project service opportunities, quotes, orders, and invoices using the project information pages for these entities.</span></span> <span data-ttu-id="f285f-164">Se você usar outra página para criar um registro, não será possível abrir o registro pela página **Informações do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="f285f-164">If you use another page to create a record, you won't be able to open the record from the **Project Information** page.</span></span> <span data-ttu-id="f285f-165">Se desejar abrir um registro na página **Informações do Projeto** , você deverá excluir o registro e recriá-lo usando a página **Informações do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="f285f-165">If you want to open a record from the **Project Information** page, you must delete the record and recreate it using the **Project Information** page.</span></span> <span data-ttu-id="f285f-166">Na página **Informações do Projeto** , uma lógica de negócios para cada um desses tipos de entidade garante que o campo **Tipo** do registro seja definido corretamente e todos os conceitos obrigatórios sejam corretamente inicializados.</span><span class="sxs-lookup"><span data-stu-id="f285f-166">On the **Project Information** page, business logic for each of these entity types ensures that the **Type** field of the record is set correctly, and all of the mandatory concepts are properly initialized.</span></span>

> ![Informações do projeto para uma nova ordem](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a><span data-ttu-id="f285f-168">Diferenças entre o Project Service Automation e o Sales</span><span class="sxs-lookup"><span data-stu-id="f285f-168">Differences between Project Service Automation and Sales</span></span>
<span data-ttu-id="f285f-169">Embora o processo de vendas no PSA use os recursos básicos do processo de vendas no Sales, ele tem algumas diferenças básicas devido a variações nas práticas de negócios das organizações baseadas em projeto.</span><span class="sxs-lookup"><span data-stu-id="f285f-169">Although the sales process in PSA uses the basic capabilities of the sales process in Sales, it does have some key differences because of variations in the business practices of project-based organizations.</span></span> <span data-ttu-id="f285f-170">Veja alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="f285f-170">Here are some examples:</span></span>

- <span data-ttu-id="f285f-171">**Cotações do projeto** – no Project Service Automation, uma cotação é fechada depois que um contrato de projeto é criado de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="f285f-171">**Project quotes** – In Project Service Automation, a quote is closed after a project contract is created from a quote.</span></span> <span data-ttu-id="f285f-172">No Sales, é possível manter uma cotação aberta depois que você a ganha.</span><span class="sxs-lookup"><span data-stu-id="f285f-172">In Sales, you can keep a quote open after you've won it.</span></span> <span data-ttu-id="f285f-173">O motivo para essa diferença é que uma correspondência entre uma cotação e um contrato de projeto é melhor para organizações baseadas em projeto.</span><span class="sxs-lookup"><span data-stu-id="f285f-173">The reason for this difference is that a match between a quote and a project contract is better for project-based organizations.</span></span> 
- <span data-ttu-id="f285f-174">**Ativação e revisões** – no PSA, a ativação e as revisões não são aceitas para cotações de projeto.</span><span class="sxs-lookup"><span data-stu-id="f285f-174">**Activation and revisions** – In PSA, activation and revisions aren't supported for project quotes.</span></span> <span data-ttu-id="f285f-175">No Sales, uma cotação pode ser bloqueada para impedir edições adicionais.</span><span class="sxs-lookup"><span data-stu-id="f285f-175">In Sales, a quote can be locked to prevent additional edits.</span></span>
- <span data-ttu-id="f285f-176">**Fechando uma cotação como perdida ou ganha** – no PSA, quando uma cotação de projeto é fechada como ganha ou perdida, a oportunidade permanece aberta.</span><span class="sxs-lookup"><span data-stu-id="f285f-176">**Closing a quote as lost or won** – In PSA, when a project quote is closed as won or lost, the opportunity remains open.</span></span> <span data-ttu-id="f285f-177">Todas as outras cotações na oportunidade são fechadas como perdidas.</span><span class="sxs-lookup"><span data-stu-id="f285f-177">All other quotes on the opportunity are closed as lost.</span></span> <span data-ttu-id="f285f-178">No Sales, quando uma cotação é fechada como ganha ou perdida, o usuário é solicitado a tomar uma medida na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="f285f-178">In Sales, when a quote is closed as won or lost, the user is prompted to take an action on the opportunity.</span></span> <span data-ttu-id="f285f-179">Dependendo da entrada do usuário, a oportunidade subjacente pode ser fechada ou deixada aberta.</span><span class="sxs-lookup"><span data-stu-id="f285f-179">Depending on the user input, the underlying opportunity might be closed or left open.</span></span>

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a><span data-ttu-id="f285f-180">Acompanhando revisões para cotações e planos de projeto no ciclo de vendas</span><span class="sxs-lookup"><span data-stu-id="f285f-180">Tracking revisions to quotes and project plans in the sales cycle</span></span>
<span data-ttu-id="f285f-181">No PSA, não é possível rastrear revisões que são feitas para uma cotação.</span><span class="sxs-lookup"><span data-stu-id="f285f-181">In PSA, you can't track revisions that are made to a quote.</span></span> <span data-ttu-id="f285f-182">Em vez disso, você deve marcar a cotação existente **Fechada como Perdida** e criar uma nova cotação.</span><span class="sxs-lookup"><span data-stu-id="f285f-182">Instead, you must mark the existing quote **Closed as Lost** and then create a new quote.</span></span> <span data-ttu-id="f285f-183">É possível copiar uma cotação ou clonar uma cotação baseada em projeto usando o PSA.</span><span class="sxs-lookup"><span data-stu-id="f285f-183">You can copy a quote or clone a project-based quote by using PSA.</span></span>

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a><span data-ttu-id="f285f-184">Acompanhar comentários e aprovações de cotações e contratos de projeto</span><span class="sxs-lookup"><span data-stu-id="f285f-184">Tracking comments and approvals of quotes and project contracts</span></span>
<span data-ttu-id="f285f-185">Você pode gerenciar a revisão e aprovação de cotações e contratos de projeto usando postagens e murais de registro.</span><span class="sxs-lookup"><span data-stu-id="f285f-185">You can manage the review and approval of quotes and project contracts by using the record wall and posts.</span></span> <span data-ttu-id="f285f-186">Sua organização pode criar fluxos de trabalho e plug-ins personalizados para atribuir, redirecionar, escalonar e gerenciar notificações de revisão e aprovação de itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f285f-186">Your organization can create custom workflows and plug-ins to assign, redirect, escalate, and manage notifications of review and approval work items.</span></span>