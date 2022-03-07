---
title: Novidades em março de 2021 – Project Operations para cenários baseados em recursos/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de março de 2021 do Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b11a57ae152be154fd6a7d330c8520f3b295ce3ef5cc7051ac9b343e3bcdbe12
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006322"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em março de 2021 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations no ambiente do Dataverse versão 4.8.0.91 
- Gerenciamento e contabilidade de projeto no ambiente do Dynamics 365 Finance versão 10.0.16 

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse


| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2133873 | Corrigida a exibição do símbolo da moeda **Preço Unitário de Venda** na grade **Estimativas de Despesas**. |
| Cobrança e preço | 2174616 | Ao ganhar uma cotação, a lista de preços personalizada do contrato é referenciada nos detalhes da linha de contrato que são copiados da cotação. |
| Gerenciamento de Oportunidades | 2167475 | Valor de imposto fixo na fatura de correção que originou uma entrada real não faturada. |
| Gerenciamento de Oportunidades | 2176285 | O valor do imposto não deve ser copiado dos detalhes da linha do contrato de venda/cotação para os detalhes da linha do contrato de custo/cotação. |
| Gerenciamento de Oportunidades | 2188079 | A regra de divisão de cobrança não deve ser criada para contratos que não sejam baseados no trabalho. |
| Planejamento e acompanhamento | 2125274 | Atributo **Project Dual Write Map** para **Project Start Date Mapping** atualizado de **msdyn\_taskearlieststart** para **msdyn\_actualstart**. |
| Planejamento e acompanhamento | 2138853 | Função de cópia do projeto atualizada para garantir que as linhas de estimativa de despesa que fazem referência às tarefas sejam copiadas para o projeto de destino. |
| Planejamento e acompanhamento | 2154306 | Corrigidos os problemas com a exclusão de estimativas de despesas em Project Operations para cenários baseados em recursos. |
| Planejamento e acompanhamento | 2173259 | Função de cópia do projeto atualizada para garantir que não exiba a mensagem de erro **Copiando WBS** em determinados cenários. |
| Tempo e Despesa | 2148910 | Corrigido o problema de exibição com a página **Editar Entrada** na grade **Entrada de Tempo**. |
| Tempo e Despesa | 2159798 | Controles mais rígidos para garantir que as entradas de despesas aprovadas não possam ser editadas. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Visão geral de gerenciamento e contabilidade de projeto no Dynamics 365 Finance

Para obter mais informações, consulte [Novidades em janeiro de 2021 – Project Operations para cenários baseados em recursos/sem estoque](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Atualizações regulatórias

Para obter informações sobre atualizações regulatórias do Finance and Operations, consulte [Atualizações regulatórias](/dynamics365/finance/localizations/regulatory-updates). Outra forma de aprender sobre atualizações regulatórias é entrar no LCS e exibir as atualizações regulatórias planejadas usando a ferramenta de pesquisa de problemas. A pesquisa de problemas permite pesquisar por país, tipo de recurso e versão.


[!INCLUDE[footer-include](../includes/footer-banner.md)]