---
title: Vincule os dados reais aos registros originais
description: Este tópico explica como vincular os valores reais aos registros originais, como entrada de horas, entrada de despesas ou registros de uso de material.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9fc49211f3c2c79e18f6dd18e9a687091793cad0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996732"
---
# <a name="link-actuals-to-original-records"></a>Vincule os dados reais aos registros originais

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


No Dynamics 365 Project Operations, uma *transação comercial* é um conceito abstrato que não é representado por nenhuma entidade. No entanto, alguns campos e processos comuns em entidades são designados para usar o conceito de transações comerciais. As seguintes entidades usam essa concepção:

- Detalhes da linha de cotação
- Detalhes da linha de contrato
- Linhas de estimativa
- Linhas do diário
- Dados Efetivos

Dessas entidades, **Detalhes da linha de cotação**, **Detalhes da linha de contrato** e **Linhas de estimativa** são mapeadas para a fase de estimativa no ciclo de vida do projeto. As **Linhas do diário** e **Entidades de valores reais** são mapeadas para a fase de execução no ciclo de vida do projeto.

O Project Operations reconhece registros dessas cinco entidades como transações comerciais. A única diferença é que os registros nas entidades que são mapeadas para a fase de estimativa são considerados previsões financeiras, enquanto os registros em entidades que são mapeadas para a fase de execução são considerados fatos financeiros que já tenham ocorrido.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceitos que são exclusivos às transações comerciais
Os seguintes conceitos são exclusivos ao conceito de transações comerciais:

- Tipo de transação
- Classe da transação
- Origem da transação
- Conexão da transação

### <a name="transaction-type"></a>Tipo de transação

O tipo de transação representa o tempo e o contexto do impacto financeiro em um projeto. Isso é representado por um conjunto de opções que tem os seguintes valores permitidos no Project Operations:

  - Custo
  - Contrato do projeto
  - Vendas não cobradas
  - Vendas cobradas
  - Vendas entre organizações
  - Custo da unidade de recursos

### <a name="transaction-class"></a>Classe da transação

A classe da transação representa os diferentes tipos de custo que incorreram nos projetos. Isso é representado por um conjunto de opções que tem os seguintes valores permitidos no Project Operations:

  - Hora
  - Despesa
  - Material
  - Taxa
  - Etapa
  - Imposto

**Etapa** geralmente é usada pela lógica de negócios para cobrança de preço fixo no Project Operations.

### <a name="transaction-origin"></a>Origem da transação

**Origem da transação** é uma entidade que armazena a origem de cada transação comercial. À medida que um projeto está em andamento, cada transação comercial dará origem a outra transação comercial que, por sua vez, criará outra e assim por diante. A entidade de origem da transação é projetada para armazenar dados sobre a origem de cada transação para ajudar na geração de relatórios e rastreabilidade. 

### <a name="transaction-connection"></a>Conexão da transação

**Conexão da transação** é uma entidade que armazena a relação entre duas transações comerciais semelhantes, como custo e dados reais de vendas relacionadas, ou reversões de transação acionadas pelas atividades de cobrança, como confirmação ou correções da fatura.

Juntas, **Origem da transação** e **Conexão da transação** ajudam você a acompanhar as relações entre transações comerciais e ações que resultaram na criação de uma transação comercial específica.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemplo: Como a Origem da transação funciona com a Conexão da transação

O exemplo a seguir mostra o processamento típico de entradas de tempo em um ciclo de vida de projeto do Project Operations.

> ![Processando entradas de tempo em um ciclo de vida do Project Service](media/basic-guide-17.png)
 
1. Um envio de tempo de entrada cria duas linhas de diário: uma para custo e outra para vendas não cobradas.
2. A aprovação eventual da entrada de tempo cria dois dados reais: um para custo e outro para vendas não cobradas.
3. Quando uma nova fatura do projeto é criada, a transação da linha da fatura é criada usando dados do valor real de vendas não cobradas. 
4. Quando a fatura é confirmada, dois dados reais novos são criados: um de reversão de vendas não cobradas e outro de vendas cobradas.

Cada um desses eventos cria um registro nas entidades **Origem da transação** e **Conexão da transação**. Esses novos registros ajudam a criar um histórico de relacionamentos entre os registros que são criados em entrada de horas, linha de diário, horas trabalhadas e detalhes de linha de fatura.

A tabela a seguir mostra os registros na entidade **Origem da transação** do fluxo de trabalho.

| Evento                        | Origem                   | Tipo de origem                       | Transação                       | Tipo de transação         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Envio de Tempo de Entrada        | GUID de Registro da Entrada de Hora   | Entrada de Hora                        | GUID de Registro da Linha do Diário (custo)   | Linha do Diário             |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Registro da Linha do Diário (vendas)  | Linha do Diário                      |                          |
| Aprovação do Tempo                | GUID de Registro da Linha do Diário | Linha do Diário                      | GUID de Registro de Vendas Não Cobradas        | Real                   |
| GUID de registro do tempo de entrada       | Entrada de Horas               | GUID de Registro de Vendas Não Cobradas        | Real                            |                          |
| GUID de Registro da Linha do Diário     | Linha do Diário             | GUID de Registro do Valor Real de Custo           | Real                            |                          |
| GUID de registro do tempo de entrada       | Entrada de Hora               | GUID de Registro do Valor Real de Custo           | Real                            |                          |
| Criação de Fatura             | GUID de Registro da Entrada de Hora   | Entrada de Hora                        | GUID de Transação da Linha da Fatura     | Transação da Linha da Fatura |
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

A tabela a seguir mostra os registros na entidade **Conexão da transação** do fluxo de trabalho.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
