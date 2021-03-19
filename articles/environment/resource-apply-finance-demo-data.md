---
title: Aplicar dados de demonstração a um ambiente hospedado na nuvem do Finance
description: Este tópico explica como aplicar dados de demonstração do Project Operations a ambientes hospedados na nuvem do Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7239301dc8b775dc4a53a1cf6c0bcba3956125a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289850"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="6dcc1-103">Aplicar dados de demonstração a um ambiente hospedado na nuvem do Finance</span><span class="sxs-lookup"><span data-stu-id="6dcc1-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="6dcc1-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="6dcc1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6dcc1-105">Este tópico é aplicável apenas ao Microsoft Dynamics 365 Finance versão 10.0.13 e pode ser executado apenas em um ambiente hospedado na nuvem.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="6dcc1-106">Conclua as etapas neste tópico **ANTES** de aplicar atualizações de qualidade ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="6dcc1-107">Em seu projeto do LCS, abra a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="6dcc1-108">Observe que ela inclui os detalhes necessários para se conectar ao ambiente usando o protocolo RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="6dcc1-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Detalhes do ambiente do ](./media/1EnvironmentDetails.png)

<span data-ttu-id="6dcc1-110">O primeiro conjunto de credenciais destacadas são as credenciais da conta local e contém um hiperlink para a conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="6dcc1-111">As credenciais incluem o nome de usuário e a senha do administrador do ambiente.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="6dcc1-112">O segundo conjunto de credenciais é usado para fazer logon no SQL Server neste ambiente.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="6dcc1-113">Faça conexão remota ao ambiente pelo hiperlink em **Contas locais** e use as **Credenciais da conta local** para autenticar.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="6dcc1-114">Acesse **Serviços de Informação da Internet** > **Pools de Aplicativos** > **AOSService** e interrompa o serviço.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="6dcc1-115">Você está interrompendo o serviço neste ponto para que possa continuar a substituir o Banco de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Interromper o AOS](./media/2StopAOS.png)

4. <span data-ttu-id="6dcc1-117">Acesse **Serviços** e interrompa os dois itens a seguir:</span><span class="sxs-lookup"><span data-stu-id="6dcc1-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="6dcc1-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span><span class="sxs-lookup"><span data-stu-id="6dcc1-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="6dcc1-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span><span class="sxs-lookup"><span data-stu-id="6dcc1-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Interromper Serviços](./media/3StopServices.png)

5. <span data-ttu-id="6dcc1-121">Abra o Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="6dcc1-122">Faça logon com as credenciais do servidor SQL e use o usuário administrador axdb e a senha da página **Detalhes de ambientes** do LCS.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="6dcc1-124">No Explorador de Objetos, **Banco de dados** e localize **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="6dcc1-125">Você substituirá o banco de dados por um novo banco de dados localizado no [Centro de Download](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="6dcc1-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="6dcc1-126">Copie o arquivo zip para a VM em que você está conectado remotamente e extraia o conteúdo do zip.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="6dcc1-127">No SQL Server Management Studio, clique com o botão direito do mouse em **AxDB** e selecione **Tarefas** > **Restaurar** > **Banco de Dados**.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Restaurar banco de dados](./media/5RestoreDatabase.png)

9. <span data-ttu-id="6dcc1-129">Selecione **Dispositivo de Origem** e navegue até o arquivo extraído do zip que você copiou.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Dispositivos de Origem](./media/6SourceDevice.png)

10. <span data-ttu-id="6dcc1-131">Selecione **Opções** e, em seguida, **Substituir o banco de dados existente** e **Fechar conexões existentes para o banco de dados de destino**.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="6dcc1-132">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-132">Select **OK**.</span></span>

![Restaurar Configurações](./media/7RestoreSetting.png)

<span data-ttu-id="6dcc1-134">Você receberá a confirmação de que a restauração do AXDB foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="6dcc1-135">Depois de receber essa confirmação, você poderá fechar o SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="6dcc1-136">Acesse novamente **Serviços de Informação da Internet** > **Pools de Aplicativos** > **AOSService** e inicie o AOSService.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="6dcc1-137">Acesse **Serviços** e inicie os dois serviços interrompidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="6dcc1-138">Localize a ferramenta AdminUserProvisioning nesta VM.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="6dcc1-139">Procure em: K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="6dcc1-140">Execute o arquivo .ext usando seu endereço de usuário no campo **Endereço de email**.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="6dcc1-141">Selecione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-141">Select **Submit**.</span></span>

![Provisionamento de Usuário Administrador](./media/8AdminUserProvisioning.png)

<span data-ttu-id="6dcc1-143">Isso pode levar alguns minutos para ser concluído.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="6dcc1-144">Você deverá receber uma mensagem de confirmação de que o usuário administrador foi atualizado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="6dcc1-145">Por último, execute o Prompt de Comando como administrador e execute iisreset</span><span class="sxs-lookup"><span data-stu-id="6dcc1-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Redefinição do IIS](./media/9IISReset.png)

18. <span data-ttu-id="6dcc1-147">Feche a sessão da área de trabalho remota e use a página **Detalhes do ambiente** do LCS para fazer logon no ambiente para confirmar se ele está funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="6dcc1-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]