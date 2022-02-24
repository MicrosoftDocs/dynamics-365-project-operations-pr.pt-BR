---
title: Gerenciar propostas de fatura do projeto
description: Este tópico fornece detalhes sobre como processar faturas voltadas para o cliente com o Project Operations para cenários baseados em recursos/não estocados.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089203"
---
# <a name="manage-project-invoice-proposals"></a>Gerenciar propostas de fatura do projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

As propostas de fatura do projeto podem ser processadas pelo seu departamento de cobrança quando as duas condições a seguir são atendidas:

  - O gerente de projeto confirma a fatura pro forma no Microsoft Dataverse.
  - Todas as transações de vendas não faturadas de tempo e material incluídas na fatura pro forma são lançadas usando o diário de **Integração do Dynamics 365 Project Operations**.

Use as seguintes etapas para concluir uma proposta de fatura do projeto no Dynamics 365 Finance.

1. Revise as informações de cobrança para transações de tempo e material e publique o diário de **Integração do Project Operations**.
2. Revise as informações de cobrança para marcos de faturamento de preço fixo.
3. Revise e formate a proposta de fatura do projeto.
4. Publique e imprima as faturas do projeto.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Gerenciar informações de cobrança no diário de integração do Project Operations

Dados reais do projeto criados no Dataverse são revisados e lançados no Finance pelo contador do projeto. Para mais informações sobre como trabalhar com o diário de integração, consulte [Diário de integração no Project Operations](../project-accounting/project-operations-integration-journal.md).

Os dados reais de custo e os dados reais de vendas não faturados são adicionados ao diário de integração como linhas separadas:

  - O padrão do preço de custo unitário e o valor de custo no Custo real é derivado da transação de custo real do projeto no Dataverse.
  - O padrão do preço de venda unitário e o valor de vendas na transação de vendas não faturadas é derivado da transação de vendas não faturada real do projeto no Dataverse.

### <a name="billing-sales-tax"></a>Cobrança de imposto sobre vendas

O cálculo do imposto sobre vendas para cobrança é determinado pela combinação dos campos **Cobrança do grupo de impostos sobre vendas** e **Grupo de imposto sobre vendas de item de cobrança** em um registro de vendas não faturadas na linha do diário de **Integração do Project Operations**. O sistema padroniza esses valores de campo com base nas configurações da guia **Finanças** na página **Parâmetros de gerenciamento e contabilidade de projeto**.

- **Método de grupo de imposto sobre vendas** determina a lógica padrão do grupo de impostos sobre vendas de cobrança:
  
  - **Projeto**: sempre padronizará o grupo de impostos sobre vendas de cobrança com base no projeto. Você pode revisar ou alterar o grupo de impostos sobre vendas de cobrança padrão em um projeto selecionando **Mostrar contabilidade padrão** na página **Todos os projetos**.
  - **Contrato do projeto**: sempre padronizará o grupo de impostos sobre vendas com base no contrato do projeto. Você pode revisar ou alterar o grupo de impostos sobre vendas padrão em um contrato selecionando **Mostrar contabilidade padrão** na página **Contratos do projeto**.
  - **Cliente**: sempre padronizará o grupo de impostos sobre vendas de cobrança com base no cliente.
  - **Pesquisar**: pesquisa em todas as entidades acima e seleciona o primeiro valor disponível. A pesquisa começa com a entidade **Projeto**, em seguida a entidade **Contrato do projeto** e, por fim, a entidade **Cliente**.

- **Método de grupo de imposto sobre vendas de item** determina a lógica padrão do grupo de impostos sobre vendas de item de cobrança:
  
  - Para os tipos de transação de tempo, despesa e taxa, o grupo de impostos sobre vendas de item de cobrança sempre usará o padrão da entidade **Categoria de projeto**.
  - Para tipos de transação de material, o grupo de impostos sobre vendas de item de cobrança é padronizado com base na configuração **Método de grupo de imposto sobre vendas de item** em **Parâmetros de gerenciamento e contabilidade de projeto**. O padrão do número do item é baseado no grupo de impostos sobre vendas de item da entidade **Produto lançado**. O padrão da categoria é baseado no grupo de impostos sobre vendas de item da entidade **Categoria de projeto**.

### <a name="financial-dimensions"></a>Dimensões financeiras

O padrão das dimensões financeiras para registros de vendas não cobradas no diário de **Integração do Project Operations** é baseado na entidade **Projeto**. As dimensões financeiras podem ser revisadas e ajustadas selecionando **Distribuir valores**. Se você precisar alterar as dimensões financeiras do registro de vendas não cobradas após o diário de integração ser lançado, mas antes que a fatura pro forma seja confirmada, vá para **Todos os Projetos** > **Gerenciar** > **Transações lançadas**, selecione a transação e, em seguida, selecione **Processo** > **Ajustar contabilidade**.

### <a name="exchange-rates"></a>Taxas de câmbio

A moeda de transação não cobrada no Dataverse é usada como moeda de transação no Finance e convertido para a moeda contábil da empresa usando taxas de câmbio definidas no Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Gerenciar os atributos financeiros dos marcos de cobrança 

As linhas de contrato de projeto usando o método de cobrança de preço fixo são cobradas por meio de [Marcos de preço fixo](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). O contador do projeto pode revisar os marcos de cobrança no Finance, acessando **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Gerenciar** > **Transações na conta**.

### <a name="billing-sales-tax"></a>Cobrança de imposto sobre vendas

O padrão dos valores de **Grupo de impostos sobre vendas** e **Grupo de impostos sobre vendas de itens** é baseado nas configurações quando um novo marco de cobrança é criado no Dataverse. O sistema padroniza os valores desses campos com base nas configurações da guia **Finanças** na página **Parâmetros de gerenciamento e contabilidade de projeto**.

- **Método de grupo de imposto sobre vendas** determina a lógica padrão do **Grupo de impostos sobre vendas de cobrança**:

    - **Projeto** sempre padronizará o grupo de impostos sobre vendas de cobrança com base no projeto. Você pode revisar ou alterar o grupo de impostos sobre vendas padrão em um projeto selecionando **Mostrar contabilidade padrão** na página **Todos os projetos**.
    - **Contrato do projeto** sempre padronizará o grupo de impostos sobre vendas com base no contrato do projeto. Você pode revisar ou alterar o grupo de impostos sobre vendas padrão em um contrato selecionando **Mostrar contabilidade padrão** na página **Contratos do projeto**.
    - **Cliente** sempre padronizará o grupo de impostos sobre vendas de cobrança com base no cliente.
    - **Pesquisar** pesquisa em todas as entidades desta lista e seleciona o primeiro valor disponível. A pesquisa começa com a entidade **Projeto**, em seguida a entidade **Contrato do projeto** e então a entidade **Cliente**.

- **Grupo de impostos de vendas de item de marco de preço fixo** é usado para padronizar o valor do campo **Grupo de impostos sobre vendas de item**.

### <a name="financial-dimensions"></a>Dimensões financeiras

As dimensões financeiras padrão para o marco de cobrança de preço fixo são definidas nas linhas de contrato do projeto. Vá para **Contratos de projeto** > **Mostrar contabilidade padrão** e na guia **Linhas de contrato**, selecione **Linha de contrato de preço** e, em seguida, configure os valores de dimensão financeira que deseja usar como o padrão.

O contador do projeto pode editar o imposto sobre vendas e as informações de dimensões financeiras nos marcos de cobrança até a Proposta de fatura do projeto ser criada.


## <a name="create-project-invoice-proposals"></a>Criar propostas de fatura do projeto

As propostas de fatura do projeto podem ser revisadas no módulo **Gerenciamento e contabilidade de projetos** acessando **Faturas de projeto** > **Propostas de fatura do projeto**.

O cabeçalho Proposta de fatura do projeto é criado no Finance quando a fatura pro forma é confirmada no Dataverse. Para uma reconciliação mais fácil, o sistema define o número da proposta de fatura do projeto no Finance com o mesmo número de ID da fatura pro forma no Dataverse. Como as faturas pro forma não são necessariamente confirmadas na mesma ordem em que são criadas, a sequência numérica da proposta de fatura do projeto no Finance deve permitir alterações para números cada vez menores. Configure as sequências numéricas usando as seguintes etapas:

1. No Finance, vá para **Administração da organização** > **Sequências numéricas** > **Sequências numéricas**.
2. No filtro **Área**, selecione **Projetos**.
3. No filtro **Referência**, selecione **Proposta de fatura**.
4. Use o campo **Empresa** para filtrar cada entidade legal com a integração do Project Operations Dataverse habilitada.
5. Abra **Detalhes da sequência numérica** e, conjunto de guias **Geral**:

    - **Permitir alterações do usuário: para um número menor** = **Sim**
    - **Permitir alterações do usuário: para um número maior** = **Sim**

As linhas da proposta de fatura do projeto são adicionadas pelo sistema usando o processo periódico **Importar da tabela de preparo** (**Gerenciamento e contabilidade de projetos** > **Periódico** > **Integração do Project Operations** > **Importar da tabela de preparo**). Esse processo pode ser feito manualmente ou usando um agendamento periódico. O sistema não adicionará linhas ao documento da proposta de fatura até que todas as linhas estejam prontas para serem cobradas. As transações de tempo e material ficam prontas para serem cobradas apenas quando são lançadas usando o diário de **Integração do Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formatar e imprimir propostas de fatura

O contador do projeto pode personalizar a impressão da fatura do projeto usando a página **Formatar proposta de fatura** e recursos de gerenciamento de impressão.

### <a name="format-invoice-proposals"></a>Formatar propostas de fatura

A página **Formatar propostas de fatura** permite que as transações de agrupamento personalizado sejam exibidas na fatura do projeto do cliente.

1. Na página **Proposta de fatura do projeto**, selecione **Impressão** > **Formatar proposta de fatura**.
2. Selecione **Novo** para criar um novo agrupamento para a impressão da fatura do projeto.
3. No campo **Detalhes/Resumo**, selecione opções para este agrupamento:

    - Selecione **Detalhes** para imprimir os detalhes da transação da fatura do cliente.
    - Selecione **Resumo** para imprimir o resumo da transação da fatura do cliente.

> [!NOTE]
> A seleção no campo **Detalhes/Resumo** na página **Formatar proposta de fatura** substitui a opção selecionada no campo **Formatar fatura** na página **Propostas de fatura** para imprimir uma fatura detalhada ou uma fatura resumida.

- Selecione as linhas de transação a serem incluídas nesta seção na guia **Transações disponíveis** e selecione **Incluir transações** para movê-las para a guia **Transações selecionadas**.
- Selecione **Mover para cima** e **Mover para baixo** para alterar a ordem das seções.
- Selecione **Visualização de impressão** para visualizar a fatura formatada.

### <a name="print-management"></a>Gerenciamento de impressão

O gerenciamento de impressão usa diferentes arquivos de relatório para imprimir, especificar destinos e personalizar o texto do rodapé da fatura. O gerenciamento de impressão pode ser configurado no nível do módulo, no entanto, essas configurações podem ser substituídas para um cliente, contrato ou proposta de fatura específica. Para acessar esta função na página **Proposta de fatura do projeto**, selecione **Impressão** > **Gerenciamento de impressão**.

A configuração do gerenciamento de impressão aparece como uma exibição em árvore, onde cada nível de nó exibe os documentos disponíveis para ajuste. Você pode atribuir impressões personalizadas no nível do módulo, cliente, contrato ou documento da proposta de fatura. Para modificar a impressão do documento original, expanda o nó desejado e selecione **Item original**. No campo **Formato de relatório**, selecione o formato de relatório a ser usado para impressão. Você pode usar formatos de relatório personalizados usando [Estrutura de gerenciamento de documentos de negócios](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Postar propostas de fatura

Depois que a fatura for revisada e editada e as linhas de proposta da fatura estiverem satisfatórias, verifique os totais da fatura e o imposto sobre vendas. No grupo **Detalhes**, selecione **Totais** e então selecione **Postar** para postar a fatura.

Para visualizar a fatura antes de postar, limpe a caixa de seleção **Postando**. **Pro forma** será impresso na fatura para indicar que é uma fatura de amostra. Para imprimir a fatura, marque a caixa de seleção **Imprimir fatura**.

Em adição à página **Proposta de fatura**, as propostas de fatura também podem ser postadas executando o trabalho periódico, **Postar propostas de fatura**. Para encontrar este trabalho, vá para **Gerenciamento e contabilidade de projetos** > **Periódico** > **Faturas de projeto** > **Postar propostas de fatura**.

Esta página mostra todas as propostas de fatura que estão prontas para postagem. Você pode programar a postagem de propostas de fatura selecionando **Lote**. Defina **Parâmetro de processamento em lote** como **Sim** e defina a recorrência do processamento em lote selecionando **Recorrência**.
