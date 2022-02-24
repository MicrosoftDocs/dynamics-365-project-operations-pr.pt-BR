---
title: Planejar seu trabalho no Microsoft Project com o suplemento do Project Service
description: Este tópico fornece informações sobre como usar o suplemento do Microsoft Project para o Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145929"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planejar seu trabalho no Microsoft Project com o suplemento do Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

Com o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], é mais fácil realizar o planejamento de projetos, incluindo estimativas. Você pode definir o trabalho para que os custos, o esforço e o valor de venda estejam claros quando a proposta final for enviada.  

Você pode instalar o [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] e fazer o seu trabalho de planejamento no ambiente familiar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Use os sólidos recursos de planejamento e gerenciamento do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e atualize seu plano de projeto no Project Service Automation.  

> [!IMPORTANT]
> - Para usar o gerenciamento de documentos do SharePoint para armazenar os arquivos [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para projetos do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o administrador do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] precisará ativar o gerenciamento de documentos. 
> - O [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] é compatível apenas com o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Baixar e instalar o suplemento  
 Prepare suas informações de suplemento do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Você precisará dessas informações para se conectar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  No Centro de Download, você pode baixar o suplemento para a versão compatível do Project Service, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ou [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Selecione o link para download.  

3.  Quando o download estiver concluído, selecione **Sim** para instalar o suplemento.  

## <a name="configure-the-add-in"></a>Configurar o suplemento  

1. Abra o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e selecione a guia **Project Service**.  

2. Selecione **Conectar**.  

3. Insira as informações do seu suplemento e, em seguida, selecione **Entrar**.  

   Agora você pode começar a usar o suplemento.  

## <a name="read-from-a-template"></a>Ler de um modelo  
 Ler usando um modelo que você criou no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copie para [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para iniciar o planejamento do projeto. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Criar um modelo de projeto (Project Service Automation)](../psa/create-project-template.md)  

1.  Na guia **Project Service**, selecione **Ler** > **Modelo de projeto do Project Service Automation**.  

2.  Selecione um modelo de projeto na lista e depois selecione **Abrir**.  

    > [!NOTE]
    >  Por padrão, as tarefas que são copiadas do modelo no Project são definidas como agendadas manualmente.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Atribuir funções de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] aos recursos do projeto  

1.  Abra um projeto e selecione a faixa de opções **Tarefa**.  

2. Selecione o menu **Gráfico de Gantt** e depois selecione **Planilha de Recursos**.  

3. Na Planilha de Recursos, selecione o menu suspenso **Função de Recurso do Project Service** e selecione uma função do Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Obter recursos para seu projeto  

1.  Na guia Project Service, selecione uma linha e selecione **Encontrar Recursos**.  

2.  Na tela **Reservar Recurso**, selecione o recurso que deseja usar no projeto.  

3.  Selecione **Reservar** e **OK**.  

## <a name="publish-your-project"></a>Publicar seu projeto  
Após a conclusão do seu planejamento de projeto, o próximo passo é importar e publicar o projeto na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

O projeto será importado para a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Os preços e o processo de geração de equipe serão aplicados. Abra o projeto no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para verificar se a equipe, as estimativas de projeto e a estrutura de detalhamento de trabalho foram gerados. A seguinte tabela mostra onde encontrar os resultados.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gráfico de Gantt**   | Importa na tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estrutura de Detalhamento de Trabalho**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Planilha de Recursos** |   Importa na tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Membros da Equipe do Projeto**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Uso**    |    Importa para a tela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estimativas do Projeto**.     |

**Para importar e publicar seu projeto**  
1. Na guia **Project Service**, vá para **Publicar** > **Novo projeto do Project Service Automation**.  

2. Na caixa de diálogo **Publicar para um novo projeto no Project Service**, insira o **Nome do projeto** e selecione o **Cliente**.  

3. Opcionalmente, selecione **Vincular plano de projeto ao Project Service Automation** para vincular o arquivo do Project do plano ao Project Service Automation.  

4. Selecione **Publicar**.  

   Vincular o arquivo do Project ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] torna o arquivo do Project o mestre e define a estrutura de detalhamento de trabalho no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como somente leitura.  Para fazer alterações no plano de projeto, você precisa fazê-las no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicá-las como atualizações para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editar um projeto que foi importado  
 Para fazer alterações em um plano de projeto que foi importado para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], você tem duas opções:  

- Abra o arquivo mestre e edite-o no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Desvincule o arquivo e edite-o diretamente no Project Service. Por padrão, um projeto que foi carregado do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] é bloqueado e só pode ser editado em Projeto. Para editar o arquivo no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o arquivo precisa estar desvinculado.  

### <a name="edit-in-pn_microsoft_project"></a>Editar no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. No menu principal, vá para **Project Service** > **Projetos**.  

2. Na lista de projetos, abra aquele que você criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Selecione **Abrir no MS Project** na faixa de opções. Isso abrirá o arquivo mestre vinculado no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Desvincule um arquivo e edite no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. No menu principal, vá para **Project Service** > **Projetos**.  

2. Na lista de projetos, abra aquele que você criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Selecione **Desvincular do MS Project** na faixa de opções.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Carregar um arquivo do Project no SharePoint ou Grupos do Office  
 É possível carregar seu arquivo do Project no SharePoint e encontrá-lo nos Documentos Associados do seu projeto do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  É preciso que o administrador configure o gerenciamento de documentos do SharePoint e ative-o para a entidade Projeto. 

 Você também pode carregar seu arquivo do projeto para [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se tiver Grupos do Office configurados.

### <a name="upload-a-file-for-sharepoint"></a>Carregar um arquivo para SharePoint  

1. No menu principal, vá para **Project Service** > **Carregar**.  

2. Selecione **Para Documentos do Projeto do Project Service Automation**.  

3. Na caixa de diálogo **Permitir Abertura no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selecione **Sim** ou **Não**.  

   - Se você selecionar **Sim**, poderá selecionar **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation, iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o arquivo do Project da biblioteca de documentos do SharePoint.  

   - Se você selecionar **Não**, o link para **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.  

4. O arquivo do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto específico do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Carregar um arquivo para Grupos do Office  

1. No menu principal, vá para **Project Service** > **Carregar**.  

2. Selecione **Para Documentos do Projeto do Project Service Automation**.  

3. Na caixa de diálogo **Permitir Abertura no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selecione **Sim** ou **Não**.  

   - Se você selecionar **Sim**, poderá selecionar **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation, iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o arquivo do Project da biblioteca de documentos do SharePoint.  

   - Se você selecionar **Não**, o link para **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.  

4. O arquivo do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto específico do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publicar seu projeto como modelo  
 Você pode salvar seu projeto e reutilizá-lo salvando-o como modelo de projeto no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Os modelos de projeto são planos de projeto reutilizáveis no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Para obter mais informações, consulte [Criar um modelo de projeto (Project Service Automation)](../psa/create-project-template.md). 

1. Na guia **Project Service**, vá para **Publicar** > **Novo modelo de projeto do Project Service Automation**.  

2. Na caixa de diálogo **Publicar para um novo projeto no modelo de Project Service**, insira o **Nome de modelo do projeto**.  

3. Opcionalmente, selecione **Vincular plano de projeto ao Project Service Automation** para vincular o arquivo de projeto ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Selecione **Publicar**.  

Vincular o arquivo do Project ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] torna o arquivo do Project o mestre e define a estrutura de detalhamento de trabalho no modelo do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como somente leitura.  Para fazer alterações no plano de projeto, você precisa fazê-las no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicá-las como atualizações para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Leia uma programação carregada de recurso

Ao ler um projeto do Project Service Automation, o calendário do recurso não é sincronizado com o cliente da área de trabalho. Se houver diferenças nas durações, esforços ou términos das tarefas, é provável que os recursos e o cliente da área de trabalho não tenham o mesmo calendário de modelo de horas de trabalho aplicado ao projeto.


## <a name="data-synchronization"></a>Sincronização de dados
As tabelas nesta seção fornecem informações sobre a sincronização de dados de entidade entre o Project Service Automation e o suplemento da área de trabalho do Microsoft Project.

### <a name="project-task-entity-table"></a>Tabela de entidade Tarefa do Projeto
A tabela a seguir descreve como os dados da entidade Tarefa do Projeto são sincronizados entre o Project Service Automation e o suplemento da área de trabalho do Microsoft Project.

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Tarefa do Projeto | Data de Vencimento | Sincronizado | Não sincronizado |
| Tarefa do Projeto | Esforço Estimado | Sincronizado | Não sincronizado |
| Tarefa do Projeto | ID do Cliente do MS Project | Sincronizado | Não sincronizado |
| Tarefa do Projeto | Tarefa Principal | Sincronizado | Não sincronizado |
| Tarefa do Projeto | Project | Sincronizado | Não sincronizado |
| Tarefa do Projeto | Tarefa do projeto | Sincronizado | Não sincronizado |
| Tarefa do Projeto | Nome da Tarefa do Projeto | Sincronizado | Não sincronizado |
| Tarefa do Projeto | Unidade de recursos (Preterido na v3.0) | Sincronizado | Não sincronizado |
| Tarefa do Projeto | Duração Agendada | Sincronizado | Não sincronizado |
| Tarefa do Projeto | Data de Início | Sincronizado | Não sincronizado |
| Tarefa do Projeto | ID da WBS | Sincronizado | Não sincronizado |

### <a name="team-member-entity-table"></a>Tabela da entidade Membro da Equipe
A tabela a seguir descreve como os dados da entidade Membro da Equipe são sincronizados entre o Project Service Automation e o suplemento da área de trabalho Microsoft Project

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Membro da Equipe | ID do Cliente do MS Project | Sincronizado | Não sincronizado |
| Membro da Equipe | Nome do Cargo | Sincronizado | Não sincronizado |
| Membro da Equipe | projeto | Sincronizado | Sincronizado |
| Membro da Equipe | Equipe do Projeto | Sincronizado | Sincronizado |
| Membro da Equipe | Unidade de Recursos | Não sincronizado | Sincronizado |
| Membro da Equipe | Função | Não sincronizado | Sincronizado |
| Membro da Equipe | Horário de Trabalho | Não sincronizado | Não sincronizado |

### <a name="resource-assignment-entity-table"></a>Tabela da entidade Atribuição de Recursos
A tabela a seguir descreve como os dados da entidade Atribuição de Recursos são sincronizados entre o Project Service Automation e o suplemento da área de trabalho Microsoft Project

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Atribuição de Recurso | Data de Início | Sincronizado | Não sincronizado |
| Atribuição de Recurso | Horário | Sincronizado | Não sincronizado |
| Atribuição de Recurso | ID do Cliente do MS Project | Sincronizado | Não sincronizado |
| Atribuição de Recurso | Trabalho Planejado | Sincronizado | Não sincronizado |
| Atribuição de Recurso | Project | Sincronizado | Não sincronizado |
| Atribuição de Recurso | Equipe do Projeto | Sincronizado | Não sincronizado |
| Atribuição de Recurso | Atribuição de Recurso | Sincronizado | Não sincronizado |
| Atribuição de Recurso | Tarefa | Sincronizado | Não sincronizado |
| Atribuição de Recurso | Data de Término | Sincronizado | Não sincronizado |

### <a name="project-task-dependencies-entity-table"></a>Tabela de entidade Dependências da Tarefa do Projeto
A tabela a seguir descreve como os dados da entidade Dependências da Tarefa do Projeto são sincronizados entre o Project Service Automation e o suplemento da área de trabalho Microsoft Project

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Dependências de Tarefa do Projeto | Dependência de Tarefa do Projeto | Sincronizado | Não sincronizado |
| Dependências de Tarefa do Projeto | Tipo de Link | Sincronizado | Não sincronizado |
| Dependências de Tarefa do Projeto | Tarefa Antecessora | Sincronizado | Não sincronizado |
| Dependências de Tarefa do Projeto | Project | Sincronizado | Não sincronizado |
| Dependências de Tarefa do Projeto | Tarefa Sucessora | Sincronizado | Não sincronizado |

### <a name="additional-resources"></a>Recursos adicionais
 [Guia do gerente de projeto](../psa/project-manager-guide.md)
