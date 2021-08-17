---
title: Instalação de dados de exemplo
description: Este tópico fornece informações sobre a instalação de dados de exemplo no Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 01e2f1f6b29e040d5c72af402031e13a867736405c4ee161e49b74a30e4b506e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985532"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalação de dados de exemplo para aplicação do Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Para ajudar você a criar seus próprios ambientes de demonstração, a Microsoft fornece pacotes de dados de exemplo baixáveis que demonstram as funcionalidades dos seus aplicativos. Há dois tipos de pacotes de dados de exemplo:
- referência/dados de configuração
- dados demonstrativos (referência/configuração e dados transacionais, como ordens de serviço e projetos)

Os pacotes de dados **referência** de amostra em três pacotes diferentes, para que você possa instalar apenas dados do Project Service, ou apenas para Field Service, ou você pode instalar dados de exemplo para ambas aplicações de uma só vez.

Os pacotes de dados de referência/configuração de amostra são:

- [**V902PSMasterData** - Apenas para a versão 3.x do Project Service](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Apenas para a versão 8.x do Field Service](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x e Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

O pacote de dados de **demonstração** mais recentes é:

 - [**FPSDemoData** - Field Service 8.x e Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Instalação e instruções diferem levemente nos usuários para criar e configurar a seção, mas o resto é o mesmo que na [**postagem de blog**](https://aka.ms/fpsdemodatablog) anterior. Este pacote apresenta um conjunto de dados de demonstração reduzido e leva aproximadamente 3 horas para ser instalado.

Esses pacotes de dados de exemplo estão disponíveis apenas em inglês.

> [!IMPORTANT]
> **Não é possível desinstalar os dados de exemplo.** Você só deve instalar esses pacotes na demonstração, avaliação, treinamento ou sistemas de teste. Observe também que não é possível instalar um pacote individual e depois instalar o outro pacote individual. (Ou seja, você não pode instalar **FSMasterData** seguido por **PSMasterData**, ou vice-versa.) Se você precisar de dados de exemplo para ambas aplicações a qualquer momento no futuro, você deve instalar o pacote **v902FPSMasterData**.

Ao instalar os pacotes de dados de exemplo, o processo de instalação realiza as ações a seguir:

- Cria ou defina-o como parâmetros o para usar o Project Service, Field Service, ou ambos aplicativos (se aplicável).

- Importa amostras de dados das aplicações, como recursos agendáveis, funções específicas de aplicação, vendas e listas de preço de venda, unidades organizacionais, registros de processos de venda e outras entidades para demonstrar funcionalidades chave.  

Com o pacote **dados de demonstração**, você recebe os dados acima e transacional adicionar, como ordens de serviço e projetos.

Quer saber quais habilidades você pode experimentar com os dados de exemplo? Consulte o cenário fictício do Fabrikam Robotics em [Notas técnicas](#technical-notes).

Se você tiver dúvidas sobre como instalar esses pacotes de dados de exemplo, [envie um e-mail para fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Requisitos

O protocolo de instalação usa o seguinte sobre sua instância de destino (org):

- O idioma base é inglês e a moeda base é dólar americano (USD, $)

- A organização não tem dados de Project Service ou Field Service prontos, ou tem apenas a base de dados padrão que vem com qualquer organização.

- A versão correta da aplicação empresarial já está instalada:
       
    - **For FPSDemoData or v902FPSMasterData:** A org tem Field Service versão 8.x e Project Service versão 3.x instalados.

    - **For v902PSMasterData:** A org tem Project Service versão 3.x instalada.

    - **For v902FSMasterData:** A org tem Field Service versão 8.x instalada.

> [!NOTE]
> Se precisar instalar dados de exemplo em um ambiente de teste ou demonstração de Project Service e Field Service existente que já tem dados (não recomendado), você precisará suspender as pré-verificações de segurança realizadas pelo instalador. Para obter mais informações, consulte as notas técnicas abaixo.

## <a name="prepare-for-installation"></a>Prepare para a instalação

Você precisa executar o instalador em um computador com uma versão recente do Windows (Windows 10 de preferência).

Você deve planejar para o computador permanecer conectado a uma rede e para a instalação para executar até **1 hora** para **configuração/dados de referência**. (Geralmente, a instalação leva cerca de 30 minutos para **FPSMasterData**, que inclui dados de amostra para ambos aplicativos.) Para **FPSDemoData**, a instalação levará cerca de **3 horas**.

O computador deve ter a função de salvar tela desativada. Caso contrário, as credenciais de sessão da instalação podem ser perdidas quando a função de salvar tela entrar (a menos que você mantenha sua sessão ativa por todo o tempo).

> [!div class="mx-imgBorder"]
> ![Captura de tela das configurações da função de salvar tela, com função de salvar tela desativada.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Baixar e tirar da compactação

O instalador de Project Service e Field Service é distribuído como um executável com extração automática. Os nomes de arquivo podem variar dependendo do pacote de dados de exemplo, mas caso contrário, as etapas são as mesmas não importa que pacote você instale.

Depois de baixar um pacote, execute o arquivo .exe e depois aceite os termos e condições para descompactar o arquivo .zip compactado. Em seguida, você precisa extrair conteúdos desse arquivo ou pasta no computador.

Dependendo do sistema operacional e das configurações de segurança, é preciso realizar as seguintes etapas depois de descompactar o arquivo .zip:

1. Encontre e clique com o botão direito no arquivo **FPSDemoData.dll** na pasta **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Escolha **Desbloquear**.

3. Selecione **Aplicar**.

4. Selecione **OK**.


## <a name="create-or-configure-users"></a>Criar ou configurar usuários

O pacote **FPSDemoData** requer que seis usuários, enquanto **FPSMasterData** requer um. Consulte o correto para obter seu pacote de dados de exemplo.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Criar ou configurar usuários - configuração/pacotes de dados de referência

O pacote **FPSMasterData** é criado para instalar com um usuário nomeado Spencer Low com as configurações descritas assim. Para instalar o pacote corretamente, você precisa criar (ou temporariamente renomear) usuários em seu ambiente para combinar a configuração de dados de exemplo de entrada.

Para criar ou configurar usuários, vá para **Configurações** > **Segurança** > **Usuários**, e faça o seguinte:

1. Defina UserFullname="Spencer Low" com nome de usuário "spencerl" (**caixa baixa**) para as funções de Gerente de projeto e Gerente de prática.

2. Selecione o usuário **Spencer Low**, e depois selecione **Gerenciar funções**. Localize e selecione a função **Administrador do sistema**, e depois selecione **OK** para conceder direitos de administrador para Spencer Low. Essa etapa é necessária para garantir que os registros de amostra sejam criados com a propriedade de usuário correte e popule as exibições corretamente.

3. No pacote de download, você precisa atualizar o arquivo de mapeamento de dados com endereços de e-mail do contexto de usuário padrão. Para fazer isso, abra **PkgFolder**, encontre o arquivo **ImportUserMapFile.xml** e abra-o no Bloco de Notas (ou Visual Studio, ou outro editor de XML). Defina o campo **DefaultUserToMapTo=** do endereço de e-mail do usuário Spencer Low.

4. Se você não estiver usando o Spencer Low com o nome de usuário **spencerl**, você precisa atualizar um arquivo adicional. Abra o arquivo **DemoDataPreImportConfig.xml**, e depois encontre a tag **userstocreateandconfigure**. Atualize a marca **\<login\>** com o nome de usuário de seu usuário Marcelo Santos. Para detalhes adicionais, consulte [Notas técnicas](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Criar ou configurar usuários - pacote de dados de demonstração

O pacote de dados demonstrativos requer seis usuários. Para o pacote instalar corretamente, faça o seguinte:

 1. Criar ou renomear temporariamente usuários existentes para combinar configuração de dados de exemplo de entrada acessando **Configurações** > **Segurança** > **Usuários**.
 
    Essas funções só são necessárias para demonstrações baseadas em identidade.  
    - Nome completo do usuário = "David So" como técnico do Field Service   
    - Usuário Fullname="Jamie Reding" como Customer Service & Field Service Dispatcher   
    - Usuário Fullname="Molly Clark" como Account Manager   
    - Usuário Fullname="Spencer Low" como Practice and Project Manager  
    - Usuário Fullname="Veronica Quek" como Team Member   
    - User Fullname="William Contoso"
  
2. Para fins de importação de demonstração de dados, atribuir os seis usuários acima a função de administrador para que registros de amostra sejam importados corretamente. 

3. Abra **PkgFolder** e depois encontre e abra **ImportUserMapFile.xml**. Atualize os campos **New=** dos endereços de e-mail de Usuários correspondentes em seu sistema.

   > [!div class="mx-imgBorder"]
   > ![Captura de tela do UserMapFile.](media/sample-data-7.png)

4. Se seu nome completo de usuário "Spencer Low" tiver um ID de usuário diferente de **"spencerl"**, então você precisa atualizar um arquivo adicional. Abra **DemoDataPreImportConfig.xml**, e encontre a tag **userstocreateandconfigure**. Atualize a marca **\<login\>** com a loginId (diferencia maiúsculas de minúsculas). 

5. O primeiro calendário de usuário (na tag **userstocreateandconfigure**) é usado para popular as horas de trabalho de todos recursos agendáveis na importação de dados de demonstração. Navegue até **Configurações** > **Segurança** > **Usuários**, encontre seu usuário "Spencer Low", e abra a opção "Horas de trabalho". Edite as horas de trabalho existentes, selecionando a opção **Programa semanal recorrente completo do início ao fim**. Verifique se **Horas de trabalho estão definidas para 8 AM - 5 PM (9 Horas), segunda-feira a sexta-feira e com o fuso horário definido como Hora do Pacífico (EUA e Canadá)**. Isso é necessário para garantir que o painel de Projeto e agenda esteja como esperado.

**Recomendação:** Considere criar um backup de seu org agora, caso você precise reverter seu ponto de início caso algo dê errado durante a instalação de dados de exemplo. Para mais informações, consulte [Backup e restaurar instâncias](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Executar o Package Deployer

1. Localize e execute **PackageDeployer.exe** na pasta **v902FPSMasterData** OU **PackageDeployer_FPSDemoData**.

2. Aceite os termos e condições.

3. Na próxima janela:

   a. Selecione o tipo de implantação do **Office 365**.

   b. Use o usuário e a senha do usuário de administrador do sistema configurada em "Criar ou configurar usuários" ("Spencer Low" com nome de usuário "spencerl").

   c. Selecione a opção **Exibir lista de organizações disponíveis**.

      > [!div class="mx-imgBorder"]
      > ![Captura de tela da janela Package Deployer com "Lista de exibição de organizações disponíveis" selecionada](media/sample-data-2.png)

4. Selecione a organização onde deseja instalar os dados de exemplo.

5. Selecione **Avançar** até ver a caixa de **Configuração de dados demonstrativos**.

   > [!div class="mx-imgBorder"]
   > ![Captura de tela da janela de status do instalador de dados de demonstração.](media/sample-data-3.png)

6. Antes de prosseguir, lembre-se que instalar dados de exemplo pode levar até uma hora (normalmente ~10 minutos). Você precisará garantir que o computador permanecerá ligado e conectado a uma rede durante todo o processo de instalação e que sua sessão se mantenha ativa.   

7. Quando estiver pronto, clique em **Avançar** para iniciar o processo de instalação dos dados de exemplo. Depois que os dados de exemplo são carregados, clique em **Concluído**.

## <a name="verify-the-sample-data-installation"></a>Verifique a instalação de dados de exemplo

Para garantir, verifique se o número de registros e tipos de entidades listados no cenário fictício Fabrikam Robotics aparece como esperado.

Depois que os dados de exemplo carregarem por completo, entre como o usuário Spencer Low e confirme o seguinte:

- Se o aplicativo Project Service estiver instalado, acesse **Project Service** > **Configurações** > **Listas de preço**. Confirmar as taxas de conta e custos de taxas existentes, com a moeda apropriada, para cada país/região no conjunto de dados.

- Se o aplicativo Project Service estiver instalado, acesse **Universal Resource Scheduling** > **Configurações** > **Unidades Organizacionais**. Confirme se a lista de preços com a moeda apropriada foi associado com cada unidade org (excluindo entradas de cidade). Se estiver faltando algum, encontre e associe a lista de preços correta.

- Se o aplicativo Field Service estiver instalado, acesse **Project Service** > **Configurações** > **Listas de preço**. Confirme que taxas de conta e custos existem. Acesse **Field Service** > **Configurações** > **Listas de preço** e verifique as taxas de conta e custos de taxas existentes, com a moeda apropriada, para cada país/região no conjunto de dados.

  > [!div class="mx-imgBorder"]
  > ![Captura de tela das listas de preço ativas.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Captura de tela de unidades organizacionais ativas.](media/sample-data-5.png)

## <a name="technical-notes"></a>Notas técnicas

Veja abaixo para obter detalhes técnicos sobre a instalação desses dados.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instalar dados de exemplo nos dados existentes (não recomendados)

Se precisar instalar dados de exemplo em um ambiente de teste ou demonstração de Field Service ou Project Service existente que já tem dados, você precisará suspender as pré-verificações de segurança realizadas pelo instalador.

Para fazer isso, vá para a pasta **PkgFolder** localize e abra o arquivo da **DemoDataPreImportConfig.xml** Notepad ou outro (editor XML).

Localize o valor a seguir e depois mude as configurações de verdadeiro ou falso:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Essa mudança fará com que a instalação verifica ignorar todas de segurança importantes, incluindo:

- Confirmando que não há mais de um ativo **Unidade organizacional** registro e, na **A Fabrikam. o.** renomeando o.

- Confirmando que não há mais de um registro ativo **Trabalhar com modelo**.

- Confirmando que não há mais de um registro ativo **Parâmetro de projeto**, e depois renomeie essa entrada como **Parâmetros**.

### <a name="configuration-components"></a>Componentes de configuração

Existem diversos outros componentes de configuração nesse arquivo de configuração antes da importação. Para os técnicos, alguns deles incluem:

- **\<RequiredSolutions\>** especifica as instalações de solução necessárias e os números de versão.

- **\<InstallSampleData\>** controla se os dados de exemplo prontos para uso dos aplicativos são instalados.

    - falso - pula a instalação destes dados integrados (que é removível)

    - verdadeiro - instala os dados integrados junto com instalação do FS e dados de amostra PSA

- **\<PreImportDataCollection\>** especifica os mapas de dados simples e dos registros associados sejam importados principal antes da instalação dos dados de exemplo.

- **\<EntitiesToEnableScheduling\>** especifica quais entidade devem ser habilitadas para Reserva no Microsoft Dynamics Scheduling (também conhecido como Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** especifica recursos reserváveis que será criado (se já não existir) antes de importar os dados de exemplo é executado. Lembre-se de que na reserva de recursos dos dados de exemplo do sistema de origem aos registros de recursos reserváveis do sistema de destino fullname no logon e de cada recurso. Portanto, NÃO é mais possível alterar os nomes neste arquivo pré-configurado a menos que você primeiro importe as amostras de dados em um sistema de destino usando esses nomes, depois renomeie os recursos agendáveis para seu nome desejado junto com o registros de usuário habilitados, e depois exporte os dados novamente para importação em seu sistema de destino final (atualização do **ImportUserMapFile.xml** antigo e novas entradas de acordo).

- **\<PluginsToDisable\>** especifica plug-ins discretos do item de linha que devem estar desabilitada durante a importação de dados de exemplo e depois reenabled ser mais tarde.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Cenário fictício da Fabrikam Robotics

Os pacotes de referência de exemplo de dados do Field Service e Project Service instala a **Solução mestre de fabricação Fabrikam de dados (v3.0.0.0) solution**, junto com aproximadamente 4.000 registros e aproximadamente 40 entidades diferentes. Os pacotes dos dados de exemplo para o Field Service ou Project Service contém um subconjunto de dados exemplo **v902FPSMasterData** para o aplicativo. O pacote **Dados de demonstração** instala a **solução do Fabrikam Manufacturing Demo Data (v3.0.0.7)** com, aproximadamente, 22.000 registros entre 148 entidades.

Empresa fictícia, a robótica de A Fabrikam, fabricante é uma cadeia de robôs manufatura de dispositivo e eletrônico é conhecida de qualidade para seus produtos e inovação, o SAC de sólido, inclusive a instalação, planejamento da implementação, serviços e em andamento. A Fabrikam é sediada nos Estados Unidos (Fabrikam US) e tem operações de serviço baseadas em projeto na França, Índia, Reno Unido e Suíça.

Operações de Field Service são centralizadas nos Estados Unidos, a maioria na área de Seattle. A empresa está focada em usar a conectividade Internet of Things (IoT) para monitorar desempenho de ativo do cliente monitore e entregar serviços no local cada vez mais proativos.

Uma visão geral resumida sobre os dados de exemplo é o seguinte:

- Elementos comuns de dados de exemplo incluídos (dos aplicativos)

    - 1 usuário

    - 71 contas

    - 137 contatos

    - Vários tipos de transação e categorias

    - 50 produtos com 1 lista de preço de produto

    - 14 listas de preço/custo

    - 31 características (habilidades de recurso) em 2 modelos de classificação com 3 níveis (valores de classificação)

- Project Service

    - 8 unidades organizacionais

    - 6 níveis de utilização específica da função

    - Mais de 2.800 especificações de função de preço

- Field Service

    - 4 territórios

    - 5 tipos de ordem de serviço

    - 22 ativos do cliente

    - 9 tipos de incidentes com uma variação de características de recurso associado (9), serviços (13) e tarefas de serviço (13)
   
O pacote **dados de demonstração** instala, aproximadamente 179 ordens de trabalho, 12 projetos e dados transacionais associados. 

### <a name="change-the-work-hours-for-sample-resources"></a>Alterar o horário de trabalho para os recursos de exemplo

Por padrão, todos os recursos reserváveis têm um calendário horas de trabalho de 24.

Se você precisar alterar o horário de trabalho para os recursos reserváveis de exemplo, vá para **Universal Resource Scheduling** > **Agendamento** > **Recursos**.

Selecione um usuário (por exemplo, Spencer Low) e as horas de trabalho de Spencer de horário alterações a serem aplicadas para vários usuários. Vá para **Universal Resource Scheduling** > **Configurações** > **Modelos de Horas de Trabalho** e edite o registro **Modelo de Trabalho Padrão**. No campo **Modelo de recursos**, selecione um usuário com horas de trabalho que você deseja aplicar a outros recursos. Vá para **Universal Resource Scheduling** > **Agendamento** > **Recursos** > **Recursos Reserváveis Ativos**. Selecione os recursos que deseja alterar e, selecione **Definir calendário**. Na lista suspensa **Modelo de trabalho** , selecione o modelo **Usar como padrão o horário de trabalho** ou outro modelo com o recurso correto. Quando você voltar para o painel de agendamento, você deverá conseguir ver os recursos possuem que agora o horário de trabalho.

> [!div class="mx-imgBorder"]
> ![Captura de tela dos recursos agendáveis ativos.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]