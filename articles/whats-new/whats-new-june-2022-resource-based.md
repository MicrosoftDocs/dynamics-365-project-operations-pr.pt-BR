---
title: Novidades em junho de 2022 – Project Operations para cenários baseados em recursos/sem estoque
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de junho de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959384"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em junho de 2022 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.43.0.77
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

A tabela a seguir mostra os mapas de gravação dupla que foram modificados ou adicionados na versão de junho de 2022 do Project Operations.

| Mapa de entidade | Versão atualizada | Comentários |
| --- | --- | --- |
| Entidade de exportação de fatura de fornecedor do projeto de integração do Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Preterido o campo herdado e mapeado para o novo campo para rastreamento do estado da fatura do fornecedor. |

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Subcontratação | 2708885 | Corrigida a mensagem de erro que aparece quando um usuário cria um registro de cabeçalho de reserva de recurso reservável em que nenhum recurso reservável é preenchido. |
| Planejamento e rastreamento de projeto | 2629441 | Corrigida a lógica de acionamento do fluxo de trabalho para ajudar a evitar um loop infinito quando as tarefas do projeto são atualizadas. |
| Horas e despesas | 2641209 | As importações de entradas de horas de atribuições/reservas devem reter uma referência de recurso reservável. |
| Planejamento e rastreamento de projeto | 2651148 | O cabeçalho do documento do projeto deve ser protegido.|
| Planejamento e rastreamento de projeto | 2653145 | Adicionadas validações para garantir que um registro de projeto não possa ser criado com caracteres inválidos em seu nome. |
| Horas e despesas | 2654710 | Corrigida a filtragem na página **Aprovações**. |
| Cobrança e preço | 2667805 | Adicionadas validações para ajudar a evitar a criação de dados reais de vendas cobradas se não existirem dados reais de vendas não cobradas. |
| Cobrança e preço | 2668378 | Validações adicionadas para ajudar a impedir que uma dimensão de preço personalizada seja adicionada, a menos que um nome lógico e um nome de campo sejam preenchidos. |
| Subcontratação | 2677485 | Atualizada a versão de destino do mapa de gravação dupla de linhas de fatura do fornecedor. |
| Horas e despesas | 2700428 | Aprimorou a lógica de aprovações para garantir que outros conjuntos de aprovações para o projeto possam ser processados mesmo se um dos conjuntos de aprovações estiver preso em trabalhos do sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Gerenciamento e contabilidade de projeto no Finance

Para obter informações sobre as correções de bug incluídas nesta atualização, entre no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [artigo da Base de Dados de Conhecimento](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
