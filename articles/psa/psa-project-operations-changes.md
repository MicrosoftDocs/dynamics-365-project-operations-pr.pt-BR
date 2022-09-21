---
title: Alterações de recursos do Project Service Automation para o Project Operations
description: Este artigo fornece uma visão geral das alterações de recursos do Project Service Automation para o Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459912"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Alterações de recursos do Project Service Automation para o Project Operations

A atualização do Dynamics 365 Project Service Automation para o Dynamics 365 Project Operations Lite será entregue em três fases. Este artigo fornece informações sobre as principais alterações esperadas quando a atualização for concluída.

| Entrega da atualização | Fase 1 <br>(Janeiro de 2022) | Fase 2 <br>(Novembro de 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nenhuma dependência da estrutura de detalhamento de trabalho (WBS) para projetos. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A WBS está incluída nos limites atualmente compatíveis do Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| A WBS fora dos limites atualmente compatíveis do Project Operations, incluindo suporte para o Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Gerenciamento de projetos

As mudanças mais significativas na experiência do usuário serão na área de planejamento de projetos. O Project Operations adota uma nova experiência moderna para gerenciar uma estrutura de detalhamento de trabalho (WBS), aproveitando os recursos de agendamento fornecidos pelo [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Diferenças na experiência de agendamento

A tabela a seguir resume as diferenças de agendamento entre o Project Service Automation e o Project Operations.

|  Agendamento     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Modelos de projeto - Capacidade de definir e aplicar modelos de projeto quando um projeto é criado  |  &nbsp;    | :heavy_check_mark: |
| Integração da estrutura de detalhamento de trabalho (WBS) do projeto com o cliente de desktop   |    &nbsp;  | :heavy_check_mark: |
| Restrições - Não iniciar antes de, não terminar depois de  | :heavy_check_mark: |   &nbsp;  |
| Etapas - Tarefas com duração zero   | :heavy_check_mark:  |  &nbsp;  |
| As tarefas orientadas por recursos respeitarão a disponibilidade de recursos atribuídos   | :heavy_check_mark: |  &nbsp;    |
| Edição em fases - Edite planos e trabalhe diariamente   |   &nbsp;  | :heavy_check_mark: |
| Agendamento automático/manual - Use o mecanismo de agendamento do Project para agendar tarefas de forma automática ou manual |  &nbsp; | :heavy_check_mark:  |
| Edite projetos grandes diretamente na interface do usuário: não há limite de tamanho dos planos editáveis  | Limite de 500 tarefas  | :heavy_check_mark:       |
| Porcentagem concluída - Marcar o andamento da tarefa   | :heavy_check_mark:  |  &nbsp;  |
| [Modos de Agendamento do Projeto](../project-management/scheduling-modes.md) - Defina o projeto com unidades fixas, esforço fixo ou duração fixa | :heavy_check_mark: | &nbsp; |
| Linha do tempo - Crie e personalize a exibição da linha do tempo para visualizar detalhes de agendamento e se comunicar com os participantes. | :heavy_check_mark:  | &nbsp; |
| Tarefas orientadas por esforço - Suporte do mecanismo de agendamento para agendar uma tarefa conforme o esforço  | :heavy_check_mark:  | &nbsp; |
| Caixa de diálogo **Informações da tarefa** - Salve detalhes da tarefa usando uma caixa de diálogo | :heavy_check_mark:  |  &nbsp;  |
| Arrastar e soltar - Selecione várias tarefas e modifique sua posição na WBS | :heavy_check_mark: | &nbsp;  |
| Exibições persistentes flexíveis - Defina exibições mais granulares dos atributos da tarefa   | :heavy_check_mark:  | &nbsp; |
| Classificar e filtrar a WBS  | :heavy_check_mark:  | &nbsp; |
| Exibição de Boards para entrega de projetos sem cascata  | :heavy_check_mark:   | &nbsp; |
| Exibição da linha do tempo - Gráfico de Gantt interativo usado para visualizar e editar a WBS   | :heavy_check_mark:  | &nbsp; |
| Atalhos de teclado - Use atalhos de teclado para operações comuns, como recuar ou inserir  | :heavy_check_mark:  |  &nbsp; |
| Desfazer em vários níveis - Execute análises de hipóteses para entender completamente o impacto das alterações revertendo e reaplicando um conjunto inteiro de operações | :heavy_check_mark: | &nbsp; |
| Recortar/Copiar/Colar - Colabore no desenvolvimento da agenda e colando os detalhes da agenda entre aplicativos  | :heavy_check_mark: | &nbsp; |
| Listas de verificação de tarefas - Adicione até 20 itens da lista de verificação a uma tarefa   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planejamento do projeto

A página **Projeto** no Project Operations tem um número significativo de diferenças em comparação com a página **Projeto** no Project Service Automation.

As seguintes ações foram removidas da página **Projetos** como parte da atualização da Fase 1:

  - **Abrir no MS Project**
  - **Criar Modelo**
  - **Desvincular do MS Project**

A página **Projeto** no Project Operations inclui as novas guias a seguir.

- **Estimativas de Material**
- **Configuração de Cobrança da Tarefa**

A guia **Status** foi removida e o campo **Status** agora fica na guia **Resumo** com o modo de agendamento do projeto.

   ![Atualizações na página Projeto.](media/projectform.png)

A guia **Agenda** foi renomeada como guia **Tarefa** e apresenta a nova experiência de planejamento de projetos com Project for the Web.

   ![Nova guia Tarefas do projeto.](media/tasktab.png)

## <a name="scheduling-modes"></a>Modos de agendamento

O Project Operations introduziu um novo recurso, [Modos de agendamento](../project-management/scheduling-modes.md). Todos os projetos existentes do Project Service Automation usarão **Duração Fixa** como padrão no Project Operations. No entanto, o padrão para novos projetos pode ser gerenciado em **Configurações** > **Parâmetros** > **Parâmetro** > **Modo de Agendamento**.

   ![Configurações de parâmetros do projeto para o modo de agendamento.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Limites de planejamento do projeto

O Project Operations depende do Project for the Web para todas as operações de agendamento do projeto. O Project for the Web gerencia a estrutura de detalhamento de trabalho usando os limites da tabela a seguir.

| **Campo**                                          | **Limit**             |
|----------------------------------------------------|-----------------------|
| Total máximo de tarefas para um projeto                  | 500                   |
| Duração máxima total para um projeto               | 3.650 dias (10 anos)  |
| Total máximo de recursos para um projeto              | 300                   |
| Total máximo de links (somente sucessor) para um projeto | 600                   |
| Total máximo de campos personalizados para um projeto          | 10                    |
| Nível máximo de hierarquia                            | 10 níveis             |
| Links máximos (sucessor + predecessor)            | 20                    |
| Duração máxima da tarefa folha                      | 1250 dias             |
| Duração máxima de uma tarefa de resumo                 | 3.650 dias (10 anos)  |
| Recursos máximos atribuídos a uma tarefa               | 20 recursos          |
| Intervalo de datas com suporte para uma tarefa                    | 1/1/2000 a 31/12/2149 |
| Itens da lista de verificação                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Extensibilidade e desenvolvimento do planejamento de projetos

Depois de atualizar para o Project Operations, você deve usar as APIs de Agendamento de Projeto para executar operações de criação, atualização e exclusão nas seguintes entidades:

|   Nome da entidade           |   Nome lógico da entidade       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tarefa do Projeto            | msdyn_projecttask           |
| Dependência de Tarefa do Projeto | msdyn_projecttaskdependency |
| Atribuição de Recurso     | msdyn_resourceassignment    |
| Bucket do Projeto          | msdyn_projectbucket         |
| Membro da Equipe do Projeto     | msdyn_projectteam           |

Se atualmente você tem personalizações que envolvem essas entidades, consulte [Usar APIs de agendamento de projeto para realizar operações com entidades de agendamento](../project-management/schedule-api-preview.md) para obter orientações de implementação.

## <a name="data-model-changes"></a>Alterações do modelo de dados

Como parte da Fase 1 de atualização, há alterações no modelo de dados. Essas alterações são principalmente mudanças de campo para entidades existentes. Na Fase 1, as entidades **msydn_project** e **msdyn_projectteam** são uma refatoração de personalizações. 

> [!IMPORTANT]
> Esta seção será atualizada com entidades adicionais à medida que as fases de atualização futuras forem concluídas.

Os campos a seguir foram substituídos por novos campos.

|   Entity          |   Nome lógico antigo   |   Nome lógico novo    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Os campos a seguir foram adicionados.

|   Entity          |   Nome lógico                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Mostra a agregação das vendas reais de taxa no projeto. Somente para uso no Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Mostra a agregação do custo real dos materiais no projeto. Somente para uso no Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Mostra a agregação das vendas reais de materiais no projeto. Somente para uso no Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | A linha de contrato associada a este projeto. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Este é um campo interno do sistema usado para **Copiar Projeto** relacionado ao Identificador de Correlação. Somente para uso no Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Este é um campo interno do sistema usado para **Copiar Projeto** relacionado ao Identificador de Sessão. Somente para uso no Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Token de Revisão Global xRM da última sincronização do serviço de agendamento do projeto. |
| msdyn_project     | msdyn_msprojectdocument                      | O documento do Microsoft Project que pertence ao projeto. |
| msdyn_project     | msdyn_plannedmaterialcost                    | A agregação do custo planejado dos materiais no projeto. Somente para uso no Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | A agregação das vendas planejadas dos materiais no projeto. Somente para uso no Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programa a que este projeto está relacionado. |
| msdyn_project     | msdyn_quotelineproject                       | A linha de cotação associada a este projeto. |
| msdyn_project     | msdyn_replaylogheader                        | O cabeçalho dos logs de repetição. |
| msdyn_project     | msdyn_schedulemode                           | O modo de agendamento padrão usado em todas as tarefas no projeto.  |
| msdyn_project     | msdyn_taskearlieststart                      | A data de início mais antiga de qualquer tarefa no projeto.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | O membro da equipe do projeto de onde esse membro da equipe do projeto foi copiado. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indica se é necessário criar o requisito de recurso para um membro da equipe genérico criado recentemente.  |
| msdyn_projectteam | msdyn_deletestatus                           | O status de exclusão do membro da equipe para acompanhar se há uma solicitação de exclusão enviada ao serviço de agendamento do projeto e se ele envia uma resposta de volta com êxito dentro o intervalo de tempo esperado. |
| msdyn_projectteam | msdyn_effortcompleted                        | Rastreia o esforço realizado pelo membro da equipe nas atribuições dele. |
| msdyn_projectteam | msdyn_effortremaining                        | Rastreia o esforço a ser realizado pelo membro da equipe nas atribuições dele. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | O período de espera desde quando o membro da equipe envia uma solicitação de exclusão ao serviço de agendamento do projeto até que o membro da equipe seja realmente excluído no Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | O carimbo de data/hora a ser registrado quando a solicitação de exclusão do membro da equipe é enviada ao serviço de agendamento do projeto. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Mostra o membro da equipe do projeto de onde esse membro da equipe do projeto foi copiado.  |

## <a name="project-templates"></a>Modelos de projeto

O Project Operations não oferece suporte para modelos de projeto. No entanto, você pode replicar grande parte da funcionalidade principal com o uso da [API Copiar Projeto](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Suporte ao suplemento da área de trabalho

O suporte para o suplemento da Área de Trabalho do Microsoft Project não estará disponível nas duas primeiras fases da atualização. Na Fase 3, os clientes que tiverem projetos maiores do que os limites atualmente suportados do Project for the Web poderão usar o suplemento da área de trabalho.

## <a name="editing-resource-assignment-contours"></a>Edição de contornos de atribuição de recursos

A capacidade de editar os contornos de atribuição de recursos estará disponível com a Fase 2 de atualização.

## <a name="billing-and-pricing"></a>Cobrança e preço

Os novos recursos a seguir foram adicionados no Project Operations. Esses recursos são de natureza aditiva e não afetam o modelo de dados do Project Service Automation.

- [Registro do uso de material em projetos e tarefas de projeto](../material/material-usage-log.md)
- [Gerenciamento de subcontratos](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos baseados em adiantamentos e honorários](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status e validações de contrato que não devem ser não excedidos](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Cobrança baseada em tarefas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Componentes preteridos

As tabelas a seguir documentam todos os campos preteridos que serão movidos para a solução de componentes preteridos após a atualização. Para obter mais informações e um link para a solução, consulte [Dynamics 365 Project Service Automation 3x to Project Operations 4x deprecated components](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

