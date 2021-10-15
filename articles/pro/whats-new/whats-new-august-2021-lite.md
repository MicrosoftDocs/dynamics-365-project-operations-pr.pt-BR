---
title: O que há de novo em agosto de 2021 - Implantação lite do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de agosto de 2021 da implantação lite do Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323492"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>O que há de novo em agosto de 2021 - Implantação lite do Project Operations

_Aplica-se a: Implantação lite – gerenciar faturamento pro forma_

Este tópico se aplica aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations no ambiente do Dataverse versão 4.13.0.152

## <a name="features-included-in-this-release"></a>Os recursos incluídos nesta versão

Os seguintes recursos estão incluídos nesta versão:

- **Conjuntos de aprovações**: a aprovação define tempo do grupo, despesa ou solicitações de aprovação de uso de material em subconjuntos menores de operações. Esse agrupamento permite que as aprovações sejam processadas por projeto, em uma ordem específica, e permite novas tentativas e sequenciamento. O agrupamento das solicitações de aprovação aumenta a confiabilidade e a capacidade de rastreamento do processamento de aprovações para grandes volumes de aprovações. Para obter mais informações, veja [Conjuntos de aprovações](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área do recurso** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Cobrança e preço | 2295625 | O nome do marco deve ser copiado da agenda da fatura para o detalhe da linha da fatura. |
| Cobrança e preço | 2316323 | O desconto não deve ser editável em uma fatura pró-forma no Project Operations para cenários baseados em recursos. |
| Gerenciamento de oportunidades | 2338619 | As regras de negócios **Oportunidade** e **Cotação** devem ser chamadas apenas nas páginas. |
| Gerenciamento de recursos | 2316523 | O uso de **Enviar Solicitação** de um requisito de recurso com uma função anexada não deve exibir um erro. |
| Gerenciamento de recursos | 2326885 | A criação de um requisito de recurso por meio de um projeto não deve exibir um erro. |
| Horas e despesas | 2335584 | Fluxos de tarefas obsoletas na entrada de tempo. |
| Horas e despesas | 2336884 | O botão de entrada de tempo **Copiar Semana** deve funcionar para mais do que apenas o usuário atual. |