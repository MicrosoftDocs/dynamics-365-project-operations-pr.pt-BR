---
title: Configurar e aplicar dados de configuração no Common Data Service
description: Este tópico fornece informações sobre a configuração e aplicação de dados de configuração no Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401114"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="4c84f-103">Configurar e aplicar dados de configuração no Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4c84f-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="4c84f-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="4c84f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4c84f-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4c84f-105">Prerequisites</span></span>

<span data-ttu-id="4c84f-106">Antes de começar a configurar os dados no Common Data Service (CDS), os seguintes pré-requisitos devem ser atendidos:</span><span class="sxs-lookup"><span data-stu-id="4c84f-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="4c84f-107">Provisione um ambiente CDS e um ambiente do Dynamics 365 Finance para o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4c84f-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="4c84f-108">As informações de pessoa jurídica do Dynamics 365 Finance são compartilhadas no ambiente CDS.</span><span class="sxs-lookup"><span data-stu-id="4c84f-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="4c84f-109">Isso significa que a entidade **Empresa** no CDS tem os seguintes registros da empresa:</span><span class="sxs-lookup"><span data-stu-id="4c84f-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="4c84f-110">THPM</span><span class="sxs-lookup"><span data-stu-id="4c84f-110">THPM</span></span>
  - <span data-ttu-id="4c84f-111">USPM</span><span class="sxs-lookup"><span data-stu-id="4c84f-111">USPM</span></span>
  - <span data-ttu-id="4c84f-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="4c84f-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="4c84f-113">Instalar dados de configuração</span><span class="sxs-lookup"><span data-stu-id="4c84f-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="4c84f-114">Baixe, desbloqueie e descompacte o [Pacote de dados de configuração](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="4c84f-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="4c84f-115">Navegue até a pasta descompactada e execute o arquivo executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="4c84f-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4c84f-116">Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migração de Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4c84f-118">Na página 2 do Assistente CMT, selecione **Microsoft 365** como o **Tipo de Implantação**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4c84f-119">Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4c84f-120">Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Entrar na configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4c84f-122">Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="4c84f-123">Na página 4, selecione o arquivo zip *SampleSetupAndConfigData* da pasta descompactada.</span><span class="sxs-lookup"><span data-stu-id="4c84f-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Seleção do arquivo zip](./media/3ZipFile.png)

![Selecionar um arquivo](./media/4SelectAFile.png)

9. <span data-ttu-id="4c84f-126">Depois que o arquivo zip for selecionado, selecione **Importar dados**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-126">After the zip file is selected, select **Import Data**.</span></span>

![Importar Dados](./media/5ImportData.png)

10. <span data-ttu-id="4c84f-128">A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="4c84f-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4c84f-129">Após a conclusão da importação, saia do Assistente do CMT.</span><span class="sxs-lookup"><span data-stu-id="4c84f-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4c84f-130">Verifique se há dados na sua organização nas 19 entidades a seguir:</span><span class="sxs-lookup"><span data-stu-id="4c84f-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="4c84f-131">Moeda</span><span class="sxs-lookup"><span data-stu-id="4c84f-131">Currency</span></span>
  - <span data-ttu-id="4c84f-132">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="4c84f-132">Organizational Unit</span></span>
  - <span data-ttu-id="4c84f-133">Contato</span><span class="sxs-lookup"><span data-stu-id="4c84f-133">Contact</span></span>
  - <span data-ttu-id="4c84f-134">Grupo de Impostos</span><span class="sxs-lookup"><span data-stu-id="4c84f-134">Tax Group</span></span>
  - <span data-ttu-id="4c84f-135">Grupo de Clientes</span><span class="sxs-lookup"><span data-stu-id="4c84f-135">Customer Group</span></span>
  - <span data-ttu-id="4c84f-136">Unidade</span><span class="sxs-lookup"><span data-stu-id="4c84f-136">Unit</span></span>
  - <span data-ttu-id="4c84f-137">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="4c84f-137">Unit Group</span></span>
  - <span data-ttu-id="4c84f-138">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="4c84f-138">Price List</span></span>
  - <span data-ttu-id="4c84f-139">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="4c84f-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="4c84f-140">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="4c84f-140">Invoice Frequency</span></span>
  - <span data-ttu-id="4c84f-141">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="4c84f-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="4c84f-142">Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="4c84f-142">Transaction Category</span></span>
  - <span data-ttu-id="4c84f-143">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="4c84f-143">Expense Category</span></span>
  - <span data-ttu-id="4c84f-144">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="4c84f-144">Role Price</span></span>
  - <span data-ttu-id="4c84f-145">Preço da Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="4c84f-145">Transaction Category Price</span></span>
  - <span data-ttu-id="4c84f-146">Característica</span><span class="sxs-lookup"><span data-stu-id="4c84f-146">Characteristic</span></span>
  - <span data-ttu-id="4c84f-147">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="4c84f-147">Bookable Resource</span></span>
  - <span data-ttu-id="4c84f-148">Associação de Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="4c84f-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="4c84f-149">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="4c84f-149">Bookable Resource Characteristic</span></span>

![Concluir Importação](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="4c84f-151">Atualizar configurações do Project Operations</span><span class="sxs-lookup"><span data-stu-id="4c84f-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="4c84f-152">Navegue até o ambiente CE.</span><span class="sxs-lookup"><span data-stu-id="4c84f-152">Navigate to the CE environment.</span></span> <span data-ttu-id="4c84f-153">Você pode encontrá-lo ao abrir o [Centro de Administração da Power Platform](https://admin.powerplatform.microsoft.com/environments), selecionar o ambiente e, em seguida, **Abrir Ambiente**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir Ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="4c84f-155">Acesse **Projetos** > **Recursos** e selecione **Novo** para criar um recurso reservável para seu usuário.</span><span class="sxs-lookup"><span data-stu-id="4c84f-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos Reserváveis](./media/8BookableResources.png)

3. <span data-ttu-id="4c84f-157">Na guia **Geral**, selecione seu usuário administrador.</span><span class="sxs-lookup"><span data-stu-id="4c84f-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="4c84f-158">Verifique se o fuso horário corresponde ao que você está.</span><span class="sxs-lookup"><span data-stu-id="4c84f-158">Verify that the time zone matches the one you are in.</span></span> 

![Novo Recurso Reservável](./media/9NewBookableResource.png)

4. <span data-ttu-id="4c84f-160">Na guia **Agendamento**, no campo **Empresa**, escolha a empresa **USPM** e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Guia Agendamento](./media/10SchedulingTab.png)

5. <span data-ttu-id="4c84f-162">Selecione a guia **Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-162">Select the **Work hours** tab.</span></span>  

![Horas de Trabalho](./media/11WorkHours.png)

6. <span data-ttu-id="4c84f-164">Clique duas vezes em qualquer valor no calendário e selecione **Editar** > **Todos os eventos da série**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendário de Atividades](./media/12WorkCalendar.png)

7. <span data-ttu-id="4c84f-166">Altere as horas de trabalho para um dia de trabalho de oito (8) horas, marque os finais de semana como dias não úteis e certifique-se de que o fuso horário corresponda ao seu.</span><span class="sxs-lookup"><span data-stu-id="4c84f-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="4c84f-167">Selecione **Salvar e fechar**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-167">Select **Save and close**.</span></span>

![Atualizar Calendário](./media/13UpdateCalendar.png)

9. <span data-ttu-id="4c84f-169">Acesse **Configurações** > **Modelos de calendário** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelos de Calendário](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="4c84f-171">Insira um nome, selecione o recurso do modelo que você criou e, em seguida, **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Salvar Modelo de Calendário](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="4c84f-173">Acesse **Parâmetros** e clique duas vezes no registro.</span><span class="sxs-lookup"><span data-stu-id="4c84f-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parâmetros do Projeto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="4c84f-175">Atualize os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="4c84f-175">Update the following fields:</span></span>

 - <span data-ttu-id="4c84f-176">**Empresa Padrão**: USPM</span><span class="sxs-lookup"><span data-stu-id="4c84f-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="4c84f-177">**Unidade Organizacional Padrão**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="4c84f-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="4c84f-178">**Frequência da Fatura**: sétimo e último dia</span><span class="sxs-lookup"><span data-stu-id="4c84f-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="4c84f-179">**Modelo de horas de trabalho**: altere para o modelo que você criou.</span><span class="sxs-lookup"><span data-stu-id="4c84f-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="4c84f-180">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="4c84f-180">Select **Save**.</span></span> 

![Atualizar Parâmetros do Projeto](./media/17UpdatedProjectParameters.png)
