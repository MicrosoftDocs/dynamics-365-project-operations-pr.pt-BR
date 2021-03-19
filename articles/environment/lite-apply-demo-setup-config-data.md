---
title: Aplicar configuração de demonstração e dados de configuração - lite
description: Este tópico fornece informações sobre como aplicar os dados de configuração e instalação de demonstração para Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 694dbc74591de74895095a9da6e590069711fc83
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290120"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="b7a31-103">Aplicar configuração de demonstração e dados de configuração para o Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="b7a31-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="b7a31-104">_\*\*Fazer implantação do Project Operations Lite - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="b7a31-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="b7a31-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b7a31-105">Prerequisites</span></span>

<span data-ttu-id="b7a31-106">Antes de iniciar a configuração, você deve ter um ambiente do Common Data Service (CDS) provisionado para o Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b7a31-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="b7a31-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="b7a31-107">Instructions</span></span>

1. <span data-ttu-id="b7a31-108">Faça o download do [Pacote de dados mestre](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="b7a31-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="b7a31-109">Navegue até a pasta *ProjOpsDemoDataSetupAndMaster - CMT integrado* e execute o arquivo executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="b7a31-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="b7a31-110">Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="b7a31-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migração de Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="b7a31-112">Na página 2 do Assistente CMT, selecione **Microsoft 365** como o **Tipo de Implantação**.</span><span class="sxs-lookup"><span data-stu-id="b7a31-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="b7a31-113">Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.</span><span class="sxs-lookup"><span data-stu-id="b7a31-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="b7a31-114">Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="b7a31-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Entrar na configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="b7a31-116">Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="b7a31-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="b7a31-117">Na página 4, selecione o arquivo zip *MasterAndSetupData* da pasta descompactada *ProjOpsDemoDataSetupAndMaster - CMT integrado*.</span><span class="sxs-lookup"><span data-stu-id="b7a31-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Arquivo compactado](./media/3ZipFile.png)

   ![Selecionar um arquivo](./media/4SelectAFile.png)

9. <span data-ttu-id="b7a31-120">Depois que o arquivo zip for selecionado, selecione **Importar dados**.</span><span class="sxs-lookup"><span data-stu-id="b7a31-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importar dados](./media/5ImportData.png)

10. <span data-ttu-id="b7a31-122">A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="b7a31-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="b7a31-123">Após da conclusão, saia do Assistente do CMT.</span><span class="sxs-lookup"><span data-stu-id="b7a31-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="b7a31-124">Verifique se há dados na sua organização nas 20 entidades a seguir:</span><span class="sxs-lookup"><span data-stu-id="b7a31-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="b7a31-125">Moeda</span><span class="sxs-lookup"><span data-stu-id="b7a31-125">Currency</span></span>
    -   <span data-ttu-id="b7a31-126">Conta</span><span class="sxs-lookup"><span data-stu-id="b7a31-126">Account</span></span>
    -   <span data-ttu-id="b7a31-127">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="b7a31-127">Organizational Unit</span></span>
    -   <span data-ttu-id="b7a31-128">Contato</span><span class="sxs-lookup"><span data-stu-id="b7a31-128">Contact</span></span>
    -   <span data-ttu-id="b7a31-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="b7a31-129">Unit</span></span>
    -   <span data-ttu-id="b7a31-130">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="b7a31-130">Unit Group</span></span>
    -   <span data-ttu-id="b7a31-131">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="b7a31-131">Price List</span></span>
    -   <span data-ttu-id="b7a31-132">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="b7a31-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="b7a31-133">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="b7a31-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="b7a31-134">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="b7a31-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="b7a31-135">Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="b7a31-135">Transaction Category</span></span>
    -   <span data-ttu-id="b7a31-136">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="b7a31-136">Expense Category</span></span>
    -   <span data-ttu-id="b7a31-137">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="b7a31-137">Role Price</span></span>
    -   <span data-ttu-id="b7a31-138">Preço da Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="b7a31-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="b7a31-139">Característica</span><span class="sxs-lookup"><span data-stu-id="b7a31-139">Characteristic</span></span>
    -   <span data-ttu-id="b7a31-140">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="b7a31-140">Bookable Resource</span></span>
    -   <span data-ttu-id="b7a31-141">Associação de Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="b7a31-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="b7a31-142">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="b7a31-142">Bookable Resource Characteristic</span></span>

    ![Concluir importação](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]