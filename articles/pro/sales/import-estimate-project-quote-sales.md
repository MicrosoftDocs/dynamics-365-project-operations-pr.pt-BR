---
title: Importar estimativas de um projeto para uma linha de cotação baseada em projeto - lite
description: Este artigo fornece informações sobre como importar estimativas de um projeto para uma linha de cotação.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 820d858fecf70e50a9ce8943db706ff6cac29992
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917286"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importar estimativas de um projeto para uma linha de cotação baseada em projeto 

_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma, Project Operations para cenários com base em recursos/sem estoque_

Se um projeto for criado durante o estágio de pré-vendas, você pode optar por importar a estimativa financeira do projeto para a linha de cotação baseada no projeto.

1. Certifique-se de que a linha de cotação baseada no projeto tenha as informações do projeto no campo **Projeto**.
2. Na guia **Detalhes da linha de cotação**, selecione **Importar da Estimativa do Projeto**.
3. Na página de diálogo aberta, selecione uma das seguintes opções de resumo.

  - **Classe da transação**
  - **Categoria**
  - **Função** 
  - **Tarefa do projeto**

Com base em sua seleção, a estimativa do projeto para todas as classes de transação incluídas nesta linha de cotação é copiada. Para verificar quais classes de transação estão incluídas, selecione a guia **Geral** na linha de cotação baseada em projeto e verifique os valores de **Incluir Hora**, **Incluir Despesas**, **Incluir Materiais** e **Incluir Taxas**.  Para verificar quais tarefas estão incluídas, selecione a guia **Tarefas Passíveis de Cobrança** na linha de cotação.

Dependendo das tarefas associadas e classes de transação incluídas, as estimativas para essas combinações de tarefa e classe de transação são importadas para a linha de cotação.

Ao importar estimativas, o sistema padronizará o preço com base nas listas de preços de projeto anexadas à cotação e a configuração do tipo de cobrança na linha de cotação baseada no projeto. Se uma tarefa, função ou categoria for configurada na linha de cotação baseada em projeto como não cobrável, a linha de estimativa importada será definida como não cobrável e não será adicionada ao valor cotado da linha de cotação.

Quando uma linha de cotação tiver detalhes de linha, os campos **Valor da Cotação** e **Imposto Estimado** na linha de cotação serão resumidos e não poderão ser editados.

Quando várias opções de resumo são selecionadas, o sistema tenta resumir por todas as opções selecionadas. O resultado é que a saída de linhas de cotação importadas será maior do que se você tivesse selecionado apenas uma opção de resumo.

Por exemplo, se o projeto teve as seguintes linhas de estimativa para despesas.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Quando o usuário selecionar a opção de resumir por Classe de transação, as seguintes informações serão importadas.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
|||1/10/2020 | 3.34 | 840 | 2800 |

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
