---
title: Importar uma estimativa para uma linha de contrato baseada em projeto
description: Este tópico fornece informações sobre como importar estimativas financeiras de um projeto para uma linha de contrato.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9ac367baba4529e86a42d812b7d9b2550812e297
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4071661"
---
# <a name="importing-an-estimate-to-a-project-based-contract-line"></a>Importar uma estimativa para uma linha de contrato baseada em projeto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_

No Dynamics 365 Project Operations, você pode importar estimativas de um projeto para uma linha de contrato baseada em projeto.

1. Verifique se o campo **Projeto** na linha de contrato baseada no projeto foi preenchido.
2. Na guia **Detalhes da Linha de Contrato** , na subgrade, selecione **Importar da Estimativa do Projeto**. Uma página de diálogo com opções de resumo é aberta. As opções de resumo disponíveis são **Classe de Transação** , **Categoria** , **Função** e **Tarefa do Projeto**.
3. Com base na seleção para resumo, a estimativa do projeto para todas as classes e tarefas da transação incluídas nesta linha de contrato é copiada. Para verificar quais classes de transação estão incluídas, na guia **Geral** da linha de contrato baseada em projeto, verifique os valores nos campos **Incluir Hora** , **Incluir Despesas** e **Incluir Taxas**. 
4. Para verificar quais tarefas estão incluídas, selecione a guia **Tarefas Passíveis de Cobrança** na linha de contrato. Com base nas tarefas associadas que têm o campo **Classes de Transação Incluídas** definido como **Sim** , todas as estimativas para essas combinações de tarefa e classe de transação são importadas para a linha de contrato.

Quando você importa estimativas, o sistema padroniza preços com base nas listas de preços do projeto anexadas ao contrato e na configuração do tipo de cobrança na linha do contrato. Se uma tarefa, função ou categoria for configurada na linha do contrato como não cobrável, a linha de estimativa importada será não cobrável e não será adicionada ao valor contratado da linha do contrato.

Quando uma linha do contrato tiver detalhes de linha, os campos **Valor do Contrato** e **Imposto Estimado** na linha do contrato serão resumidos e não poderão ser editados.

Quando várias opções de resumo são selecionadas, o sistema tenta resumir por todas as opções selecionadas. A saída de resumo resulta em mais linhas de contrato importadas do que se você selecionar apenas uma opção de resumo.

Por exemplo, se o projeto tiver as seguintes linhas de estimativa para despesas:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Quando o usuário selecionar a opção de resumir por **Classe de Transação** , as seguintes informações serão importadas:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1/10/2020 | 3.34 | 840 | 2800 |

Quando o usuário selecionar a opção de resumir por **Classe de Transação** e **Categoria** , as seguintes informações serão importadas:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 1/10/2020 | 6 | 200 | 1200 |

Quando o usuário selecionar a opção de resumir por **Classe de Transação** , **Categoria** e **Tarefa de Nó Folha** , as seguintes informações serão importadas. Observe que esse resultado é o mesmo que está no projeto:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Valor |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 1/10/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 1/11/2020 | 2 | 200 | 400 |
