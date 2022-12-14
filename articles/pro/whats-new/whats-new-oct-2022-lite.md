---
title: Novidades de outubro de 2022 – implantação do Project Operations lite
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de outubro de 2022 da implantação lite do Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806589"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Novidades de outubro de 2022 – implantação do Project Operations lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este artigo se aplica aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations em um ambiente do Dataverse versão 4.57.0.176

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

| Área do recurso | Nome do recurso | Mais informações |
| --- | --- | --- |
| Planejamento e acompanhamento de projeto | **Agendamento externo do Project Operations**<br>O modo de agendamento externo permite que os clientes criem, atualizem e excluam nativamente entidades relacionadas às estruturas analíticas de trabalho (WBS) usando as APIs do Dataverse nativas, sem os limites atuais impostos pelo Project for the Web. | [Agendamento externo](/dynamics365/project-operations/project-management/external-scheduling) |
| Implantação e Configuração | <p>**Permitir que os clientes escolham o tipo de implantação**<br>Atualizações baseadas no produto (PDUs) do Project Operations são usadas para instalar automaticamente a solução de gravação dupla do Project Operations quando as soluções de orquestração e núcleo de gravação dupla são instaladas no ambiente.</p><p>Este recurso apresenta um novo parâmetro **Comportamento da atualização da solução** nos parâmetros do projeto. Quando esse parâmetro é definido como **Somente Lite**, as PUDs não instalarão mais automaticamente a solução de gravação dupla do Project Operations, mesmo se as soluções de orquestração e núcleo de gravação dupla estiverem instaladas no ambiente. Esse comportamento beneficiará os clientes que planejam usar soluções de gravação dupla para integrar pedidos de vendas a aplicativos de finanças e operações, mas desejam usar o Project Operations no modo Lite (ou seja, sem integração a aplicativos de finanças e operações).</p> | |

## <a name="quality-updates"></a>Atualizações de qualidade

| Área do recurso | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Cobrança e preço | 2316317 | O sistema permite que sejam criadas faturas que não tenham transações passíveis de cobrança. |
| Cobrança e preço | 2737300 | Valide a disponibilidade do campo Cliente antes de acessar o formulário. |
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
| Gerenciamento de Recursos | 2751560 | Unidades organizacionais preferenciais inconsistentes em requisitos de recursos. |
| Subcontratação | 2907231 | A etapa do processo de faturas de fornecedor não pode avançar. |
| Tempo e Despesa | 2867363 | Os registros não saem da exibição Ausências/Férias para aprovação quando são colocados na fila para aprovação. |
| Tempo e Despesa | 2894405 | TESA: o diretório POC não utilizado está causando problemas de conformidade. |
