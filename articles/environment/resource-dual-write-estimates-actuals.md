---
title: Integração de estimativas e dados reais do projeto
description: Este artigo fornece informações sobre a integração de gravação dupla no Project Operations para estimativas e dados reais de projetos.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029066"
---
# <a name="project-estimates-and-actuals-integration"></a>Integração de estimativas e dados reais do projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo fornece informações sobre a integração de gravação dupla no Project Operations para estimativas e dados reais de projetos.

## <a name="project-estimates"></a>Estimativas do projeto

As estimativas de mão de obra, despesas e materiais do projeto são criadas e mantidas no Microsoft Dataverse e sincronizadas com os aplicativos de finanças e operações para fins de contabilidade. Não há suporte às operações de criação, atualização e exclusão nos aplicativos de finanças e operações.

A criação de estimativas exige uma configuração de contabilidade válida para o projeto. Os projetos associados a linhas de contrato devem ter um perfil de custo e receita de projeto válido definido nas regras de perfil de custo e receita do projeto. Para obter mais informações, consulte [Configure a contabilidade para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimativas de mão de obra

Estimativas de mão de obra são criadas pelo Project Manager ou pelo gerente de recursos que também atribui um recurso genérico ou nomeado à tarefa do projeto. Os registros de atribuição de recursos podem ser revisados na guia **Atribuições de recursos** na página **Detalhes do Projeto** no Dataverse. Os registros de atribuição de recursos no Dataverse criam registros de previsão de horas nos aplicativos de finanças e operações usando a **Entidade de integração do Project Operations para estimativas de horas estimativas de horas (msdyn\_resourceassignments)**.

   ![Integração de estimativas de mão de obra.](./Media/DW4LaborEstimates.png)

A gravação dupla sincroniza registros de atribuição de recursos com a tabela de preparo (**ProjCDSEstimateHoursImport**) e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de horas (**ProjForecastEmpl**).

Para revisar a previsão de registros de horas criados em aplicativos de finanças e operações, o contador do projeto vai para **Gerenciamento e contabilidade de projeto** > **Todos os projetos** > **Plano** > **Previsões de horas**.

## <a name="expense-estimates"></a>Estimativas de despesas

As estimativas de despesas são criadas pelo gerente de projeto na guia **Estimativas de Despesas** na página **Detalhes do Projeto** no Dataverse. Os registros de estimativa de despesas são armazenados na entidade **Linha de Estimativa** no Dataverse. Esses registros de estimativas têm a classe de transação **Despesa** e são sincronizados com registros de previsão de despesas em aplicativos de finanças e operações usando a **Entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimatelines)**.

   ![Integração de estimativas de despesas.](./Media/DW4ExpenseEstimates.png)

A gravação dupla sincroniza registros de estimativas de despesas para a tabela de preparo **ProjCDSEstimateExpenseImport** e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de despesas (**ProjForecastCost**). As linhas de estimativa armazenam a estimativa de vendas e os registros de estimativa de custo separadamente. A lógica de negócios nos aplicativos de finanças e operações preenche um único registro de previsão de despesas usando esse detalhe na tabela de preparo.

Para revisar a previsão de registros de despesas em aplicativos de finanças e operações, o contador do projeto vai para **Gerenciamento e contabilidade de projeto** > **Todos os projetos** > **Plano** > **Previsões de despesas**.

## <a name="material-estimates"></a>Estimativas de material

As estimativas de material são criadas pelo gerente de projeto na guia **Estimativas de material** na página **Detalhes do Projeto** no Dataverse. Os registros de estimativa de material são armazenados na entidade **Linha de Estimativa** no Dataverse. Esses registros de estimativas têm a classe de transação **Material** e são sincronizados com registros de previsão de itens em aplicativos de finanças e operações usando a **Tabela de integração de projeto para estimativas de materiais (msdyn\_estimatelines)**.

   ![Integração de estimativas de material.](./Media/DW4MaterialEstimates.png)

A gravação dupla sincroniza registros de estimativas de material para a tabela de preparo, **ProjForecastSalesImpor** e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de itens (**ForecastSales**). As linhas de estimativa armazenam a estimativa de vendas e os registros de estimativa de custo separadamente. A lógica de negócios nos aplicativos de finanças e operações preenche um único registro de previsão de itens usando esse detalhe na tabela de preparo.

Para revisar a previsão de registros de itens em aplicativos de finanças e operações, o contador do projeto vai para **Gerenciamento e contabilidade de projeto** > **Todos os projetos** > **Plano** > **Previsões de itens**.

## <a name="project-actuals"></a>Dados reais do projeto

Os dados reais do projeto são criados no Dataverse, com base em tempo, despesas, material e atividade de cobrança. Todos os atributos operacionais dessas transações, incluindo quantidade, preço de custo, preço de venda e projeto são capturados nesta entidade do Dataverse. Para obter mais informações, consulte [Dados reais](../actuals/actuals-overview.md). Os registros reais são sincronizados com aplicativos de finanças e operações usando o mapa de tabela de gravação dupla **Valores reais de integração do Project Operations (msdyn\_actuals)** para fins de contabilidade downstream.

   ![Integração de dados reais.](./Media/DW4Actuals.png)

O mapa de tabela **Dados reais de integração do Project Operations** sincroniza todos os registros da entidade **Dados Reais** no Dataverse, com o atributo **Ignorar Sincronização (apenas para uso interno)** definido como **Falso**. Este valor de atributo é definido no Dataverse automaticamente quando o registro é criado. Exemplos em que este atributo é definido como **Verdadeiro**:

  - Dados reais de custo do projeto para transações intercompanhia. Para obter mais informações, consulte [Criar transações intercompanhia](../project-accounting/create-intercompany-transactions.md). Esses registros são ignorados porque o sistema recria o custo real do projeto nos aplicativos de finanças e operações quando a fatura de fornecedor intercompanhia é lançada.
  - Registros negativos de vendas não cobradas criados quando a fatura pro forma é confirmada. Esses registros são ignorados porque a razão auxiliar do projeto nos aplicativos de finanças e operações não reverte o registro de vendas não faturadas no faturamento, mas altera o status para totalmente faturado.

O mapa da tabela de gravação dupla sincroniza os registros de dados reais com a tabela de preparo, **ProjCDSActualsImport**. Esses registros são processados pelo processo periódico **Importar da tabela de preparo** ao criar linhas de diário de integração do Project Operations e linhas de proposta de fatura do projeto. Para obter mais informações, consulte [Diário de integração no Project Operations](../project-accounting/project-operations-integration-journal.md).

O Dataverse também captura os links entre as transações reais do projeto na entidade **Conexão de transação**. Para obter mais informações, consulte [Vincule dados reais a registros originais](../actuals/linkingactuals.md). Os links entre transações reais também são sincronizados com os aplicativos de finanças e operações usando o mapa de tabela de gravação dupla **Entidade de integração para relacionamentos de transações de projeto (msdyn\_transactionconnections)**. Esses registros são usados pelo processo periódico, **Importar da tabela de preparo**, ao criar linhas de diário de integração do Project Operations e linhas de proposta de fatura do projeto.

Postar um diário de integração do Project Operations e uma proposta de fatura de projeto dispara uma atualização nos respectivos registros na tabela de preparo, **ProjCDSActualsImport**. O sistema captura e registra os seguintes atributos de contabilidade para transações de dados reais:

- Valor da moeda contábil
- Taxa de câmbio
- Número do comprovante
- Valor do imposto

O mapa de tabela **Dados reais de integração do Project Operations** atualiza os respectivos registros de dados reais no Dataverse com essas informações.
