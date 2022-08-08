---
title: Sincronize categorias de despesa do projeto entre finanças e operações e o Project Service Automation
description: Este artigo descreve os modelos e as tarefas subjacentes usadas para sincronizar categorias de despesa do projeto entre o Microsoft Dynamics 365 Finance e o Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8eba7defb93bd880db4b0e8fe425d07312cf5cb9
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028918"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sincronize categorias de despesa do projeto entre finanças e operações e o Project Service Automation

[!include[banner](../includes/banner.md)]

Este artigo descreve os modelos e as tarefas subjacentes usadas para sincronizar categorias de despesa do projeto entre o Dynamics 365 Finance e o Dynamics 365 Project Service Automation.

> [!NOTE]
> - A integração de tarefas de projeto, as categorias de transação de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.
> - A integração dos valores reais está disponível na versão 8.0.1 ou posterior.
> - Se você estiver usando a Enterprise Edition 7.3.0, após instalar o KB 4132657 e o KB 4132660, será possível usar os modelos para integrar as tarefas de projeto, as categorias de transação, as estimativas de horas, as estimativas de despesas e os dados reais, além de configurar o bloqueio de funcionalidades. Caso seja necessário redefinir as distribuições contábeis, recomendamos instalar o KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Fluxo de dados para Project Service Automation e o Finance

A solução de integração do Project Service Automation e do Finance usa o recurso de Integração de dados para sincronizar dados em instâncias do Project Service Automation e do Finance. Os modelos de integração disponíveis com o recurso de Integração de dados permitem o fluxo de dados sobre categorias de transação de despesas do projeto entre o Finance e o Project Service Automation.

Se as categorias de despesas do projeto forem masterizadas em Finance, o fluxo de integração será primeiro do Finance para o Project Service Automation. A integração de IDs das categorias de despesas do projeto serão atualizadas por meio de sincronização do Project Service Automation para o Finance.

Se as categorias de despesas do projeto forem masterizadas em Project Service Automation, o fluxo de integração será primeiro do serviço de projeto para o Finance. As categorias de projeto já devem estar configuradas no Finance antes da sincronização do Project Service Automation. Em seguida, sincronize do Finance para o Project Service Automation e depois do Project Service Automation para o Finance novamente. Dessa forma, você ajuda a garantir que as categorias sejam vinculadas e que nenhuma duplicata seja criada.

> [!NOTE]
> Normalmente, as categorias de despesas de projeto são masterizadas no Finance. No entanto, caso não sejam ou se as categorias de despesas já tiverem sido criadas no Project Service Automation, é necessário sincronizar primeiro usando o modelo de categorias de transação de despesas do Projeto (PSA para Fin e Ops). Em seguida, sincronize usando o modelo de categorias de transação de despesas do Projeto (Fin e Ops para PSA). Em seguida, é necessário executar a sincronização do Project Service Automation para o Finance mais uma vez.
>
> Se você sincronizar o Project Service Automation primeiro, os seguintes requisitos devem ser atendidos no Finance antes que a sincronização seja executada:
>
> - A categoria compartilhada que corresponde à categoria do projeto configurada no Project Service Automation deve existir e deve estar habilitada para **Projeto** e **Despesa**.
> - Para cada entidade legal do Finance à qual deve estar integrada, as seguintes categorias de projeto devem existir:
>
>     - A **Categoria de projeto** existe. 
>     - **Usar em Despesa** está habilitado.
>     - **Ativo no diário** está habilitado.
>     - O **Tipo de transação** está definido como **Despesa**.

A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation ao Finance.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sincronização de categorias de despesas de projeto do Finance para o Project Service Automation

### <a name="template-and-task"></a>Modelo e tarefa

Para acessar o modelo, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

O seguinte modelo e a tarefa subjacente são usados para sincronizar as categorias de despesas de projeto do Finance com o Project Service Automation:

- **Nome do modelo na Integração de dados:** categorias de transação de despesas do Projeto (Fin e Ops para PSA)
- **Nome da tarefa raiz no projeto:** sincronizar categorias com o PSA

### <a name="entity-set"></a>Conjunto de entidades

| Financeiro                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entidade da integração para categorias | Categorias de transação     |

### <a name="entity-flow"></a>Fluxo de entidade

As categorias de despesas de projeto são gerenciadas em Finance e podem ser sincronizadas com o Project Service Automation como categorias de transação.

### <a name="power-query"></a>Power Query

Ao sincronizar com o Project Service Automation, você deve usar o Microsoft Power Query para Excel para definir o tipo de cobrança na categoria de transação. O modelo de categorias de transação de despesas do Projeto (Fin e Ops para PSA) oferece um mapeamento e uma coluna padrão. Se você criar seu próprio modelo, adicione uma coluna condicional no Power Query. Siga estas etapas.

1. Clique na seta para abrir o mapeamento da tarefa de categorias de despesas de projeto no modelo de categorias de transação de despesas do Projeto (Fin e Ops para PSA).
2. Clique no link **Consulta e Filtragem Avançadas** para abrir o Power Query.
2. Selecione **Adicionar Coluna Condicional**.
3. Insira um nome para a nova coluna, como **TipoCobrança**.
4. Insira a seguinte condição: **se CATEGORYID não for igual a nulo, ele será 19235001; caso contrário, ele será nulo**.
5. Clique em **OK** na coluna.
6. Certifique-se de mapear essa nova coluna na página de mapeamento.

A ilustração a seguir mostra um exemplo do mapeamento de tarefas do modelo na integração de dados. O mapeamento mostra as informações de campo que serão sincronizadas do Finance para o Project Service Automation.

[![Categoria de despesas do projeto para mapeamento de modelo do Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sincronização de categorias de despesas de projeto do Project Service Automation para o Finance

### <a name="template-and-task"></a>Modelo e tarefa

O seguinte modelo e a tarefa subjacente são usados para sincronizar as categorias de despesas de projeto do Project Service Automation com o Project Service Automation:

- **Nome do modelo na Integração de dados:** categorias de transação de despesas do Projeto (PSA para Fin e Ops)
- **Nome da tarefa raiz no projeto:** sincronizar categorias com o Fin Ops

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Financeiro                           |
|----------------------------|-----------------------------------|
| Categorias de transação     | Entidade da integração para categorias |

### <a name="entity-flow"></a>Fluxo de entidade

As categorias de despesas de projeto são gerenciadas em Finance e podem ser sincronizadas com o Project Service Automation como categorias de transação. A nova sincronização para o Finance atualiza a categoria do projeto no Finance com a ID de integração do Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na integração de dados

A ilustração a seguir mostra um exemplo do mapeamento de tarefas do modelo na integração de dados.

> [!NOTE]
> O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.

[![Mapeamento de modelo do Project Service Automation ao Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]