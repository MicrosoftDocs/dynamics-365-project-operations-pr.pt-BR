---
title: Logs de agendamento de projetos
description: Este tópico fornece informações e exemplos que o ajudarão a usar os logs de Agendamento de Projeto para rastrear falhas relacionadas ao Serviço de Agendamento de Projeto e APIs de Agendamento de Projeto.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589504"
---
# <a name="project-scheduling-logs"></a>Logs de agendamento de projetos

_**Aplicável a:** Project Operations para cenários baseados em recursos/sem estoque, Implantação lite – gerenciar faturamento pro forma_, _Project for the Web_

O Microsoft Dynamics 365 Project Operations usa o [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) como o mecanismo de agendamento principal. Em vez de usar as interfaces de programação de aplicativos (APIs) do Microsoft Dataverse padrão da Web, o Project Operations usa as novas APIs de Agendamento de Projeto para criar, atualizar e excluir tarefas de projeto, atribuições de recursos, dependências de tarefas, buckets de projeto e membros de equipes de projeto. No entanto, quando as operações de criação, atualização ou exclusão são executadas programaticamente em entidades de detalhamento de trabalho (WBS), podem ocorrer erros. Para rastrear esses erros e o histórico de operações, dois novos logs administrativos foram implementados: **Conjunto de Operações** e **Serviço de Agendamento de Projeto (PSS)**. Para acessar esses logs, vá para **Configurações** \> **Integração de Agenda**.

A ilustração a seguir mostra o modelo de dados para logs de Agendamento de Projeto.

![Modelo de dados para os logs de Agendamento do Projeto.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Log do Conjunto de Operações

O log do Conjunto de Operações rastreia a execução de um conjunto de operações usado para executar uma ou várias operações de criação, atualização ou exclusão em um lote em projetos, tarefas de projeto, atribuições de recursos, dependências de tarefas, buckets de projeto ou membros da equipe do projeto. O campo **Operação em Status** mostra o status geral do conjunto de operações. Os detalhes do conteúdo do conjunto de operações são capturados em registros de Detalhes do Conjunto de Operações relacionados.

### <a name="operation-set"></a>Conjunto de Operações

A tabela a seguir mostra os campos relacionados à entidade **Conjunto de Operações**.

| SchemaName            | Descrição                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | A data/hora quando o conjunto de operações foi concluído ou falhou.                                                | CompletedOn            |
| msdyn_correlationid   | O valor **correlationId** da solicitação.                                                                  | CorrelationId          |
| msdyn_description     | A descrição do conjunto de operações.                                                                        | Description            |
| msdyn_executedon      | A data/hora em que o registro foi executado.                                                                       | Execução em            |
| msdyn_operationsetId  | O identificador exclusivo de instâncias da entidade.                                                                   | OperationSet           |
| msdyn_Project         | O projeto que está relacionado ao conjunto de operações.                                                            | Projeto                |
| msdyn_projectid       | O valor **projectId** da solicitação.                                                                      | ProjectId (Preterido) |
| msdyn_projectName     | Não aplicável.                                                                                              | Não aplicável         |
| msdyn_PSSErrorLog     | O identificador exclusivo do log de erros do Serviço de Agendamento de Projeto associado ao conjunto de operações. | Log de Erros do PSS          |
| msdyn_PSSErrorLogName | Não aplicável.                                                                                              | Não aplicável         |
| msdyn_status          | O status do conjunto de operações.                                                                             | Status                 |
| msdyn_statusName      | Não aplicável.                                                                                              | Não aplicável         |
| msdyn_useraadid       | A ID do objeto Azure Active Directory (Azure AD) do usuário ao qual a solicitação pertence.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalhes do Conjunto de Operações

A tabela a seguir mostra os campos relacionados à entidade **Detalhes do Conjunto de Operações**.

| SchemaName                 | Descrição                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Campos serializados do Dataverse para a solicitação.                                            | CdsPayload            |
| msdyn_entityname           | O nome da entidade para a solicitação.                                                     | EntityName            |
| msdyn_httpverb             | O método de solicitação.                                                                         | Verbo HTTP (Preterido) |
| msdyn_httpverbName         | Não aplicável.                                                                             | Não aplicável        |
| msdyn_operationset         | O identificador exclusivo do conjunto de operações ao qual o registro pertence.                      | OperationSet          |
| msdyn_operationsetdetailId | O identificador exclusivo de instâncias da entidade.                                                  | Detalhe do OperationSet   |
| msdyn_operationsetName     | Não aplicável.                                                                             | Não aplicável        |
| msdyn_operationtype        | O tipo de operação dos detalhes do conjunto de operações.                                             | OperationType         |
| msdyn_operationtypeName    | Não aplicável.                                                                             | Não aplicável        |
| msdyn_psspayload           | Os campos serializados do Serviço de Agendamento de Projeto para a solicitação.                           | PssPayload            |
| msdyn_recordid             | O identificador do registro da solicitação.                                                       | ID de Registro             |
| msdyn_requestnumber        | Um número gerado automaticamente que identifica a ordem em que as solicitações foram recebidas | Número da Solicitação        |

## <a name="project-scheduling-service-error-logs"></a>Logs de erros do Serviço de Agendamento de Projeto

Os logs de erros do Serviço de Agendamento de Projeto capturam falhas que ocorrem quando o Serviço de Agendamento de Projeto tenta uma operação **Salvar** ou **Abrir**. Existem três cenários compatíveis em que esses logs são gerados:

- As ações iniciadas pelo usuário falham criticamente (por exemplo, uma atribuição não pode ser criada devido à falta de privilégios).
- O Serviço de Agendamento de Projeto não pode criar, atualizar, excluir ou executar outras operações em cascata em uma entidade de forma programática.
- O usuário encontra erros quando um registro falha ao abrir (por exemplo, quando um projeto é aberto ou as informações de um membro da equipe são atualizadas).

### <a name="project-scheduling-service-log"></a>Log do Serviço de Agendamento de Projeto

A tabela a seguir mostra os campos que são incluídos no log do Serviço de Agendamento de Projeto.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | A pilha de chamadas da exceção.                                               | Pilha de Chamadas     |
| msdyn_correlationid | A ID de correlação do erro.                                               | CorrelationId  |
| msdyn_errorcode     | Um campo que é usado para armazenar o código de erro do Dataverse ou o código de erro HTTP. | Código de Erro     |
| msdyn_HelpLink      | Um link da documentação pública de ajuda.                                       | Link de Ajuda      |
| msdyn_log           | O log do Serviço de Agendamento de Projeto.                                   | Log            |
| msdyn_project       | O projeto que é associado ao log de erros.                             | Project        |
| msdyn_projectName   | O nome do projeto se o conteúdo do conjunto de operações for persistente. | Não aplicável |
| msdyn_psserrorlogId | O identificador exclusivo de instâncias da entidade.                                     | Log de Erros do PSS  |
| msdyn_SessionId     | A ID da sessão do projeto.                                                        | Id da Sessão     |

## <a name="error-log-cleanup"></a>Limpeza do log de erros

Por padrão, os logs de erro do Serviço de Agendamento de Projeto e o log do Conjunto de Operações podem ser limpos a cada 90 dias. Registros com mais de 90 dias serão excluídos. No entanto, ao alterar o valor do campo **msdyn_StateOperationSetAge** na página **Parâmetros do Projeto**, os administradores podem ajustar o intervalo de limpeza para que ocorra entre 1 e 120 dias. Vários métodos para alterar este valor estão disponíveis:

- Personalize a entidade **Parâmetro do Projeto** criando uma página personalizada e adicionando o campo **Idade do Conjunto de Operações Obsoleto**.
- Use o código do cliente que utiliza o [Kit de desenvolvimento de software WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Use o código do Service SDK que usa o método **updateRecord** de Xrm SDK (referência da API do cliente) em aplicativos baseados em modelo. O Power Apps inclui uma descrição e parâmetros compatíveis para o método **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
