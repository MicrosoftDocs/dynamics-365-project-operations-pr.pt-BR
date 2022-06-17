---
title: Origens da transação – Vincular dados reais à fonte
description: Este artigo explica como o conceito de origens da transação é usado para vincular dados reais a registros de fonte originais, como os logs de entrada de hora, entrada de despesa ou uso de material.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921288"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Origens da transação – Vincular dados reais à fonte

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os registros de origem da transação são criados para vincular os dados reais à sua origem, como os logs de entradas de hora, entradas de despesa e uso de material e as faturas de projeto.

O exemplo a seguir mostra o processamento típico de entradas de tempo em um ciclo de vida de projeto do Project Operations.

> ![Processando entradas de hora no Project Operations.](media/basic-guide-17.png)
 
1. O envio de uma entrada de hora faz com que duas linhas de diário sejam criadas: uma para custo e outra para vendas não cobradas.
2. A eventual aprovação da entrada de hora faz com que dois dados reais sejam criados: um para custo e outro para vendas não cobradas.
3. Quando o usuário cria uma fatura de projeto, a transação da linha da fatura é criada usando dados do valor real de vendas não cobradas.
4. Quando a fatura é confirmada, dois dados reais novos são criados: uma reversão de vendas não cobradas e dados reais de vendas cobradas.

Cada evento desse fluxo de trabalho de processamento dispara a criação de registros na entidade Origem da transação para ajudar a criar um rastreamento das relações entre esses registros que são criados na entrada de hora, na linha do diário, nos dados reais e nos detalhes da linha da fatura.

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


A ilustração a seguir mostra os links que são criados entre dados reais e suas origens em vários eventos usando o exemplo de entradas de hora no Project Operations.

> ![Como os dados reais são vinculados aos registros de origem no Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
