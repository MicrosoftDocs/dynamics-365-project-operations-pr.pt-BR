---
title: Aplicar instalação de demonstração e dados de configuração
description: Este tópico fornece informações sobre como aplicar os dados de configuração e instalação de demonstração para Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071293"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="f42fb-103">Aplicar instalação de demonstração e dados de configuração para implantação do Project Operations Lite - transação para faturamento pró-forma</span><span class="sxs-lookup"><span data-stu-id="f42fb-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="f42fb-104">_\*\*Fazer implantação do Project Operations Lite - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="f42fb-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="f42fb-105">Faça o download do [Pacote de dados mestre](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="f42fb-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="f42fb-106">Navegue até a pasta *ProjOpsDemoDataSetupAndMaster - CMT integrado* e execute o arquivo executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f42fb-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f42fb-107">Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="f42fb-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migração de Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f42fb-109">Na página 2 do Assistente CMT, selecione **Microsoft 365** como o **Tipo de Implantação**.</span><span class="sxs-lookup"><span data-stu-id="f42fb-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f42fb-110">Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.</span><span class="sxs-lookup"><span data-stu-id="f42fb-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f42fb-111">Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="f42fb-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Entrar na configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f42fb-113">Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="f42fb-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="f42fb-114">Na página 4, selecione o arquivo zip *MasterAndSetupData* da pasta descompactada *ProjOpsDemoDataSetupAndMaster - CMT integrado*.</span><span class="sxs-lookup"><span data-stu-id="f42fb-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Arquivo compactado](./media/3ZipFile.png)

![Selecionar um arquivo](./media/4SelectAFile.png)

9. <span data-ttu-id="f42fb-117">Depois que o arquivo zip for selecionado, selecione **Importar dados**.</span><span class="sxs-lookup"><span data-stu-id="f42fb-117">After the zip file is selected, select **Import Data**.</span></span>

![Importar dados](./media/5ImportData.png)

10. <span data-ttu-id="f42fb-119">A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="f42fb-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f42fb-120">Após da conclusão, saia do Assistente do CMT.</span><span class="sxs-lookup"><span data-stu-id="f42fb-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f42fb-121">Verifique se há dados na sua organização nas 20 entidades a seguir:</span><span class="sxs-lookup"><span data-stu-id="f42fb-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="f42fb-122">Moeda</span><span class="sxs-lookup"><span data-stu-id="f42fb-122">Currency</span></span>
- <span data-ttu-id="f42fb-123">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="f42fb-123">Organizational Unit</span></span>
- <span data-ttu-id="f42fb-124">Contato</span><span class="sxs-lookup"><span data-stu-id="f42fb-124">Contact</span></span>
- <span data-ttu-id="f42fb-125">Grupo tributário</span><span class="sxs-lookup"><span data-stu-id="f42fb-125">Tax Group</span></span>
- <span data-ttu-id="f42fb-126">Grupo de Clientes</span><span class="sxs-lookup"><span data-stu-id="f42fb-126">Customer Group</span></span>
- <span data-ttu-id="f42fb-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="f42fb-127">Unit</span></span>
- <span data-ttu-id="f42fb-128">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="f42fb-128">Unit Group</span></span>
- <span data-ttu-id="f42fb-129">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="f42fb-129">Price List</span></span>
- <span data-ttu-id="f42fb-130">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="f42fb-130">Project Parameter Price List</span></span>
- <span data-ttu-id="f42fb-131">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="f42fb-131">Invoice Frequency</span></span>
- <span data-ttu-id="f42fb-132">Detalhe da Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="f42fb-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="f42fb-133">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="f42fb-133">Bookable Resource Category</span></span>
- <span data-ttu-id="f42fb-134">Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="f42fb-134">Transaction Category</span></span>
- <span data-ttu-id="f42fb-135">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="f42fb-135">Expense Category</span></span>
- <span data-ttu-id="f42fb-136">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="f42fb-136">Role Price</span></span>
- <span data-ttu-id="f42fb-137">Preço da Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="f42fb-137">Transaction Category Price</span></span>
- <span data-ttu-id="f42fb-138">Característica</span><span class="sxs-lookup"><span data-stu-id="f42fb-138">Characteristic</span></span>
- <span data-ttu-id="f42fb-139">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="f42fb-139">Bookable Resource</span></span>
- <span data-ttu-id="f42fb-140">Associação de Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="f42fb-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="f42fb-141">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="f42fb-141">Bookable Resource Characteristic</span></span>

![Concluir importação](./media/6CompleteImport.png)
