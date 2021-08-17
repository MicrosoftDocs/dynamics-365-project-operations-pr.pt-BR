---
title: Integração de dados de instalação e configuração do Project Operations
description: Este tópico fornece informações sobre como instalar e configurar mapas de gravação dupla do Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986522"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integração de dados de instalação e configuração do Project Operations

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico fornece informações sobre a integração de gravação dupla do Project Operations para entidades de instalação e configuração.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratos de projeto, linhas de contrato e projetos

Contratos de projeto, linhas de contrato e projetos são criados no Dataverse e sincronizados com aplicativos do Finance and Operations para contabilidade adicional. Os registros nessas entidades podem ser criados e excluídos apenas no Dataverse. No entanto, atributos contábeis, como padrões de grupo de impostos e dimensões financeiras, podem ser adicionados a esses registros em aplicativos do Finance and Operations.

  ![Conceitos de integração do contrato de projeto.](./media/1ProjectContract.jpg)

Vendas de atividade potenciais, oportunidades e cotações são rastreadas no Dataverse e não são sincronizadas para aplicações do Finance and Operations porque não há contabilidade derivada associada a essa atividade.

A funcionalidade do contrato de projeto no Dataverse cria um registro de contrato de projeto em aplicativos do Finance and Operations usando o mapa de tabela **Cabeçalhos de contrato de projeto (salesorders)**. Salvar um contrato de projeto no Dataverse também inicia a criação de um registro de entidade de cliente do contrato de projeto. Este registro é sincronizado com aplicativos do Finance and Operations usando o mapa de tabela **Fonte de financiamento do projeto (msdyn\_projectcontractssplitbillingrules)**. Este mapa também sincroniza adições, atualizações e exclusões de clientes de contratos de projeto. As porcentagens de cobranças divididas entre clientes de contrato de projeto são masterizadas apenas no Dataverse e não sincronizadas para aplicativos do Finance and Operations.

Depois que um contrato de projeto é criado no Dataverse, o contador do projeto pode atualizar os atributos contábeis para esse contrato de projeto em aplicativos do Finance and Operations, acessando **Gerenciamento e contabilidade de projetos** > **Contratos de projeto** > **Configuração** > **Mostrar contabilidade padrão**. O contador pode revisar os atributos do contrato do projeto operacional, como data de entrega solicitada e valor do contrato, selecionando a ID do contrato do projeto em aplicativos do Finance and Operations, que abre o registro de contrato de projeto relacionado no Dataverse.

A entidade do projeto é sincronizada com aplicativos do Finance and Operations usando o mapa de tabela **Projetos V2 (msdyn\_projects)**. O contador do projeto pode:

  - Rever projetos em aplicativos do Finance and Operations, acessando **Gerenciamento e contabilidade de projetos** > **Todos os projetos**. 
  - Atualize atributos de contabilidade para o projeto em aplicativos do Finance and Operations, acessando **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Configuração** > **Mostrar contabilidade padrão**.  
  - Revise atributos operacionais do projeto, como datas estimadas de início e término, selecionando a ID do projeto em aplicativos do Finance and Operations, que abre o registro do projeto relacionado no Dataverse.

Um projeto está associado a um contrato de projeto por meio da entidade **Linha de contrato de projeto**.

As linhas de contrato do projeto no Dataverse criam uma regra de cobrança de contrato de projeto em aplicativos do Finance and Operations usando o mapa de tabela **Linhas de contrato de projeto (salesorderdetails)**. O método de cobrança define o tipo de regra de cobrança do contrato do projeto em aplicativos do Finance and Operations:

  - As linhas de contrato do projeto com um método de cobrança de tempo e material criam uma regra de cobrança de tempo e tipo de material.
  - As linhas de contrato do método de cobrança de preço fixo criam uma regra de cobrança em etapas.

As linhas do contrato do projeto podem ser revisadas pelo contador do projeto em aplicativos do Finance and Operations, acessando **Gerenciamento e contabilidade de projetos** > **Contratos de projeto** > **Configuração** > **Mostrar contabilidade padrão**, e revisando os detalhes na guia **Linhas de contrato**. O contador também pode definir dimensões financeiras padrão para as linhas de contrato do método de cobrança de preço fixo nessa guia.

## <a name="billing-milestones"></a>Etapas de cobrança

As linhas do contrato do projeto que usam o método de cobrança de preço fixo são faturadas por meio de etapas de cobrança. As etapas de cobrança são sincronizadas para transações de conta de projeto em aplicativos do Finance and Operations usando o mapa de tabela **Etapas da linha do contrato de integração do Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integração de etapas de cobrança.](./media/2Milestones.jpg)

O contador pode revisar transações de conta e ajustar os atributos contábeis para essas transações, acessando **Gerenciamento e contabilidade de projetos** > **Contratos de projeto** > **Manter** > **Transações na conta** ou **Gerenciamento e contabilidade de projetos** > **Todos os projetos** > **Manter** > **Transações na conta**.

Quando você cria pela primeira vez uma etapa de cobrança para determinada linha de contrato de projeto, o sistema cria automaticamente um projeto de estimativa de receita de preço fixo para o projeto associado a essa linha de contrato. Projetos de estimativa de receita de preço fixo podem ser revisados acessando **Gerenciamento e contabilidade de projetos** > **Projetos de estimativa de receita de preço fixo**.

### <a name="project-tasks"></a>Tarefas do projeto

As tarefas do projeto são sincronizadas com aplicativos do Finance and Operations por meio do mapa de tabela **Tarefas do projeto (msdyn\_projecttasks)** apenas para fins de referência. Não há suporte a operações de criação, atualização e exclusão por meio de aplicativos do Finance and Operations.

  ![Integração de tarefas de projeto.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de projeto

A entidade **Funções de recursos do projeto** está sincronizada com aplicativos do Finance and Operations usando o mapa de tabela **Funções de recursos do projeto para todas as empresas (bookableresourcecategories)** apenas para fins de referência. Como funções de recursos no Dataverse não são específicas da empresa, o sistema cria automaticamente os respectivos registros de funções de recursos específicos da empresa em aplicativos do Finance and Operations para todas as entidades legais incluídas no escopo de integração de gravação dupla.

![Integração de funções do recurso.](./media/5Resources.jpg)

Recursos de projeto no Project Operations são mantidos no Dataverse e não são sincronizados com aplicativos do Finance and Operations.

### <a name="transaction-categories"></a>Categorias de transação

As categorias de transação são mantidas no Dataverse e sincronizadas com aplicativos do Finance and Operations usando o mapa de tabela **Categorias de transação do projeto (msdyn\_transactioncategories)**. Após a sincronização do registro da categoria da transação, o sistema cria automaticamente quatro registros da categoria compartilhada. Cada registro corresponde a um tipo de transação em aplicativos do Finance and Operations e os vincula ao registro da categoria de transação.

![Integração de categorias de transação.](./media/4TransactionCategories.jpg)

O uso de categorias de transação para estimativas e dados reais exige que o contador do projeto ou administrador do sistema crie categorias de projeto correspondentes em cada entidade legal. Para obter mais informações, consulte [Configurar categorias de projeto](../project-accounting/configure-project-categories.md).
