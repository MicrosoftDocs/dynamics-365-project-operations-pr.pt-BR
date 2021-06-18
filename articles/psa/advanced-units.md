---
title: Grupos de unidades e unidades
description: Este tópico fornece informações sobre grupos de unidades e unidades.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: e981f39bbb6ca4277778382a5816952df2a8a1fb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009557"
---
# <a name="unit-groups-and-units"></a>Grupos de unidades e unidades

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os grupos de unidades e unidades são entidades básicas no Microsoft Dynamics 365. Uma unidade é uma unidade de medida, e várias unidades podem ser agrupadas em grupos de unidades. Um grupo de unidades às vezes é tratado como um agendamento de unidades na interface do usuário do Dynamics 365. 

Veja a seguir alguns exemplos de unidades e grupos de unidades:
 
- **Grupo de unidades**: distância 
    - **Unidades**: milha, quilômetro, etc.
- **Grupo de unidades**: tempo
    - **Unidades**: hora, dia, semana, etc. 

Quando você configura várias unidades em um grupo de unidades, também é necessário configurar um fator de conversão entre elas designando a primeira unidade que é configurada como a unidade padrão ou principal para o grupo de unidades. 

Por exemplo, em um grupo de unidades **Tempo**, se você configurar **Hora** como a primeira unidade, o sistema designará **Hora** como a unidade padrão. Se a próxima unidade configurada for **Dia**, será necessário configurar um fator de conversão para **Dia** em **Hora**. Se você adicionar **Semana** como uma terceira unidade, será necessário configurar um fator de conversão para **Semana** em termos de **Dia** ou **Hora**. 

A imagem a seguir mostra um exemplo de configuração para a unidade **Dia**, em que o campo **Quantidade** mostra o número de horas que há em um dia, e **Semana**, em que o campo **Quantidade** mostra o número de dias que há em uma semana.

> ![Grupo de unidades: página de informações](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Usando unidades e grupos de unidades

O Dynamics 365 Project Service Automation usa unidades e grupos de unidades para processar estimativas e entradas de despesas e tempo. 

Para despesas, cada categoria de despesa tem um grupo de unidades e uma unidade padrão. Esses valores são inseridos como valores padrão nas entradas da lista de preços para categorias de despesa. 

Por exemplo, você tem uma categoria de despesa chamada **Milhagem**. Ela tem um grupo de unidades chamado **Distância** e uma unidade padrão chamada **Milha**. Se você configurar o grupo de unidades **Distância** para que ele tenha duas unidades (**Milha** e **Quilômetro**), será possível configurar dois preços para a categoria **Milhagem** em uma lista de preços: preço por milha e preço por quilômetro.

| Categoria de despesa  | Grupo de unidades  | Unidade      | Método de precificação  | Preço por unidade  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Milhagem           | Distância      | Milha      | Preço por unidade    | 10 USD            |
| Milhagem           | Distância      | Quilômetro | Preço por unidade    |  6 USD            |

Quando você insere uma despesa em um projeto, o sistema determina o preço por meio da combinação da categoria e da unidade na despesa. 

| Descrição da despesa        | Categoria da despesa  | Unidade  | Quantidade  | Preço unitário   |
|----------------------------|---------------------|-------|-----------|----------------|
| Dirigir até o local do cliente | Milhagem             | Milha  | 10        | 10 USD         |

Para tempo, o cabeçalho de cada lista de preços tem um campo **Unidade de Tempo Padrão**. O valor é definido quando você cria o cabeçalho da lista de preços. Essa unidade é usada para definir todos os preços baseados em função nessa lista de preços.

As linhas de estimativa para o campo **Tempo em Cotação** podem ser expressadas em qualquer unidade de tempo. No entanto, as linhas de estimativa em projetos e entradas de tempo para projetos podem usar apenas a unidade de tempo **Hora**. Se a unidade na entrada de tempo ou linha de estimativa não corresponder à unidade na lista de preços da função, o sistema converterá o preço nas unidades que são definidas na estimativa do projeto ou na transação real do projeto.

O exemplo a seguir mostra como o PSA usa os grupo de unidades, unidades e fatores de conversão.
- Unidades

   - **Grupo de unidades**: tempo 
   - **Unidades**: hora 
    
    - **Dia** – fator de conversão: 8 horas       
    - **Semana** – fator de conversão: 40 horas  
        
- Configuração da lista de preços no Projeto A:

    - **Nome**: preços de venda em 2016 do Reino Unido 
    - **Unidade de tempo padrão**: dia 
    - **Moeda**: GBP

| Função      | Grupo de unidades | Unidade | Unidade organizacional | Preço   |
|-----------|------------|------|---------------------|---------|
| Desenvolvedor | Hora       | Dia  | Contoso Reino Unido          | 800 GBP |

### <a name="time-entry"></a>Entrada de hora

A tabela a seguir mostra a transação resultante do lado de vendas criada pelo PSA para um projeto de três horas.


| Projeto   | Tarefa    | Função      | Quantidade | Unidade  | Preço unitário | Valor de vendas não cobrado |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projeto A | Design  | Desenvolvedor | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Perguntas frequentes sobre unidade de tempo

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>O PSA é convertido em diferentes unidades no caso de despesas?
Nº A conversão de unidade funciona apenas para tempo. Para despesas, se o sistema não puder encontrar um preço para a combinação da categoria de despesa e unidade, o preço será definido com 0,00 por padrão.

### <a name="why-does-psa-convert-time-units"></a>Por que o PSA converte unidades de tempo?
Em alguns países ou regiões, há um requisito legal para que as taxas de cobrança sejam configuradas em dias. A negociação de preço e descontos durante o ciclo de cotação é feita usando taxas do dia para cada função cobrável. A estimativa do cronograma e a entrada de tempo são feitas em horas. Para aceitar essa diferença em unidades de tempo, o PSA converte unidades de tempo.

### <a name="can-time-units-be-changed-on-project-estimates"></a>As unidades de tempo podem ser alteradas em estimativas de projeto?
Nº A estimativa do cronograma atualmente está restrita a horas e não pode ser alterada.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>As unidades e os grupos de unidades podem ser editados, excluídos e adicionados?
Sim. Com exceção do grupo de unidades **Tempo** e da unidade **Hora**, todas as unidades podem ser excluídas ou editadas, e novas unidades podem ser adicionadas. No PSA, o grupo de unidades **Tempo** e a unidade **Hora** não podem ser excluídos. Entretanto, eles podem ser atualizados com um texto traduzido para o campo **Nome**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]