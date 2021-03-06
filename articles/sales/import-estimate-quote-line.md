---
title: Importar estimativas de projeto para uma linha de cotação baseada no projeto
description: Este tópico fornece informações sobre como importar estimativas de um projeto para uma linha de cotação.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907853"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importar estimativas de projeto para uma linha de cotação baseada no projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_


Se um projeto for criado durante o estágio de pré-vendas, você pode optar por importar a estimativa financeira do projeto para a linha de cotação baseada no projeto.

1. Certifique-se de que a linha de cotação baseada no projeto tenha as informações do projeto no campo **Projeto**.
2. Na guia **Detalhes da linha de cotação**, selecione **Importar da Estimativa do Projeto**.
3. Na página de diálogo aberta, selecione uma das seguintes opções de resumo.

  - **Classe da transação**
  - **Categoria**
  - **Função** 
  - **Tarefa do projeto**

Com base em sua seleção, a estimativa do projeto para todas as classes de transação incluídas nesta linha de cotação é copiada. Para verificar quais classes de transação estão incluídas, selecione a guia **Geral** na linha de cotação baseada no projeto e verifique os valores de **Incluir Hora**, **Incluir Despesas** e **Incluir Taxas**.

Ao importar estimativas, o sistema padronizará o preço com base nas listas de preços de projeto anexadas à cotação e a configuração do tipo de cobrança na linha de cotação baseada no projeto. Se uma função ou categoria for configurada na linha de cotação baseada no projeto como não cobrável, a linha de estimativa importada será definida como não cobrável e não será adicionada ao valor cotado da linha de cotação.

Quando uma linha de cotação tiver detalhes de linha, os campos **Valor da Cotação** e **Imposto Estimado** na linha de cotação serão resumidos e não poderão ser editados.

Quando várias opções de resumo são selecionadas, o recurso tenta criar um resumo com todas as opções selecionadas. Isso significa que a saída de linhas de cotação importadas será maior do que se você tivesse selecionado apenas uma opção de resumo.

Por exemplo, se o projeto tiver as seguintes linhas de estimativa para despesas.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Quando o usuário selecionar a opção de resumir por Classe de transação, as seguintes informações serão importadas.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| | | 1/10/2020 | 3.34 | 840 | 2800 |

Quando o usuário selecionar a opção de resumir por Classe de transação e Categoria, as seguintes informações serão importadas.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| | Hotel | 1/10/2020 | 6 | 200 | 1200 |

Quando o usuário selecionar a opção de resumir por Classe de transação, Categoria e Tarefa de Nó Folha, as seguintes informações serão importadas. Observe que esse resultado é o mesmo que estava no projeto.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 1/11/2020 | 2 | 200 | 400 |