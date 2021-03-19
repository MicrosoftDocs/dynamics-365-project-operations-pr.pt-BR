---
title: Sincronizar estimativas de projetos diretamente do Project Service Automation para o Finance and Operations
description: Este tópico descreve os modelos e as tarefas subjacentes usados para sincronizar as estimativas de horas e de despesas do projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 58e204b2c1238e00ffb16533cc82dad69fbf77a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289445"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizar estimativas de projetos diretamente do Project Service Automation para o Finance and Operations

[!include[banner](../includes/banner.md)]

Este tópico descreve os modelos e as tarefas subjacentes usados para sincronizar as estimativas de horas e de despesas do projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.

> [!NOTE]
> - Integração de tarefas do projeto, categorias de transações de despesas, estimativas de horas, estimativas de despesas e bloqueio de funcionalidade estão disponíveis na versão 8.0.
> - A integração dos valores reais está disponível na versão 8.0.1 ou posterior.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de dados do Project Service Automation para o Finance

A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Project Service Automation e do Finance. Os modelos de integração disponíveis com o recurso de integração de dados permitem transferir dados sobre estimativas de horas e de despesas do projeto do Project Service Automation para o Finance.

A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation ao Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimativas de horas do projeto

### <a name="template-and-tasks"></a>Modelo e tarefas

Para acessar os modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

O seguinte modelo e as tarefas subjacentes são usados para sincronizar estimativas de horas do projeto do Project Service Automation para o Finance:

- **Nome do modelo na integração de dados:** Estimativas de horas do projeto (PSA para Fin and Ops)
- **Nome das tarefas no projeto:**

    - Relacionamentos de transações
    - Estimativas de despesas

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Financeiro                                       |
|----------------------------|-----------------------------------------------|
| Tarefas do projeto              | Entidade de integração para estimativas de horas do projeto |

### <a name="entity-flow"></a>Fluxo da entidade

As estimativas de horas do projeto são gerenciados no Project Service Automation e são sincronizados com o Finance como previsões de horas do projeto.

### <a name="prerequisites"></a>Pré-requisitos

Para que a sincronização das estimativas de horas do projeto ocorra, você deve primeiro sincronizar projetos, tarefas do projeto e categorias de transações das despesas do projeto.

### <a name="power-query"></a>Power Query

No modelo de estimativas de horas do projeto, você deve usar o Microsoft Power Query para Excel para concluir estas tarefas:

- Definir a ID do modelo de previsão padrão que será usada quando a integração criar novas previsões de horas.
- Filtrar todos os registros específicos de recursos na tarefa que terão falha na integração com previsões de horas.
- Filtrar todas as linhas de categoria de transação vazias. A falha na conclusão dessa tarefa poderá resultar em previsões de horas incorretas.

#### <a name="set-the-default-forecast-model-id"></a>Definir a ID do modelo de previsão padrão

Para atualizar a ID do modelo de previsão padrão no modelo, clique na seta **Mapear** para abrir o mapeamento. Em seguida, selecione o link **Consulta e filtragem avançadas**.

- Se você estiver usando o modelo de estimativas de horas do projeto padrão (PSA para Fin and Ops), selecione a **Condição inserida** na lista de **Etapas aplicadas**. Na entrada da **Função**, substitua **O\_forecast** pelo nome da ID do modelo de previsão que deve ser usado com a integração. O modelo padrão tem uma ID do modelo de previsão nos dados de demonstração.
- Se estiver criando um novo modelo, você deverá adicionar essa coluna. Em Power Query, selecione **Adicionar coluna condicional** e insira um nome para a nova coluna, como **IDModelo**. Insira a condição para a coluna, em que, se a tarefa do projeto não for nula (null), então \<enter the forecast model ID\>; senão nula (null).

#### <a name="filter-out-resource-specific-records"></a>Filtrar registros específicos de recursos

O modelo de estimativas de horas do projeto (PSA para Fin and Ops) tem um filtro padrão que remove todos os registros específicos do recurso. Se você criar seu próprio modelo, deverá adicionar esse filtro. Selecione o link **Consulta e filtragem avançadas** para filtrar na coluna **msdyn\_islinetask** para que apenas registros com resultado **Falso** sejam são incluídos.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrar linhas de categoria de transação vazias

Você deve adicionar um filtro para remover todas as linhas que possuem categorias de transação vazias. Essa tarefa é necessária, independentemente de você estar usando o modelo padrão ou criando seu próprio modelo. Esse filtro remove todas as linhas de resumo do Project Service Automation que possam fazer com que as previsões de horas no Finance fiquem incorretas. Selecione o link **Consulta e filtragem avançadas** para filtrar registros nulos na coluna **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na integração de dados

A ilustração a seguir mostra um exemplo do mapeamento de tarefas do modelo na integração de dados. O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.

[![Mapeamento de tarefa de modelo na integração de dados](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Estimativas de despesas do projeto

### <a name="template-and-tasks"></a>Modelo e tarefas

O seguinte modelo e as tarefas subjacentes são usados para sincronizar estimativas de despesas do projeto do Project Service Automation para o Finance:

- **Nome do modelo na integração de dados:** Estimativas de despesas do projeto (PSA para Fin and Ops)
- **Nome das tarefas no projeto:**

    - Relacionamentos de transações 
    - Estimativas de despesas

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Financeiro                                                  |
|----------------------------|----------------------------------------------------------|
| Conexões da Transação    | Entidade de integração para relacionamentos de transações do projeto |
| Linhas de Estimativa             | Entidade de integração para estimativas de despesas do projeto         |

### <a name="entity-flow"></a>Fluxo da entidade

As estimativas de despesas do projeto são gerenciados no Project Service Automation e são sincronizados com o Finance como previsões de despesas do projeto.

### <a name="prerequisites"></a>Pré-requisitos

Para que a sincronização das estimativas de despesas do projeto ocorra, você deve primeiro sincronizar projetos, tarefas do projeto e categorias de transações das despesas do projeto.

### <a name="power-query"></a>Power Query

No modelo de estimativas de despesas do projeto, você deve usar o Microsoft Power Query para Excel para concluir estas tarefas:

- Filtrar para incluir apenas registros de linha de estimativas de despesas.
- Definir a ID do modelo de previsão padrão que será usada quando a integração criar novas previsões de horas.
- Transformar os tipos de cobrança.
- Transformar os tipos de transação.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrar para incluir apenas linhas de estimativas de despesas

O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) tem um filtro padrão que inclui apenas as linhas de despesas na integração. Se você criar seu próprio modelo, deverá adicionar esse filtro. Selecione a tarefa **Relacionamentos de transações** e, em seguida, clique na seta **Mapear** para abrir o mapeamento. Selecione o link **Consulta e filtragem avançadas**. Filtre a coluna **msdyn\_transactiontype1** para que inclua apenas **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Definir a ID do modelo de previsão padrão

Para atualizar a ID do modelo de previsão padrão no modelo, selecione a tarefa **Estimativas de despesas** e, em seguida, clique na seta **Mapear** para abrir o mapeamento. Selecione o link **Consulta e filtragem avançadas**.

- Se você estiver usando o modelo de estimativas de despesas do projeto padrão (PSA para Fin and Ops), no Power Query, selecione a primeira **Condição inserida** na seção **Etapas aplicadas**. Na entrada da **Função**, substitua **O\_forecast** pelo nome da ID do modelo de previsão que deve ser usado com a integração. O modelo padrão tem uma ID do modelo de previsão nos dados de demonstração.
- Se estiver criando um novo modelo, você deverá adicionar essa coluna. Em Power Query, selecione **Adicionar coluna condicional** e insira um nome para a nova coluna, como **IDModelo**. Insira a condição para a coluna, em que, se a ID de linha da estimativa não for nula (null), então \<enter the forecast model ID\>; senão nula (null).

#### <a name="transform-the-billing-types"></a>Transformar os tipos de cobrança

O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é usada para transformar os tipos de cobrança que são recebidos do Project Service Automation durante a integração. Se você criar seu próprio modelo, deverá adicionar essa coluna condicional. Selecione o link **Consulta e filtragem avançadas** e, em seguida, **Adicionar coluna condicional**. Insira um nome para a nova coluna, como **TipoCobrança**. Depois, insira a seguinte condição:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformar os tipos de transação

O modelo de estimativas de despesas do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é usada para transformar os tipos de transação que são recebidos do Project Service Automation durante a integração. Se você criar seu próprio modelo, deverá adicionar essa coluna condicional. Selecione o link **Consulta e filtragem avançadas** e, em seguida, **Adicionar coluna condicional**. Insira um nome para a nova coluna, como **TipoTransação**. Depois, insira a seguinte condição:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na integração de dados

As ilustrações a seguir mostram exemplos de mapeamentos de tarefas do modelo na integração de dados. O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.

[![Mapeamento de modelo de transações de estimativa de despesas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mapeamento de modelo de estimativas de despesas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]