---
title: Importar estimativas de projeto para uma linha de cotação baseada no projeto
description: Este tópico fornece informações sobre como importar estimativas de um projeto para uma linha de cotação.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b32ac22188922a56fa13ea67e0ead77b9b045d9f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278314"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importar estimativas de projeto para uma linha de cotação baseada no projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


Se um projeto for criado durante o estágio de pré-vendas, você pode optar por importar a estimativa financeira do projeto para a linha de cotação baseada no projeto.

1. Certifique-se de que a linha de cotação baseada no projeto tenha as informações do projeto no campo **Projeto**.
2. Na guia **Detalhes da linha de cotação**, selecione **Importar da Estimativa do Projeto**.
3. Na página de diálogo aberta, selecione uma das seguintes opções de resumo:

  - **Classe da transação**
  - **Categoria**
  - **Função** 
  - **Tarefa do projeto**

Com base em sua seleção, a estimativa do projeto para todas as classes de transação incluídas nesta linha de cotação é copiada. Para verificar quais classes de transação estão incluídas, selecione a guia **Geral** na linha de cotação baseada no projeto e verifique os valores de **Incluir Hora**, **Incluir Despesas** e **Incluir Taxas**.

Ao importar estimativas, o sistema padronizará o preço com base nas listas de preços do projeto anexadas à cotação e a configuração do tipo de cobrança na linha de cotação baseada em projeto. Se uma função ou categoria for configurada na linha de cotação baseada no projeto como não cobrável, a linha de estimativa importada será definida como não cobrável e não será adicionada ao valor cotado da linha de cotação.

Quando uma linha de cotação tiver detalhes de linha, os campos **Valor da Cotação** e **Imposto Estimado** na linha de cotação serão resumidos e não poderão ser editados.

Quando várias opções de resumo são selecionadas, o sistema tenta resumir por todas as opções selecionadas. O resultado é que a saída de linhas de cotação importadas será maior do que se você tivesse selecionado apenas uma opção de resumo.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]