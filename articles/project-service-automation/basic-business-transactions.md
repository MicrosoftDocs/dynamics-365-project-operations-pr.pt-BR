---
title: Transações comerciais
description: Este tópico fornece informações sobre transações comerciais.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f059d9ec-878d-40c1-bd00-a8966bdf4e29
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe93ec07e9eed0af02c62d08f18a0b2aaeff7996
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749173"
---
# <a name="business-transactions"></a>Transações comerciais

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

No Dynamics 365 Project Service Automation, a *transação comercial* é um conceito abstrato que não é representado por nenhuma entidade. No entanto, alguns campos e processos comuns em entidades são designados para usar o conceito de transações comerciais. As seguintes entidades usam essa abstração:

- Detalhes da linha de cotação
- Detalhes da linha de contrato
- Linhas de estimativa
- Linhas do diário
- Dados Efetivos

Dessas entidades, Detalhes da linha de cotação, Detalhes da linha de contrato e Linhas de estimativa são mapeadas para a fase de estimativa no ciclo de vida do projeto. As entidades Linhas do diário e Dados reais são mapeadas para a fase de execução no ciclo de vida do projeto.

O PSA trata registros nessas cinco entidades como transações comerciais. A única diferença é que os registros nas entidades que são mapeadas para a fase de estimativa são considerados previsões financeiras, enquanto os registros em entidades que são mapeadas para a fase de execução são considerados fatos financeiros que já tenham ocorrido.

Para obter mais informações, consulte [Estimativas](estimates.md) e [dados reais](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceitos que são exclusivos às transações comerciais
Os seguintes conceitos são exclusivos ao conceito de transações comerciais:

- Tipo de transação
- Classe da transação
- Origem da transação
- Conexão da transação

### <a name="transaction-type"></a>Tipo de transação

O tipo de transação representa o tempo e o contexto do impacto financeiro em um projeto. Ele é representado por um conjunto de opções que tem os seguintes valores permitidos no PSA:
- Custo
- Contrato de projeto
- Vendas não cobradas
- Vendas cobradas
- Vendas entre organizações
- Custo da unidade de recursos

### <a name="transaction-class"></a>Classe da transação

A classe da transação representa os diferentes tipos de custo que incorreram nos projetos. Ele é representado por um conjunto de opções que tem os seguintes valores permitidos no PSA:

- Hora
- Expense
- Material
- Taxa
- Etapa
- Imposto

O valor **Etapa** geralmente é usado pela lógica de negócios para cobrança de preço fixo no PSA.

### <a name="transaction-origin"></a>Origem da transação

A origem da transação é uma entidade que armazena a origem de cada transação comercial. Conforme a execução do projeto é iniciada, cada transação comercial gerará outra transação comercial que, por sua vez, criará outra e assim por diante. A entidade da origem de transação foi desenvolvida para armazenar dados sobre a origem de cada transação a fim de facilitar a criação de relatórios e a rastreabilidade. 

### <a name="transaction-connection"></a>Conexão da transação

A conexão da transação é uma entidade que armazena a relação entre duas transações comerciais semelhantes, como custo e dados reais de vendas relacionadas, ou reversões de transação acionadas pelas atividades de cobrança, como confirmação ou correções da fatura.

Juntas, as entidades Origem da transação e Conexão da transação ajudam você a acompanhar as relações entre transações comerciais e ações que resultaram na criação de uma transação comercial específica.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemplo: Como a Origem da transação funciona com a Conexão da transação

O exemplo a seguir mostra o processamento típico de entradas de tempo em um ciclo de vida de projeto do PSA.

> ![Processando entradas de tempo em um ciclo de vida do Project Service](media/basic-guide-17.png)
 
1. O envio de uma entrada de tempo causa a criação de duas linhas de diário: um para custo e outro para vendas não cobradas.
2. A aprovação eventual da entrada de tempo causa a criação de dois dados reais: um para custo e outro para vendas não cobradas.
3. Quando o usuário cria uma fatura de projeto, a transação da linha da fatura é criada usando dados do valor real de vendas não cobradas. 
4. Quando a fatura é confirmada, dois dados reais novos são criados: uma reversão de vendas não cobradas e dados reais de vendas cobradas.

Cada um desses eventos dispara a criação de registros nas entidades Origem da transação e Conexão da transação para ajudar a criar um rastreamento de relações entre esses registros que são criados na entrada de tempo, na linha do diário, nos dados reais e nos detalhes da linha fatura.

A tabela a seguir mostra os registros na entidade Origem da transação para o fluxo de trabalho anterior.

| Evento                        | Origem                   | Tipo de origem                       | Transação                       | Tipo de transação         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Envio de Tempo de Entrada        | GUID de registro do tempo de entrada   | Entrada de Horas                        | GUID de Registro da Linha do Diário (custo)   | Linha do Diário             |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Registro da Linha do Diário (vendas)  | Linha do Diário                      |                          |
| Aprovação do Tempo                | GUID de Registro da Linha do Diário | Linha do Diário                      | GUID de Registro de Vendas Não Cobradas        | Real                   |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Registro de Vendas Não Cobradas        | Real                            |                          |
| GUID de Registro da Linha do Diário     | Linha do Diário             | GUID de Registro do Valor Real de Custo           | Real                            |                          |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Registro do Valor Real de Custo           | Real                            |                          |
| Criação de Fatura             | GUID de registro do tempo de entrada   | Entrada de Horas                        | GUID de Transação da Linha da Fatura     | Transação da Linha da Fatura |
| GUID de Registro da Linha do Diário     | Linha do Diário             | GUID de Transação da Linha da Fatura     | Transação da Linha da Fatura          |                          |
| Confirmação da Fatura         | GUID da Linha da Fatura        | Linha da Fatura                      | GUID de Registro de Vendas Cobradas          | Real                   |
| GUID da Fatura                 | Fatura                  | GUID de Registro de Vendas Cobradas          | Real                            |                          |
| GUID de Detalhes da Linha da Fatura     | Detalhes da Linha da Fatura      | GUID de Registro de Vendas Cobradas          | Real                            |                          |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Registro de Vendas Cobradas          | Real                            |                          |
| GUID de Registro da Linha do Diário     | Linha do Diário             | GUID de Registro de Vendas Cobradas          | Real                            |                          |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Reversão de Vendas Não Cobradas      | Real                            |                          |
| GUID de Registro da Linha do Diário     | Linha do Diário             | GUID de Reversão de Vendas Não Cobradas      | Real                            |                          |
| Correção do Valor de Rascunho     | GUID de Detalhe da Linha de Fatura Antigo             | Transação da Linha da Fatura          | GUID de Detalhe da Linha de Fatura da Correção               | Transação da Linha da Fatura |
| GUID de Linha de Fatura Antigo                  | Linha da Fatura             | GUID de Detalhe da Linha de Fatura da Correção               | Transação da Linha da Fatura          |                          |
| GUID da Fatura Antiga             | Fatura                  | GUID de Detalhe da Linha de Fatura da Correção               | Transação da Linha da Fatura          |                          |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Detalhe da Linha de Fatura da Correção               | Transação da Linha da Fatura          |                          |
| GUID de Registro da Linha do Diário     | Linha do Diário             | GUID de Detalhe da Linha de Fatura da Correção               | Transação da Linha da Fatura          |                          |
| Correção da fatura confirmada | GUID de Detalhe da Linha de Fatura Antigo             | Transação da Linha da Fatura          | GUID de Valor Real de Vendas Cobradas Revertidas | Real                   |
| GUID de Linha de Fatura Antigo                  | Linha da Fatura             | GUID de Valor Real de Vendas Cobradas Revertidas | Real                            |                          |
| GUID da Fatura Antiga             | Fatura                  | GUID de Valor Real de Vendas Cobradas Revertidas | Real                            |                          |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Valor Real de Vendas Cobradas Revertidas | Real                            |                          |
| GUID de Registro da Linha do Diário     | Linha do Diário             | GUID de Valor Real de Vendas Cobradas Revertidas | Real                            |                          |
| GUID de Detalhe da Linha de Fatura Antigo                 | Transação da Linha da Fatura | GUID de Valor Real de Novas Vendas Não Cobradas    | Real                            |                          |
| GUID de Linha de Fatura Antigo                  | Linha da Fatura             | GUID de Valor Real de Novas Vendas Não Cobradas    | Real                            |                          |
| GUID da Fatura Antiga             | Fatura                  | GUID de Valor Real de Novas Vendas Não Cobradas    | Real                            |                          |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Valor Real de Novas Vendas Não Cobradas    | Real                            |                          |
| GUID de Registro da Linha do Diário     | Linha do Diário             | GUID de Valor Real de Novas Vendas Não Cobradas    | Real                            |                          |
| GUID de Detalhe da Linha de Fatura da Correção          | Transação da Linha da Fatura | GUID de Valor Real de Novas Vendas Não Cobradas    | Real                            |                          |
| GUID de Linha de Fatura da Correção           | Linha da Fatura             | GUID de Valor Real de Novas Vendas Não Cobradas    | Real                            |                          |
| GUID da Fatura da Correção      | Fatura                  | GUID de Valor Real de Novas Vendas Não Cobradas    | Real                            |                          |

A tabela a seguir mostra os registros na entidade Conexão da transação para o fluxo de trabalho anterior.

| Evento                          | Transação 1                 | Função da Transação 1 | Tipo de Transação 1           | Transação 2                | Função da Transação 2 | Tipo de Transação 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Envio de Tempo de Entrada          | GUID da Linha do Diário (Vendas)     | Vendas Não Cobradas     | msdyn_journalline            | GUID da Linha do Diário (custo)     | Custo               | msdyn_journalline  |
| Aprovação do Tempo                  | GUID de Dados Reais Não Cobrados (Vendas)  | Vendas Não Cobradas     | msdyn_actual                 | GUID de Dados Reais de Custo (custo)       | Custo               | msdyn_actual       |
| Criação de Fatura               | GUID de Detalhes da Linha da Fatura      | Vendas Cobradas       | msdyn_invoicelinetransaction | GUID de Dados Reais de Vendas Não Cobradas   | Vendas Não Cobradas     | msdyn_actual       |
| Confirmação da Fatura           | GUID de Reversão de Dados Reais         | Reversão          | msdyn_actual                 | GUID de vendas originais não cobradas | Original           | msdyn_actual       |
| GUID de Vendas Cobradas              | Vendas Cobradas                  | msdyn_actual       | GUID de Dados Reais de Vendas Não Cobradas   | Vendas Não Cobradas               | msdyn_actual       |                    |
| Correção do Valor de Rascunho       | GUID de Transação da Linha da Fatura | Substituição          | msdyn_invoicelinetransaction | GUID de Vendas Cobradas            | Original           | msdyn_actual       |
| Confirmar Correção da Fatura     | GUID da Reversão de Vendas Cobradas    | Reversão          | msdyn_actual                 | GUID de Vendas Cobradas            | Original           | msdyn_actual       |
| GUID de Valor Real de Novas Vendas Não Cobradas | Substituição                     | msdyn_actual       | GUID de Vendas Cobradas            | Original                     | msdyn_actual       |                    |
