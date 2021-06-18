---
title: Consulta sobre agendamento de despesas de prêmios federais
description: Este tópico fornece informações sobre a consulta sobre agendamento de despesas de prêmios federais.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010052"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="cd19a-103">Consulta sobre agendamento de despesas de prêmios federais</span><span class="sxs-lookup"><span data-stu-id="cd19a-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd19a-104">De acordo com a Circular A-133 do Office of Management and Budget, as agências que recebem fundos federais estão sujeitas a exigências de auditoria, também conhecidas como auditorias únicas.</span><span class="sxs-lookup"><span data-stu-id="cd19a-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="cd19a-105">O processo de auditoria é usado para relatar as receitas e despesas dos subsídios federais de maneira recorrente.</span><span class="sxs-lookup"><span data-stu-id="cd19a-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="cd19a-106">Parte do relatório de auditoria única inclui o agendamento de despesas de prêmios federais (Schedule of Expenditures of Federal Awards, SEFA).</span><span class="sxs-lookup"><span data-stu-id="cd19a-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="cd19a-107">A consulta sobre agendamento de despesas de prêmios federais inclui o título e número do catálogo de assistência doméstica federal (Catalog of Federal Domestic Assistance, CFDA), o número da concessão, o ano da concessão, o nome da agência federal que fornece os fundos e o nome da entidade de passagem.</span><span class="sxs-lookup"><span data-stu-id="cd19a-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="cd19a-108">A consulta ocorre por um período específico.</span><span class="sxs-lookup"><span data-stu-id="cd19a-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="cd19a-109">Geralmente, esse período é igual ao período das demonstrações financeiras, que é um ano fiscal.</span><span class="sxs-lookup"><span data-stu-id="cd19a-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="cd19a-110">A consulta inclui concessões que têm datas de projeção no intervalo de datas selecionado.</span><span class="sxs-lookup"><span data-stu-id="cd19a-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="cd19a-111">A coluna **Agência concedente** da consulta mostra o cliente da concessão ou, para uma concessão de passagem, a agência concedente.</span><span class="sxs-lookup"><span data-stu-id="cd19a-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="cd19a-112">Para uma concessão de passagem, a coluna **Agência de passagem** mostra o cliente da concessão.</span><span class="sxs-lookup"><span data-stu-id="cd19a-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="cd19a-113">Se a concessão não for uma concessão de passagem, a coluna **Agência de passagem** ficará em branco.</span><span class="sxs-lookup"><span data-stu-id="cd19a-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="cd19a-114">Configurar os clusters do CFDA</span><span class="sxs-lookup"><span data-stu-id="cd19a-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="cd19a-115">Você deve configurar os clusters do CFDA que podem ser associados aos números do CFDA na consulta sobre agendamento de despesas de prêmios federais.</span><span class="sxs-lookup"><span data-stu-id="cd19a-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="cd19a-116">Acesse **Gerenciamento e contabilidade de projeto \> Configuração \> Concessões \> Clusters do catálogo de assistência doméstica federal**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="cd19a-117">Selecione **Novo** para criar um cluster do CFDA.</span><span class="sxs-lookup"><span data-stu-id="cd19a-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="cd19a-118">Insira o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="cd19a-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="cd19a-119">Selecione **Salvar** para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="cd19a-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="cd19a-120">Configurar os números do CFDA</span><span class="sxs-lookup"><span data-stu-id="cd19a-120">Set up CFDA numbers</span></span>

<span data-ttu-id="cd19a-121">Você deve configurar os números do CFDA que podem ser adicionados às concessões e incluídos na consulta sobre agendamento de despesas de prêmios federais.</span><span class="sxs-lookup"><span data-stu-id="cd19a-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="cd19a-122">Acesse **Gerenciamento e contabilidade de projeto \> Configuração \> Concessões \> Números do catálogo de assistência doméstica federal**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="cd19a-123">Selecione **Novo** para criar um número do CFDA.</span><span class="sxs-lookup"><span data-stu-id="cd19a-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="cd19a-124">Na coluna **Número**, insira o número do CFDA.</span><span class="sxs-lookup"><span data-stu-id="cd19a-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="cd19a-125">Pressione a tecla **Tab**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="cd19a-126">Na coluna **Descrição**, insira o título do CFDA.</span><span class="sxs-lookup"><span data-stu-id="cd19a-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="cd19a-127">Pressione a tecla **Tab**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="cd19a-128">Opcional: no campo **Cluster de programas**, inclua o cluster do CFDA apropriado.</span><span class="sxs-lookup"><span data-stu-id="cd19a-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="cd19a-129">Selecione **Salvar** para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="cd19a-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="cd19a-130">Configurar concessões para relatar para a consulta sobre agendamento de despesas de prêmios federais</span><span class="sxs-lookup"><span data-stu-id="cd19a-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="cd19a-131">Acesse **Gerenciamento e contabilidade de projeto \> Concessões \> Concessões** e selecione uma concessão existente.</span><span class="sxs-lookup"><span data-stu-id="cd19a-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="cd19a-132">Na FastTab **Configuração**, no campo **Catálogo de assistência doméstica federal**, atribua o número do CFDA.</span><span class="sxs-lookup"><span data-stu-id="cd19a-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="cd19a-133">O número do CFDA na concessão determina o cluster do CFDA para relatórios.</span><span class="sxs-lookup"><span data-stu-id="cd19a-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="cd19a-134">Na FastTab **Informações de contato**, insira as informações do concedente seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="cd19a-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="cd19a-135">No campo **Cliente da concessão**, insira o cliente que é responsável pela concessão.</span><span class="sxs-lookup"><span data-stu-id="cd19a-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="cd19a-136">Para uma concessão existente, essas informações podem já ter sido inseridas.</span><span class="sxs-lookup"><span data-stu-id="cd19a-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="cd19a-137">Indique se o cliente da concessão é o financiador.</span><span class="sxs-lookup"><span data-stu-id="cd19a-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="cd19a-138">Se o cliente da concessão for o financiador, deixe a caixa de seleção **Passagem** desmarcada.</span><span class="sxs-lookup"><span data-stu-id="cd19a-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="cd19a-139">Se outro cliente for o financiador e o cliente da concessão for responsável por gastar e rastrear o dinheiro, marque a caixa de seleção **Passagem**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="cd19a-140">Se você marcou a caixa de seleção **Passagem** na etapa anterior, no campo **Agência concedente**, insira o cliente que forneceu a concessão.</span><span class="sxs-lookup"><span data-stu-id="cd19a-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="cd19a-141">A agência concedente e o cliente da concessão não podem ser o mesmo cliente.</span><span class="sxs-lookup"><span data-stu-id="cd19a-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="cd19a-142">Aqui está um exemplo de concessão de passagem:</span><span class="sxs-lookup"><span data-stu-id="cd19a-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="cd19a-143">O governo federal financiou um projeto de infraestrutura para um estado.</span><span class="sxs-lookup"><span data-stu-id="cd19a-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="cd19a-144">O governo federal deu o dinheiro para o estado gastar.</span><span class="sxs-lookup"><span data-stu-id="cd19a-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="cd19a-145">Nesse caso, o governo federal é a agência concedente e o estado é o cliente da concessão.</span><span class="sxs-lookup"><span data-stu-id="cd19a-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="cd19a-146">Quando você ativa o recurso pela primeira vez, os números do CFDA iniciais serão inseridos usando os números existentes nas concessões.</span><span class="sxs-lookup"><span data-stu-id="cd19a-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="cd19a-147">Excluir concessões de relatórios do SEFA com base no tipo de concessão</span><span class="sxs-lookup"><span data-stu-id="cd19a-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="cd19a-148">Acesse **Gerenciamento e contabilidade de projeto \> Configuração \> Concessões \> Tipos de concessão**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="cd19a-149">Na FastTab **Informações padrão**, marque a caixa de seleção **Excluir do agendamento de despesas de prêmios federais**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="cd19a-150">Selecione **Salvar** para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="cd19a-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="cd19a-151">Executar a consulta sobre agendamento de despesas de prêmios federais</span><span class="sxs-lookup"><span data-stu-id="cd19a-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="cd19a-152">Acesse **Gerenciamento e contabilidade de projeto \> Consultas e relatórios \> Consulta de concessão \> Agendamento de despesas de prêmios federais**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="cd19a-153">Na seção **Parâmetros**, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="cd19a-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="cd19a-154">No campo **Intervalo de data**, selecione o código para o intervalo de data.</span><span class="sxs-lookup"><span data-stu-id="cd19a-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="cd19a-155">Se desejar, nos campos **Data inicial** e **Data final**, defina o intervalo de data.</span><span class="sxs-lookup"><span data-stu-id="cd19a-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="cd19a-156">Opcional: para incluir apenas transações cobradas como receita na consulta, defina a opção **Incluir somente receitas cobradas** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="cd19a-157">Colunas</span><span class="sxs-lookup"><span data-stu-id="cd19a-157">Columns</span></span>

<span data-ttu-id="cd19a-158">A consulta sobre agendamento de despesas de prêmios federais inclui as seguintes colunas:</span><span class="sxs-lookup"><span data-stu-id="cd19a-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="cd19a-159">Nome do cluster do catálogo de assistência doméstica federal</span><span class="sxs-lookup"><span data-stu-id="cd19a-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="cd19a-160">Agência concedente</span><span class="sxs-lookup"><span data-stu-id="cd19a-160">Grantor agency</span></span>
- <span data-ttu-id="cd19a-161">Agência de passagem</span><span class="sxs-lookup"><span data-stu-id="cd19a-161">Pass-through agency</span></span>
- <span data-ttu-id="cd19a-162">Nome da concessão</span><span class="sxs-lookup"><span data-stu-id="cd19a-162">Grant name</span></span>
- <span data-ttu-id="cd19a-163">ID da concessão</span><span class="sxs-lookup"><span data-stu-id="cd19a-163">Grant ID</span></span>
- <span data-ttu-id="cd19a-164">ID do pedido de concessão</span><span class="sxs-lookup"><span data-stu-id="cd19a-164">Grant application ID</span></span>
- <span data-ttu-id="cd19a-165">Catálogo de assistência doméstica federal</span><span class="sxs-lookup"><span data-stu-id="cd19a-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="cd19a-166">Recibos</span><span class="sxs-lookup"><span data-stu-id="cd19a-166">Receipts</span></span>
- <span data-ttu-id="cd19a-167">Despesas</span><span class="sxs-lookup"><span data-stu-id="cd19a-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]