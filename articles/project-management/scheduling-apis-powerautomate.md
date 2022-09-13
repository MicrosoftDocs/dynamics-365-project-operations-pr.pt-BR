---
title: Usar APIs de agendamento de projetos com o Power Automate
description: Este artigo fornece um fluxo de exemplo que usa as interfaces de programação de aplicativo (APIs) de agendamento de projetos.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404390"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Usar APIs de agendamento de projetos com o Power Automate

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Este artigo descreve um fluxo de exemplo que mostra como criar um plano de projeto completo usando o Microsoft Power Automate, como criar um Conjunto de Operações e como atualizar uma entidade. O exemplo demonstra como criar um projeto, um membro da equipe do projeto, Conjuntos de Operações, tarefas do projeto e atribuições de recursos. Este artigo também explica como atualizar uma entidade e executar um Conjunto de Operações.

Esta é uma lista completa das etapas documentadas no fluxo de exemplo neste artigo:

1. [Criar um gatilho do PowerApps](#1)
2. [Criar um projeto](#2)
3. [Inicializar uma variável para o membro da equipe](#3)
4. [Criar um membro da equipe genérico](#4)
5. [Criar um Conjunto de Operações](#5)
6. [Criar um bucket do projeto](#6)
7. [Inicializar uma variável para o status do link](#7)
8. [Inicializar uma variável para o número de tarefas](#8)
9. [Inicializar uma variável para a ID da tarefa do projeto](#9)
10. [Fazer até](#10)
11. [Definir uma tarefa do projeto](#11)
12. [Criar uma tarefa do projeto](#12)
13. [Criar uma atribuição de recurso](#13)
14. [Diminuir uma variável](#14)
15. [Renomear uma tarefa do projeto](#15)
16. [Executar um Conjunto de Operações](#16)

## <a name="assumptions"></a>Suposições

Este artigo pressupõe que você tenha conhecimento básico da plataforma Dataverse, de fluxos da nuvem e da interface de programação de aplicativo (API) de agendamento de projetos. Para obter mais informações, consulte a seção [Referências](#references) mais adiante neste artigo.

## <a name="create-a-flow"></a>Criar um fluxo

### <a name="select-an-environment"></a>Selecionar um ambiente

Você pode criar o fluxo do Power Automate em seu ambiente.

1. Vá para <https://flow.microsoft.com> e use suas credenciais de administrador para entrar.
2. No canto superior direito, selecione **Ambientes**.
3. Na lista, selecione o ambiente em que o Dynamics 365 Project Operations está instalado.

### <a name="create-a-solution"></a>Criar uma solução

Siga estas etapas para criar um [fluxo com reconhecimento de solução](/power-automate/overview-solution-flows). Ao criar um fluxo com reconhecimento de solução, você pode exportar o fluxo com mais facilidade para usá-lo posteriormente.

1. No painel de navegação, selecione **Soluções**.
2. Na página **Soluções**, selecione **Nova solução**.
3. Na caixa de diálogo **Nova solução**, defina os campos obrigatórios e selecione **Criar**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Etapa 1: Criar um gatilho do PowerApps

1. Na página **Soluções**, selecione a solução que você criou e selecione **Novo**.
2. No painel esquerdo, selecione **Fluxos da nuvem** \> **Automação** \> **Fluxo da nuvem** \> **Instantâneo**.
3. No campo **Nome do fluxo**, insira **Fluxo de Demonstração da API de Agendamento**.
4. Na lista **Escolher como disparar este fluxo**, selecione **Power Apps**. Quando você cria um gatilho do Power Apps, a lógica depende de você como autor. Neste artigo, deixe os parâmetros de entrada em branco para fins de teste.
5. Selecione **Criar**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Etapa 2: criar um projeto

Siga estas etapas para criar um projeto de amostra.

1. No fluxo que você criou, selecione **Nova etapa**.

    ![Adicionando uma nova etapa.](media/newstep.png)

2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **executar uma ação não associada**. Então, na guia **Ações**, selecione a operação na lista de resultados.

    ![Selecionando uma operação.](media/chooseactiontab.png)

3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.

![Renomeando uma etapa.](media/renamestep.png)

4. Renomeie a etapa **Criar Projeto**.
5. No campo **Nome da Ação**, selecione **msdyn\_CreateProjectV1**.
6. Abaixo do campo **msdyn\_subject**, selecione **Adicionar conteúdo dinâmico**.
7. Na guia **Expressão**, no campo de função, insira **Nome do projeto - utcNow()**.
8. Selecione **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Etapa 3: Inicializar uma variável para o membro da equipe

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **inicializar variável**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Inicializar membro da equipe**.
5. No campo **Nome**, insira **TeamMemberAction**.
6. No campo **Tipo**, selecione **Cadeia de caracteres**.
7. No campo **Valor**, insira **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Etapa 4: Criar um membro da equipe genérico

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **executar uma ação não associada**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Criar Membro da Equipe**.
5. Para o campo **Nome da Ação**, selecione **TeamMemberAction** na caixa de diálogo **Conteúdo dinâmico**.
6. No campo **Parâmetros da Ação**, insira as seguintes informações de parâmetros.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Veja aqui uma explicação dos parâmetros:

    - **\@\@odata.type** – O nome da entidade. Por exemplo, insira **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – A chave primária da ID da equipe do projeto. O valor é uma expressão de identificador global exclusivo (GUID).   A ID é gerada a partir da guia de expressão.

    - **msdyn\_project\@odata.bind** – A ID do projeto proprietário. O valor será o conteúdo dinâmico obtido na resposta da etapa "Criar Projeto". Certifique-se de inserir o caminho completo e adicionar conteúdo dinâmico entre os parênteses. As aspas são obrigatórias. Por exemplo, insira **"/msdyn\_projects(ADICIONAR CONTEÚDO DINÂMICO)"**.
    - **msdyn\_name** – O nome do membro da equipe. Por exemplo, insira **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Etapa 5: Criar um Conjunto de Operações

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **executar uma ação não associada**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Criar um Conjunto de Operações**.
5. No campo **Nome da Ação**, selecione a ação personalizada do Dataverse **msdyn\_CreateOperationSetV1**.
6. No campo **Descrição**, insira **ScheduleAPIDemoOperationSet**.
7. No campo **Projeto**, insira **/msdyn\_projects(**.
8. Na caixa de diálogo **Conteúdo dinâmico**, selecione **msdyn\_CreateProjectV1Response ProjectId**.
9. No campo **Projeto**, insira **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Etapa 6: Criar um bucket do projeto

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **adicionar nova linha**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Criar Bucket**.
5. No campo **Nome da Tabela**, selecione **Buckets do Projeto**.
6. No campo **Nome**, insira **ScheduleAPIDemoBucket1**.
7. No campo **Projeto**, selecione **msdyn\_CreateProjectV1Response ProjectId** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Etapa 7: Inicializar uma variável para o status do link

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **inicializar variável**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Inicializar status do link**.
5. No campo **Nome**, insira **linkstatus**.
6. No campo **Tipo**, selecione **Inteiro**.
7. No campo **Valor**, insira **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Etapa 8: Inicializar uma variável para o número de tarefas

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **inicializar variável**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Inicializar Número de tarefas**.
5. No campo **Nome**, insira **número de tarefas**.
6. No campo **Tipo**, selecione **Inteiro**.
7. No campo **Valor**, insira **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Etapa 9: Inicializar uma variável para a ID da tarefa do projeto

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **inicializar variável**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Inicializar ProjectTaskID**.
5. No campo **Nome**, insira **número de tarefas**.
6. No campo **Tipo**, selecione **Cadeia de caracteres**.
7. Para o campo **Valor**, insira **guid()** no Construtor de Expressões.

## <a name="step-10-do-until"></a><a id="10"></a>Etapa 10: Fazer até

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **fazer até**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Defina o primeiro valor na instrução condicional para a variável **número de tarefas** da caixa de diálogo **Conteúdo dinâmico**.
4. Defina a condição como **menor ou igual a**.
5. Defina o segundo valor na instrução condicional como **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Etapa 11: Definir uma tarefa do projeto

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **definir variável**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na nova etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Definir Tarefa do Projeto**.
5. No campo **Nome**, selecione **msdyn\_projecttaskid**.
6. Para o campo **Valor**, insira **guid()** no Construtor de Expressões.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Etapa 12: Criar uma tarefa do projeto

Siga estas etapas para criar uma tarefa do projeto com uma ID exclusiva que pertence ao projeto atual e ao bucket do projeto que você criou.

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **executar uma ação não associada**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Criar Tarefa do Projeto**.
5. No campo **Nome da Ação**, selecione **msdyn\_PssCreateV1**.
6. No campo **Entidade**, insira as seguintes informações de parâmetros.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Veja aqui uma explicação dos parâmetros:

    - **\@\@odata.type** – O nome da entidade. Por exemplo, insira **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – A ID exclusiva da tarefa. O valor deve ser definido para uma variável dinâmica de **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – A ID do projeto proprietário. O valor será o conteúdo dinâmico obtido na resposta da etapa "Criar Projeto". Certifique-se de inserir o caminho completo e adicionar conteúdo dinâmico entre os parênteses. As aspas são obrigatórias. Por exemplo, insira **"/msdyn\_projects(ADICIONAR CONTEÚDO DINÂMICO)"**.
    - **msdyn\_subject** – Nome de qualquer tarefa.
    - **msdyn\_projectbucket\@odata.bind** – O bucket do projeto que contém as tarefas. O valor será o conteúdo dinâmico obtido na resposta da etapa "Criar Bucket". Certifique-se de inserir o caminho completo e adicionar conteúdo dinâmico entre os parênteses. As aspas são obrigatórias. Por exemplo, insira **"/msdyn\_projectbuckets(ADICIONAR CONTEÚDO DINÂMICO)"**.
    - **msdyn\_start** – Conteúdo dinâmico para data de início. Por exemplo, amanhã será representado como **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – A data de início agendada. Por exemplo, amanhã será representado como **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – A data de término agendada. Selecione uma data no futuro. Por exemplo, especifique **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – O status do link. Por exemplo, insira **"192350000"**.

7. No campo **OperationSetId**, selecione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Etapa 13: Criar uma atribuição de recurso

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **executar uma ação não associada**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Criar Atribuição**.
5. No campo **Nome da Ação**, selecione **msdyn\_PssCreateV1**.
6. No campo **Entidade**, insira as seguintes informações de parâmetros.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. No campo **OperationSetId**, selecione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Etapa 14: Diminuir uma variável

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **diminuir variável**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. No campo **Nome**, selecione **número de tarefas**.
4. No campo **Valor**, insira **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Etapa 15: Renomear uma tarefa do projeto

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **executar uma ação não associada**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Renomear Tarefa do Projeto**.
5. No campo **Nome da Ação**, selecione **msdyn\_PssUpdateV1**.
6. No campo **Entidade**, insira as seguintes informações de parâmetros.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. No campo **OperationSetId**, selecione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Etapa 16: Executar um Conjunto de Operações

1. No fluxo, selecione **Nova etapa**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, insira **executar uma ação não associada**. Então, na guia **Ações**, selecione a operação na lista de resultados.
3. Na etapa, selecione as reticências (**...**) e, em seguida, **Renomear**.
4. Renomeie a etapa **Executar um Conjunto de Operações**.
5. No campo **Nome da Ação**, selecione **msdyn\_ExecuteOperationSetV1**.
6. No campo **OperationSetId**, selecione **msdyn\_CreateOperationSetV1Response OperationSetId** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="references"></a>Referências

- [Visão geral de como integrar fluxos com o Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Use APIs de agendamento do Project para realizar operações com entidades de Agendamento](schedule-api-preview.md)
- [Visão geral dos fluxos da nuvem - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Visão geral dos fluxos com reconhecimento de solução - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
