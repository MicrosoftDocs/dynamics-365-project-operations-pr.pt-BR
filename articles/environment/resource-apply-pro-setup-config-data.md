---
title: Configurar e aplicar dados de configuração no Common Data Service para o Project Operations
description: Este tópico fornece informações sobre a configuração e aplicação de dados de configuração no Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948740"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="e5d62-103">Configurar e aplicar dados de configuração no Common Data Service para o Project Operations</span><span class="sxs-lookup"><span data-stu-id="e5d62-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="e5d62-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="e5d62-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="e5d62-105">Instalar dados de configuração</span><span class="sxs-lookup"><span data-stu-id="e5d62-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="e5d62-106">Baixe, desbloqueie e descompacte o [Pacote de dados de configuração](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="e5d62-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="e5d62-107">Navegue até a pasta descompactada e execute o arquivo executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="e5d62-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e5d62-108">Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migração de Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e5d62-110">Na página 2 do assistente CMT, selecione **Office 365** como **Tipo de implantação**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e5d62-111">Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e5d62-112">Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Entrar na configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e5d62-114">Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="e5d62-115">Na página 4, selecione o arquivo zip *SampleSetupAndConfigData* da pasta descompactada.</span><span class="sxs-lookup"><span data-stu-id="e5d62-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Seleção do arquivo zip](./media/3ZipFile.png)

![Selecionar um arquivo](./media/4SelectAFile.png)

9. <span data-ttu-id="e5d62-118">Depois que o arquivo zip for selecionado, selecione **Importar dados**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-118">After the zip file is selected, select **Import Data**.</span></span>

![Importar Dados](./media/5ImportData.png)

10. <span data-ttu-id="e5d62-120">A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="e5d62-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e5d62-121">Após a conclusão da importação, saia do Assistente do CMT.</span><span class="sxs-lookup"><span data-stu-id="e5d62-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e5d62-122">Verifique se há dados na sua organização nas 19 entidades a seguir:</span><span class="sxs-lookup"><span data-stu-id="e5d62-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="e5d62-123">Moeda</span><span class="sxs-lookup"><span data-stu-id="e5d62-123">Currency</span></span>
  - <span data-ttu-id="e5d62-124">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="e5d62-124">Organizational Unit</span></span>
  - <span data-ttu-id="e5d62-125">Contato</span><span class="sxs-lookup"><span data-stu-id="e5d62-125">Contact</span></span>
  - <span data-ttu-id="e5d62-126">Grupo de Impostos</span><span class="sxs-lookup"><span data-stu-id="e5d62-126">Tax Group</span></span>
  - <span data-ttu-id="e5d62-127">Grupo de Clientes</span><span class="sxs-lookup"><span data-stu-id="e5d62-127">Customer Group</span></span>
  - <span data-ttu-id="e5d62-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="e5d62-128">Unit</span></span>
  - <span data-ttu-id="e5d62-129">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="e5d62-129">Unit Group</span></span>
  - <span data-ttu-id="e5d62-130">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="e5d62-130">Price List</span></span>
  - <span data-ttu-id="e5d62-131">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="e5d62-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="e5d62-132">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="e5d62-132">Invoice Frequency</span></span>
  - <span data-ttu-id="e5d62-133">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="e5d62-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="e5d62-134">Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="e5d62-134">Transaction Category</span></span>
  - <span data-ttu-id="e5d62-135">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="e5d62-135">Expense Category</span></span>
  - <span data-ttu-id="e5d62-136">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="e5d62-136">Role Price</span></span>
  - <span data-ttu-id="e5d62-137">Preço da Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="e5d62-137">Transaction Category Price</span></span>
  - <span data-ttu-id="e5d62-138">Característica</span><span class="sxs-lookup"><span data-stu-id="e5d62-138">Characteristic</span></span>
  - <span data-ttu-id="e5d62-139">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="e5d62-139">Bookable Resource</span></span>
  - <span data-ttu-id="e5d62-140">Associação de Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="e5d62-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="e5d62-141">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="e5d62-141">Bookable Resource Characteristic</span></span>

![Concluir Importação](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="e5d62-143">Atualizar configurações do Project Operations</span><span class="sxs-lookup"><span data-stu-id="e5d62-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="e5d62-144">Navegue até o ambiente CE.</span><span class="sxs-lookup"><span data-stu-id="e5d62-144">Navigate to the CE environment.</span></span> <span data-ttu-id="e5d62-145">Você pode encontrá-lo ao abrir o [Centro de Administração da Power Platform](https://admin.powerplatform.microsoft.com/environments), selecionar o ambiente e, em seguida, **Abrir Ambiente**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir Ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="e5d62-147">Acesse **Projetos** > **Recursos** e selecione **Novo** para criar um recurso reservável para seu usuário.</span><span class="sxs-lookup"><span data-stu-id="e5d62-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos Reserváveis](./media/8BookableResources.png)

3. <span data-ttu-id="e5d62-149">Na guia **Geral**, selecione seu usuário administrador.</span><span class="sxs-lookup"><span data-stu-id="e5d62-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="e5d62-150">Verifique se o fuso horário corresponde ao que você está.</span><span class="sxs-lookup"><span data-stu-id="e5d62-150">Verify that the time zone matches the one you are in.</span></span> 

![Novo Recurso Reservável](./media/9NewBookableResource.png)

4. <span data-ttu-id="e5d62-152">Na guia **Agendamento**, no campo **Empresa**, escolha a empresa **USPM** e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Guia Agendamento](./media/10SchedulingTab.png)

5. <span data-ttu-id="e5d62-154">Selecione a guia **Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-154">Select the **Work hours** tab.</span></span>  

![Horas de Trabalho](./media/11WorkHours.png)

6. <span data-ttu-id="e5d62-156">Clique duas vezes em qualquer valor no calendário e selecione **Editar** > **Todos os eventos da série**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendário de Atividades](./media/12WorkCalendar.png)

7. <span data-ttu-id="e5d62-158">Altere as horas de trabalho para um dia de trabalho de oito (8) horas, marque os finais de semana como dias não úteis e certifique-se de que o fuso horário corresponda ao seu.</span><span class="sxs-lookup"><span data-stu-id="e5d62-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="e5d62-159">Selecione **Salvar e fechar**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-159">Select **Save and close**.</span></span>

![Atualizar Calendário](./media/13UpdateCalendar.png)

9. <span data-ttu-id="e5d62-161">Acesse **Configurações** > **Modelos de calendário** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelos de Calendário](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="e5d62-163">Insira um nome, selecione o recurso do modelo que você criou e, em seguida, **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Salvar Modelo de Calendário](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="e5d62-165">Acesse **Parâmetros** e clique duas vezes no registro.</span><span class="sxs-lookup"><span data-stu-id="e5d62-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parâmetros do Projeto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="e5d62-167">Atualize os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="e5d62-167">Update the following fields:</span></span>

 - <span data-ttu-id="e5d62-168">**Empresa Padrão**: USPM</span><span class="sxs-lookup"><span data-stu-id="e5d62-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="e5d62-169">**Unidade Organizacional Padrão**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="e5d62-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="e5d62-170">**Frequência da Fatura**: sétimo e último dia</span><span class="sxs-lookup"><span data-stu-id="e5d62-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="e5d62-171">**Modelo de horas de trabalho**: altere para o modelo que você criou.</span><span class="sxs-lookup"><span data-stu-id="e5d62-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="e5d62-172">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-172">Select **Save**.</span></span> 

![Atualizar Parâmetros do Projeto](./media/17UpdatedProjectParameters.png)
