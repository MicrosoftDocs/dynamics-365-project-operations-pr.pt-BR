---
title: Instalação de dados de exemplo
description: Este tópico fornece informações sobre a instalação de dados de exemplo no Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: c521fb4000b4856fc5c2fbf3275bf3b3e0dfa458
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950565"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="cdd58-103">Instalação de dados de exemplo para aplicação do Project Service</span><span class="sxs-lookup"><span data-stu-id="cdd58-103">Sample data installation for the Project Service application</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cdd58-104">Para ajudar você a criar seus próprios ambientes de demonstração, a Microsoft fornece pacotes de dados de exemplo baixáveis que demonstram as funcionalidades dos seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="cdd58-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="cdd58-105">Há dois tipos de pacotes de dados de exemplo:</span><span class="sxs-lookup"><span data-stu-id="cdd58-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="cdd58-106">referência/dados de configuração</span><span class="sxs-lookup"><span data-stu-id="cdd58-106">reference/setup data</span></span>
- <span data-ttu-id="cdd58-107">dados demonstrativos (referência/configuração e dados transacionais, como ordens de serviço e projetos)</span><span class="sxs-lookup"><span data-stu-id="cdd58-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="cdd58-108">Os pacotes de dados **referência** de amostra em três pacotes diferentes, para que você possa instalar apenas dados do Project Service, ou apenas para Field Service, ou você pode instalar dados de exemplo para ambas aplicações de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="cdd58-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="cdd58-109">Os pacotes de dados de referência/configuração de amostra são:</span><span class="sxs-lookup"><span data-stu-id="cdd58-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="cdd58-110">**V902PSMasterData** - Apenas para a versão 3.x do Project Service</span><span class="sxs-lookup"><span data-stu-id="cdd58-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="cdd58-111">**V902FSMasterData** - Apenas para a versão 8.x do Field Service</span><span class="sxs-lookup"><span data-stu-id="cdd58-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="cdd58-112">**V902FPSMasterData** - Field Service 8.x e Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="cdd58-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="cdd58-113">O pacote de dados de **demonstração** mais recentes é:</span><span class="sxs-lookup"><span data-stu-id="cdd58-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="cdd58-114">**FPSDemoData** - Field Service 8.x e Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="cdd58-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="cdd58-115">Instalação e instruções diferem levemente nos usuários para criar e configurar a seção, mas o resto é o mesmo que na [**postagem de blog**](https://aka.ms/fpsdemodatablog) anterior.</span><span class="sxs-lookup"><span data-stu-id="cdd58-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="cdd58-116">Este pacote apresenta um conjunto de dados de demonstração reduzido e leva aproximadamente 3 horas para ser instalado.</span><span class="sxs-lookup"><span data-stu-id="cdd58-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="cdd58-117">Esses pacotes de dados de exemplo estão disponíveis apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="cdd58-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdd58-118">**Não é possível desinstalar os dados de exemplo.**</span><span class="sxs-lookup"><span data-stu-id="cdd58-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="cdd58-119">Você só deve instalar esses pacotes na demonstração, avaliação, treinamento ou sistemas de teste.</span><span class="sxs-lookup"><span data-stu-id="cdd58-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="cdd58-120">Observe também que não é possível instalar um pacote individual e depois instalar o outro pacote individual.</span><span class="sxs-lookup"><span data-stu-id="cdd58-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="cdd58-121">(Ou seja, você não pode instalar **FSMasterData** seguido por **PSMasterData**, ou vice-versa.) Se você precisar de dados de exemplo para ambas aplicações a qualquer momento no futuro, você deve instalar o pacote **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="cdd58-122">Ao instalar os pacotes de dados de exemplo, o processo de instalação realiza as ações a seguir:</span><span class="sxs-lookup"><span data-stu-id="cdd58-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="cdd58-123">Cria ou defina-o como parâmetros o para usar o Project Service, Field Service, ou ambos aplicativos (se aplicável).</span><span class="sxs-lookup"><span data-stu-id="cdd58-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="cdd58-124">Importa amostras de dados das aplicações, como recursos agendáveis, funções específicas de aplicação, vendas e listas de preço de venda, unidades organizacionais, registros de processos de venda e outras entidades para demonstrar funcionalidades chave.</span><span class="sxs-lookup"><span data-stu-id="cdd58-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="cdd58-125">Com o pacote **dados de demonstração**, você recebe os dados acima e transacional adicionar, como ordens de serviço e projetos.</span><span class="sxs-lookup"><span data-stu-id="cdd58-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="cdd58-126">Quer saber quais habilidades você pode experimentar com os dados de exemplo?</span><span class="sxs-lookup"><span data-stu-id="cdd58-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="cdd58-127">Consulte o cenário fictício do Fabrikam Robotics em [Notas técnicas](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="cdd58-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="cdd58-128">Se você tiver dúvidas sobre como instalar esses pacotes de dados de exemplo, [envie um e-mail para fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="cdd58-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd58-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdd58-129">Requirements</span></span>

<span data-ttu-id="cdd58-130">O protocolo de instalação usa o seguinte sobre sua instância de destino (org):</span><span class="sxs-lookup"><span data-stu-id="cdd58-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="cdd58-131">O idioma base é inglês e a moeda base é dólar americano (USD, $)</span><span class="sxs-lookup"><span data-stu-id="cdd58-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="cdd58-132">A organização não tem dados de Project Service ou Field Service prontos, ou tem apenas a base de dados padrão que vem com qualquer organização.</span><span class="sxs-lookup"><span data-stu-id="cdd58-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="cdd58-133">A versão correta da aplicação empresarial já está instalada:</span><span class="sxs-lookup"><span data-stu-id="cdd58-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="cdd58-134">**For FPSDemoData or v902FPSMasterData:** A org tem Field Service versão 8.x e Project Service versão 3.x instalados.</span><span class="sxs-lookup"><span data-stu-id="cdd58-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="cdd58-135">**For v902PSMasterData:** A org tem Project Service versão 3.x instalada.</span><span class="sxs-lookup"><span data-stu-id="cdd58-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="cdd58-136">**For v902FSMasterData:** A org tem Field Service versão 8.x instalada.</span><span class="sxs-lookup"><span data-stu-id="cdd58-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="cdd58-137">Se precisar instalar dados de exemplo em um ambiente de teste ou demonstração de Project Service e Field Service existente que já tem dados (não recomendado), você precisará suspender as pré-verificações de segurança realizadas pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="cdd58-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="cdd58-138">Para obter mais informações, consulte as notas técnicas abaixo.</span><span class="sxs-lookup"><span data-stu-id="cdd58-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="cdd58-139">Prepare para a instalação</span><span class="sxs-lookup"><span data-stu-id="cdd58-139">Prepare for installation</span></span>

<span data-ttu-id="cdd58-140">Você precisa executar o instalador em um computador com uma versão recente do Windows (Windows 10 de preferência).</span><span class="sxs-lookup"><span data-stu-id="cdd58-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="cdd58-141">Você deve planejar para o computador permanecer conectado a uma rede e para a instalação para executar até **1 hora** para **configuração/dados de referência**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="cdd58-142">(Geralmente, a instalação leva cerca de 30 minutos para **FPSMasterData**, que inclui dados de amostra para ambos aplicativos.) Para **FPSDemoData**, a instalação levará cerca de **3 horas**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-142">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="cdd58-143">O computador deve ter a função de salvar tela desativada.</span><span class="sxs-lookup"><span data-stu-id="cdd58-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="cdd58-144">Caso contrário, as credenciais de sessão da instalação podem ser perdidas quando a função de salvar tela entrar (a menos que você mantenha sua sessão ativa por todo o tempo).</span><span class="sxs-lookup"><span data-stu-id="cdd58-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="cdd58-145">![Captura de tela das configurações da função de salvar tela, com função de salvar tela desativada](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="cdd58-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="cdd58-146">Baixar e tirar da compactação</span><span class="sxs-lookup"><span data-stu-id="cdd58-146">Download and unpack</span></span>

<span data-ttu-id="cdd58-147">O instalador de Project Service e Field Service é distribuído como um executável com extração automática.</span><span class="sxs-lookup"><span data-stu-id="cdd58-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="cdd58-148">Os nomes de arquivo podem variar dependendo do pacote de dados de exemplo, mas caso contrário, as etapas são as mesmas não importa que pacote você instale.</span><span class="sxs-lookup"><span data-stu-id="cdd58-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="cdd58-149">Depois de baixar um pacote, execute o arquivo .exe e depois aceite os termos e condições para descompactar o arquivo .zip compactado.</span><span class="sxs-lookup"><span data-stu-id="cdd58-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="cdd58-150">Em seguida, você precisa extrair conteúdos desse arquivo ou pasta no computador.</span><span class="sxs-lookup"><span data-stu-id="cdd58-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="cdd58-151">Dependendo do sistema operacional e das configurações de segurança, é preciso realizar as seguintes etapas depois de descompactar o arquivo .zip:</span><span class="sxs-lookup"><span data-stu-id="cdd58-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="cdd58-152">Encontre e clique com o botão direito no arquivo **FPSDemoData.dll** na pasta **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="cdd58-153">Escolha **Desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="cdd58-154">Selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-154">Select **Apply**.</span></span>

4. <span data-ttu-id="cdd58-155">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="cdd58-156">Criar ou configurar usuários</span><span class="sxs-lookup"><span data-stu-id="cdd58-156">Create or configure users</span></span>

<span data-ttu-id="cdd58-157">O pacote **FPSDemoData** requer que seis usuários, enquanto **FPSMasterData** requer um.</span><span class="sxs-lookup"><span data-stu-id="cdd58-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="cdd58-158">Consulte o correto para obter seu pacote de dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="cdd58-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="cdd58-159">Criar ou configurar usuários - configuração/pacotes de dados de referência</span><span class="sxs-lookup"><span data-stu-id="cdd58-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="cdd58-160">O pacote **FPSMasterData** é criado para instalar com um usuário nomeado Spencer Low com as configurações descritas assim.</span><span class="sxs-lookup"><span data-stu-id="cdd58-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="cdd58-161">Para instalar o pacote corretamente, você precisa criar (ou temporariamente renomear) usuários em seu ambiente para combinar a configuração de dados de exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="cdd58-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="cdd58-162">Para criar ou configurar usuários, vá para **Configurações** > **Segurança** > **Usuários**, e faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cdd58-162">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="cdd58-163">Defina UserFullname="Spencer Low" com nome de usuário "spencerl" (**caixa baixa**) para as funções de Gerente de projeto e Gerente de prática.</span><span class="sxs-lookup"><span data-stu-id="cdd58-163">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="cdd58-164">Selecione o usuário **Spencer Low**, e depois selecione **Gerenciar funções**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="cdd58-165">Localize e selecione a função **Administrador do sistema**, e depois selecione **OK** para conceder direitos de administrador para Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="cdd58-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="cdd58-166">Essa etapa é necessária para garantir que os registros de amostra sejam criados com a propriedade de usuário correte e popule as exibições corretamente.</span><span class="sxs-lookup"><span data-stu-id="cdd58-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="cdd58-167">No pacote de download, você precisa atualizar o arquivo de mapeamento de dados com endereços de e-mail do contexto de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="cdd58-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="cdd58-168">Para fazer isso, abra **PkgFolder**, encontre o arquivo **ImportUserMapFile.xml** e abra-o no Bloco de Notas (ou Visual Studio, ou outro editor de XML).</span><span class="sxs-lookup"><span data-stu-id="cdd58-168">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="cdd58-169">Defina o campo **DefaultUserToMapTo=** do endereço de e-mail do usuário Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="cdd58-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="cdd58-170">Se você não estiver usando o Spencer Low com o nome de usuário **spencerl**, você precisa atualizar um arquivo adicional.</span><span class="sxs-lookup"><span data-stu-id="cdd58-170">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="cdd58-171">Abra o arquivo **DemoDataPreImportConfig.xml**, e depois encontre a tag **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="cdd58-172">Atualize a marca **\<login\>** com o nome de usuário de seu usuário Marcelo Santos.</span><span class="sxs-lookup"><span data-stu-id="cdd58-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="cdd58-173">Para detalhes adicionais, consulte [Notas técnicas](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="cdd58-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="cdd58-174">Criar ou configurar usuários - pacote de dados de demonstração</span><span class="sxs-lookup"><span data-stu-id="cdd58-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="cdd58-175">O pacote de dados demonstrativos requer seis usuários.</span><span class="sxs-lookup"><span data-stu-id="cdd58-175">The demo data package requires six users.</span></span> <span data-ttu-id="cdd58-176">Para o pacote instalar corretamente, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cdd58-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="cdd58-177">Criar ou renomear temporariamente usuários existentes para combinar configuração de dados de exemplo de entrada acessando **Configurações** > **Segurança** > **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="cdd58-178">Essas funções só são necessárias para demonstrações baseadas em identidade.</span><span class="sxs-lookup"><span data-stu-id="cdd58-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="cdd58-179">Nome completo do usuário = "David So" como técnico do Field Service</span><span class="sxs-lookup"><span data-stu-id="cdd58-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="cdd58-180">Usuário Fullname="Jamie Reding" como Customer Service & Field Service Dispatcher</span><span class="sxs-lookup"><span data-stu-id="cdd58-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="cdd58-181">Usuário Fullname="Molly Clark" como Account Manager</span><span class="sxs-lookup"><span data-stu-id="cdd58-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="cdd58-182">Usuário Fullname="Spencer Low" como Practice and Project Manager</span><span class="sxs-lookup"><span data-stu-id="cdd58-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="cdd58-183">Usuário Fullname="Veronica Quek" como Team Member</span><span class="sxs-lookup"><span data-stu-id="cdd58-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="cdd58-184">User Fullname="William Contoso"</span><span class="sxs-lookup"><span data-stu-id="cdd58-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="cdd58-185">Para fins de importação de demonstração de dados, atribuir os seis usuários acima a função de administrador para que registros de amostra sejam importados corretamente.</span><span class="sxs-lookup"><span data-stu-id="cdd58-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="cdd58-186">Abra **PkgFolder** e depois encontre e abra **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="cdd58-187">Atualize os campos **New=** dos endereços de e-mail de Usuários correspondentes em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="cdd58-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cdd58-188">![Captura de tela do UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="cdd58-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="cdd58-189">Se seu nome completo de usuário "Spencer Low" tiver um ID de usuário diferente de **"spencerl"**, então você precisa atualizar um arquivo adicional.</span><span class="sxs-lookup"><span data-stu-id="cdd58-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="cdd58-190">Abra **DemoDataPreImportConfig.xml**, e encontre a tag **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="cdd58-191">Atualize a marca **\<login\>** com a loginId (diferencia maiúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="cdd58-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="cdd58-192">O primeiro calendário de usuário (na tag **userstocreateandconfigure**) é usado para popular as horas de trabalho de todos recursos agendáveis na importação de dados de demonstração.</span><span class="sxs-lookup"><span data-stu-id="cdd58-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="cdd58-193">Navegue até **Configurações** > **Segurança** > **Usuários**, encontre seu usuário "Spencer Low", e abra a opção "Horas de trabalho".</span><span class="sxs-lookup"><span data-stu-id="cdd58-193">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="cdd58-194">Edite as horas de trabalho existentes, selecionando a opção **Programa semanal recorrente completo do início ao fim**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="cdd58-195">Verifique se **Horas de trabalho estão definidas para 8 AM - 5 PM (9 Horas), segunda-feira a sexta-feira e com o fuso horário definido como Hora do Pacífico (EUA e Canadá)**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="cdd58-196">Isso é necessário para garantir que o painel de Projeto e agenda esteja como esperado.</span><span class="sxs-lookup"><span data-stu-id="cdd58-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="cdd58-197">**Recomendação:** Considere criar um backup de seu org agora, caso você precise reverter seu ponto de início caso algo dê errado durante a instalação de dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="cdd58-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="cdd58-198">Para mais informações, consulte [Backup e restaurar instâncias](/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="cdd58-198">For more information, see [Backup and restore instances](/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="cdd58-199">Executar o Package Deployer</span><span class="sxs-lookup"><span data-stu-id="cdd58-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="cdd58-200">Localize e execute **PackageDeployer.exe** na pasta **v902FPSMasterData** OU **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="cdd58-201">Aceite os termos e condições.</span><span class="sxs-lookup"><span data-stu-id="cdd58-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="cdd58-202">Na próxima janela:</span><span class="sxs-lookup"><span data-stu-id="cdd58-202">On the next window:</span></span>

   <span data-ttu-id="cdd58-203">a.</span><span class="sxs-lookup"><span data-stu-id="cdd58-203">a.</span></span> <span data-ttu-id="cdd58-204">Selecione o tipo de implantação do **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="cdd58-205">b.</span><span class="sxs-lookup"><span data-stu-id="cdd58-205">b.</span></span> <span data-ttu-id="cdd58-206">Use o usuário e a senha do usuário de administrador do sistema configurada em "Criar ou configurar usuários" ("Spencer Low" com nome de usuário "spencerl").</span><span class="sxs-lookup"><span data-stu-id="cdd58-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="cdd58-207">c.</span><span class="sxs-lookup"><span data-stu-id="cdd58-207">c.</span></span> <span data-ttu-id="cdd58-208">Selecione a opção **Exibir lista de organizações disponíveis**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="cdd58-209">![Captura de tela da janela Package Deployer com "Lista de exibição de organizações disponíveis" selecionada](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="cdd58-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="cdd58-210">Selecione a organização onde deseja instalar os dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="cdd58-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="cdd58-211">Selecione **Avançar** até ver a caixa de **Configuração de dados demonstrativos**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cdd58-212">![Captura de tela da janela de status do instalador de dados de demonstração](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="cdd58-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="cdd58-213">Antes de prosseguir, lembre-se que instalar dados de exemplo pode levar até uma hora (normalmente ~10 minutos).</span><span class="sxs-lookup"><span data-stu-id="cdd58-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="cdd58-214">Você precisará garantir que o computador permanecerá ligado e conectado a uma rede durante todo o processo de instalação e que sua sessão se mantenha ativa.</span><span class="sxs-lookup"><span data-stu-id="cdd58-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="cdd58-215">Quando estiver pronto, clique em **Avançar** para iniciar o processo de instalação dos dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="cdd58-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="cdd58-216">Depois que os dados de exemplo são carregados, clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="cdd58-217">Verifique a instalação de dados de exemplo</span><span class="sxs-lookup"><span data-stu-id="cdd58-217">Verify the sample data installation</span></span>

<span data-ttu-id="cdd58-218">Para garantir, verifique se o número de registros e tipos de entidades listados no cenário fictício Fabrikam Robotics aparece como esperado.</span><span class="sxs-lookup"><span data-stu-id="cdd58-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="cdd58-219">Depois que os dados de exemplo carregarem por completo, entre como o usuário Spencer Low e confirme o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cdd58-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="cdd58-220">Se o aplicativo Project Service estiver instalado, acesse **Project Service** > **Configurações** > **Listas de preço**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="cdd58-221">Confirmar as taxas de conta e custos de taxas existentes, com a moeda apropriada, para cada país/região no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="cdd58-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="cdd58-222">Se o aplicativo Project Service estiver instalado, acesse **Universal Resource Scheduling** > **Configurações** > **Unidades Organizacionais**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="cdd58-223">Confirme se a lista de preços com a moeda apropriada foi associado com cada unidade org (excluindo entradas de cidade).</span><span class="sxs-lookup"><span data-stu-id="cdd58-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="cdd58-224">Se estiver faltando algum, encontre e associe a lista de preços correta.</span><span class="sxs-lookup"><span data-stu-id="cdd58-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="cdd58-225">Se o aplicativo Field Service estiver instalado, acesse **Project Service** > **Configurações** > **Listas de preço**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="cdd58-226">Confirme que taxas de conta e custos existem.</span><span class="sxs-lookup"><span data-stu-id="cdd58-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="cdd58-227">Acesse **Field Service** > **Configurações** > **Listas de preço** e verifique as taxas de conta e custos de taxas existentes, com a moeda apropriada, para cada país/região no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="cdd58-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="cdd58-228">![Captura de tela das listas de preço ativas](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="cdd58-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="cdd58-229">![Captura de tela de unidades organizacionais ativas](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="cdd58-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="cdd58-230">Notas técnicas</span><span class="sxs-lookup"><span data-stu-id="cdd58-230">Technical notes</span></span>

<span data-ttu-id="cdd58-231">Veja abaixo para obter detalhes técnicos sobre a instalação desses dados.</span><span class="sxs-lookup"><span data-stu-id="cdd58-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="cdd58-232">Instalar dados de exemplo nos dados existentes (não recomendados)</span><span class="sxs-lookup"><span data-stu-id="cdd58-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="cdd58-233">Se precisar instalar dados de exemplo em um ambiente de teste ou demonstração de Field Service ou Project Service existente que já tem dados, você precisará suspender as pré-verificações de segurança realizadas pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="cdd58-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="cdd58-234">Para fazer isso, vá para a pasta **PkgFolder** localize e abra o arquivo da **DemoDataPreImportConfig.xml** Notepad ou outro (editor XML).</span><span class="sxs-lookup"><span data-stu-id="cdd58-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="cdd58-235">Localize o valor a seguir e depois mude as configurações de verdadeiro ou falso:</span><span class="sxs-lookup"><span data-stu-id="cdd58-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="cdd58-236">Essa mudança fará com que a instalação verifica ignorar todas de segurança importantes, incluindo:</span><span class="sxs-lookup"><span data-stu-id="cdd58-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="cdd58-237">Confirmando que não há mais de um ativo **Unidade organizacional** registro e, na **A Fabrikam. o.** renomeando o.</span><span class="sxs-lookup"><span data-stu-id="cdd58-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="cdd58-238">Confirmando que não há mais de um registro ativo **Trabalhar com modelo**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="cdd58-239">Confirmando que não há mais de um registro ativo **Parâmetro de projeto**, e depois renomeie essa entrada como **Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="cdd58-240">Componentes de configuração</span><span class="sxs-lookup"><span data-stu-id="cdd58-240">Configuration components</span></span>

<span data-ttu-id="cdd58-241">Existem diversos outros componentes de configuração nesse arquivo de configuração antes da importação.</span><span class="sxs-lookup"><span data-stu-id="cdd58-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="cdd58-242">Para os técnicos, alguns deles incluem:</span><span class="sxs-lookup"><span data-stu-id="cdd58-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="cdd58-243">**\<RequiredSolutions\>** especifica as instalações de solução necessárias e os números de versão.</span><span class="sxs-lookup"><span data-stu-id="cdd58-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="cdd58-244">**\<InstallSampleData\>** controla se os dados de exemplo prontos para uso dos aplicativos são instalados.</span><span class="sxs-lookup"><span data-stu-id="cdd58-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="cdd58-245">falso - pula a instalação destes dados integrados (que é removível)</span><span class="sxs-lookup"><span data-stu-id="cdd58-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="cdd58-246">verdadeiro - instala os dados integrados junto com instalação do FS e dados de amostra PSA</span><span class="sxs-lookup"><span data-stu-id="cdd58-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="cdd58-247">**\<PreImportDataCollection\>** especifica os mapas de dados simples e dos registros associados sejam importados principal antes da instalação dos dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="cdd58-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="cdd58-248">**\<EntitiesToEnableScheduling\>** especifica quais entidade devem ser habilitadas para Reserva no Microsoft Dynamics Scheduling (também conhecido como Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="cdd58-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="cdd58-249">**\<UsersToCreateAndConfigure\>** especifica recursos reserváveis que será criado (se já não existir) antes de importar os dados de exemplo é executado.</span><span class="sxs-lookup"><span data-stu-id="cdd58-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="cdd58-250">Lembre-se de que na reserva de recursos dos dados de exemplo do sistema de origem aos registros de recursos reserváveis do sistema de destino fullname no logon e de cada recurso.</span><span class="sxs-lookup"><span data-stu-id="cdd58-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="cdd58-251">Portanto, NÃO é mais possível alterar os nomes neste arquivo pré-configurado a menos que você primeiro importe as amostras de dados em um sistema de destino usando esses nomes, depois renomeie os recursos agendáveis para seu nome desejado junto com o registros de usuário habilitados, e depois exporte os dados novamente para importação em seu sistema de destino final (atualização do **ImportUserMapFile.xml** antigo e novas entradas de acordo).</span><span class="sxs-lookup"><span data-stu-id="cdd58-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="cdd58-252">**\<PluginsToDisable\>** especifica plug-ins discretos do item de linha que devem estar desabilitada durante a importação de dados de exemplo e depois reenabled ser mais tarde.</span><span class="sxs-lookup"><span data-stu-id="cdd58-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="cdd58-253">Cenário fictício da Fabrikam Robotics</span><span class="sxs-lookup"><span data-stu-id="cdd58-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="cdd58-254">Os pacotes de referência de exemplo de dados do Field Service e Project Service instala a **Solução mestre de fabricação Fabrikam de dados (v3.0.0.0) solution**, junto com aproximadamente 4.000 registros e aproximadamente 40 entidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="cdd58-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="cdd58-255">Os pacotes dos dados de exemplo para o Field Service ou Project Service contém um subconjunto de dados exemplo **v902FPSMasterData** para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cdd58-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="cdd58-256">O pacote **Dados de demonstração** instala a **solução do Fabrikam Manufacturing Demo Data (v3.0.0.7)** com, aproximadamente, 22.000 registros entre 148 entidades.</span><span class="sxs-lookup"><span data-stu-id="cdd58-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="cdd58-257">Empresa fictícia, a robótica de A Fabrikam, fabricante é uma cadeia de robôs manufatura de dispositivo e eletrônico é conhecida de qualidade para seus produtos e inovação, o SAC de sólido, inclusive a instalação, planejamento da implementação, serviços e em andamento.</span><span class="sxs-lookup"><span data-stu-id="cdd58-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="cdd58-258">A Fabrikam é sediada nos Estados Unidos (Fabrikam US) e tem operações de serviço baseadas em projeto na França, Índia, Reno Unido e Suíça.</span><span class="sxs-lookup"><span data-stu-id="cdd58-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="cdd58-259">Operações de Field Service são centralizadas nos Estados Unidos, a maioria na área de Seattle.</span><span class="sxs-lookup"><span data-stu-id="cdd58-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="cdd58-260">A empresa está focada em usar a conectividade Internet of Things (IoT) para monitorar desempenho de ativo do cliente monitore e entregar serviços no local cada vez mais proativos.</span><span class="sxs-lookup"><span data-stu-id="cdd58-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="cdd58-261">Uma visão geral resumida sobre os dados de exemplo é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cdd58-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="cdd58-262">Elementos comuns de dados de exemplo incluídos (dos aplicativos)</span><span class="sxs-lookup"><span data-stu-id="cdd58-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="cdd58-263">1 usuário</span><span class="sxs-lookup"><span data-stu-id="cdd58-263">1 user</span></span>

    - <span data-ttu-id="cdd58-264">71 contas</span><span class="sxs-lookup"><span data-stu-id="cdd58-264">71 accounts</span></span>

    - <span data-ttu-id="cdd58-265">137 contatos</span><span class="sxs-lookup"><span data-stu-id="cdd58-265">137 contacts</span></span>

    - <span data-ttu-id="cdd58-266">Vários tipos de transação e categorias</span><span class="sxs-lookup"><span data-stu-id="cdd58-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="cdd58-267">50 produtos com 1 lista de preço de produto</span><span class="sxs-lookup"><span data-stu-id="cdd58-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="cdd58-268">14 listas de preço/custo</span><span class="sxs-lookup"><span data-stu-id="cdd58-268">14 price/cost lists</span></span>

    - <span data-ttu-id="cdd58-269">31 características (habilidades de recurso) em 2 modelos de classificação com 3 níveis (valores de classificação)</span><span class="sxs-lookup"><span data-stu-id="cdd58-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="cdd58-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="cdd58-270">Project Service</span></span>

    - <span data-ttu-id="cdd58-271">8 unidades organizacionais</span><span class="sxs-lookup"><span data-stu-id="cdd58-271">8 organizational units</span></span>

    - <span data-ttu-id="cdd58-272">6 níveis de utilização específica da função</span><span class="sxs-lookup"><span data-stu-id="cdd58-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="cdd58-273">Mais de 2.800 especificações de função de preço</span><span class="sxs-lookup"><span data-stu-id="cdd58-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="cdd58-274">Field Service</span><span class="sxs-lookup"><span data-stu-id="cdd58-274">Field Service</span></span>

    - <span data-ttu-id="cdd58-275">4 territórios</span><span class="sxs-lookup"><span data-stu-id="cdd58-275">4 territories</span></span>

    - <span data-ttu-id="cdd58-276">5 tipos de ordem de serviço</span><span class="sxs-lookup"><span data-stu-id="cdd58-276">5 work order types</span></span>

    - <span data-ttu-id="cdd58-277">22 ativos do cliente</span><span class="sxs-lookup"><span data-stu-id="cdd58-277">22 customer assets</span></span>

    - <span data-ttu-id="cdd58-278">9 tipos de incidentes com uma variação de características de recurso associado (9), serviços (13) e tarefas de serviço (13)</span><span class="sxs-lookup"><span data-stu-id="cdd58-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="cdd58-279">O pacote **dados de demonstração** instala, aproximadamente 179 ordens de trabalho, 12 projetos e dados transacionais associados.</span><span class="sxs-lookup"><span data-stu-id="cdd58-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="cdd58-280">Alterar o horário de trabalho para os recursos de exemplo</span><span class="sxs-lookup"><span data-stu-id="cdd58-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="cdd58-281">Por padrão, todos os recursos reserváveis têm um calendário horas de trabalho de 24.</span><span class="sxs-lookup"><span data-stu-id="cdd58-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="cdd58-282">Se você precisar alterar o horário de trabalho para os recursos reserváveis de exemplo, vá para **Universal Resource Scheduling** > **Agendamento** > **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="cdd58-283">Selecione um usuário (por exemplo, Spencer Low) e as horas de trabalho de Spencer de horário alterações a serem aplicadas para vários usuários.</span><span class="sxs-lookup"><span data-stu-id="cdd58-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="cdd58-284">Vá para **Universal Resource Scheduling** > **Configurações** > **Modelos de Horas de Trabalho** e edite o registro **Modelo de Trabalho Padrão**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="cdd58-285">No campo **Modelo de recursos**, selecione um usuário com horas de trabalho que você deseja aplicar a outros recursos.</span><span class="sxs-lookup"><span data-stu-id="cdd58-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="cdd58-286">Vá para **Universal Resource Scheduling** > **Agendamento** > **Recursos** > **Recursos Reserváveis Ativos**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="cdd58-287">Selecione os recursos que deseja alterar e, selecione **Definir calendário**.</span><span class="sxs-lookup"><span data-stu-id="cdd58-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="cdd58-288">Na lista suspensa **Modelo de trabalho** , selecione o modelo **Usar como padrão o horário de trabalho** ou outro modelo com o recurso correto.</span><span class="sxs-lookup"><span data-stu-id="cdd58-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="cdd58-289">Quando você voltar para o painel de agendamento, você deverá conseguir ver os recursos possuem que agora o horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cdd58-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="cdd58-290">![Captura de tela dos recursos agendáveis ativos](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="cdd58-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]