---
title: Cenários de multimoeda (versão 3.x)
description: Este tópico fornece informações sobre cenários de multimoeda.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 33e44297dc80801c3e4416cd9fc3bedae5f3c4ba
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291695"
---
# <a name="multiple-currency-scenarios"></a>Cenários de várias moedas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Microsoft Dynamics 365 têm dois conceitos de moeda:

- **Moeda de transação** – a moeda que em que ocorre uma transação. 
- **Moeda base** – a moeda da instância do Dynamics 365. Essa moeda é configurada quando uma instância do Dynamics 365 é provisionada. Não é possível alterá-la.

Por exemplo, a unidade Cabral US vendeu 100 camisetas a um cliente no Reino Unido, cada uma por 15 libras esterlinas (GBP). A tabela a seguir mostra como essa transação é registrada na entidade Produto da Ordem.

| Produto | Quantidade | Preço por unidade | Moeda | Quantidade | Taxa de câmbio | Preço por unidade (Base)| Valor (Base)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Camiseta | 100      | 15             | GBP      | 1500   | 0.94          | US$ 17,25.               | US$ 1.725       |

A coluna **Moeda** mostra a moeda da transação, que é a moeda em que a venda ocorreu. A coluna **Taxa de câmbio** é a taxa de câmbio entre a moeda da transação e a moeda base. A moeda base é dólar americano (USD). Essa moeda base foi configurada quando a instância do Dynamics 365 foi provisionada.
Como mostrado na tabela, cada transação é registrada na moeda de transação e na moeda base. O Dynamics 365 usa a taxa de câmbio para calcular os valores da moeda base.

## <a name="project-service-automation-extensions"></a>Extensões do Project Service Automation

O Dynamics 365 Project Service Automation influencia a moeda de transação, pois transações comerciais geralmente têm dois aspectos: custo e vendas.

As seguintes entidades são consideradas transações comerciais:

- Detalhes da linha de cotação
- Detalhes da linha de contrato de projeto
- Linha de estimativa
- Linha do diário
- Detalhes da linha da fatura
- Real

Em cada uma dessas entidades, há apenas um registro que representa o valor do custo ou o valor de vendas. Como para qualquer entidade do Dynamics 365 que tenha um campo **Valor**, cada registro inclui valores na moeda de transação e na moeda base. 

O PSA estende o conceito de moeda de transação para o custo e as vendas das seguintes maneiras:

- A moeda de transação de custo para transações de tempo sempre se origina da moeda da unidade organizacional que possui ou gerencia o projeto. Essa unidade organizacional é conhecida como a unidade de contratação.
- A moeda da transação de vendas para transações de tempo e despesa sempre se origina da moeda do contrato de projeto.
- A moeda da transação de custo para despesas se origina da moeda que em que a entrada de despesa foi criada.

## <a name="multiple-currency-scenario"></a>Cenário de várias moedas

Esta seção descreve o exemplo de um projeto que a unidade Cabral UK entrega para um cliente chamado Fabrikam, do Japão. Veja a seguir como o cenário foi configurado:

1. A libra esterlina e o iene japonês (JPY) são definidos em **Configurações** \> **Gerenciamento de Negócios** \> **Moedas**. 
2. Uma conta de cliente chamada **Fabrikam – Japan** é configurada e JPY está marcada como a moeda da conta.
3. Uma unidade organizacional chamada **Cabral UK** é configurada e GBP é selecionada como a moeda.
4. Um contrato de projeto é criado, onde **Cabral UK** é especificada como a unidade de contratação e **Fabrikam – Japan** é especificada como a cliente.
5. As linhas de contrato de projeto são criadas, com base nas disposições de cobrança para as diversas classes de transação no projeto, como cobrança por tempo vs. cobrança por despesas.
6. Um projeto é criado, onde **Cabral UK** é especificado como a unidade de contratação. Esse projeto é criado e mapeado para as linhas de contrato de projeto.


Durante a estimativa que usa os detalhes da linha de cotação, os detalhes da linha de contrato de projeto ou a linha de estimativa da agenda, dois registros são sempre criados na entidade. Um registro é para custo e o outro é para vendas.

- Por padrão, a moeda de transação no registro de custo é definida como a moeda da unidade de contratação do projeto. Neste exemplo, a moeda é GBP.
- Por padrão, a moeda de transação no registro de vendas é definida como a moeda do contrato de projeto. Neste exemplo, a moeda é JPY.

Quando os dados reais são criados por tempo usando a entrada de tempo ou a linha do diário, ocorre o seguinte comportamento:

- Por padrão, a moeda de transação no registro de custo é definida como a moeda da unidade de contratação do projeto.
- Por padrão, a moeda de transação no registro de vendas é definida como a moeda do contrato de projeto.

Quando os dados reais são criados para despesas pela entrada de despesa ou linha do diário, ocorre o seguinte comportamento:

- Você pode registrar o valor da despesa em qualquer moeda. Selecione a moeda usando o seletor de moeda na página **Entrada de Despesa** ou na página **Linha do Diário**. Por padrão, a moeda de transação para o registro de custo é definida para a moeda na entrada de despesa. 
- Por padrão, a moeda de transação para o registro de vendas é a moeda do contrato de projeto. Para definir essa moeda, primeiramente, o sistema converte o valor da transação na moeda que o usuário inseriu para a moeda base. Ele então converte o valor na moeda do contrato de projeto. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Calculando acúmulos quando dados reais do projeto são registrados em várias moedas de transação

O Dynamics 365 trata automaticamente dos acúmulos de valores em diferentes moedas. Veja a seguir um exemplo.

| Classe da transação | Tipo de transação| Date   | Recurso | Categoria da transação | Quantidade | Preço unitário | Quantidade      | Taxa de câmbio | Valor na base |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Vendas não cobradas   | 14 de junho | Joaquim  |                      | 8 horas    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Vendas não cobradas   | 15 de junho | Joaquim  |                      | 8 horas    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Expense           | Vendas não cobradas   | 16 de junho | Joaquim  | Hotel                | 1 cada     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Expense           | Vendas não cobradas   | 17 de junho | Joaquim  | Aluguel de Carros           | 1 cada     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Para calcular o valor total de vendas não cobrado no projeto, você pode criar um campo de acúmulo para o campo **Valor** em todos os dados reais de vendas não cobrados. O campo de acúmulo é uma construção do Dynamics 365 que permite fórmulas rápidas em registros relacionados.


[!INCLUDE[footer-include](../includes/footer-banner.md)]