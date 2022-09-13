---
title: Listas de preços padrão
description: Este artigo fornece informações sobre listas de preço de custo e vendas padrão no Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410248"
---
# <a name="default-price-lists"></a>Listas de preços padrão

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

## <a name="sales-price-lists"></a>Listas de preços de venda

Todos os contratos e cotações do projeto no Dynamics 365 Project Operations contêm uma lista de preços de venda padrão. 

### <a name="price-list-default-on-project-quotes"></a>Lista de preços padrão em cotações do projeto
O sistema conclui o seguinte processo para determinar a lista de preços a ser padronizada em uma cotação de projeto:

1. O sistema examina as listas de preços anexadas às listas de preços do projeto da conta. 
1. Se não houver nenhuma lista de preços do projeto anexadas ao registro da conta, o sistema verificará as listas de preços de venda anexadas aos parâmetros do projeto que correspondem à moeda da cotação do projeto.
1. Em seguida, o sistema verifica a data efetiva das listas de preços que correspondem ao intervalo de datas da cotação do projeto. Especificamente, a data em que a cotação foi criada.
1. Se houver várias listas de preços em vigor para a data da cotação do projeto, todas as listas de preços serão padronizadas na cotação do projeto.
1. Se nenhuma lista de preços estiver em vigor para a data da cotação do projeto, não haverá lista de preços do projeto padrão na cotação do projeto. Uma mensagem de aviso ocorrerá na cotação do projeto. A mensagem informa que dados efetivos e estimativas do projeto não terão preço porque não há listas de preços do projeto anexadas.

### <a name="price-list-default-on-project-contracts"></a>Lista de preços padrão em contratos do projeto 
O sistema conclui o seguinte processo para determinar a lista de preços a ser padronizada em um contrato de projeto:

1. Se o contrato for criado a partir de uma cotação, as listas de preços do projeto na cotação serão copiadas separadamente e anexadas ao contrato do projeto.
1. Se o contrato for criado do zero, o sistema examinará as listas de preços anexadas às listas de preços do projeto da conta. Se não houver listas de preços de projeto anexadas ao registro da conta, o sistema verificará as listas de preços de venda anexadas aos parâmetros do projeto que correspondem à moeda do contrato do projeto.
1. Em seguida, o sistema verifica a data efetiva das listas de preços que correspondem ao intervalo de datas do contrato do projeto. Especificamente, a data em que o contrato foi criado.
1. Se houver várias listas de preços em vigor para a data do contrato, todas as listas de preços serão padronizadas no contrato.
1. Se nenhuma lista de preços estiver em vigor para a data do contrato, não haverá listas de preços do projeto padrão para o contrato. Uma mensagem de aviso ocorrerá no contrato do projeto. A mensagem informa que dados efetivos e estimativas do projeto não terão preço porque não há listas de preços do projeto anexadas.

## <a name="cost-price-lists"></a>Listas de preços de custo

As listas de preços de custo não são padronizadas para entidades no Project Operations. A determinação da lista de preços de custo a ser usada para custos do projeto é sempre feita por transação. O sistema conclui o seguinte processo para determinar a lista de preços a ser usada para custos do projeto:

1. O sistema examina as listas de preços anexadas à unidade organizacional contratante do projeto.
1. Em seguida, o sistema verifica a data efetiva das listas de preços que correspondem à data do contexto de estimativa de entrada ou contexto real.

    - *Contexto de estimativa* refere-se a qualquer um dos três contextos de estimativa em Project Operations:

        - Linha de estimativa do projeto
        - Detalhes da linha de cotação
        - Detalhe da linha de contrato

    - *Contexto real* refere-se a qualquer uma das três fontes de dados reais em Project Operations:

       - Linhas do diário de entrada criadas manualmente ou linhas do diário de correção criadas em um diário de correção
       - Linhas do diário criadas durante o envio de logs de uso de tempo, despesa ou material
       - Detalhes da linha da fatura

    Quando o Project Operations corresponde à data efetiva da linha do diário de entrada ou do detalhe da linha da fatura no *contexto real*, ele usa o campo **Data da transação**.

    - Se várias listas de preços estiverem em vigor para a data do contexto de estimativa de entrada ou contexto real, a lista de preços criada mais recentemente será selecionada.
    - Se nenhuma lista de preços estiver anexada à unidade organizacional contratante do projeto, o sistema verificará as listas de preços de custo anexadas aos parâmetros do projeto que correspondem à moeda do projeto.

## <a name="enable-multi-currency-cost-price-list"></a>Habilitar a lista de preços de custo em várias moedas

Essa configuração pode ser encontrada em **Configurações** \> **Parâmetros**. O valor padrão é **Não**.

Quando esta configuração está habilitada (ou seja, o valor é definido como **Sim**), o sistema se comporta da seguinte maneira:

- Ele permite que listas de preços de custo em qualquer moeda sejam associadas à unidade organizacional. Por exemplo, uma lista de preços de custo na moeda EUR pode ser anexada a uma unidade organizacional na moeda USD. O sistema continuará a validar se as listas de preços de custo anexadas a uma unidade organizacional não tiverem sobreposição de data efetiva.
- Ele valida que as listas de preços de custo anexadas aos parâmetros do projeto não têm sobreposição de data efetiva, mesmo que tenham moedas diferentes. Esse comportamento difere do comportamento padrão (ou seja, o comportamento quando o valor é definido como **Não**). No comportamento padrão, apenas as listas de preços de custo que têm a **mesma** moeda são validadas para sem sobreposição de data efetiva.
- Para um contexto de transação de entrada, ele determina a lista de preços de custo com base apenas na data efetiva. Esse comportamento difere do comportamento padrão, em que o sistema seleciona a lista de preços de custo que corresponde à moeda do projeto e à data efetiva.

Devido a essas mudanças de comportamento, os clientes do Project Operations poderão manter uma lista de preços de custo global que será relevante para toda a empresa. Eles não precisarão ter listas de preços em cada moeda de operação. A lista de preços global terá uma data efetiva e permitirá que as taxas de custo sejam configuradas em qualquer moeda para uma combinação específica de valores de dimensão de preço. A moeda da lista de preços de custo é usada apenas para inserir valores padrão quando os registros de itens **Preços das funções**, **Preços da categoria** e **Lista de preços** são criados. Ela não será usada para determinar a lista de preços.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
