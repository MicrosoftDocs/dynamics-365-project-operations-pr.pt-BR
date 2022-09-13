---
title: Novidades em agosto de 2022 – Project Operations para cenários baseados em recursos/sem estoque
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de agosto de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403842"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em agosto de 2022 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.45.0.53
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão. Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gerenciamento de oportunidades | 2762089 | Tratamento de erros ao fechar o contrato como perdido se o salvamento automático estiver desabilitado na organização.|
|Planejamento e acompanhamento de projeto | 2767841 | A telemetria atualiza os cenários de criação ou atualização da entidade do projeto.|
|Cobrança e preço | 2771072 | Tratamento de exceção de referência nula durante a cotação vencedora.|
|Cobrança e preço | 2844181 |Falha ao obter uma ID de correlação e bloquear a criação de uma fatura.|
|Cobrança e preço | 2852836 | Faltam dados reais intercompanhia para Despesas intercompanhia criadas e aprovadas em CE.|


### <a name="project-management-and-accounting-in-finance"></a>Gerenciamento e contabilidade de projeto no Finance

Para obter informações sobre as correções de bug incluídas nesta atualização, entre no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [artigo da Base de Dados de Conhecimento](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
