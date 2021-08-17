---
title: Usar o Suplemento do Project Service para planejar seu trabalho no Microsoft Project | MicrosoftDocs
description: Este tópico fornece informações sobre como adicionar, configurar e usar o suplemento do Microsoft Project para o Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ccebf1439f49092b23da5b4fc2ebb4fc484de4dd17c870eea9fe37b00fbb3689
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005287"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Usar o Suplemento do Project Service Automation para planejar seu trabalho no Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Com o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], é mais fácil realizar o planejamento de projetos, incluindo estimativas. Você pode definir o trabalho para que os custos, o esforço e o valor de venda estejam claros quando a proposta final for enviada.  

 Agora você pode instalar o [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] e fazer o seu trabalho de planejamento no ambiente familiar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Use os sólidos recursos de planejamento e gerenciamento do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e atualize seu plano de projeto no Project Service Automation.  

> [!IMPORTANT]
> - Para usar o gerenciamento de documentos do SharePoint para armazenar os arquivos [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para projetos do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o administrador do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] precisará ativar o gerenciamento de documentos. 
> - O [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] é compatível apenas com o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Baixar e instalar o suplemento  
 Prepare suas informações de suplemento do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Você precisará dessas informações para se conectar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  No Centro de Download, você pode baixar o suplemento para a versão compatível do Project Service, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ou [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Clique no link do download.  

3.  Quando o download estiver concluído, clique em **Sim** para instalar o suplemento.  

## <a name="configure-the-add-in"></a>Configurar o suplemento  

1. Abra o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e clique na guia **Project Service**.  

2. Clique em **Conectar**.  

3. Insira as informações do seu suplemento e, em seguida, clique em **Entrar**.  

   Agora você pode começar a usar o suplemento.  

## <a name="read-from-a-template"></a>Ler de um modelo  
 Ler usando um modelo que você criou no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copie para [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para iniciar o planejamento do projeto. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Criar um modelo de projeto (Project Service Automation)](../psa/create-project-template.md)  

1.  Na guia **Project Service**, clique em **Ler** > **Modelo de projeto do Project Service Automation**.  

2.  Selecione um modelo de projeto na lista e depois clique em **Abrir**.  

    > [!NOTE]
    >  Por padrão, as tarefas que são copiadas do modelo no Project são definidas como agendadas manualmente.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Atribuir funções de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] aos recursos do projeto  

1.  Abra um projeto e clique na faixa de opções **Tarefa**.  

2.  Clique no menu **Gráfico de Gantt** e depois selecione **Planilha de Recursos**.  

3.  Na Planilha de Recursos, clique no menu suspenso **Função de Recurso do Project Service** e selecione uma função do Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Obter recursos para seu projeto  

1.  Na guia Project Service, selecione uma linha e clique em **Encontrar Recursos**.  

2.  Na tela **Reservar Recurso**, selecione o recurso que deseja usar no projeto.  

3.  Clique em **Reservar** e depois clique em **OK**.  

## <a name="publish-your-project"></a>Publicar seu projeto  
Após a conclusão do seu planejamento de projeto, o próximo passo é importar e publicar o projeto na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

O projeto será importado para a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Os preços e o processo de geração de equipe serão aplicados. Abra o projeto no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para verificar se a equipe, as estimativas de projeto e a estrutura de detalhamento de trabalho foram gerados. A seguinte tabela mostra onde encontrar os resultados:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gráfico de Gantt**   | Importa na tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estrutura de Detalhamento de Trabalho**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Planilha de Recursos** |   Importa na tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Membros da Equipe do Projeto**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Uso**    |    Importa para a tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estimativas do Projeto**.     |

**Para importar e publicar seu projeto**  
1. Na guia **Project Service**, clique em **Publicar** > **Novo Projeto do Project Service Automation**.  

2. Na caixa de diálogo **Publicar para um novo projeto no Project Service**, insira o **Nome do Projeto** e selecione o **Cliente**.  

3. Opcionalmente, verifique a opção **Vincular plano de projeto ao Project Service Automation** para vincular o arquivo do Project do plano ao Project Service Automation.  

4. Clique em **Publicar**.  

   Vincular o arquivo do Project ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] torna o arquivo do Project o mestre e define a estrutura de detalhamento de trabalho no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como somente leitura.  Para fazer alterações no plano de projeto, você precisa fazê-las no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicá-las como atualizações para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editar um projeto que foi importado  
 Para fazer alterações em um plano de projeto que foi importado para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], você tem duas opções:  

- Abra o arquivo mestre e edite-o no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Desvincule o arquivo e edite-o diretamente no Project Service. Por padrão, um projeto que foi carregado do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] é bloqueado e só pode ser editado em Projeto. Para editar o arquivo no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o arquivo precisa estar desvinculado.  

### <a name="edit-in-pn_microsoft_project"></a>Edite no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. No menu principal, clique em **Project Service** > **Projetos**.  

2. Na lista de projetos, abra aquele que você criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Clique em **Abrir no MS Project** na faixa de opções. Isso abrirá o arquivo mestre vinculado no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Desvincule um arquivo e edite no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. No menu principal, clique em **Project Service** > **Projetos**.  

2. Na lista de projetos, abra aquele que você criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Clique em **Desvincular do MS Project** na faixa de opções.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Carregar um arquivo do Project no SharePoint ou Grupos do Office  
 É possível carregar seu arquivo do Project no SharePoint e encontrá-lo nos Documentos Associados do seu projeto do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  É preciso que o administrador configure o gerenciamento de documentos do SharePoint e ative-o para a entidade Projeto. 

 Você também pode carregar seu arquivo do projeto para [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se tiver Grupos do Office configurados.

### <a name="upload-a-file-for-sharepoint"></a>Carregar um arquivo para SharePoint  

1. No menu principal, clique em **Project Service** > **Carregar**.  

2. Selecione **Para Documentos do Projeto do Project Service Automation**.  

3. Na caixa de diálogo **Permitir Abertura no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selecione **Sim** ou **Não**.  

   - Se clicar em **Sim**, você poderá selecionar o botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation, iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o arquivo do Project da biblioteca de documentos do SharePoint.  

   - Se clicar em **Não**, o link do botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.  

4. O arquivo do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto específico do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Carregar um arquivo para Grupos do Office  

1. No menu principal, clique em **Project Service** > **Carregar**.  

2. Selecione **Para Documentos do Projeto do Project Service Automation**.  

3. Na caixa de diálogo **Permitir Abertura no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selecione **Sim** ou **Não**.  

   - Se clicar em **Sim**, você poderá selecionar o botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation, iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o arquivo do Project da biblioteca de documentos do SharePoint.  

   - Se clicar em **Não**, o link do botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.  

4. O arquivo do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto específico do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publicar seu projeto como modelo  
 Você pode salvar seu projeto e reutilizá-lo salvando-o como modelo de projeto no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Os modelos de projeto são planos de projeto reutilizáveis no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Criar um modelo de projeto (Project Service Automation)](../psa/create-project-template.md)  

1. Na guia **Project Service**, clique em **Publicar** > **Novo Modelo de Projeto do Project Service Automation**.  

2. Na caixa de diálogo **Publicar para um novo projeto no modelo de Project Service**, insira o **Nome de modelo do projeto**.  

3. Opcionalmente, clique em **Vincular plano de projeto ao Project Service Automation** para vincular o arquivo do Project ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Clique em **Publicar**.  

Vincular o arquivo do Project ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] torna o arquivo do Project o mestre e define a estrutura de detalhamento de trabalho no modelo do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como somente leitura.  Para fazer alterações no plano de projeto, você precisa fazê-las no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicá-las como atualizações para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Leia uma programação carregada de recurso

Ao ler um projeto do Project Service Automation, o calendário do recurso não é sincronizado com o cliente da área de trabalho. Se houver diferenças nas durações, esforços ou términos das tarefas, é provável que os recursos e o cliente da área de trabalho não tenham o mesmo calendário de modelo de horas de trabalho aplicado ao projeto.


## <a name="data-synchronization"></a>Sincronização de dados

A tabela a seguir descreve como os dados são sincronizados entre o Project Service Automation e o suplemento da área de trabalho Microsoft Project.

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Tarefa do Projeto | Data de Vencimento | ● | - |
| Tarefa do Projeto | Esforço Estimado | ● | - |
| Tarefa do Projeto | ID do Cliente do MS Project | ● | - |
| Tarefa do Projeto | Tarefa Principal | ● | - |
| Tarefa do Projeto | Project | ● | - |
| Tarefa do Projeto | Tarefa do projeto | ● | - |
| Tarefa do Projeto | Nome da Tarefa do Projeto | ● | - |
| Tarefa do Projeto | Unidade de recursos (Preterido na v3.0) | ● | - |
| Tarefa do Projeto | Duração Agendada | ● | - |
| Tarefa do Projeto | Data de Início | ● | - |
| Tarefa do Projeto | ID da WBS | ● | - |

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Membro da Equipe | ID do Cliente do MS Project | ● | - |
| Membro da Equipe | Nome do Cargo | ● | - |
| Membro da Equipe | projeto | ● | ● |
| Membro da Equipe | Equipe do Projeto | ● | ● |
| Membro da Equipe | Unidade de Recursos | - | ● |
| Membro da Equipe | Função | - | ● |
| Membro da Equipe | Horário de Trabalho | Não sincronizado | Não sincronizado |

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Atribuição de Recurso | Da Data | ● | - |
| Atribuição de Recurso | Horário | ● | - |
| Atribuição de Recurso | ID do Cliente do MS Project | ● | - |
| Atribuição de Recurso | Trabalho Planejado | ● | - |
| Atribuição de Recurso | Project | ● | - |
| Atribuição de Recurso | Equipe do Projeto | ● | - |
| Atribuição de Recurso | Atribuição de Recurso | ● | - |
| Atribuição de Recurso | Tarefa | ● | - |
| Atribuição de Recurso | Até Esta Data | ● | - |

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Dependências de Tarefa do Projeto | Dependência de Tarefa do Projeto | ● | - |
| Dependências de Tarefa do Projeto | Tipo de Link | ● | - |
| Dependências de Tarefa do Projeto | Tarefa Antecessora | ● | - |
| Dependências de Tarefa do Projeto | Project | ● | - |
| Dependências de Tarefa do Projeto | Tarefa Sucessora | ● | - |

### <a name="see-also"></a>Consulte também  
 [Guia do gerente de projeto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]