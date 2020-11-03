---
title: Configurar faturamento intercompanhia de projetos
description: Este tópico mostra como configurar o faturamento de projetos entre duas empresas em sua organização.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071487"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="ffe0f-103">Configurar faturamento intercompanhia de projetos</span><span class="sxs-lookup"><span data-stu-id="ffe0f-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffe0f-104">Este tópico mostra como configurar o faturamento de projetos entre duas empresas em sua organização.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="ffe0f-105">Esta tarefa usa o conjunto de dados USSI.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="ffe0f-106">No painel de navegação, acesse **Módulos > Contas a pagar > Fornecedores > Todos os fornecedores**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="ffe0f-107">Na lista **Todos os fornecedores** , encontre e selecione o registro desejado.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="ffe0f-108">No Painel de Ações, selecione **Geral**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="ffe0f-109">Selecione **Intercompanhia**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="ffe0f-110">Defina **Ativo** como **Sim** para habilitar o comércio intercompanhia.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="ffe0f-111">No campo **Empresa do cliente** , insira ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="ffe0f-112">No campo **Minha conta** , insira ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="ffe0f-113">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-113">Select **Save**.</span></span>
9. <span data-ttu-id="ffe0f-114">Feche as páginas para retornar à home page.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="ffe0f-115">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Parâmetros de gerenciamento e contabilidade de projeto**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="ffe0f-116">Selecione a guia **Intercompanhia**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="ffe0f-117">Mova o controle deslizante para **Sim** para habilitar o agendamento e as folhas de ponto dos recursos.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="ffe0f-118">Na lista, marque a linha selecionada.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ffe0f-119">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-119">Select **New**.</span></span>
15. <span data-ttu-id="ffe0f-120">No campo **Entidade legal que toma o empréstimo** , insira ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="ffe0f-121">Marque a caixa de seleção **Acumular receita**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="ffe0f-122">No campo **Categoria de folha de ponto padrão** , insira ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="ffe0f-123">No campo **Categoria de despesa padrão** , insira ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="ffe0f-124">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-124">Select **Save**.</span></span>
20. <span data-ttu-id="ffe0f-125">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-125">Close the page.</span></span>
21. <span data-ttu-id="ffe0f-126">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Lançamento > Configuração de lançamento contábil**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="ffe0f-127">No campo **Tipos de conta contábil** , insira ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="ffe0f-128">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-128">Select **New**.</span></span>
24. <span data-ttu-id="ffe0f-129">No campo **Conta principal** da nova linha, especifique os valores desejados.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="ffe0f-130">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-130">Select **Save**.</span></span>
26. <span data-ttu-id="ffe0f-131">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-131">Close the page.</span></span>
27. <span data-ttu-id="ffe0f-132">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de transferência**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="ffe0f-133">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-133">Select **New**.</span></span>
29. <span data-ttu-id="ffe0f-134">No campo **Data de efetivação** , insira uma data.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="ffe0f-135">No campo **Entidade legal que toma o empréstimo** , insira ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="ffe0f-136">No campo **Modelo de preço de transferência** , insira ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="ffe0f-137">No campo **Preço** , insira um número.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="ffe0f-138">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-138">Select **Save**.</span></span>

