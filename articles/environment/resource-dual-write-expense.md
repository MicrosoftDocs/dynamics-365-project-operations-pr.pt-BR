---
title: Integração do gerenciamento de despesas
description: Este artigo fornece informações sobre a integração do relatório de despesas no Project Operations usando a gravação dupla.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e11f1cfd714212691146eed59bcfb5b5facd750c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029195"
---
# <a name="expense-management-integration"></a>Integração do gerenciamento de despesas

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo fornece informações sobre a integração de relatórios de despesas no Project Operations [implantação de despesa total](../expense/expense-overview.md) usando a gravação dupla.

## <a name="expense-categories"></a>Categorias de despesa

Em uma implantação de despesa total, as categorias de despesa são criadas e mantidas nos aplicativos de finanças e operações. Para criar uma nova categoria de despesas, conclua as seguintes etapas:

1. No Microsoft Dataverse, crie uma categoria **Transação**. A integração de gravação dupla sincronizará essa categoria de transação com os aplicativos de finanças e operações. Para obter mais informações, consulte [Configurar categorias de projeto](/dynamics365/project-operations/project-accounting/configure-project-categories) e [Configuração do Project Operations e integração de dados de configuração](resource-dual-write-setup-integration.md). Como resultado dessa integração, o sistema cria quatro registros de categoria compartilhados nos aplicativos de finanças e operações
2. No Finance, acesse **Gerenciamento de despesas** > **Configuração** > **Categorias compartilhadas** e selecione uma categoria compartilhada com uma classe de transação **Despesa**. Defina o parâmetro **Pode ser usado em Despesa** como **Verdadeiro** e defina o tipo de despesa a ser usado.
3. Usando este registro de categoria compartilhada, crie uma nova categoria de despesas acessando **Gerenciamento de despesas** > **Configuração** > **Categorias de despesas** e selecione **Novo**. Quando o registro é salvo, a gravação dupla usa o mapa da tabela, **Entidade de exportação de categorias de despesas de projeto de integração do Project Operations (msdyn\_expensecategories)** para sincronizar esse registro com o Dataverse.

  ![Integração de categorias de despesas.](./media/DW6ExpenseCategories.png)

As categorias de despesa nos aplicativos de finanças e operações são específicas da empresa ou da entidade legal. Existem registros específicos de entidade legal separados e correspondentes no Dataverse. Quando um gerente de projeto estima despesas, ele não pode selecionar categorias de despesas que foram criadas para um projeto que pertence a uma empresa diferente da que possui o projeto em que está trabalhando. 

## <a name="expense-reports"></a>Relatórios de despesas

Os relatórios de despesas são criados e aprovados nos aplicativos de finanças e operações. Para obter mais informações, consulte [Criar e processar relatórios de despesas no Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Depois que o relatório de despesas é aprovado pelo gerente de projeto, ele é postado na contabilidade. No Project Operations, as linhas do relatório de despesas relativas ao projeto são postadas usando regras especiais de postagem:

  - O custo relacionado ao projeto (incluindo imposto não recuperável) não é postado logo na conta de custo do projeto na contabilidade, mas é postado na conta de integração de despesas. Esta conta está configurada na guia **Gerenciamento e contabilidade de projetos** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projeto**, **Project Operations no Dynamics 365 Customer Engagement**.
  - A gravação dupla é sincronizada com o Dataverse usando o mapa de tabela **Entidade de exportação de despesas de projeto de integração do Project Operations (msdyn\_expenses)**.
  - Razão auxiliar de imposto, razão auxiliar de fornecedor e outras postagens financeiras são registrados conforme aplicável no momento de postagem do relatório de despesas.

  ![Integração de relatórios de despesas.](./media/DW6ExpenseReports.png)

Quando um registro é gravado na entidade **Despesa** no Dataverse, o sistema dispara o processo de aprovação automatizado do registro. Se necessário, o status do processo de aprovação automatizado pode ser revisado no Dataverse acessando **Configurações avançadas** > **Sistema** > **Trabalhos do sistema**. Após a aprovação ser concluída, os registros da classe de transações de despesas são criados na entidade **Dados Reais**.

Os dados reais relativos a despesas são processados usando o mapa da tabela de gravação dupla **Dados reais de integração do Project Operations (msdyn\_actuals)**. Para obter mais informações, consulte [Estimativas e dados reais de projeto](resource-dual-write-estimates-actuals.md).

O processo periódico, **Importar de preparo** cria linhas de diário relacionadas ao relatório de despesas no diário de integração do Project Operations. O padrão da conta de compensação é a conta de integração de despesas. O diário de integração de postagem limpa o saldo da conta para a transação de despesas e move o valor da despesa para a conta de custo do projeto. O sistema também cria transações do razão auxiliar do projeto para fins de faturamento derivado e reconhecimento de receita.
