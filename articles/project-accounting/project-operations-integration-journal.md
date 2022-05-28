---
title: Diário de integração no Project Operations
description: Este tópico fornece informações sobre como trabalhar com o diário de integração no Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5e1a455d055fe562a1946cc3b90c8274ef1a4b12
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582420"
---
# <a name="integration-journal-in-project-operations"></a>Diário de integração no Project Operations

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

As entradas de hora e despesas criam transações **Reais** que representam a visão operacional do trabalho concluído em um projeto. O Dynamics 365 Project Operations fornece aos contadores uma ferramenta para revisar as transações e ajustar os atributos de contabilidade, conforme necessário. Após a revisão e os ajustes serem concluídos, as transações são lançadas na subconta do Projeto e na Contabilidade. Um contador pode executar essas atividades usando o diário **Integração do Project Operations** (**Dynamics 365 Finance** > **Gerenciamento e contabilidade de projeto** > **Diários** > **Diário de Integração do Project Operations**).

![Fluxo diário de integração.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Cria registros no diário de integração do Project Operations

Os registros no diário de integração do Project Operations são criados usando o processo periódico, **Importar da tabela de preparo**. Você pode executar esse processo acessando **Dynamics 365 Finance** > **Gerenciamento e contabilidade de projeto** > **Periódico** > **Integração do Project Operations** > **Importar da tabela de preparo**. Você pode executar o processo interativamente ou configurá-lo para ser executado em segundo plano, conforme necessário.

Quando o processo periódico é executado, quaisquer dados reais que ainda não foram adicionados ao diário de integração do Project Operations são encontrados. Uma linha do diário para cada transação real é criada.
O sistema agrupa linhas do diário em diários separados com base no valor selecionado no campo **Unidade de período no diário de Integração do Project Operations** (**Finanças** > **Gerenciamento e contabilidade de projeto** > **Configuração** > **Parâmetros de gerenciamento e contabilidade de projetos**, guia **Project Operations no Dynamics 365 Customer Engagement**). Os valores possíveis para este campo incluem:

  - **Dias**: os dados reais são agrupados pela data da transação. Um diário separado é criado para cada dia.
  - **Meses**: Os dados reais são agrupados por mês do calendário. Um diário separado é criado para cada mês.
  - **Anos**: Os dados reais são agrupados por ano do calendário. Um diário separado é criado para cada ano.
  - **Todos**: Todas as transações reais são incluídas no mesmo diário de integração. Se o diário não estiver disponível quando o processo periódico for executado, por exemplo, se o diário estiver no processo de lançar transações, um novo diário será criado.

As linhas do diário são criadas com base nos dados reais do projeto. A lista a seguir inclui algumas das regras padrão e de transformação mais notáveis:

  - Cada transação real do projeto tem uma linha no diário de Integração do Project Operations. As transações de vendas de custo e não faturadas para tipo de faturamento de tempo e material são mostradas em linhas separadas.
  - O campo **Data** representa a data da transação. O campo **Data da contabilidade** representa a data em que a transação é registrada no razão. Se a data contábil estiver em um [período financeiro fechado](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), e o parâmetro **Definir automaticamente a data contábil para abrir o período contábil** estiver definido na guia **Financeiro** da página **Parâmetros de gerenciamento e contabilidade de projeto**, o sistema ajustará a data contábil da transação para a primeira data no próximo período de razão aberto.
  - O campo **Comprovante** mostra o número do comprovante para cada transação real. A sequência do número do comprovante é definida na guia **Sequências numéricas**, na página **Parâmetros de gerenciamento e contabilidade de projeto**. Cada linha recebe um novo número. Depois que o comprovante for postado, você pode ver como o custo e a transação de vendas não faturadas estão relacionados selecionando **Comprovantes relacionados** na página **Transação de comprovante**.
  - O campo **Categoria** representa uma transação do projeto e os padrões com base na categoria de transação para o projeto real relacionado.
    - Se **Categoria da transação** for definida no Projeto real e houver uma **Categoria do projeto** em determinada entidade legal fornecida, a categoria é padronizada para esta categoria do projeto.
    - Se **Categoria da transação** não estiver definida no Projeto real, o sistema usará o valor no campo **Padrões de categoria do projeto** na guia **Project Operations no Dynamics 365 Customer Engagement** da página **Parâmetros de Gerenciamento e contabilidade de projetos**.
  - O campo **Recurso** representa o recurso do projeto relacionado a esta transação. O recurso é usado como referência nas propostas de fatura do Project para clientes.
  - O campo **Taxa de câmbio** usa os padrões de **Taxa de câmbio da moeda** definidos no Dynamics 365 Finance. Se a configuração da taxa de câmbio estiver faltando, o processo periódico **Importar da tabela de preparo** não adicionará o registro a um diário e uma mensagem de erro será adicionada ao log de execução do trabalho.
  - O campo **Propriedade da linha** representa o tipo de faturamento nos dados reais do Project. A propriedade de linha e o mapeamento de tipos de cobrança são definidos na guia **Project Operations no Dynamics 365 Customer Engagement** da página **Parâmetros de gerenciamento e contabilidade de projetos**.

Apenas os seguintes atributos de contabilidade podem ser atualizados nas linhas do diário de integração do Project Operations:

- **Grupo de impostos de vendas de faturamento** e **Grupo de impostos de vendas de item de faturamento**
- **Dimensões financeiras** (usando a ação **Distribuir valores**)

As linhas do diário de integração podem ser excluídas, no entanto, quaisquer linhas não publicadas serão inseridas no diário novamente após você executar novamente o processo periódico **Importar da tabela de preparo**.

Quando você lança o diário de integração, uma subconta do projeto e transações do razão geral são criadas. Eles são usadas no faturamento de clientes downstream, reconhecimento de receita e relatórios financeiros.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
