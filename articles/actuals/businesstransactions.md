---
title: Transações comerciais no Project Operations
description: Este tópico apresenta uma visão geral do conceito de transações comerciais no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582190"
---
# <a name="business-transactions-in-project-operations"></a>Transações comerciais no Project Operations

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

No Microsoft Dynamics 365 Project Operations, *transação comercial* é um conceito abstrato que não é representado por nenhuma entidade. No entanto, alguns campos e processos comuns em entidades são designados para usar o conceito de transações comerciais. As seguintes entidades usam essa abstração:

- Detalhes da linha de cotação
- Detalhes da linha de contrato
- Linhas de estimativa
- Linhas do diário
- Dados Efetivos

Dessas entidades, Detalhes da linha de cotação, Detalhes da linha do contrato e Linhas de estimativa são mapeadas para a *fase de estimativa* no ciclo de vida do projeto. As entidades Linhas do diário e Dados reais são mapeadas para a *fase de execução* no ciclo de vida do projeto.

O Project Operations trata os registros em todas essas cinco entidades como transações comerciais. A única diferença é que os registros nas entidades mapeadas para a fase de estimativa (Detalhes da linha de cotação, Detalhes da linha do contrato e Linhas de estimativa) são considerados *previsões financeiras*, enquanto os registros nas entidades mapeadas para a fase de execução (Linhas do diário e Dados reais) são considerados *fatos financeiros* já ocorridos.

Para obter mais informações, consulte [Estimativas](../project-management/estimating-projects-overview.md) e [dados reais](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceitos que são exclusivos às transações comerciais

Os seguintes conceitos são exclusivos ao conceito de transações comerciais:

- Tipo de transação
- Classe da transação
- Origem da transação
- Conexão da transação

### <a name="transaction-type"></a>Tipo de transação

O tipo de transação representa o tempo e o contexto do impacto financeiro em um projeto. Ele é definido por um conjunto de opções que tem os seguintes valores permitidos no Project Operations:

- Custo
- Contrato do projeto
- Vendas não cobradas
- Vendas cobradas
- Vendas entre organizações
- Custo da unidade de recursos

### <a name="transaction-class"></a>Classe da transação

A classe da transação representa os diferentes tipos de custo que incorreram nos projetos. Ele é definido por um conjunto de opções que tem os seguintes valores permitidos no Project Operations:

- Hora
- Despesa
- Material
- Taxa
- Etapa
- Imposto

> [!NOTE]
> O valor **Etapa** geralmente é usado pela lógica de negócios para cobrança de preço fixo no Project Operations.

### <a name="transaction-origin"></a>Origem da transação

Origem da transação é uma entidade que armazena a origem de cada transação comercial para ajudar na geração de relatórios e na rastreabilidade. À medida que a execução do projeto começa, cada transação comercial cria outra transação comercial, que, por sua vez, cria outra transação comercial e assim por diante.

### <a name="transaction-connection"></a>Conexão da transação

Conexão da transação é uma entidade que armazena a relação entre duas transações comerciais semelhantes, como custo e dados reais de vendas relacionadas ou reversões de transação que são acionadas por atividades de cobrança, como confirmação da fatura ou correções da fatura.

Juntas, as entidades Origem da transação e Conexão da transação ajudam você a rastrear relações entre transações comerciais e ações que fizeram com que uma transação comercial específica fosse criada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
