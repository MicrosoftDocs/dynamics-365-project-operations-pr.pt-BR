---
title: Configurar e aplicar dados de configuração no Common Data Service
description: Este tópico fornece informações sobre a configuração e aplicação de dados de configuração no Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001277"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="7d6f1-103">Configurar e aplicar dados de configuração no Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7d6f1-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="7d6f1-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="7d6f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="7d6f1-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7d6f1-105">Prerequisites</span></span>

<span data-ttu-id="7d6f1-106">Antes de começar a configurar os dados no Common Data Service (CDS), os seguintes pré-requisitos devem ser atendidos:</span><span class="sxs-lookup"><span data-stu-id="7d6f1-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="7d6f1-107">Provisione um ambiente CDS e um ambiente do Dynamics 365 Finance para o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="7d6f1-108">As informações de pessoa jurídica do Dynamics 365 Finance são compartilhadas no ambiente CDS.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="7d6f1-109">Isso significa que a entidade **Empresa** no CDS tem os seguintes registros da empresa:</span><span class="sxs-lookup"><span data-stu-id="7d6f1-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="7d6f1-110">THPM</span><span class="sxs-lookup"><span data-stu-id="7d6f1-110">THPM</span></span>
  - <span data-ttu-id="7d6f1-111">USPM</span><span class="sxs-lookup"><span data-stu-id="7d6f1-111">USPM</span></span>
  - <span data-ttu-id="7d6f1-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="7d6f1-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="7d6f1-113">Instalar dados de configuração</span><span class="sxs-lookup"><span data-stu-id="7d6f1-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="7d6f1-114">Baixe, desbloqueie e descompacte o [Pacote de dados de configuração](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="7d6f1-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="7d6f1-115">Navegue até a pasta descompactada e execute o arquivo executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7d6f1-116">Na página 1 do Assistente de migração de configuração (CMT) do Common Data Service, selecione **Importar dados** e então selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migração de Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7d6f1-118">Na página 2 do Assistente CMT, selecione **Microsoft 365** como o **Tipo de Implantação**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7d6f1-119">Marque as caixas de seleção **Exibir uma lista de organizações disponíveis** e **Mostrar avançado**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7d6f1-120">Selecione a região do seu locatário, insira suas credenciais e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Entrar na configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7d6f1-122">Na página 3, na lista de organizações no locatário, selecione a organização para a qual deseja importar os dados de demonstração e selecione **Logon**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="7d6f1-123">Na página 4, selecione o arquivo zip *SampleSetupAndConfigData* da pasta descompactada.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Seleção do arquivo zip](./media/3ZipFile.png)

![Selecionar um arquivo](./media/4SelectAFile.png)

9. <span data-ttu-id="7d6f1-126">Depois que o arquivo zip for selecionado, selecione **Importar dados**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-126">After the zip file is selected, select **Import Data**.</span></span>

![Importar Dados](./media/5ImportData.png)

10. <span data-ttu-id="7d6f1-128">A importação será executada por aproximadamente dois a dez minutos, dependendo da velocidade da rede.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7d6f1-129">Após a conclusão da importação, saia do Assistente do CMT.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7d6f1-130">Verifique se há dados na sua organização nas 26 entidades a seguir:</span><span class="sxs-lookup"><span data-stu-id="7d6f1-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="7d6f1-131">Moeda</span><span class="sxs-lookup"><span data-stu-id="7d6f1-131">Currency</span></span>
  - <span data-ttu-id="7d6f1-132">Plano de Contas</span><span class="sxs-lookup"><span data-stu-id="7d6f1-132">Chart of Accounts</span></span>
  - <span data-ttu-id="7d6f1-133">Calendário fiscal</span><span class="sxs-lookup"><span data-stu-id="7d6f1-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="7d6f1-134">Tipos de Taxa de Câmbio da Moeda</span><span class="sxs-lookup"><span data-stu-id="7d6f1-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="7d6f1-135">Dia do Pagamento</span><span class="sxs-lookup"><span data-stu-id="7d6f1-135">Payment Day</span></span>
  - <span data-ttu-id="7d6f1-136">Agenda de Pagamento</span><span class="sxs-lookup"><span data-stu-id="7d6f1-136">Payment Schedule</span></span>
  - <span data-ttu-id="7d6f1-137">Condição de Pagamento</span><span class="sxs-lookup"><span data-stu-id="7d6f1-137">Payment Term</span></span>
  - <span data-ttu-id="7d6f1-138">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="7d6f1-138">Organizational Unit</span></span>
  - <span data-ttu-id="7d6f1-139">Contato</span><span class="sxs-lookup"><span data-stu-id="7d6f1-139">Contact</span></span>
  - <span data-ttu-id="7d6f1-140">Grupo tributário</span><span class="sxs-lookup"><span data-stu-id="7d6f1-140">Tax Group</span></span>
  - <span data-ttu-id="7d6f1-141">Grupo de Clientes</span><span class="sxs-lookup"><span data-stu-id="7d6f1-141">Customer Group</span></span>
  - <span data-ttu-id="7d6f1-142">Grupo de Fornecedores</span><span class="sxs-lookup"><span data-stu-id="7d6f1-142">Vendor Group</span></span>
  - <span data-ttu-id="7d6f1-143">Unidade</span><span class="sxs-lookup"><span data-stu-id="7d6f1-143">Unit</span></span>
  - <span data-ttu-id="7d6f1-144">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="7d6f1-144">Unit Group</span></span>
  - <span data-ttu-id="7d6f1-145">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="7d6f1-145">Price List</span></span>
  - <span data-ttu-id="7d6f1-146">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="7d6f1-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="7d6f1-147">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="7d6f1-147">Invoice Frequency</span></span>
  - <span data-ttu-id="7d6f1-148">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="7d6f1-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="7d6f1-149">Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="7d6f1-149">Transaction Category</span></span>
  - <span data-ttu-id="7d6f1-150">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="7d6f1-150">Expense Category</span></span>
  - <span data-ttu-id="7d6f1-151">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="7d6f1-151">Role Price</span></span>
  - <span data-ttu-id="7d6f1-152">Preço da Categoria da Transação</span><span class="sxs-lookup"><span data-stu-id="7d6f1-152">Transaction Category Price</span></span>
  - <span data-ttu-id="7d6f1-153">Característica</span><span class="sxs-lookup"><span data-stu-id="7d6f1-153">Characteristic</span></span>
  - <span data-ttu-id="7d6f1-154">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="7d6f1-154">Bookable Resource</span></span>
  - <span data-ttu-id="7d6f1-155">Associação de Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="7d6f1-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="7d6f1-156">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="7d6f1-156">Bookable Resource Characteristic</span></span>

![Concluir Importação](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="7d6f1-158">Atualizar configurações do Project Operations</span><span class="sxs-lookup"><span data-stu-id="7d6f1-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="7d6f1-159">Navegue até o ambiente CE.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-159">Navigate to the CE environment.</span></span> <span data-ttu-id="7d6f1-160">Você pode encontrá-lo ao abrir o [Centro de Administração da Power Platform](https://admin.powerplatform.microsoft.com/environments), selecionar o ambiente e, em seguida, **Abrir Ambiente**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir Ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="7d6f1-162">Acesse **Projetos** > **Recursos** e selecione **Novo** para criar um recurso reservável para seu usuário.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos Reserváveis](./media/8BookableResources.png)

3. <span data-ttu-id="7d6f1-164">Na guia **Geral**, selecione seu usuário administrador.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="7d6f1-165">Verifique se o fuso horário corresponde ao que você está.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-165">Verify that the time zone matches the one you are in.</span></span> 

![Novo Recurso Reservável](./media/9NewBookableResource.png)

4. <span data-ttu-id="7d6f1-167">Na guia **Agendamento**, no campo **Empresa**, escolha a empresa **USPM** e selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Guia Agendamento](./media/10SchedulingTab.png)

5. <span data-ttu-id="7d6f1-169">Selecione a guia **Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-169">Select the **Work hours** tab.</span></span>  

![Horas de Trabalho](./media/11WorkHours.png)

6. <span data-ttu-id="7d6f1-171">Clique duas vezes em qualquer valor no calendário e selecione **Editar** > **Todos os eventos da série**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendário de Atividades](./media/12WorkCalendar.png)

7. <span data-ttu-id="7d6f1-173">Altere as horas de trabalho para um dia de trabalho de oito (8) horas, marque os finais de semana como dias não úteis e certifique-se de que o fuso horário corresponda ao seu.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="7d6f1-174">Selecione **Salvar e fechar**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-174">Select **Save and close**.</span></span>

![Atualizar Calendário](./media/13UpdateCalendar.png)

9. <span data-ttu-id="7d6f1-176">Acesse **Configurações** > **Modelos de calendário** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelos de Calendário](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="7d6f1-178">Insira um nome, selecione o recurso do modelo que você criou e, em seguida, **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Salvar Modelo de Calendário](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="7d6f1-180">Acesse **Parâmetros** e clique duas vezes no registro.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parâmetros do Projeto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="7d6f1-182">Atualize os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="7d6f1-182">Update the following fields:</span></span>

 - <span data-ttu-id="7d6f1-183">**Empresa Padrão**: USPM</span><span class="sxs-lookup"><span data-stu-id="7d6f1-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="7d6f1-184">**Unidade Organizacional Padrão**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="7d6f1-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="7d6f1-185">**Frequência da Fatura**: sétimo e último dia</span><span class="sxs-lookup"><span data-stu-id="7d6f1-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="7d6f1-186">**Modelo de horas de trabalho**: altere para o modelo que você criou.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="7d6f1-187">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="7d6f1-187">Select **Save**.</span></span> 

![Atualizar Parâmetros do Projeto](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
