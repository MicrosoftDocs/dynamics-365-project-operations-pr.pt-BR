---
title: Determinar as taxas de custo para estimativas de projeto e dados reais
description: Este artigo fornece informações sobre como as taxas de custo para estimativas e dados reais do projeto são determinadas.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410084"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Determinar as taxas de custo para estimativas de projeto e dados reais

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Para determinar a lista de preços de custo e as taxas de custo nos contextos de estimativa e dados reais, o sistema usa as informações nos campos **Data**, **Moeda** e **Unidade de Contratação** do projeto relacionado.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinar taxas de custo em contextos de estimativa e dados reais para Tempo

Contexto de estimativa para **Tempo** refere-se a:

- Detalhes da linha de cotação para **Tempo**.
- Detalhes da linha de contrato para **Tempo**.
- Atribuições de recursos em um projeto.

Contexto de dados reais para **Tempo** refere-se a:

- Linhas do diário de entrada e correção para **Tempo**.
- Linhas de diário criadas quando uma entrada de tempo é enviada.

Depois que uma lista de preços de custo é determinada, o sistema conclui as etapas a seguir para inserir a taxa de custo padrão.

1. O sistema compara a combinação dos campos **Função** e **Unidade de Recursos** no contexto de estimativa ou dados reais para **Tempo** com as linhas de preço de função na lista de preços. Essa correspondência pressupõe que você está usando as dimensões de preço padrão para custo de mão de obra. Se você configurou o sistema para corresponder a campos diferentes ou além de **Função** e **Unidade de Recursos**, uma combinação diferente será usada para recuperar uma linha de preço de função correspondente.
1. Se o sistema encontrar uma linha de preço de função que tenha uma taxa de custo para a combinação **Função** e **Unidade de Recursos**, essa taxa de custo será usada como a taxa de custo padrão.
1. Se o sistema não corresponder aos valores **Função** e **Unidade de Recursos**, ele recuperará as linhas de preço da função que têm valores correspondentes para o campo **Função**, mas valores nulos para o campo **Unidade de Recursos**. Depois que o sistema tiver um registro de preço de função correspondente, a taxa de custo desse registro será usada como a taxa de custo padrão.

> [!NOTE]
> Se você configurar uma priorização diferente dos campos **Função** e **Unidade de Recursos** ou se tiver outras dimensões com prioridade mais alta, o comportamento anterior será devidamente alterado. O sistema recupera registros de preço de função que possuem valores que correspondem a cada valor de dimensão de preço em ordem de prioridade. As linhas que têm valores nulos para essas dimensões vêm por último.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinar taxas de custo em linhas de dados reais e estimativa para Despesa

Contexto de estimativa para **Despesa** refere-se a:

- Detalhes da linha de cotação para **Despesa**.
- Detalhes da linha de contrato para **Despesa**.
- Estimativas de despesas em um projeto.

Contexto real para **Despesa** refere-se a:

- Linhas do diário de entrada e correção para **Despesa**.
- Linhas de diário criadas quando uma entrada de despesa é enviada.

Depois que uma lista de preços de custo é determinada, o sistema conclui as etapas a seguir para inserir a taxa de custo padrão.

1. O sistema compara a combinação dos campos **Categoria** e **Unidade** no contexto de estimativa ou dados reais para **Despesa** com as linhas de preço de categoria na lista de preços.
1. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de custo para a combinação de **Categoria** e **Unidade**, essa taxa de custo será usada como a taxa de custo padrão.
1. Se o sistema não corresponder aos valores **Categoria** e **Unidade**, o preço será definido como **0** (zero) por padrão.
1. No contexto de estimativa, se o sistema puder encontrar uma linha de preço de categoria correspondente, mas o método de precificação for diferente de **Preço por Unidade**, a taxa de custo será definida como **0** (zero) por padrão.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinar taxas de custo em linhas de dados reais e estimativa para material

Contexto de estimativa para **Material** refere-se a:

- Detalhes da linha de cotação para **Material**.
- Detalhes da linha de contrato para **Material**.
- Estimativas de materiais em um projeto.

Contexto real para **Material** refere-se a:

- Linhas do diário de entrada e correção para **Material**.
- Linhas de diário criadas quando um registro de uso de material é enviado.

Depois que uma lista de preços de custo é determinada, o sistema conclui as etapas a seguir para inserir a taxa de custo padrão.

1. O sistema usa a combinação dos campos **Produto** e **Unidade** no contexto de estimativa ou dados reais para **Material** com as linhas de item da lista de preços na lista de preços.
1. Se o sistema encontrar uma linha de item da lista de preços que tenha uma taxa de custo para a combinação de **Produto** e **Unidade**, essa taxa de custo será usada como a taxa de custo padrão.
1. Se o sistema não corresponder aos valores de **Produto** e **Unidade**, o custo unitário será definido como **0** (zero) por padrão.
1. No contexto de estimativa ou dados reais, se o sistema encontrar uma linha de item da lista de preços correspondente, mas o método de precificação for diferente de **Preço por Unidade**, o custo unitário será definido como **0** (zero) por padrão. Esse comportamento ocorre porque o Project Operations oferece suporte apenas ao método de precificação **Valor da moeda** para materiais usados em um projeto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
