---
title: Preço do projeto
description: Este tópico fornece informações sobre como funciona o preço no Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: dfbfb59547f295e5fb275264b9222bfa20517f6278144ca013e14a99454b6840
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000562"
---
# <a name="project-pricing"></a>Preço do projeto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Dynamics 365 Project Service Automation estende a entidade Lista de preços no Dynamics 365 Sales. 

## <a name="key-entities"></a>Entidades principais

Uma lista de preços inclui informações que são fornecidas por quatro entidades diferentes:

- **Lista de Preços** – essa entidade armazena informações sobre contexto, moeda, data efetiva e unidade de tempo para precificação de tempo. Contexto mostra se a lista de preços é expressa em taxas de custo ou taxas de vendas. 
- **Moeda** – essa entidade armazena a moeda de preços na lista de preços. 
- **Data** – essa entidade é usada quando o sistema tenta inserir um preço padrão em uma transação. O preço do PSA seleciona a lista de preços que tem data efetiva que inclui a data da transação. Se o preço do PSA encontrar mais de uma lista de preços em vigor para a transação, a data é anexada à cotação, ao contrato ou a unidade organizacional relacionada, e nenhum preço é padronizado. 
- **Tempo** – Essa entidade armazena a unidade de tempo em que os preços são expressados, como taxas diárias ou por hora. 

A entidade Lista de preços tem três tabelas relacionadas que armazenam preços:

  - **Preço da Função** – essa tabela armazena uma taxa para uma combinação de valores de função e unidade organizacional e é usada para configurar preços baseados em função para recursos humanos.
  - **Preço da Categoria de Transação** – essa tabela armazena preços por categoria de transação e é usada para configurar preços da categoria de despesa.
  - **Itens da Lista de Preços** – essa tabela armazena preços para produtos do catálogo.

> ![Configurando preços usando uma lista de preços.](media/basic-guide-12.png)
 
A lista de preços é uma tabela de tarifas. Uma tabela de tarifas é uma combinação da entidade Lista de preços e linhas relacionadas nas tabelas Preço da Função, Preço da Categoria de Transação e Itens da Lista de Preços.

## <a name="resource-roles"></a>Funções do recurso

O termo *função do recurso* se refere a um conjunto de habilidades, competências e certificações que uma pessoa deve ter para realizar um conjunto de tarefas específicas em um projeto.

O tempo de recursos humanos geralmente é cotado com base na função que um recurso preenche em um projeto específico. Para tempo de recurso humano, o PSA trabalha com custo e cobrança que se baseiam na função do recurso. O tempo pode ser precificado em qualquer unidade no grupo de unidades **Tempo**.

O grupo de unidades **Tempo** é criado quando um PSA é instalado. Ele tem uma unidade padrão de **Hora**. Não é possível excluir, renomear nem editar os atributos para o grupo de unidades **Tempo** ou a unidade **Hora**. No entanto, é possível adicionar outras unidades ao grupo de unidades **Tempo**. Se você tentar excluir o grupo de unidades **Tempo** ou a unidade **Hora**, você poderá causar falhas na lógica de negócios do PSA.

> ![Configurando preços por função.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Categorias de transação e categorias de despesa

Viagens e outras despesas geradas por consultores de projeto geralmente são cobradas do cliente. O PSA dá suporte ao preço das categorias de despesa usando listas de preços. Tarifa aérea, hotel e aluguel de carro são exemplos de categorias de despesa. Cada linha da lista de preços para despesas especifica o preço para uma categoria de despesa específica. Para preço das categorias de despesa, o PSA dá suporte aos três seguintes métodos de precificação:

- **A preço de custo** – o custo da despesa é cobrado do cliente e nenhum markup é aplicado.
- **Porcentagem de markup** – a porcentagem sobre o custo real é cobrado do cliente. 
- **Preço por unidade** – um preço de cobrança é definido para cada unidade da categoria de despesa. O valor que é cobrado do cliente é calculado com base no número de unidades de despesa reportado pelo consultor. A milhagem usa o método de precificação de preço por unidade. Por exemplo, a categoria de despesa de milhagem pode ser configurada para 30 dólares americanos (USD) por dia ou 2 USD por milha. Quando um consultor relata milhagem em um projeto, o valor a ser cobrado é calculado com base no número de milhas reportado pelo consultor.

> ![Configurando preço para categorias de despesa.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Preço de vendas e substituições do projeto

Em cotações e contratos do projeto, uma lista de preços de projeto tem um padrão de substituição de preço diferente de uma lista de preços de produto. Em uma linha de cotação baseada em catálogo de produtos, você pode substituir o preço de funções e categorias diretamente na linha de cotação, pois cada linha de cotação aponta exatamente para um item do catálogo. No entanto, em uma linha de cotação baseada em projeto, não é possível substituir o preço de funções e categorias diretamente na linha de cotação. Para trabalhar com os dois padrões distintos de substituição, o PSA introduziu uma nova associação de lista de preços, a lista de preços de projeto.

> [!NOTE]
> É recomendável ter uma lista de preços separada para seus recursos de projeto e itens de catálogo devido às diferenças de comportamento entre as duas quando você substitui preços.

Cada uma das seguintes entidades pode ter uma ou mais listas de preços de vendas associadas para preço de projeto:

- Cliente (conta) 
- Oportunidade 
- Cotação 
- Contrato de Projeto

A associação dessas entidades a uma lista de preços é indicada pelas listas de preços de projeto. Você pode associar uma ou mais listas de preços às entidades de vendas Cliente, Oportunidade, Cotação e Contrato de Projeto.

Uma lista de preços de projeto padrão não é inserida automaticamente em um registro do cliente. No entanto, você pode anexar manualmente uma lista de preços de projeto ao registro do cliente. Todavia, você deve anexar manualmente uma lista de preço de projeto somente quando tiver um contrato de preço personalizado com o cliente. 

Quando uma lista de preços de projeto é anexada a uma entidade de vendas, o PSA valida as seguintes informações:

- A lista de preços tem um contexto de **Vendas**. 
- A moeda da lista de preços corresponde à moeda do cliente. 

Em um contrato de projeto, o PSA usa a seguinte ordem de precedência para definir automaticamente listas de preços de preços relacionadas:

1. Cotação
2. Oportunidade
3. Cliente 
4. Configurações globais para PSA

Quando uma lista de preços de projeto é inserida por padrão, o PSA valida que a moeda corresponde à moeda do cliente e que as listas de preços padrão que foram inseridas têm um contexto de **Vendas**.

Você pode associar várias listas de preços de projeto às entidades Cliente, Oportunidade, Cotação e Contrato de Projeto. Esse recurso aceita preços padrão específicos de data para um contrato de projeto de longa duração, onde você pode exigir mais de uma lista de preços para considerar atualizações de preço que ocorrem por conta da inflação. No entanto, se as listas de preços que você associa à entidade Cliente, Oportunidade, Cotação ou Contrato de Projeto tiverem sobreposição de data efetiva, os preços padrão poderão estar incorretos. Desse modo, é preciso ter certeza de que as listas de preços de projeto que tenham sobreposição de data efetiva não sejam associadas a essas entidades.

### <a name="deal-specific-price-overrides"></a>Substituições de preço especificas de negociação

No PSA, você pode criar substituições específicas de negociação para preços selecionados em listas de preços de projeto que são inseridas por padrão em uma cotação ou contrato de projeto.

Por padrão, um contrato de projeto sempre tem uma cópia da lista de preços de vendas mestre em vez de um link direto para ela. Esse comportamento ajuda a garantir que os contratos de preço celebrados com um cliente para uma SOW (declaração de trabalho) não mudem se a lista de preços mestre for alterada.

Entretanto, em uma cotação, você pode usar uma lista de preços mestre. Como alternativa, é possível copiar uma lista de preços mestre e editá-la para criar uma lista de preços personalizada que se aplique apenas a essa cotação. Para criar uma nova lista de preços específica a uma cotação, na página **Cotação**, selecione **Criar precificação personalizada**. Você pode acessar a lista de preços de projeto específica de negociação somente pela cotação. 

Quando você cria uma lista de preços de projeto personalizada, somente os componentes da lista de preços do projeto são copiados. Em outras palavras, uma nova lista de preços é criada como cópia da lista de preços de projeto existente que é anexada na cotação, e essa nova lista de preços tem apenas preços de função relacionada e preços da categoria de transação.

> ![Exibindo e configurando a precificação personalizada para um contrato de projeto.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Acompanhando custos

O PSA rastreia custos para o uso de tempo do recurso humano em projetos. Ele também rastreia custos para outras despesas que são incorridas durante o projeto, como despesas com viagens.

Assim como as taxas de cobrança, as taxas de custo para recursos humanos também são configuradas usando listas de preços. Veja a seguir as principais diferenças no comportamento da lista de preços de custo e lista de preços de vendas:

- A taxa de custo de um recurso não pode ser substituída em um projeto, cotação ou contrato específico. No entanto, as taxas de cobrança podem ser substituídas de acordo com a negociação caso sejam feitas mudanças específicas à natureza da negociação. 

- A seguinte ordem é usada para resolver uma lista de preços de custo:

    1. A lista de preços de custo que é anexada à unidade organizacional.
    2. A lista de preços de custo que é anexada aos parâmetros do serviço do projeto. Uma vez que as listas de preços de custo em muitas moedas diferentes podem ser anexadas aos parâmetros de serviço do projeto, o PSA faz a correspondência de moeda entre a moeda da unidade organizacional da contratação do projeto, contrato ou cotação e a moeda da lista de preços de custo.
    3. Para despesas, os métodos de precificação a preço de custo e markup sobre custo não se aplicam às listas de preços de custo. Mesmo que esses métodos de precificação sejam usados nas linhas da lista de preços de custo para configurar custos da categoria de transação, o sistema os ignora, e nenhum preço de custo padrão é inserido.


[!INCLUDE[footer-include](../includes/footer-banner.md)]