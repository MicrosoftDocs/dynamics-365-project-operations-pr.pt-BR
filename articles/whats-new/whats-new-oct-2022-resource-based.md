---
title: Novidades de outubro de 2022 – Project Operations para cenários baseados em recursos/não estocados
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de outubro de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem estoque.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806588"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de outubro de 2022 – Project Operations para cenários baseados em recursos/não estocados

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.57.0.176
- Gerenciamento e contabilidade de projetos em um ambiente do Dynamics 365 Finance versão 10.0.30

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

| Área do recurso | Nome do recurso | Mais informações |
| --- | --- | --- |
| Planejamento e acompanhamento de projeto | **Agendamento externo do Project Operations**<br>O modo de agendamento externo permite que os clientes criem, atualizem e excluam nativamente entidades relacionadas às estruturas analíticas de trabalho (WBS) usando as APIs do Dataverse nativas, sem os limites atuais impostos pelo Project for the Web. | [Agendamento externo](/dynamics365/project-operations/project-management/external-scheduling) |
| Implantação e Configuração | <p>**Permitir que os clientes escolham o tipo de implantação**<br>Atualizações baseadas no produto (PDUs) do Project Operations são usadas para instalar automaticamente a solução de gravação dupla do Project Operations quando as soluções de orquestração e núcleo de gravação dupla são instaladas no ambiente.</p><p>Este recurso apresenta um novo parâmetro **Comportamento da atualização da solução** nos parâmetros do projeto. Quando esse parâmetro é definido como **Somente Lite**, as PUDs não instalarão mais automaticamente a solução de gravação dupla do Project Operations, mesmo se as soluções de orquestração e núcleo de gravação dupla estiverem instaladas no ambiente. Esse comportamento beneficiará os clientes que planejam usar soluções de gravação dupla para integrar pedidos de vendas a aplicativos de finanças e operações, mas desejam usar o Project Operations no modo Lite (ou seja, sem integração a aplicativos de finanças e operações).</p> | |
| Cobrança e preço | <p>**Conversão de moeda para transação de venda de despesa não faturada em ambientes integrados**<br>Para clientes que usam o Project Operations integrado com aplicativos de finanças e operações (ou seja, no tipo de implantação de recurso/sem estoque), as taxas de câmbio geralmente são controladas em aplicativos de finanças e operações. No entanto, se uma categoria de despesa deve ser precificada usando o método de cálculo de preço "ao custo" ou "markup sobre custo" quando o cliente é cobrado, a taxa de câmbio usada para calcular o valor das vendas usa as taxas de câmbio no Dataverse, não a taxa de câmbio taxas de aplicativos de finanças e operações.</p><p>Este recurso apresenta um novo parâmetro **Comportamento de conversão de moeda** nos parâmetros do projeto. Quando esse parâmetro é definido como **Estendido com fallback**, os valores de vendas não faturadas em transações de despesas são calculados usando as taxas de câmbio dos aplicativos de finanças e operações.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações dos mapas de gravação dupla do Project Operations

Não há atualizações para mapas de gravação dupla do Project Operations nesta versão. Para obter uma lista atual e versões dos mapas de gravação dupla do Project Operations, consulte [Versões de mapa de gravação dupla do Project Operations](../environment/resource-dual-write-maps.md).

Sempre execute a versão mais recente do mapa em seu ambiente e ative todos os mapas de tabela relacionados, à medida você atualizar a solução do Project Operations Dataverse e a versão da solução do Finance. Alguns recursos e capacidades poderão não funcionar corretamente se a versão mais recente do mapa não estiver ativada. É possível exibir a versão ativa do mapa na coluna **Versão** na página **Gravação dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e salve a versão selecionada. Se você personalizou um mapa de tabela pronto para uso, reaplique as alterações. Para obter mais informações, consulte [Gerenciamento do ciclo de vida do aplicativo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se você encontrar um problema ao iniciar o mapa, siga as instruções na seção [Problema de colunas de tabela ausentes em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de solução de problemas de gravação dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2316317 | O sistema permite que sejam criadas faturas que não tenham transações passíveis de cobrança. |
| Cobrança e preço | 2737300 | Valide a disponibilidade do campo **Cliente** antes de acessar o formulário. |
| Cobrança e preço | 2744948 | Adicione uma verificação nula para o método de cobrança. |
| Cobrança e preço | 2763515 | Tratamento de erro de referência nula quando falta o contrato de venda da fatura. |
| Cobrança e preço | 2844301 | A criação da fatura em lote falha devido a um erro. |
| Cobrança e preço | 2845869 | Armazenamento incorreto do Serviço da Organização. |
| Cobrança e preço | 2853729 | Os detalhes da função e do preço são atualizados quando o tipo de cobrança é modificado. |
| Cobrança e preço | 2940350 | Quando os preços reais são precificados, apenas as listas de preços ativas devem ser inseridas automaticamente. |
| Implantação e Configuração | 3001206 | A entidade msdyn\_replaylogheader está impedindo atualizações de organizações de clientes. |
| Gerenciamento de Oportunidades | 2755582 | Tratamento de exceções de referência nula no Auxiliar de Regra de Cobrança Dividida. |
| Gerenciamento de Oportunidades | 2761477 | Quando o faturamento dividido é usado, a exclusão de um marco (cabeçalho) deixa os marcos órfãos. |
| Gerenciamento de Oportunidades | 2767595 | Quando um registro de uso de material é aberto no formulário principal, o recurso reservável para o registro é alterado para o usuário conectado no momento. |
| Planejamento e acompanhamento de projeto | 2790384 | O tempo limite Pending OperationSet é muito curto. |
| Planejamento e acompanhamento de projeto | 2957840 | Tarefas não podem ser salvas e colunas não podem ser adicionadas à página **Tarefas** no Project Operations integrado. |
| Gerenciamento de Recursos | 2751560 | Unidades organizacionais preferenciais inconsistentes em requisitos de recursos. |
| Subcontratação | 2853245 | A correspondência de dados reais da linha da fatura do fornecedor não atualiza o status de verificação se uma linha do contrato já estiver vinculada à linha da fatura do fornecedor. |
| Subcontratação | 2907231 | A etapa do processo de faturas de fornecedor não pode avançar. |
| Tempo e Despesa | 2867363 | Os registros não saem da exibição Ausências/Férias para aprovação quando são colocados na fila para aprovação. |
| Tempo e Despesa | 2894405 | TESA: o diretório POC não utilizado está causando problemas de conformidade. |

### <a name="project-management-and-accounting-in-finance"></a>Gerenciamento e contabilidade de projeto no Finance

Para obter informações sobre as correções de bug incluídas nesta atualização, entre no Microsoft Dynamics Lifecycle Services e consulte o [artigo da Base de Dados de Conhecimento](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
