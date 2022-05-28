---
title: Listas de preços padrão
description: Este tópico fornece informações sobre vendas padrão e listas de preço de custo no Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 83458d6f62c8790eb967cf07c21ffe7851e14a3a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591758"
---
# <a name="default-price-lists"></a>Listas de preços padrão

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

## <a name="sales-price-lists"></a>Listas de preços de venda

Todos os contratos e cotações do projeto no Dynamics 365 Project Operations contêm uma lista de preços de venda padrão. 

### <a name="price-list-default-on-project-quotes"></a>Lista de preços padrão em cotações do projeto
O sistema conclui o seguinte processo para determinar a lista de preços a ser padronizada em uma cotação de projeto:

1. O sistema examina as listas de preços anexadas às listas de preços do projeto da conta. 
2. Se houver listas de preços de projeto anexadas ao registro da conta, o sistema verificará as listas de preços de venda anexadas aos parâmetros do projeto que correspondem à moeda da cotação do projeto.
3. Em seguida, o sistema verifica a data efetiva das listas de preços que correspondem ao intervalo de datas da cotação do projeto. Especificamente, a data em que a cotação foi criada.
4. Se houver várias listas de preços em vigor para a data da cotação do projeto, todas as listas de preços serão padronizadas na cotação do projeto.
5. Se nenhuma lista de preços estiver em vigor para a data da cotação do projeto, não haverá lista de preços do projeto padrão na cotação do projeto. Uma mensagem de aviso ocorrerá na cotação do projeto. A mensagem informa que dados efetivos e estimativas do projeto não terão preço porque não há listas de preços do projeto anexadas.

### <a name="price-list-default-on-project-contracts"></a>Lista de preços padrão em contratos do projeto 
O sistema conclui o seguinte processo para determinar a lista de preços a ser padronizada em um contrato de projeto:

1. Se o contrato for criado a partir de uma cotação, as listas de preços do projeto na cotação serão copiadas separadamente e anexadas ao contrato do projeto.
2. Se o contrato for criado do zero, o sistema examinará as listas de preços anexadas às listas de preços do projeto da conta. Se não houver listas de preços de projeto anexadas ao registro da conta, o sistema verificará as listas de preços de venda anexadas aos parâmetros do projeto que correspondem à moeda do contrato do projeto.
4. Em seguida, o sistema verifica a data efetiva das listas de preços que correspondem ao intervalo de datas do contrato do projeto. Especificamente, a data em que o contrato foi criado.
5. Se houver várias listas de preços em vigor para a data do contrato, todas as listas de preços serão padronizadas no contrato.
6. Se nenhuma lista de preços estiver em vigor para a data do contrato, não haverá listas de preços do projeto padrão para o contrato. Uma mensagem de aviso ocorrerá no contrato do projeto. A mensagem informa que dados efetivos e estimativas do projeto não terão preço porque não há listas de preços do projeto anexadas.

## <a name="cost-price-lists"></a>Listas de preços de custo

As listas de preços de custo não são padronizadas para entidades no Project Operations. A determinação da lista de preços de custo a ser usada para custos do projeto é sempre feita no momento. O sistema conclui o seguinte processo para determinar a lista de preços a ser usada para custos do projeto:

1. O sistema primeiro examina as listas de preços anexadas à unidade organizacional contratante do projeto.
2. O sistema verifica a data efetiva das listas de preços que correspondem à data da estimativa de entrada ou linha real. Nesta situação, *linha de estimativa* refere-se aos três contextos de estimativa em Project Operations:

    - Linha de estimativa do projeto
    - Detalhes da linha de cotação
    - Detalhe da linha de contrato
  
3. Se houver várias listas de preços em vigor para a data na estimativa de entrada ou real, a lista de preços recém-criada será selecionada.
4. Se não houver listas de preços anexadas à unidade organizacional contratante do projeto, o sistema verificará as listas de preços de custo anexadas aos parâmetros do projeto que correspondem à moeda do projeto.
5. Em seguida, o sistema verifica a data efetiva das listas de preços que correspondem à data da estimativa de entrada ou linha real. 
6. Se houver várias listas de preços em vigor para a data na estimativa de entrada ou real, a lista de preços recém-criada será selecionada.
7. Se não houver listas de preços de custo anexadas aos parâmetros do projeto que correspondam à moeda e à data efetiva, o sistema padronizará a taxa de custo como zero (0) na estimativa de entrada ou linha real.


[!INCLUDE[footer-include](../includes/footer-banner.md)]