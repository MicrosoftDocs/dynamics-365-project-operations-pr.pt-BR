---
title: Copiar contratos de projeto - lite
description: Este tópico fornece informações sobre como copiar contratos de projetos no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4137fc400c7fdd8fecd9d8349bf7f57f3470b51f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181393"
---
# <a name="copy-project-contracts---lite"></a><span data-ttu-id="51323-103">Copiar contratos de projeto - lite</span><span class="sxs-lookup"><span data-stu-id="51323-103">Copy project contracts - lite</span></span>

<span data-ttu-id="51323-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="51323-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="51323-105">Você pode criar facilmente novos contratos de projeto fazendo cópias dos contratos existentes de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="51323-105">You can easily create new project contracts by making copies of existing contracts in one of two ways:</span></span> 

  - <span data-ttu-id="51323-106">Na página de listagem **Contratos de Projeto**, selecione um contrato de projeto e selecione **Copiar**.</span><span class="sxs-lookup"><span data-stu-id="51323-106">On the **Project Contracts** list page, select a project contract and then select **Copy**.</span></span>
  - <span data-ttu-id="51323-107">Na página **Contrato de Projeto**, selecione **Copiar**.</span><span class="sxs-lookup"><span data-stu-id="51323-107">On the **Project Contract** details page, select **Copy**.</span></span>

<span data-ttu-id="51323-108">Uma página de diálogo será aberta, onde você poderá selecionar os parâmetros do contrato copiado.</span><span class="sxs-lookup"><span data-stu-id="51323-108">A dialog page will open where you can select the parameters of the copied contract.</span></span> <span data-ttu-id="51323-109">Os campos a seguir são incluídos no diálogo.</span><span class="sxs-lookup"><span data-stu-id="51323-109">The following fields are included on the dialog.</span></span> <span data-ttu-id="51323-110">Dependendo dos valores que você selecionar nesse diálogo, o processo de cópia poderá mudar.</span><span class="sxs-lookup"><span data-stu-id="51323-110">Depending on the values you select in this dialog, the copy process may change.</span></span>

| <span data-ttu-id="51323-111">**Campo**</span><span class="sxs-lookup"><span data-stu-id="51323-111">**Field**</span></span> | <span data-ttu-id="51323-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="51323-112">**Description**</span></span> | <span data-ttu-id="51323-113">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="51323-113">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="51323-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="51323-114">Topic</span></span> | <span data-ttu-id="51323-115">Insira o tópico do contrato de destino.</span><span class="sxs-lookup"><span data-stu-id="51323-115">Enter the topic of the target contract.</span></span> <span data-ttu-id="51323-116">Quando a página de diálogo for aberta, o sistema definirá esse campo com o nome do contrato de origem com **cópia** acrescentado.</span><span class="sxs-lookup"><span data-stu-id="51323-116">When the dialog page opens, the system will set this field to the name of the source contract with **copy** appended to it.</span></span> | <span data-ttu-id="51323-117">Não há impacto posterior para esse campo.</span><span class="sxs-lookup"><span data-stu-id="51323-117">There's no downstream impact for this field.</span></span> |
| <span data-ttu-id="51323-118">Cliente</span><span class="sxs-lookup"><span data-stu-id="51323-118">Customer</span></span> | <span data-ttu-id="51323-119">Referência à empresa do cliente ou registro de conta.</span><span class="sxs-lookup"><span data-stu-id="51323-119">Reference to the customer's company or account record.</span></span> <span data-ttu-id="51323-120">Quando a caixa de diálogo for aberta, o sistema definirá esse campo para a conta no contrato de origem.</span><span class="sxs-lookup"><span data-stu-id="51323-120">When the dialog opens, the system will set this field to the account on the source contract.</span></span> | <span data-ttu-id="51323-121">Esse campo é o cliente principal no contrato.</span><span class="sxs-lookup"><span data-stu-id="51323-121">This field is the primary customer on the contract.</span></span> |
| <span data-ttu-id="51323-122">Unidade de Contratação</span><span class="sxs-lookup"><span data-stu-id="51323-122">Contracting Unit</span></span> | <span data-ttu-id="51323-123">A Unidade organizacional responsável pela entrega do projeto ou projetos associados a este negócio.</span><span class="sxs-lookup"><span data-stu-id="51323-123">The Organization unit that is responsible for the delivery of the project(s) associated with this deal.</span></span> <span data-ttu-id="51323-124">Quando a página de diálogo for aberta, o sistema irá configurá-lo para a unidade de contratação no contrato de origem.</span><span class="sxs-lookup"><span data-stu-id="51323-124">When the dialog page opens, the system will set it to the contracting unit of the source contract.</span></span> | <span data-ttu-id="51323-125">A unidade de contratação é a divisão da empresa que executará os projetos após o fechamento do negócio.</span><span class="sxs-lookup"><span data-stu-id="51323-125">The contracting unit is the division of the company that will be executing the projects after the deal is closed.</span></span> <span data-ttu-id="51323-126">Cada unidade contratante tem uma moeda.</span><span class="sxs-lookup"><span data-stu-id="51323-126">Every contracting unit has a currency.</span></span> <span data-ttu-id="51323-127">Essa moeda é usada para relatar os custos estimados e reais incorridos durante o projeto.</span><span class="sxs-lookup"><span data-stu-id="51323-127">This currency is used to report estimated and actual costs incurred during the project.</span></span> |
| <span data-ttu-id="51323-128">Moeda</span><span class="sxs-lookup"><span data-stu-id="51323-128">Currency</span></span> | <span data-ttu-id="51323-129">A moeda de transação do negócio.</span><span class="sxs-lookup"><span data-stu-id="51323-129">The currency that the deal is transacted in.</span></span> <span data-ttu-id="51323-130">Quando a página de diálogo for aberta, o sistema definirá o campo como a moeda do contrato de origem.</span><span class="sxs-lookup"><span data-stu-id="51323-130">When the dialog page opens, the system will set the field to the currency of the source contract.</span></span> <span data-ttu-id="51323-131">A moeda pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="51323-131">The currency can be changed.</span></span> <span data-ttu-id="51323-132">Se for, o campo **Copiar Preços** sempre será definido como **Não** porque as listas de preços no contrato de origem não serão mais relevantes.</span><span class="sxs-lookup"><span data-stu-id="51323-132">If it is, the **Copy Pricing** field is always set to **No** because the price lists on source contract are no longer relevant.</span></span> | <span data-ttu-id="51323-133">A moeda é usada para listas de preços padrão, para a criação de estimativas financeiras no contrato e para faturar o cliente quando o negócio for ganho.</span><span class="sxs-lookup"><span data-stu-id="51323-133">Currency is used for default price lists, for building financial estimates on the contract, and for invoicing the customer when the deal is won.</span></span> |
| <span data-ttu-id="51323-134">Data de Entrega da Solicitação</span><span class="sxs-lookup"><span data-stu-id="51323-134">Requested Delivery Date</span></span> | <span data-ttu-id="51323-135">A data de entrega solicitada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="51323-135">The delivery date requested by the customer.</span></span> | <span data-ttu-id="51323-136">Essa data é usada como a data de término quando você criar datas de faturamento ao longo de uma frequência específica.</span><span class="sxs-lookup"><span data-stu-id="51323-136">This date is used as the end date when you create invoicing dates along a specific frequency.</span></span> |
| <span data-ttu-id="51323-137">Copiar precificação</span><span class="sxs-lookup"><span data-stu-id="51323-137">Copy pricing</span></span> | <span data-ttu-id="51323-138">Indica se os preços no contrato deverão ser copiados do contrato de origem.</span><span class="sxs-lookup"><span data-stu-id="51323-138">Indicates whether the pricing on the contract should be copied from the source contract.</span></span> | <span data-ttu-id="51323-139">Se o campo estiver definido como **Sim**, as referências de lista de preços de projeto e produto serão copiadas do contrato de origem para o contrato de destino.</span><span class="sxs-lookup"><span data-stu-id="51323-139">If the field is set to **Yes**, project and product price list references are copied from the source to the target contract.</span></span> <span data-ttu-id="51323-140">Se **Não** estiver selecionado, as listas de preços terão o padrão baseado nas listas de preços mais recentes nos parâmetros de conta ou de projeto.</span><span class="sxs-lookup"><span data-stu-id="51323-140">If **No** is selected, price lists default based on the latest price lists on the account or project parameters.</span></span> |

<span data-ttu-id="51323-141">Quando você seleciona **OK** na página de diálogo, o sistema cria uma cópia do contrato com base nos parâmetros selecionados.</span><span class="sxs-lookup"><span data-stu-id="51323-141">When you select **OK** on the dialog page, the system creates a copy of the contract based on the parameters selected.</span></span> <span data-ttu-id="51323-142">O novo contrato será aberto.</span><span class="sxs-lookup"><span data-stu-id="51323-142">The new contract will open.</span></span>

<span data-ttu-id="51323-143">As seguintes informações não são copiadas da **Origem** para o **Contrato de Destino**:</span><span class="sxs-lookup"><span data-stu-id="51323-143">The following information isn't copied from the **Source** to the **Target Contract**:</span></span>

  - <span data-ttu-id="51323-144">Agendamento de faturas</span><span class="sxs-lookup"><span data-stu-id="51323-144">Invoice schedules</span></span>
  - <span data-ttu-id="51323-145">Clientes de contrato e de linha de contrato</span><span class="sxs-lookup"><span data-stu-id="51323-145">Contract and contract line customers</span></span>
  - <span data-ttu-id="51323-146">Referência de projeto nas linhas de contrato baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="51323-146">Project reference on the project-based contract lines</span></span>
  - <span data-ttu-id="51323-147">Informações de orçamento do cliente</span><span class="sxs-lookup"><span data-stu-id="51323-147">Customer budget information</span></span>

<span data-ttu-id="51323-148">Como essas informações são específicas para cada contrato, esses campos e registros não são copiados.</span><span class="sxs-lookup"><span data-stu-id="51323-148">Because this information is specific to each contract, these fields and records aren't copied.</span></span> <span data-ttu-id="51323-149">Linhas de contrato para projetos e produtos, estimativas em detalhes da linha de contrato e valores que não devem ser excedidos no nível de contrato são copiados.</span><span class="sxs-lookup"><span data-stu-id="51323-149">Contract lines for projects and products, estimations on contract line details, and not-to-exceed values at the contract level are copied.</span></span> <span data-ttu-id="51323-150">Os padrões de preço e taxa de custo dependem da seleção no campo **Preços de cópia** na página de diálogo **Parâmetros de Cópia**.</span><span class="sxs-lookup"><span data-stu-id="51323-150">Price and cost rate defaulting depend on the selection in the **Copy pricing** field on the **Copy Parameters** dialog page.</span></span>