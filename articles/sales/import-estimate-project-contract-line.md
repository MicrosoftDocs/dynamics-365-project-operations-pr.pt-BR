---
title: Importar uma estimativa para uma linha de contrato baseada em projeto
description: Este tópico fornece informações sobre como importar estimativas de um projeto para uma linha de contrato.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6dde924c24dcffe2a8fb690e6eb429e4c3d9fb28
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126379"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importar uma estimativa para uma linha de contrato baseada em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

No Dynamics 365 Project Operations, você pode importar estimativas de um projeto para uma linha de contrato baseada em projeto.

1. Verifique se o campo **Projeto** na linha de contrato com base no projeto está preenchido.
2. Na guia **Detalhes da Linha de Contrato**, na subgrade, selecione **Importar da Estimativa do Projeto**. Uma página de diálogo com opções de resumo é aberta. As opções de resumo disponíveis são **Classe de Transação**, **Categoria**, **Função** e **Tarefa do projeto**. Com base nas seleções para resumo, a estimativa do projeto para todas as classes da transação incluídas nesta linha de contrato é copiada. 
3. Para verificar quais classes de transação estão incluídas, na guia **Geral** da linha de contrato, verifique os valores nos campos **Incluir Hora**, **Incluir Despesas** e **Incluir Taxas**.

Ao importar estimativas, a aplicação padroniza o preço com base nas listas de preços do projeto anexadas ao contrato e a configuração do tipo de cobrança na linha do contrato. Se uma função ou categoria for configurada na linha do contrato como não cobrável, a linha de estimativa importada para essa função ou categoria será não cobrável e não será adicionada ao valor contratado da linha do contrato.

Quando uma linha do contrato tiver detalhes de linha, os campos **Valor do Contrato** e **Imposto Estimado** na linha do contrato serão resumidos e não poderão ser editados.

Quando várias opções de resumo são selecionadas, o sistema tenta resumir por todas as opções selecionadas. A saída de resumo resulta em mais linhas de contrato importadas do que se você selecionar apenas uma opção de resumo.

Por exemplo, se o projeto teve as seguintes linhas de estimativa para despesas:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Quando o usuário selecionar a opção de resumir por **Classe de Transação**, as seguintes informações serão importadas:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 1/10/2020 | 3.34 | 840 | 2800 |

Quando o usuário selecionar a opção de resumir por **Classe de Transação** e **Categoria**, as seguintes informações serão importadas:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 1/10/2020 | 6 | 200 | 1200 |

Quando o usuário selecionar a opção de resumir por **Classe de Transação**, **Categoria** e **Tarefa de Nó Folha**, as seguintes informações serão importadas. Observe que esse resultado é o mesmo que estava no projeto:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 1/11/2020 | 2 | 200 | 400 |
