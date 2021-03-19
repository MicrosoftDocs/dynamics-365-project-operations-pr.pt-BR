---
title: Visão geral de faturamento intercompanhia
description: Este tópico fornece informações e exemplos sobre como o faturamento intercompanhia de projetos.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287314"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="1b58b-103">Visão geral de faturamento intercompanhia</span><span class="sxs-lookup"><span data-stu-id="1b58b-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="1b58b-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="1b58b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1b58b-105">Sua organização pode ter várias divisões, subsidiárias e outras entidades legais que transferem produtos e serviços de outros projetos entre si.</span><span class="sxs-lookup"><span data-stu-id="1b58b-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="1b58b-106">A entidade legal que fornece o serviço ou produto é chamada de *entidade legal que faz o empréstimo*.</span><span class="sxs-lookup"><span data-stu-id="1b58b-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="1b58b-107">A entidade legal que recebe o serviço ou produto é chamada de *entidade legal que toma o empréstimo*.</span><span class="sxs-lookup"><span data-stu-id="1b58b-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="1b58b-108">A ilustração a seguir mostra um cenário típico em que duas entidades legais, a Contoso Robotics USA (a entidade legal que toma o empréstimo) e a Contoso Robotics UK (a entidade legal que faz o empréstimo) compartilham recursos para entregar um projeto para o cliente, a Adventure works.</span><span class="sxs-lookup"><span data-stu-id="1b58b-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="1b58b-109">Neste cenário, a Contoso Robotics USA é contratada para entregar o trabalho à Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="1b58b-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Faturamento intercompanhia](./media/IntercompanyScenario.png) 

<span data-ttu-id="1b58b-111">O Dynamics 365 Project Operations usa o seguinte fluxo para processar transações intercompanhia:</span><span class="sxs-lookup"><span data-stu-id="1b58b-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="1b58b-112">Os recursos da entidade legal que faz o empréstimo registram as transações de horas ou de despesas intercompanhia reservando tempo e despesas em relação aos projetos na entidade legal que toma o empréstimo.</span><span class="sxs-lookup"><span data-stu-id="1b58b-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="1b58b-113">Os custos de tempo e despesas são registrados na empresa que faz o empréstimo usando a lista de preços de custo da unidade da empresa que toma o empréstimo.</span><span class="sxs-lookup"><span data-stu-id="1b58b-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="1b58b-114">As transações intercompanhia de venda não cobradas são registradas na empresa que faz o empréstimo usando a lista de preços de custo da unidade da empresa que toma o empréstimo.</span><span class="sxs-lookup"><span data-stu-id="1b58b-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="1b58b-115">A receita não cobrada é registrada na empresa que toma o empréstimo usando a lista de preços de venda do contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="1b58b-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="1b58b-116">O cliente poderá ser cobrado quando a receita não cobrada for registrada.</span><span class="sxs-lookup"><span data-stu-id="1b58b-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="1b58b-117">O cliente não precisa esperar até que o processamento da fatura intercompanhia seja concluído.</span><span class="sxs-lookup"><span data-stu-id="1b58b-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="1b58b-118">As faturas intercompanhia de clientes são criadas periodicamente na empresa que faz o empréstimo.</span><span class="sxs-lookup"><span data-stu-id="1b58b-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="1b58b-119">As faturas são criadas manualmente ou usando um processo periódico automatizado.</span><span class="sxs-lookup"><span data-stu-id="1b58b-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="1b58b-120">Uma única fatura pode ser criada para cada entidade legal que toma o empréstimo ou podem ser criadas faturas separadas por projeto.</span><span class="sxs-lookup"><span data-stu-id="1b58b-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="1b58b-121">Quando a fatura intercompanhia do cliente é lançada na entidade legal que faz o empréstimo, a fatura de fornecedor pendente correspondente é criada na entidade legal que toma o empréstimo.</span><span class="sxs-lookup"><span data-stu-id="1b58b-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="1b58b-122">Os custos na fatura de fornecedor pendente serão registrados no razão auxiliar do projeto quando a fatura for lançada.</span><span class="sxs-lookup"><span data-stu-id="1b58b-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="1b58b-123">O diagrama a seguir ilustra o faturamento intercompanhia no que se refere a eventos contábeis e lançamentos esperados na contabilidade.</span><span class="sxs-lookup"><span data-stu-id="1b58b-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Fluxo intercompanhia](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="1b58b-125">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="1b58b-125">Additional resources</span></span>

- [<span data-ttu-id="1b58b-126">Configurar faturamento intercompanhia</span><span class="sxs-lookup"><span data-stu-id="1b58b-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="1b58b-127">Registrar transações intercompanhia</span><span class="sxs-lookup"><span data-stu-id="1b58b-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="1b58b-128">Criar faturas intercompanhia de clientes e fornecedores</span><span class="sxs-lookup"><span data-stu-id="1b58b-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]