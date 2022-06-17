---
title: Gerenciar listas de preços de projeto em uma cotação
description: Este artigo fornece informações sobre a entidade lista de preços de projeto.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8439a03e6557ec531405048ec4149344e283242e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933120"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Gerenciar listas de preços de projeto em uma cotação

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations estende a entidade Lista de preços no Dynamics 365 Sales. 

## <a name="key-entities"></a>Entidades principais

Uma lista de preços inclui informações que são fornecidas por quatro entidades diferentes:

- **Lista de Preços**: essa entidade armazena informações sobre contexto, moeda, data efetiva e unidade de tempo para precificação de tempo. O contexto mostra se a lista de preços expressa taxas de custo ou taxas de vendas. 
- **Moeda**: essa entidade armazena a moeda de preços na lista de preços. 
- **Data**: essa entidade é usada quando o sistema tenta inserir um preço padrão em uma transação. Uma lista de preços que tem data efetiva que inclui a data da transação é selecionada. Se for encontrada mais de uma lista de preços em vigor para a data da transação e anexadas à cotação, ao contrato ou à unidade organizacional relacionada, nenhum preço será padronizado. 
- **Tempo**: essa entidade armazena a unidade de tempo em que os preços são expressos, como taxas diárias ou por hora. 

A entidade Lista de preços tem três tabelas relacionadas que armazenam preços:

  - **Preço da Função**: essa tabela armazena uma taxa para uma combinação de valores de função e unidade organizacional e é usada para configurar preços baseados em função para recursos humanos.
  - **Preço da Categoria de Transação**: essa tabela armazena preços por categoria de transação e é usada para configurar preços da categoria de despesa.
  - **Itens da Lista de Preços**: essa tabela armazena preços para produtos do catálogo.
 
A lista de preços é uma tabela de tarifas. Uma tabela de tarifas é uma combinação da entidade Lista de preços e linhas relacionadas nas tabelas Preço da Função, Preço da Categoria de Transação e Itens da Lista de Preços.

## <a name="resource-roles"></a>Funções do recurso

O termo *função do recurso* se refere a um conjunto de habilidades, competências e certificações que uma pessoa deve ter para realizar um conjunto de tarefas específicas em um projeto.

O tempo de recursos humanos é cotado com base na função que um recurso preenche em um projeto específico. Para tempo de recurso humano, custo e cobrança que se baseiam na função do recurso. O tempo pode ser precificado em qualquer unidade no grupo de unidades **Tempo**.

O grupo de unidades **Tempo** é criado quando você instala o Project Operations. Ele tem uma unidade padrão de **Hora**. Não é possível excluir, renomear ou editar os atributos do grupo de unidades **Tempo** ou a unidade **Hora**. No entanto, é possível adicionar outras unidades ao grupo de unidades **Tempo**. Se você tentar excluir o grupo de unidades **Tempo** ou a unidade **Hora**, poderá causar falhas na lógica de negócios.
 
## <a name="transaction-categories-and-expense-categories"></a>Categorias de transação e categorias de despesa

Viagens e outras despesas geradas por consultores de projeto são cobradas do cliente. O preço das categorias de despesa é concluído usando listas de preços. Tarifa aérea, hotel e aluguel de carro são exemplos de categorias de despesa. Cada linha da lista de preços para despesas especifica o preço para uma categoria de despesa específica. Estes três métodos são usados para precificar categorias de despesas:

- **A preço de custo**: o custo da despesa é cobrado do cliente e nenhum markup é aplicado.
- **Porcentagem de markup**: a porcentagem sobre o custo real é cobrada do cliente. 
- **Preço por unidade**: um preço de cobrança é definido para cada unidade da categoria de despesa. O valor que é cobrado do cliente é calculado com base no número de unidades de despesa reportado pelo consultor. A milhagem usa o método de precificação de preço por unidade. Por exemplo, a categoria de despesa de milhagem pode ser configurada para 30 dólares americanos (USD) por dia ou 2 USD por milha. Quando um consultor relata milhagem em um projeto, o valor a ser cobrado é calculado com base no número de milhas reportado pelo consultor.
 
## <a name="project-sales-pricing-and-overrides"></a>Preço de vendas e substituições do projeto

Em cotações e contratos do projeto, uma lista de preços de projeto tem um padrão de substituição de preço diferente de uma lista de preços de produto. Em uma linha de cotação baseada em catálogo de produtos, você pode substituir o preço de funções e categorias diretamente na linha de cotação, pois cada linha de cotação aponta exatamente para um item do catálogo. No entanto, em uma linha de cotação baseada em projeto, não é possível substituir o preço de funções e categorias diretamente na linha de cotação. Use a lista de preços de projeto para dar suporte aos dois padrões de substituição distintos.

> [!NOTE]
> É recomendável ter uma lista de preços separada para seus recursos de projeto e itens de catálogo devido às diferenças de comportamento entre as duas quando você substitui preços.

Cada uma das seguintes entidades pode ter uma ou mais listas de preços de vendas associadas para preço de projeto:

- Cliente (conta) 
- Oportunidade 
- Cotação 
- Contrato de Projeto

A associação dessas entidades a uma lista de preços é indicada pelas listas de preços de projeto. Você pode associar uma ou mais listas de preços às entidades de vendas Cliente, Oportunidade, Cotação e Contrato de Projeto.

Uma lista de preços de projeto padrão não é inserida automaticamente em um registro do cliente. No entanto, você pode anexar manualmente uma lista de preços de projeto ao registro do cliente. Todavia, você deve anexar manualmente uma lista de preço de projeto somente quando tiver um contrato de preço personalizado com o cliente. 

Quando uma lista de preços de projeto é anexada a uma entidade de vendas, as seguintes informações são validadas:

- A lista de preços tem um contexto de **Vendas**. 
- A moeda da lista de preços corresponde à moeda do cliente. 

Em um contrato de projeto, use a seguinte ordem de precedência para definir automaticamente listas de preços de projetos relacionadas:

1. Cotação
2. Oportunidade
3. Cliente 
4. Configurações globais 

Quando uma lista de preços de projeto é inserida por padrão, o sistema valida que a moeda corresponde à moeda do cliente e que as listas de preços padrão que foram inseridas têm um contexto de **Vendas**.

Você pode associar várias listas de preços de projeto às entidades Cliente, Oportunidade, Cotação e Contrato de Projeto. Esse recurso aceita preços padrão específicos de data para um contrato de projeto de longa duração, onde você pode exigir mais de uma lista de preços para considerar atualizações de preço que ocorrem por conta da inflação. No entanto, se as listas de preços que você associa à entidade Cliente, Oportunidade, Cotação ou Contrato de Projeto tiverem sobreposição de data efetiva, os preços padrão poderão estar incorretos. Desse modo, é preciso ter certeza de que as listas de preços de projeto que tenham sobreposição de data efetiva não sejam associadas a essas entidades.

### <a name="deal-specific-price-overrides"></a>Substituições de preço especificas de negociação

Você pode criar substituições específicas de negociação para preços selecionados em listas de preços de projetos que são inseridas por padrão em uma cotação ou contrato de projeto.

Por padrão, um contrato de projeto sempre tem uma cópia da lista de preços de vendas mestre em vez de um link direto para ela. Esse comportamento ajuda a garantir que os contratos de preço celebrados com um cliente para uma SOW (declaração de trabalho) não mudem se a lista de preços mestre for alterada.

Entretanto, em uma cotação, você pode usar uma lista de preços mestre. Como alternativa, é possível copiar uma lista de preços mestre e editá-la para criar uma lista de preços personalizada que se aplique apenas a essa cotação. Para criar uma nova lista de preços específica a uma cotação, na página **Cotação**, selecione **Criar precificação personalizada**. Você pode acessar a lista de preços de projeto específica de negociação somente pela cotação. 

Quando você cria uma lista de preços de projeto personalizada, somente os componentes da lista de preços do projeto são copiados. Em outras palavras, uma nova lista de preços é criada como cópia da lista de preços de projeto existente que é anexada na cotação, e essa nova lista de preços tem apenas preços de função relacionada e preços da categoria de transação.
  
## <a name="tracking-costs"></a>Acompanhando custos

O Project Operations rastreia custos para o uso de tempo do recurso humano em projetos. Ele também rastreia custos para outras despesas que são incorridas durante o projeto, como despesas com viagens.

Assim como as taxas de cobrança, as taxas de custo para recursos humanos também são configuradas usando listas de preços. Veja a seguir as principais diferenças no comportamento da lista de preços de custo e lista de preços de vendas:

- A taxa de custo de um recurso não pode ser substituída em um projeto, cotação ou contrato específico. No entanto, as taxas de cobrança podem ser substituídas de acordo com a negociação caso sejam feitas mudanças específicas à natureza da negociação. 

- A seguinte ordem é usada para resolver uma lista de preços de custo:

    1. A lista de preços de custo que é anexada à unidade organizacional.
    2. A lista de preços de custo que é anexada aos parâmetros do Project Operations. Uma vez que as listas de preços de custo em muitas moedas diferentes podem ser anexadas aos parâmetros, a correspondência de moeda é concluída entre a moeda da unidade organizacional da contratação do projeto, o contrato ou cotação e a moeda da lista de preços de custo.
    3. Para despesas, os métodos de precificação a preço de custo e markup sobre custo não se aplicam às listas de preços de custo. Mesmo que esses métodos de precificação sejam usados nas linhas da lista de preços de custo para configurar custos da categoria de transação, o sistema os ignora, e nenhum preço de custo padrão é inserido.


[!INCLUDE[footer-include](../includes/footer-banner.md)]