---
title: Versões do mapa de gravação dupla do Project Operations
description: Este tópico fornece a lista de mapas de gravação dupla necessárias para o Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 385893e8ecdb29f4dc411c233b9ae19bb2448dfd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612736"
---
# <a name="project-operations-dual-write-map-versions"></a>Versões do mapa de gravação dupla do Project Operations

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

O uso do Dynamics 365 Project Operations para cenários de recursos/sem estoque exige um conjunto de mapas de gravação dupla para execução no ambiente. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Mapas de pré-requisito: solução de orquestração de gravação dupla

Os mapas a seguir são pré-requisitos necessários para a solução Project Operations. Execute os mapas listados na tabela a seguir e mapas de tabela relacionados em seu ambiente.

| Mapa de tabela | Sincronização inicial |
| --- | --- |
| Contabilidade (msdyn_ledgers) | Requer sincronização inicial para o mapa da tabela e todos os pré-requisitos. O mestre para sincronização inicial são os aplicativos de finanças e operações. |
| Entidades legais (cdm_companies) | Não obrigatório. O sistema preenche essa entidade automaticamente quando os ambientes são vinculados usando gravação dupla. |
| Clientes V3 (contas) | Não é necessário para provisionamento. |
| Fornecedores V2 (msdyn_vendors) | Não é necessário para provisionamento. |

1. Na lista de mapas, selecione o mapa Razão **(msdyn\_ledgers)** com todos os pré-requisitos e marque a caixa de seleção **Sincronização inicial**. No campo **Mestre para sincronização inicial**, selecione **Aplicativos de Finanças e Operações** para o mapa do razão e todos os mapas de pré-requisitos. Selecione **Executar**.

![Sincronização do mapa do razão.](media/DW6.png)

2. Siga as mesmas etapas para todos os mapas de tabela restantes listados na tabela acima. Não marque a caixa de seleção **Sincronização inicial** ao executar esses mapas.

## <a name="project-operations-dual-write-maps"></a>Mapas de gravação dupla do Project Operations

Os mapas a seguir são necessários para uma solução Project Operations. As versões de mapas de gravação dupla estão listadas a partir da atualização do Project Operations de maio de 2021, versão 4.10.0.186.

| Mapa de entidade | Última versão | Sincronização inicial | Versão obrigatória do Dynamics 365 Finance |
| --- | --- | --- | --- |
| Entidade de integração para relacionamentos de transações do projeto (msdyn\_transactionconnections) | 1.0.0.0 | Não é necessário para provisionamento. ||
| Cabeçalhos de contrato de projeto (ordens de venda) | 1.0.0.1 | Não é necessário para provisionamento. ||
| Linhas de contrato do projeto (salesorderdetails) | 1.0.0.0 | Não é necessário para provisionamento. ||
| Fonte de financiamento do projeto (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Não é necessário para provisionamento. ||
| Tabela de integração do Project Operations para estimativas de material (msdyn\_estimateslines) | 1.0.0.0 | Não é necessário para provisionamento. ||
| Propostas de fatura do projeto V2 (faturas) | 1.0.0.3 | Não é necessário para provisionamento. ||
| Valores reais da integração do Project Operations (msdyn_actuals) | 1.0.0.14 | Não é necessário para provisionamento. ||
| Marcos de linha de contrato de integração do Project Operations (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Não é necessário para provisionamento. ||
| Entidade de integração do Project Operations para estimativas de despesas (msdyn_estimatelines) | 1.0.0.2 | Não é necessário para provisionamento. ||
| Entidade de integração do Project Operations para estimativas de horas (msdyn_resourceassignments) | 1.0.0.5 | Não é necessário para provisionamento. ||
| Entidade de exportação de categorias de despesas do projeto de integração do Project Operations (msdyn_expensecategories) | 1.0.0.1 | Não é necessário para provisionamento. ||
| Entidade de exportação de despesas do projeto de integração do Project Operations (msdyn_expenses) | 1.0.0.3 | Não é necessário para provisionamento. ||
| Entidade de exportação de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Não é necessário para provisionamento. ||
| Entidade de exportação de linha de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.4 | Não é necessário para provisionamento. | 10.0.26 ou posterior |
| Funções de recursos do projeto para todas as empresas (bookableresourcecategories) | 1.0.0.1 | Requer uma sincronização inicial para o mapa da tabela para sincronizar funções de recurso de gerente de projeto e membro de equipe que são preenchidas no ambiente do Dynamics 365 Dataverse durante o provisionamento. O Dataverse é a principal fonte para a sincronização inicial. ||
| Tarefas do projeto (msdyn_projecttasks) | 1.0.0.4 | Não é necessário para provisionamento. ||
| Categorias de transação do projeto (msdyn_transactioncategories) | 1.0.0.0 | Não é necessário para provisionamento. ||
| Projetos V2 (msdyn_projects) | 1.0.0.2 | Não é necessário para provisionamento. ||

Conclua as etapas a seguir para executar os mapas listados.

1. Habilite as funções de recurso do projeto para o mapa da tabela **todas as empresas (bookableresourcecategories)**, pois este mapa exige a sincronização inicial. No campo **Mestre para sincronização inicial**, selecione **Common Data Service**. 

 ![Sincronização do mapa de tabela de função de recurso.](media/6ResourceInitialSync.jpg)

 Espere até que o status do mapa seja **Em execução** antes de passar para a próxima etapa.

2. Selecione todos os mapas necessários restantes. Você pode filtrá-los na lista de mapas de gravação dupla usando a palavra-chave, **Projeto** em pesquisa no canto superior direito. Você pode selecionar vários mapas e depois executá-los. Para obter mais informações, consulte [Gerenciar vários mapas de tabela](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Verifique também se você habilitou e executou mapas de entidade relacionados.

### <a name="project-operations-dual-write-map-versions"></a>Versões do mapa de gravação dupla do Project Operations

Sempre execute a versão mais recente do mapa em seu ambiente. Certos recursos e funcionalidades talvez não funcionem corretamente se uma das seguintes condições existir:

- Um mapa não está ativado.
- A versão mais recente do mapa não está ativada. 
- Os mapas de tabela relacionados não estão ativados.

É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Você pode ativar uma nova versão do mapa selecionando **Versões do mapa de tabela**, selecionando a versão mais recente e salvando a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, precisará reaplicar as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
