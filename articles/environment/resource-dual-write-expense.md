---
title: Integração do gerenciamento de despesas
description: Este tópico fornece informações sobre a integração de relatórios de despesas no Project Operations usando a gravação dupla.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986567"
---
# <a name="expense-management-integration"></a>Integração do gerenciamento de despesas

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico fornece informações sobre a integração de relatórios de despesas no Project Operations [implantação de despesa total](../expense/expense-overview.md) usando a gravação dupla.

## <a name="expense-categories"></a>Categorias de despesa

Em uma implantação de despesa total, categorias de despesas são criadas e mantidas em aplicativos do Finance and Operations. Para criar uma nova categoria de despesas, conclua as seguintes etapas:

1. No Microsoft Dataverse, crie uma categoria **Transação**. A integração de gravação dupla sincronizará esta categoria de transação para aplicativos do Finance and Operations. Para obter mais informações, consulte [Configurar categorias de projeto](/dynamics365/project-operations/project-accounting/configure-project-categories) e [Configuração do Project Operations e integração de dados de configuração](resource-dual-write-setup-integration.md). Como resultado dessa integração, o sistema cria quatro registros de categoria compartilhados em aplicativos do Finance and Operations.
2. No Finance, acesse **Gerenciamento de despesas** > **Configuração** > **Categorias compartilhadas** e selecione uma categoria compartilhada com uma classe de transação **Despesa**. Defina o parâmetro **Pode ser usado em Despesa** como **Verdadeiro** e defina o tipo de despesa a ser usado.
3. Usando este registro de categoria compartilhada, crie uma nova categoria de despesas acessando **Gerenciamento de despesas** > **Configuração** > **Categorias de despesas** e selecione **Novo**. Quando o registro é salvo, a gravação dupla usa o mapa da tabela, **Entidade de exportação de categorias de despesas de projeto de integração do Project Operations (msdyn\_expensecategories)** para sincronizar esse registro para o Dataverse.

  ![Integração de categorias de despesas.](./media/DW6ExpenseCategories.png)

Categorias de despesas em aplicativos do Finance and Operations são específicos da empresa ou entidade legal. Existem registros específicos de entidade legal separados e correspondentes no Dataverse. Quando um gerente de projeto estima despesas, ele não pode selecionar categorias de despesas que foram criadas para um projeto que pertence a uma empresa diferente da que possui o projeto em que está trabalhando. 

## <a name="expense-reports"></a>Relatórios de despesas

Os relatórios de despesas são criados e aprovados em aplicativos do Finance and Operations. Para obter mais informações, consulte [Criar e processar relatórios de despesas no Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Depois que o relatório de despesas é aprovado pelo gerente de projeto, ele é postado na contabilidade. No Project Operations, as linhas do relatório de despesas relativas ao projeto são postadas usando regras especiais de postagem:

  - O custo relacionado ao projeto (incluindo imposto não recuperável) não é postado logo na conta de custo do projeto na contabilidade, mas é postado na conta de integração de despesas. Esta conta está configurada na guia **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto**, **Project Operations no Dynamics 365 Customer Engagement**.
  - A gravação dupla é sincronizada com o Dataverse usando o mapa de tabela **Entidade de exportação de despesas de projeto de integração do Project Operations (msdyn\_expenses)**.
  - Razão auxiliar de imposto, razão auxiliar de fornecedor e outras postagens financeiras são registrados conforme aplicável no momento de postagem do relatório de despesas.

  ![Integração de relatórios de despesas.](./media/DW6ExpenseReports.png)

Quando um registro é gravado na entidade **Despesa** no Dataverse, o sistema dispara o processo de aprovação automatizado do registro. Se necessário, o status do processo de aprovação automatizado pode ser revisado no Dataverse acessando **Configurações avançadas** > **Sistema** > **Trabalhos do sistema**. Após a aprovação ser concluída, os registros da classe de transações de despesas são criados na entidade **Dados Reais**.

Os dados reais relativos a despesas são processados usando o mapa da tabela de gravação dupla **Dados reais de integração do Project Operations (msdyn\_actuals)**. Para obter mais informações, consulte [Estimativas e dados reais de projeto](resource-dual-write-estimates-actuals.md).

O processo periódico, **Importar de preparo** cria linhas de diário relacionadas ao relatório de despesas no diário de integração do Project Operations. O padrão da conta de compensação é a conta de integração de despesas. O diário de integração de postagem limpa o saldo da conta para a transação de despesas e move o valor da despesa para a conta de custo do projeto. O sistema também cria transações do razão auxiliar do projeto para fins de faturamento derivado e reconhecimento de receita.
