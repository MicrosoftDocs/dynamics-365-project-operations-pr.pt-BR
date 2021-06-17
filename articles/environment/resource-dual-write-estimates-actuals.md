---
title: Integração de estimativas e dados reais do projeto
description: Este tópico fornece informações sobre a integração de gravação dupla do Project Operations para estimativas e dados reais do projeto.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d8aa1541a3560db175acead1d000895312b299db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000017"
---
# <a name="project-estimates-and-actuals-integration"></a>Integração de estimativas e dados reais do projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico fornece informações sobre a integração de gravação dupla do Project Operations para estimativas e dados reais do projeto.

## <a name="project-estimates"></a>Estimativas do projeto

As estimativas de mão de obra, despesas e material do projeto são criadas e mantidas no Microsoft Dataverse e sincronizada com aplicativos do Finance and Operations para fins contábeis. As operações de criação, atualização e exclusão não têm suporte de aplicativos do Finance and Operations.

A criação de estimativas exige uma configuração de contabilidade válida para o projeto. Os projetos associados a linhas de contrato devem ter um perfil de custo e receita de projeto válido definido nas regras de perfil de custo e receita do projeto. Para obter mais informações, consulte [Configure a contabilidade para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimativas de mão de obra

Estimativas de mão de obra são criadas pelo Project Manager ou pelo gerente de recursos que também atribui um recurso genérico ou nomeado à tarefa do projeto. Os registros de atribuição de recursos podem ser revisados na guia **Atribuições de recursos** na página **Detalhes do Projeto** no Dataverse. Registros de atribuição de recursos no Dataverse criam registros de previsão de horas em aplicativos do Finance and Operations usando **Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)**.

   ![Integração de estimativas de mão de obra](./Media/DW4LaborEstimates.png)

A gravação dupla sincroniza registros de atribuição de recursos com a tabela de preparo (**ProjCDSEstimateHoursImport**) e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de horas (**ProjForecastEmpl**).

O contador do projeto revisa registros de previsão de horas criados em aplicativos do Finance and Operations ao acessar **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Plano** > **Previsões de horas**.

## <a name="expense-estimates"></a>Estimativas de despesas

As estimativas de despesas são criadas pelo gerente de projeto na guia **Estimativas de Despesas** na página **Detalhes do Projeto** no Dataverse. Os registros de estimativa de despesas são armazenados na entidade **Linha de Estimativa** no Dataverse. Esses registros de estimativa têm classe de transação, **Despesa** e são sincronizados com os registros de previsão de despesas em aplicativos do Finance and Operations usando **Entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimatelines)**.

   ![Integração de estimativas de despesas](./Media/DW4ExpenseEstimates.png)

A gravação dupla sincroniza registros de estimativas de despesas para a tabela de preparo **ProjCDSEstimateExpenseImport** e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de despesas (**ProjForecastCost**). As linhas de estimativa armazenam a estimativa de vendas e os registros de estimativa de custo separadamente. A lógica de negócios em aplicativos do Finance and Operations preenche um único registro de previsão de despesas usando esse detalhe na tabela de preparo.

O contador do projeto pode revisar registros de previsão de despesas em aplicativos do Finance and Operations ao acessar **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Plano** > **Previsões de despesas**.

## <a name="material-estimates"></a>Estimativas de material

As estimativas de material são criadas pelo gerente de projeto na guia **Estimativas de material** na página **Detalhes do Projeto** no Dataverse. Os registros de estimativa de material são armazenados na entidade **Linha de Estimativa** no Dataverse. Esses registros de estimativa têm a classe de transação, **Material** e são sincronizados com os registros de previsão de itens em aplicativos do Finance and Operations usando **Tabela de integração de projeto para estimativas de material (msdyn\_estimatelines)**.

   ![Integração de estimativas de material](./Media/DW4MaterialEstimates.png)

A gravação dupla sincroniza registros de estimativas de material para a tabela de preparo, **ProjForecastSalesImpor** e, depois, usa a lógica de negócios para criar e atualizar registros de previsão de itens (**ForecastSales**). As linhas de estimativa armazenam a estimativa de vendas e os registros de estimativa de custo separadamente. A lógica de negócios em aplicativos do Finance and Operations preenche um único registro de previsão de itens usando esse detalhe na tabela de preparo.

O contador do projeto pode revisar registros de previsão de itens em aplicativos do Finance and Operations ao acessar **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Plano** > **Previsões de itens**.

## <a name="project-actuals"></a>Dados reais do projeto

Os dados reais do projeto são criados no Dataverse, com base em tempo, despesas, material e atividade de cobrança. Todos os atributos operacionais dessas transações, incluindo quantidade, preço de custo, preço de venda e projeto são capturados nesta entidade do Dataverse. Para obter mais informações, consulte [Dados reais](../actuals/actuals-overview.md). Os registros de dados reais são sincronizados com aplicativos do Finance and Operations usando o mapa da tabela de gravação dupla **Dados reais de integração do Project Operations (msdyn\_actuals)** para contabilidade derivada.

   ![Integração de dados reais](./Media/DW4Actuals.png)

O mapa de tabela **Dados reais de integração do Project Operations** sincroniza todos os registros da entidade **Dados Reais** no Dataverse, com o atributo **Ignorar Sincronização (apenas para uso interno)** definido como **Falso**. Este valor de atributo é definido no Dataverse automaticamente quando o registro é criado. Exemplos em que este atributo é definido como **Verdadeiro**:

  - Dados reais de custo do projeto para transações intercompanhia. Para obter mais informações, consulte [Criar transações intercompanhia](../project-accounting/create-intercompany-transactions.md). Esses registros são ignorados porque o sistema recria os dados reais de custo do projeto em aplicativos do Finance and Operations quando a fatura do fornecedor intercompanhia é postada.
  - Registros negativos de vendas não cobradas criados quando a fatura pro forma é confirmada. Esses registros são ignorados porque o razão auxiliar do projeto em aplicativos do Finance and Operations não reverte o registro de vendas não cobradas no faturamento, mas altera o status para totalmente faturado.

O mapa da tabela de gravação dupla sincroniza os registros de dados reais com a tabela de preparo, **ProjCDSActualsImport**. Esses registros são processados pelo processo periódico **Importar da tabela de preparo** ao criar linhas de diário de integração do Project Operations e linhas de proposta de fatura do projeto. Para obter mais informações, consulte [Diário de integração no Project Operations](../project-accounting/project-operations-integration-journal.md).

O Dataverse também captura os links entre as transações reais do projeto na entidade **Conexão de transação**. Para obter mais informações, consulte [Vincule dados reais a registros originais](../actuals/linkingactuals.md). Links entre transações reais também são sincronizados com aplicativos do Finance and Operations usando o mapa de tabela de gravação dupla, **Entidade de integração para relacionamentos de transação do projeto (msdyn\_transactionconnections)**. Esses registros são usados pelo processo periódico, **Importar da tabela de preparo**, ao criar linhas de diário de integração do Project Operations e linhas de proposta de fatura do projeto.

Postar um diário de integração do Project Operations e uma proposta de fatura de projeto dispara uma atualização nos respectivos registros na tabela de preparo, **ProjCDSActualsImport**. O sistema captura e registra os seguintes atributos de contabilidade para transações de dados reais:

- Valor da moeda contábil
- Taxa de câmbio
- Número do comprovante
- Valor do imposto

O mapa de tabela **Dados reais de integração do Project Operations** atualiza os respectivos registros de dados reais no Dataverse com essas informações.
