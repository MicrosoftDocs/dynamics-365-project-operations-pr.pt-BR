---
title: Conexões de transação – Vincular dados reais de diferentes tipos de transação
description: Este artigo explica como uma conexão de transação é usada para vincular dados reais de diferentes tipos para ajudar a rastrear a lucratividade, a lista de pendências de cobrança e os cálculos de receita cobrada versus não cobrada.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926072"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Conexões de transação – Vincular dados reais de diferentes tipos de transação

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os registros de conexão de transação são criados para vincular dados reais de diferentes tipos à medida que os dados de horas, despesas ou o uso de material vão migrando no ciclo de vida, passando pelo estágio de cotação ou pré-venda até o estágio de contrato, aprovações e/ou recuperações, faturamento e possivelmente crédito ou faturamento corretivo.

O exemplo a seguir mostra o processamento típico de entradas de tempo em um ciclo de vida de projeto do Project Operations.

> ![Processando entradas de hora no Project Operations.](media/basic-guide-17.png)

O processamento de entradas de hora no ciclo de vida de um projeto do Project Operations segue estas etapas: 

1. O envio de uma entrada de hora faz com que duas linhas de diário sejam criadas: uma para custo e outra para vendas não cobradas. 
2. A eventual aprovação da entrada de hora faz com que dois dados reais sejam criados: um para custo e outro para vendas não cobradas. Esses 2 dados reais são vinculados usando conexões de transação.
3. Quando o usuário cria uma fatura de projeto, a transação da linha da fatura é criada usando dados do valor real de vendas não cobradas.
4. Quando a fatura é confirmada, isso cria dois novos dados reais: dados reais de uma reversão de vendas não cobradas e dados reais de vendas cobradas. A reversão de vendas não cobradas e os dados reais originais de vendas não cobradas são conectados usando conexões de transação reversíveis. As vendas cobradas e os dados reais originais de vendas não cobradas também são conectados para mostrar os links entre o que antes era receita de WIP (trabalho em andamento) ou lista de pendências e o que agora é receita cobrada.   

Cada evento no fluxo de trabalho de processamento aciona a criação de registros na tabela **Conexão da transação**. Isso ajuda a rastrear os relacionamentos entre os registros que são criados na entrada de hora, na linha de diário, nos dados reais e nos detalhes da linha de fatura.

A tabela a seguir mostra os registros na entidade **Conexão da transação** para o fluxo de trabalho anterior.

|Evento                   |Transação 1                 |Função da Transação 1 |Tipo de Transação 1       |Transação 2          |Função da Transação 2 |Tipo de Transação 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Envio de Tempo de Entrada   |GUID da Linha do Diário (Vendas)     |Vendas Não Cobradas |msdyn_journalline            |GUID da Linha do Diário (custo)     |Custo            |msdyn_journalline  |
|Aprovação do Tempo           |GUID de Dados Reais Não Cobrados (Vendas)  |Vendas Não Cobradas |msdyn_actual                 |GUID de Dados Reais de Custo (custo)       |Custo            |msdyn_actual       |
|Criação de Fatura        |GUID de Detalhes da Linha da Fatura      |Vendas Cobradas   |msdyn_invoicelinetransaction |GUID de Dados Reais de Vendas Não Cobradas   |Vendas Não Cobradas  |msdyn_actual       |
|Confirmação da Fatura    |GUID de Reversão de Dados Reais         |Reversão      |msdyn_actual                 |GUID de vendas originais não cobradas |Original        |msdyn_actual       |
|                        |GUID de Vendas Cobradas             |Vendas Cobradas   |msdyn_actual                 |GUID de Dados Reais de Vendas Não Cobradas   |Vendas Não Cobradas  |msdyn_actual       |
|Correção do Valor de Rascunho |GUID de Transação da Linha da Fatura|Substituição      |msdyn_invoicelinetransaction |GUID de Vendas Cobradas            |Original        |msdyn_actual       |
|Confirmar Correção da Fatura|GUID da Reversão de Vendas Cobradas  |Reversão      |msdyn_actual                 |GUID de Vendas Cobradas            |Original        |msdyn_actual       |
|                        |GUID de novas vendas não cobradas |Substituição            |msdyn_actual                 |GUID de Vendas Cobradas            |Original        |msdyn_actual       |


A ilustração a seguir mostra os links que são criados entre diferentes tipos de dados reais em vários eventos usando o exemplo de entradas de hora no Project Operations.

> ![Como os dados reais de diferentes tipos são vinculados entre si no Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
