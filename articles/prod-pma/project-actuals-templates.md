---
title: Sincronize dados reais de projeto diretamente do Project Service Automation com o diário de integração de projetos para lançamento no Finance and Operations
description: Este tópico descreve os modelos e as tarefas subjacentes usadas para sincronizar dados reais de projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071560"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sincronize dados reais de projeto diretamente do Project Service Automation com o diário de integração de projetos para lançamento no Finance and Operations

[!include[banner](../includes/banner.md)]

Este tópico descreve os modelos e as tarefas subjacentes usadas para sincronizar dados reais de projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.

O modelo sincroniza as transações do Project Service Automation com uma tabela de preparo no Finance. Após a sincronização ser concluída, é **necessário** importar os dados da tabela de preparo para o diário de integração.

> [!NOTE]
> - A integração de dados reais do projeto está disponível a partir da versão 8.0.1.
> - Se você estiver usando a Enterprise Edition 7.3.0, após instalar o KB 4132657 e o KB 4132660, será possível usar os modelos para integrar as tarefas de projeto, as categorias de transação, as estimativas de horas, as estimativas de despesas e os dados reais, além de configurar o bloqueio de funcionalidades. Caso seja necessário redefinir as distribuições contábeis, recomendamos instalar o KB 4131710.
> - Se você estiver usando a versão 7.3.0 e estiver transferindo as transações de taxa do Project Service Automation, instale o KB 4345320 para incluir essas taxas na fatura do projeto.
> - Se você estiver inserindo valores de impostos sobre vendas em transações de horas ou despesas no Project Service Automation, será necessário instalar o Project Service Automation Atualização 7. Caso contrário, os dados reais de impostos não serão vinculados aos dados reais de tempo ou de despesas associados e não serão sincronizados com o Finance. Para obter mais informações, entre em contato com o Suporte.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de dados do Project Service Automation para o Finance

A solução de integração do Project Service Automation ao Finance usa o recurso de integração de dados para sincronizar dados entre instâncias do Project Service Automation e do Finance. Os modelos de integração disponíveis com o recurso de Integração de dados permitem o fluxo de dados sobre dados reais de projeto do Project Service Automation para o Finance.

A ilustração a seguir mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation com o Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Dados reais de projeto do Project Service Automation

### <a name="template-and-tasks"></a>Modelo e tarefas

Para acessar os modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

O seguinte modelo e as tarefas subjacentes são usados para sincronizar os dados reais de projeto do Project Service Automation para o Finance:

- **Nome do modelo na Integração de dados:** dados reais do Projeto (PSA para Fin e Ops)
- **Nome das tarefas no projeto:**

    - Dados reais
    - TransactionConnections

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Financeiro                                   |
|----------------------------|----------------------------------------------------------|
| Dados reais                    | Entidade da integração para dados reais do projeto                   |
| Conexões da Transação    | Entidade de integração para relacionamentos de transações do projeto |

### <a name="entity-flow"></a>Fluxo de entidade

Os dados reais do projeto são gerenciados no Project Service Automation e são sincronizados com o diário de integração do projeto no Finance. A contabilidade será aplicada com base nas dimensões financeiras padrão e a configuração de lançamento.

### <a name="prerequisites"></a>Pré-requisitos

Antes que a sincronização de dados reais possa ocorrer, é necessário configurar os parâmetros de integração do Project Service Automation e sincronizar projetos, tarefas de projetos e categorias de transação de despesas de projetos.

### <a name="power-query"></a>Power Query

No modelo de dados reais do projeto, é necessário usar o Microsoft Power Query para Excel para concluir estas tarefas:

- Transformar o tipo de transação no Project Service Automation no tipo de transação correto no Finance. Essa transformação já está definida no modelo de dados reais do Projeto (PSA para Fin e Ops).
- Transformar o tipo de cobrança no Project Service Automation no tipo de cobrança correto no Finance. Essa transformação já está definida no modelo de dados reais do Projeto (PSA para Fin e Ops). Em seguida, o tipo de cobrança será mapeado para a propriedade da linha, com base na configuração na página **Parâmetros de integração do Project Service Automation**.
- Filtre para unidades organizacionais de recurso específicas que devem ser sincronizadas com esse modelo.
- Se tempo intercompanhia ou dados reais de despesas intercompanhia forem sincronizados com o Finance, será necessário transformar a unidade organizacional de contrato na entidade legal correta no Finance. No modelo de dados reais do projeto (PSA para Fin and Ops), uma coluna condicional é definida com base em dados de demonstração. Você deve atualizar a última coluna condicional inserida para as entidades legais corretas. Caso contrário, poderá ocorrer um erro de integração ou transações de dados reais incorretas poderão ser importadas para o Finance.
- Se tempo intercompanhia ou dados reais de despesas intercompanhia não forem sincronizados com o Finance, você deverá excluir a última coluna condicional inserida do modelo. Caso contrário, poderá ocorrer um erro de integração ou transações de dados reais incorretas poderão ser importadas para o Finance.

#### <a name="contract-organizational-unit"></a>Unidade organizacional de contrato
Para atualizar a coluna condicional inserida no modelo, clique na seta **Mapa** para abrir o mapeamento. Selecione o link **Filtragem e consulta avançada** para abrir o Power Query.

- Se você estiver usando o modelo de dados reais do Project padrão (PSA para Fin and Ops), no Power Query, selecione a última **Condição inserida** na seção **Etapas aplicadas**. Na entrada **Função** , substitua **USSI** pelo nome da entidade legal que deve ser usado com a integração. Inclua condições adicionais à entrada **Função** conforme necessário e atualize a condição **else** do **USMF** para a entidade legal correta.
- Se você estiver criando um modelo, será necessário adicionar a coluna para oferecer suporte a tempo e despesas intercompanhia. Selecione **Adicionar Coluna Condicional** e insira um nome para a coluna, como **LegalEntity**. Insira uma condição para a coluna, em que, se **msdyn\_contractorganizationalunitid.msdyn\_name** é \<organizational unit\>, então \<enter the legal entity\>; senão nula (null).

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na integração de dados

As ilustrações a seguir mostram um exemplo do mapeamento da tarefa de modelo na Integração de dados. O mapeamento mostra as informações de campos que serão sincronizadas do Project Service Automation para o Finance.

[![Mapeamento de modelo - Reais](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapeamento de modelo - Conexões de transação](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importar da tabela de preparação após a integração do Project Service Automation

A importação do processo periódico da tabela de preparo deve ser executada após a sincronização de dados reais do Project Service Automation com o Finance. Este processo importará as transações do projeto da tabela de preparo para o diário de integração do Project Service Automation, em que a contabilidade é aplicada e as transações importadas podem ser lançadas. Recomendamos executar esse processo em modo de lote; opcionalmente, ele pode ser configurado para ser executado como um lote recorrente.

## <a name="update-actuals-from-finance"></a>Atualizar dados reais no Finance

### <a name="template-and-tasks"></a>Modelo e tarefas

O seguinte modelo e as tarefas subjacentes são usados para sincronizar o número do comprovante e os impostos para transações de projeto lançadas do Finance com o Project Service Automation:

- **Nome do modelo na Integração de dados:** dados reais do Projeto (Fin Ops para PSA)
- **Nome das tarefas no projeto:**

    - Dados reais 
    - TransactionConnections

### <a name="entity-set"></a>Conjunto de entidades

| Financeiro                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entidade da integração para dados reais do projeto                   | Dados reais                    |
| Entidade de integração para relacionamentos de transações do projeto | Conexões da Transação    |

### <a name="entity-flow"></a>Fluxo de entidade

Os dados reais do projeto são gerenciados no Project Service Automation e são sincronizados com o diário de integração do projeto no Finance. Após os dados reais serem lançados no Finance, eles são atualizados no Project Service Automation com o número de comprovante do Finance. Se os impostos tiverem sido adicionados no Finance, os novos dados reais de impostos serão criados no Project Service Automation.

### <a name="power-query"></a>Power Query

No modelo de atualização de dados reais, você deve usar o Power Query para concluir estas tarefas:

- Transformar o tipo de transação no Finance no tipo de transação correto no Project Service Automation. Essa transformação já está definida no modelo atualização de dados reais do projeto (Fin and Ops para PSA).
- Transformar o tipo de cobrança no Finance no tipo de cobrança correto no Project Service Automation. Essa transformação já está definida no modelo atualização de dados reais do projeto (Fin and Ops para PSA).

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na integração de dados

As ilustrações a seguir mostram exemplos de mapeamentos de tarefas do modelo na integração de dados. O mapeamento mostra as informações de campo que serão sincronizadas do Finance para o Project Service Automation.

[![Mapeamento de modelo - Atualização de reais](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapeamento de modelo - Atualização de transação](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
