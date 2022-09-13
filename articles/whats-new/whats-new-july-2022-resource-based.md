---
title: Novidades em julho de 2022 – Project Operations para cenários baseados em recursos/sem estoque
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de julho de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403937"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em julho de 2022 – Project Operations para cenários baseados em recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.44.0.22
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão. Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Implantação e Configuração | 2761472 | Um erro de instalação do Project Operations é tratado. |
| Cobrança e preço | 2746940 | O nome da linha do subcontrato deve ter um tamanho máximo de 100 caracteres. |
| Cobrança e preço | 2739162 | Os clientes devem poder ver os botões da faixa de opções na exibição de grade de dados reais. |
| Planejamento e acompanhamento de projeto | 2730318 | Validação atualizada para caracteres sem suporte no assunto do projeto. |
| Cobrança e preço | 2705361 | Os dados reais de vendas cobradas com base em etapa devem ser incluídos nos campos de rastreamento do projeto. |
| Cobrança e preço | 2675880 | Impedir que um projeto seja vinculado a uma linha de contrato que não seja baseada em trabalho. |
| Cobrança e preço | 2664396 | Se uma lista de preços de cotação for salva sem uma cotação, deve haver um erro informando que a cotação não pode estar vazia. |
| Cobrança e preço | 2184019 | A guia **Cobrança Baseada em Tarefas** não deve ser exibida para projetos que não tenham contrato ou cotação de apoio. |
| Tempo e Despesa | 2754459 | Quando o fluxo da nuvem de agendamento recorrente estiver inativo, mostre o banner e ignore o processamento assíncrono. |
| Cobrança e preço | 2724391 | A exceção errada é lançada quando a regra de cobrança dividida do contrato do projeto não possui um valor do cliente. |
| Cobrança e preço | 2708638 | O registro não foi encontrado durante a pesquisa de grade em Usos de materiais e Aprovações para usos de materiais.|
| Cobrança e preço | 2686977 | Impedir a validação da linha da fatura durante a criação da fatura. |
| Cobrança e preço | 2683032 | A cópia de funções e categorias passíveis de cobrança não ultrapassa 5.000 registros.|
| Cobrança e preço | 2673363 | A porcentagem de consumo de custo no projeto é corrompida quando existem estimativas e dados reais de esforço e despesas para um projeto. |

### <a name="project-management-and-accounting-in-finance"></a>Gerenciamento e contabilidade de projeto no Finance

Para obter informações sobre as correções de bug incluídas nesta atualização, entre no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [artigo da Base de Dados de Conhecimento](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Recursos ativados por padrão na futura versão

A tabela a seguir lista os recursos ativados por padrão na versão 10.0.29. A maioria dos recursos ativados automaticamente pode ser desativada no [Gerenciamento de recursos](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). No futuro, alguns recursos que foram ativados automaticamente poderão ser removidos do Gerenciamento de recursos e se tornarem obrigatórios. Essa mudança garante que os clientes estejam usando a funcionalidade atual, para que os aprimoramentos possam ser baseados na funcionalidade atual à medida que forem adicionados. Os recursos nunca serão ativados automaticamente em menos de um ano, a menos que sejam considerados essenciais.

| Nome do recurso | Habilitar data | Recurso adicionado | Estado do recurso | Módulo |
| --- | --- | --- |--- |--- |
| Ativar o ajuste da transação de hora com base na mudança na alocação da regra de financiamento | 16 de setembro de 2022 | 7 de outubro de 2020 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Recurso de estorno de fatura de pré-pagamento de ordem de compra do projeto | 16 de setembro de 2022 | 6 de outubro de 2021 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Excluir linhas de proposta de fatura ao usar o Project Operations para cenários baseados em recursos/sem estoque | 16 de setembro de 2022 | 6 de outubro de 2021 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Ajustar a contabilidade em uma transação de projeto lançada | 16 de setembro de 2022 | 10 de maio de 2020 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Ativar a configuração de contabilidade padrão para o projeto | 16 de setembro de 2022 | 19 de fevereiro de 2020 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Habilitar várias linhas de contrato para um projeto | 16 de setembro de 2022 | 29 de junho de 2020 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Tornar os diários de horas do projeto somente leitura se o status de aprovação atual não permitir a edição | 16 de setembro de 2022 | 6 de outubro de 2021 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Ativar a sincronização de linhas de vendas de linhas de compra quando as linhas de compra forem atualizadas e o parâmetro de gerenciamento de alterações de pedidos de compra estiver ativado | 16 de setembro de 2022 | 7 de outubro de 2020 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Habilitar o Project Operations no Dynamics 365 Customer Engagement | 16 de setembro de 2022 | 29 de junho de 2020 | Ativado por padrão | Gerenciamento e contabilidade de projeto |
| Recurso de correção de reversão de transação do projeto | 16 de setembro de 2022 | 13 de julho de 2020 | Ativado por padrão | Gerenciamento e contabilidade de projeto |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Recursos que se tornam obrigatórios na próxima versão

A tabela a seguir lista os recursos que serão obrigatórios a partir da versão 10.0.29.

| Nome do recurso | Habilitar data | Recurso adicionado | Estado do recurso | Módulo |
| --- | --- | --- | --- | --- |
| Calcular o valor comprometido na fonte de financiamento sem arredondar a taxa de câmbio | 16 de setembro de 2022 | 14 de junho de 2020 | Obrigatório | Gerenciamento e contabilidade de projeto |
| Ativar lançamento de ajuste do projeto com a mesma conta contábil da transação original | 16 de setembro de 2022 | 14 de junho de 2020 | Obrigatório | Gerenciamento e contabilidade de projeto |
| Detalhe do valor comprometido do contrato do projeto | 16 de setembro de 2022 | 31 de agosto de 2019 | Obrigatório | Gerenciamento e contabilidade de projeto |
| Ativar a classificação por recurso durante a criação da proposta de fatura do projeto | 16 de setembro de 2022 | 31 de agosto de 2019 | Obrigatório | Gerenciamento e contabilidade de projeto |
