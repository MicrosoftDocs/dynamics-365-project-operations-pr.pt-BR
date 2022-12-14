---
title: Novidades em novembro de 2022 – Project Operations para cenários baseados em recursos/sem estoque
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de novembro de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831069"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em novembro de 2022 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.58.0.119
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão. Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, conforme você atualiza sua solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2781818 | Erro de chave não encontrada ao definir o preço padrão para o log de uso de material. |
| Cobrança e preço | 2922373 | Não é possível vincular a linha de cotação ao projeto que foi encerrado como cotação perdida. |
| Cobrança e preço | 2943206 | O campo **Linha de Contrato** na Entidade de Projeto deve ser opcional. |
| Cobrança e preço | 2953182 | Melhore a mensagem de erro para notas fiscais de correção.|
| Cobrança e preço | 2959500 | Não é possível vincular a linha de cotação a uma tarefa de projeto que já está associada a uma cotação perdida.|
| Cobrança e preço | 2959560 | Mensagem "Este cliente já está no contrato do projeto" recebida ao encerrar a cotação como ganha em determinados locais. |
| Cobrança e preço | 3031727 | As atribuições de recursos falham com o erro O campo obrigatório "msdyn_Company" está ausente. |
| Cobrança e preço | 3036905 | A empresa proprietária nunca é inicializada no ProjectTeamMember. |
| Gerenciamento de Oportunidades | 2763519 | Erro de referência nula em EnsureProjectContractAllowsUpdates. |
| Gerenciamento de Oportunidades | 2783798 | Ao importar estimativas de projeto na linha de cotação, faltam descrições de tarefas para estimativas de despesas e materiais.|
| Gerenciamento de Oportunidades | 2988635 | Melhore a descrição da mensagem de erro ao excluir o cliente na cotação. |
| Gerenciamento de Oportunidades | 3001191 | Não é possível criar a cotação da oportunidade em que o método de cobrança é especificado como nulo. |
| Atualizar | 3012324 | A conversão do projeto falhou em um projeto com caracteres de controle como Tab em seu nome. || Planejamento e acompanhamento de projeto | 2790384 | O tempo limite Pending OperationSet é muito curto. |
| Planejamento e acompanhamento de projeto | 3044275 | Localização ausente para: missingProjectSchedulerErrorMessage. |
| Planejamento e acompanhamento de projeto | 3044277 | A grade de reconhecimento de projeto não é carregada quando o agendador não está definido.|
| Gerenciamento de Recursos | 2943153 | Atualize a guia Rastreamento para mostrar duas casas decimais para Duração.|
| Subcontratação | 2932774 | Linha de fatura do fornecedor somente leitura gerando erro incorretamente. |
| Subcontratação | 2939556 | O status do cabeçalho da fatura do fornecedor não deve ser definido como rascunho na exclusão de linha se estiver inativo. |
| Tempo e Despesa | 2939998 | Adquira a nova versão do TESA no ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Gerenciamento e contabilidade de projeto no Finance

Para obter informações sobre as correções de bug incluídas nesta atualização, entre no Microsoft Dynamics Lifecycle Services e consulte o [artigo da Base de Dados de Conhecimento](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
