---
title: Integração de dados de instalação e configuração do Project Operations
description: Este artigo fornece informações sobre como configurar e aplicar mapas de gravação dupla no Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914526"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integração de dados de instalação e configuração do Project Operations

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo fornece informações sobre a integração de gravação dupla no Project Operations para configuração e entidades de configuração.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratos de projeto, linhas de contrato e projetos

Contratos do projeto, linhas de contrato e projetos são criados no Dataverse e sincronizados com os aplicativos de finanças e operações para a contabilidade adicional. Os registros nessas entidades podem ser criados e excluídos apenas no Dataverse. No entanto, atributos contábeis, como padrões do grupo de impostos sobre vendas e dimensões financeiras, podem ser adicionados a esses registros nos aplicativos de finanças e operações.

  ![Conceitos de integração do contrato de projeto.](./media/1ProjectContract.jpg)

Leads, oportunidades e cotações de atividades de vendas são rastreados no Dataverse e não são sincronizados com os aplicativos de finanças e operações porque não há contabilidade downstream associada a essa atividade.

A funcionalidade de contrato de projeto no Dataverse cria um registro do contrato do projeto nos aplicativos de finanças e operações usando o mapa de tabela **Cabeçalhos de contratos do projeto (salesorders)**. Salvar um contrato de projeto no Dataverse também inicia a criação de um registro de entidade de cliente do contrato de projeto. Esse registro é sincronizado com os aplicativos de finanças e operações usando o mapa de tabela **Fonte de financiamento de projeto (msdyn\_projectcontractssplitbillingrules)**. Este mapa também sincroniza adições, atualizações e exclusões de clientes de contratos de projeto. As porcentagens de faturamento divididas entre os clientes do contrato do projeto são dominadas apenas no Dataverse e não são sincronizadas com os aplicativos de finanças e operações.

Depois que um contrato do projeto é criado no Dataverse, o contador do projeto pode atualizar os atributos contábeis desse contrato do projeto nos aplicativos de finanças e operações, acessando **Gerenciamento e contabilidade de projeto** > **Contratos do projeto** > **Configurar** > **Mostrar contabilidade padrão**. O contador pode revisar os atributos do contrato do projeto operacional, como data de entrega solicitada e valor do contrato, selecionando a ID do contrato do projeto nos aplicativos de finanças e operações, que abrem o registro do contrato do projeto relacionado no Dataverse.

A entidade do projeto é sincronizada com os aplicativos de finanças e operações usando o mapa de tabela **Projetos V2 (msdyn\_projects)**. O contador do projeto pode:

  - Revise os projetos nos aplicativos de finanças e operações acessando **Gerenciamento e contabilidade de projeto** > **Todos os projetos**. 
  - Atualize os atributos contábeis do projeto nos aplicativos de finanças e operações acessando **Gerenciamento e contabilidade de projeto** > **Todos os projetos** > **Configurar** > **Mostrar contabilidade padrão**.  
  - Revise os atributos do projeto operacional, como datas de início e de término estimadas, selecionando a ID do projeto nos aplicativos de finanças e operações, que abrem o registro do projeto relacionado no Dataverse.

Um projeto está associado a um contrato de projeto por meio da entidade **Linha de contrato de projeto**.

As linhas de contrato de projeto no Dataverse criam uma regra de cobrança do contrato do projeto nos aplicativos de finanças e operações usando o mapa de tabela **Linhas de contrato de projeto (salesorderdetails)**. O método de cobrança define o tipo de regra de cobrança do contrato do projeto nos aplicativos de finanças e operações:

  - As linhas de contrato do projeto com um método de cobrança de tempo e material criam uma regra de cobrança de tempo e tipo de material.
  - As linhas de contrato do método de cobrança de preço fixo criam uma regra de cobrança em etapas.

As linhas de contrato de projeto podem ser revisadas pelo contador do projeto nos aplicativos de finanças e operações acessando **Gerenciamento e contabilidade de projeto** > **Contratos do projeto** > **Configurar** > **Mostrar contabilidade padrão** e revisando os detalhes na guia **Linhas do contrato**. O contador também pode definir dimensões financeiras padrão para as linhas de contrato do método de cobrança de preço fixo nesta guia.

## <a name="billing-milestones"></a>Etapas de cobrança

As linhas do contrato do projeto que usam o método de cobrança de preço fixo são faturadas por meio de etapas de cobrança. As etapas de cobrança são sincronizadas com as transações por conta do projeto nos aplicativos de finanças e operações usando o mapa de tabela **Etapas da linha de contrato da integração do Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integração de etapas de cobrança.](./media/2Milestones.jpg)

O contador pode revisar transações de conta e ajustar os atributos contábeis para essas transações, acessando **Gerenciamento e contabilidade de projetos** > **Contratos de projeto** > **Manter** > **Transações na conta** ou **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Manter** > **Transações na conta**.

Quando você cria pela primeira vez uma etapa de cobrança para determinada linha de contrato de projeto, o sistema cria automaticamente um projeto de estimativa de receita de preço fixo para o projeto associado a essa linha de contrato. Projetos de estimativa de receita de preço fixo podem ser revisados acessando **Gerenciamento e contabilidade de projetos** > **Projetos de estimativa de receita de preço fixo**.

### <a name="project-tasks"></a>Tarefas do projeto

As tarefas do projeto são sincronizadas com os aplicativos de finanças e operações por meio do mapa de tabela **Tarefas do projeto (msdyn\_projecttasks)** somente para fins de referência. Não há suporte para as operações de criação, atualização e exclusão por meio dos aplicativos de finanças e operações.

  ![Integração de tarefas de projeto.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de projeto

A entidade **Funções de recursos de projeto** é sincronizada com os aplicativos de finanças e operações usando o mapa de tabela **Funções de recursos de projeto para todas as empresas (bookableresourcecategories)** somente para fins de referência. Como as funções de recursos no Dataverse não são específicos da empresa, o sistema cria automaticamente os respectivos registros de funções de recursos específicos da empresa nos aplicativos de finanças e operações para todas as entidades legais incluídas no escopo de integração de gravação dupla.

![Integração de funções do recurso.](./media/5Resources.jpg)

Os recursos do projeto no Project Operations são mantidos no Dataverse e não são sincronizados com os aplicativos de finanças e operações.

### <a name="transaction-categories"></a>Categorias de transação

As categorias de transação são mantidas no Dataverse e sincronizadas com os aplicativos de finanças e operações usando o mapa de tabela **Categorias de transação do projeto (msdyn\_transactioncategories)**. Após a sincronização do registro da categoria da transação, o sistema cria automaticamente quatro registros da categoria compartilhada. Cada registro corresponde a um tipo de transação nos aplicativos de finanças e operações e os vincula ao registro de categoria de transação.

![Integração de categorias de transação.](./media/4TransactionCategories.jpg)

O uso de categorias de transação para estimativas e dados reais exige que o contador do projeto ou administrador do sistema crie categorias de projeto correspondentes em cada entidade legal. Para obter mais informações, consulte [Configurar categorias de projeto](../project-accounting/configure-project-categories.md).
