---
title: Linhas da fatura de fornecedor para produtos
description: Este artigo explica como registrar linhas da fatura de fornecedor para produtos e usar os diferentes campos para registrar compras de produtos de fornecedores.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261544"
---
# <a name="vendor-invoice-lines-for-products"></a>Linhas da fatura de fornecedor para produtos

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations pode ter linhas da fatura de fornecedor para produtos (também chamados de materiais). Os gerentes de projeto podem usar as linhas da fatura de fornecedor para produtos para registrar os custos de produtos comprados nos projetos.

As linhas da fatura do fornecedor para produtos podem ou não fazer referência a uma linha de subcontrato para materiais. Se uma linha da fatura de fornecedor para produtos fizer referência a um subcontrato, os gerentes de projeto poderão comparar e verificar os produtos que estão sendo faturados pela linha da fatura de fornecedor em relação ao uso de produtos comprados registrados e aprovados por gerentes de projeto.

A tabela a seguir apresenta informações sobre os campos nas linhas da fatura de fornecedor para produtos.

| Campo | Descrição | Impacto funcional |
| --- | --- | --- |
| Nome | O nome da linha da fatura de fornecedor para ajudar na identificação. | Esse nome será exibido como a primeira coluna em todas as pesquisas baseadas em linhas da fatura de fornecedor. |
| Descrição | Uma breve descrição dos produtos que estão sendo faturados pelo fornecedor na linha da fatura de fornecedor. | Nenhum |
| Subcontrato | O subcontrato em que os produtos foram pedidos originalmente. | Quando um subcontrato for selecionado para a fatura de fornecedor, todas as linhas da fatura de fornecedor herdarão essa seleção. Uma fatura de fornecedor não pode ter linhas da fatura de fornecedor que fazem referência a subcontratos diferentes. |
| Linha de subcontrato | A linha de subcontrato em que os produtos foram pedidos. A lista de linhas de subcontrato que podem ser selecionadas é limitada às linhas do subcontrato selecionado. | Quando uma linha de subcontrato é selecionada em uma linha da fatura de fornecedor para produtos, os valores padrão dos campos **Projeto**, **Tarefa** e **Produto** são inseridos a partir dos campos correspondentes na linha de subcontrato. Se a linha de subcontrato selecionada tiver valores nos campos **Projeto**, **Tarefa** e **Produto**, os valores dos campos correspondentes na linha da fatura de fornecedor não podem diferir desses valores. |
| Data da transação | A data em que o dado real de custo da linha da fatura de fornecedor será registrado no projeto. | Nenhum|
| Classe da transação | Quando produtos são faturados, este campo deve ser definido como **Material**. | O valor **Material** indica que a linha da fatura de fornecedor está sendo usada para registrar o valor da fatura de materiais que foram comprados. |
| Projeto | O nome do projeto no qual os produtos que estão sendo faturados foram usados. | Este campo é obrigatório e não pode ficar em branco. |
| Tarefa | O nome da tarefa do projeto no qual os produtos que estão sendo faturados foram usados. Este campo estará disponível somente se houver um projeto selecionado. A seleção de uma tarefa do projeto é opcional. | Se este campo estiver em branco, o gerente de projeto poderá corresponder a linha da fatura de fornecedor com o produto comprado usado em qualquer tarefa do projeto. Se a linha da fatura de fornecedor não fizer referência a uma linha de subcontrato e esse campo ficar em branco, o dado real de custo criado pela linha da fatura de fornecedor não será vinculado a nenhum valor real de vendas não faturado. Nesse caso, se o faturamento baseado em tarefas estiver configurado, os custos não poderão ser faturados para o cliente final. |
| Selecionar produto | Selecione se o produto que está sendo faturado é um produto existente no catálogo ou se é um produto fora do catálogo. | O valor padrão é inserido a partir da linha de subcontrato quando uma linha de subcontrato é selecionada. |
| Produto | Selecionar um produto do catálogo. Se for um produto fora do catálogo, insira o nome do produto. | Este campo é usado para inserir preços de compra padrão de produtos existentes. |
| Quantidade | Insira a quantidade de material que está sendo faturada pelo fornecedor nesta linha da fatura. | Nenhum |
| Grupo de unidades | Selecione o grupo de unidades da unidade em que a quantidade que está sendo faturada é expressa. | Nenhum |
| Unidade | O valor padrão é unidade base do grupo de unidades selecionado. Você pode alterar esse valor para pagar em qualquer unidade do grupo de unidades selecionado. | A combinação dos valores de **Produto** e **Unidade** será usada como valor padrão ou calculado para o campo **Preço unitário** na linha da fatura de fornecedor. |
| Preço unitário | O preço unitário padrão usa a combinação dos valores de **Produto** e **Unidade** da lista de preços do projeto aplicável à data da transação da linha da fatura de fornecedor. | Nenhum |
| Subtotal | Este campo somente leitura será calculado como *Quantidade* &times; *Preço unitário*, se forem inseridos valores nos campos **Quantidade** e **Preço unitário**. Se um ou ambos os campos estiverem em branco, você poderá inserir um valor no campo. | Nenhum |
| Imposto sobre vendas | Insira o valor do imposto sobre venda. | Nenhum |
| Valor total | O valor total da linha da fatura de fornecedor, incluindo impostos. Esse campo é calculado como *Subtotal* + *Imposto sobre vendas*. | Nenhum |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
