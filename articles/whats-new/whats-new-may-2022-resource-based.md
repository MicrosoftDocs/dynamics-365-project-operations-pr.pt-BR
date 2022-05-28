---
title: Novidades em maio de 2022 – Project Operations para cenários baseados em recurso/sem estoque
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de maio de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709958"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em maio de 2022 – Project Operations para cenários baseados em recurso/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.42.0.70
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão. Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade
### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gerenciamento de recursos | 2634019 | Aprimoradas as mensagens de erro para validações de negócios ao adicionar membros genéricos da equipe como recursos. |
| Planejamento e acompanhamento de projeto | 2648515 | Atualizações restritas de **ownerid**, **state** e **status** em entidades de agendamento. |
| Cobrança e preço | 2653167 | O separador decimal da grade **Estimativas** deve seguir as configurações de formato em **Opções Pessoais**. |
| Cobrança e preço| 2662251 | Os valores nos campos **Unidade corrigida** e **Grupo de unidades** são padrão ao criar registros em estimativas de material. |
| Cobrança e preço| 2571408 | Os dados reais de vendas não cobradas são carimbados com uma ID de fatura proforma ao criar uma fatura de rascunho. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gerenciamento e contabilidade de projetos no Dynamics 365 Finance

Para obter informações sobre as correções de bug incluídas nesta atualização, entre no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [artigo da Base de Dados de Conhecimento](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
