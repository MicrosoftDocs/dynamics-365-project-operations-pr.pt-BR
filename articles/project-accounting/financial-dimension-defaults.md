---
title: Padrões de dimensão financeira
description: Este tópico fornece informações sobre como configurar padrões de dimensão financeira.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950115"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="adf00-103">Padrões de dimensão financeira</span><span class="sxs-lookup"><span data-stu-id="adf00-103">Financial dimension defaults</span></span>

<span data-ttu-id="adf00-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="adf00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="adf00-105">O Dynamics 365 Project Operations usa a estrutura de [Dimensões financeiras](/dynamics365/finance/general-ledger/financial-dimensions) no Dynamics 365 Finance para fornecer insights adicionais sobre transações de contabilidade e do razão auxiliar do projeto.</span><span class="sxs-lookup"><span data-stu-id="adf00-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="adf00-106">As dimensões financeiras padrão podem ser definidas em um cliente, fonte de financiamento do projeto, etapa, linha de contrato do projeto ou projeto.</span><span class="sxs-lookup"><span data-stu-id="adf00-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="adf00-107">Defina as dimensões financeiras padrão para um cliente</span><span class="sxs-lookup"><span data-stu-id="adf00-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="adf00-108">Os padrões de dimensão do cliente são especificados em Finanças.</span><span class="sxs-lookup"><span data-stu-id="adf00-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="adf00-109">Conclua as etapas a seguir para definir padrões de dimensão.</span><span class="sxs-lookup"><span data-stu-id="adf00-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="adf00-110">Vá para **Contas a receber** > **Clientes** > **Todos os clientes**.</span><span class="sxs-lookup"><span data-stu-id="adf00-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="adf00-111">Na página **Clientes**, na guia **Dimensões financeiras**, defina os valores de dimensão financeira para o cliente específico.</span><span class="sxs-lookup"><span data-stu-id="adf00-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="adf00-112">Defina as dimensões financeiras padrão para contratos de projeto</span><span class="sxs-lookup"><span data-stu-id="adf00-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="adf00-113">Os contratos de projeto são criados e mantidos no Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="adf00-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="adf00-114">Atributos de contabilidade para contratos de projeto são definidos no módulo **Gerenciamento e contabilidade de projetos** em Finanças.</span><span class="sxs-lookup"><span data-stu-id="adf00-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="adf00-115">Defina as dimensões financeiras para uma fonte de financiamento do projeto</span><span class="sxs-lookup"><span data-stu-id="adf00-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="adf00-116">Acesse **Gerenciamento e contabilidade de projetos** > **Projetos** > **Contratos do projeto**.</span><span class="sxs-lookup"><span data-stu-id="adf00-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="adf00-117">Selecione o registro que deseja atualizar e na guia **Contrato do projeto**, selecione **Mostrar contabilidade padrão**.</span><span class="sxs-lookup"><span data-stu-id="adf00-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="adf00-118">Expanda **Informações relacionadas** e selecione a guia **Fontes de financiamento**.</span><span class="sxs-lookup"><span data-stu-id="adf00-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="adf00-119">Defina os padrões de dimensão financeira.</span><span class="sxs-lookup"><span data-stu-id="adf00-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="adf00-120">Observe que as dimensões financeiras são padronizadas a partir da conta do cliente.</span><span class="sxs-lookup"><span data-stu-id="adf00-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="adf00-121">Definir dimensões financeiras para uma linha de contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="adf00-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="adf00-122">Acesse **Gerenciamento e contabilidade de projetos** > **Projetos** > **Contratos do projeto**.</span><span class="sxs-lookup"><span data-stu-id="adf00-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="adf00-123">Selecione o registro a ser atualizado e, na guia **Contrato do projeto**, selecione **Mostrar contabilidade padrão**.</span><span class="sxs-lookup"><span data-stu-id="adf00-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="adf00-124">Expanda **Informações relacionadas** e selecione a guia **Linhas do contrato**.</span><span class="sxs-lookup"><span data-stu-id="adf00-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="adf00-125">Defina os padrões de dimensão financeira.</span><span class="sxs-lookup"><span data-stu-id="adf00-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="adf00-126">Os padrões de dimensão financeira são aplicáveis e podem ser usados apenas com linhas de contrato de preço fixo (etapa).</span><span class="sxs-lookup"><span data-stu-id="adf00-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="adf00-127">Esses padrões são usados em transações por conta de projetos relacionados e linhas de fatura.</span><span class="sxs-lookup"><span data-stu-id="adf00-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="adf00-128">Defina as dimensões financeiras padrão para projetos</span><span class="sxs-lookup"><span data-stu-id="adf00-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="adf00-129">Projetos são criados e mantidos no CDS.</span><span class="sxs-lookup"><span data-stu-id="adf00-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="adf00-130">Atributos de contabilidade para projetos são definidos no módulo **Gerenciamento e contabilidade de projetos** em Finanças.</span><span class="sxs-lookup"><span data-stu-id="adf00-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="adf00-131">Acesse **Gerenciamento e contabilidade de projeto** > **Projetos** > **Todos os projetos**.</span><span class="sxs-lookup"><span data-stu-id="adf00-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="adf00-132">Selecione o registro a ser atualizado e, na guia **Projeto**, selecione **Mostrar contabilidade padrão**.</span><span class="sxs-lookup"><span data-stu-id="adf00-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="adf00-133">Expanda **Informações relacionadas** e selecione a guia **Configuração**.</span><span class="sxs-lookup"><span data-stu-id="adf00-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="adf00-134">Defina os padrões de dimensão financeira.</span><span class="sxs-lookup"><span data-stu-id="adf00-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="adf00-135">Observe que dimensões financeiras são padronizadas a partir da conta do cliente.</span><span class="sxs-lookup"><span data-stu-id="adf00-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="adf00-136">Se o projeto estiver associado a uma linha de contrato com vários clientes de contrato de projeto, o cliente principal será usado para dimensões financeiras padrão.</span><span class="sxs-lookup"><span data-stu-id="adf00-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="adf00-137">As dimensões financeiras padrão do projeto são usadas para definir padrões de linha de diário para transações de hora, despesas e taxas no **Diário de Integração de Operações do Projeto** e nas linhas de fatura do projeto relacionado.</span><span class="sxs-lookup"><span data-stu-id="adf00-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]