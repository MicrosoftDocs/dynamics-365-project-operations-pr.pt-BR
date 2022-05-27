---
title: Linhas da fatura de fornecedor para categorias de despesa
description: Este tópico explica como registrar linhas da fatura de fornecedor para categorias de despesa.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579522"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Linhas da fatura de fornecedor para categorias de despesa

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations pode ter linhas da fatura de fornecedor para categorias de despesa. Os gerentes de projeto podem usar linhas da fatura de fornecedor para categorias de despesa para registrar os custos de serviços adquiridos como categorias de despesa.

As linhas da fatura de fornecedor para categorias de despesa podem ou não fazer referência a uma linha de subcontrato para categorias de despesa. Se uma linha da fatura de fornecedor para categorias de despesa fizer referência a um subcontrato, os gerentes de projeto poderão comparar e verificar as despesas que estão sendo faturadas pela linha da fatura de fornecedor em relação a despesas registradas nessas categorias de despesa e aprovadas por gerentes de projeto no projeto.

A tabela a seguir apresenta informações sobre os campos nas linhas da fatura de fornecedor para categorias de despesa.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | O nome da linha da fatura de fornecedor para ajudar na identificação. | Esse nome será exibido como a primeira coluna em todas as pesquisas baseadas em linhas da fatura de fornecedor. |
| Description | Uma breve descrição dos serviços que estão sendo faturados pelo fornecedor na linha da fatura de fornecedor. | Nenhum |
| Subcontrato | O subcontrato em que os serviços foram pedidos originalmente. | Quando um subcontrato for selecionado para a fatura de fornecedor, todas as linhas da fatura de fornecedor herdarão essa seleção. Uma fatura de fornecedor não pode ter linhas da fatura de fornecedor que fazem referência a subcontratos diferentes. |
| Linha de subcontrato | A linha de subcontrato em que os serviços foram pedidos. A lista de linhas de subcontrato que podem ser selecionadas é limitada às linhas do subcontrato selecionado. | Quando uma linha de subcontrato é selecionada em uma linha da fatura de fornecedor para categorias de despesa, os valores padrão dos campos **Projeto**, **Tarefa** e **Categoria de transação** são inseridos a partir dos campos correspondentes na linha de subcontrato. Se a linha de subcontrato selecionada tiver valores nos campos **Projeto**, **Tarefa do projeto** e **Categoria de transação**, os valores dos campos correspondentes na linha da fatura de fornecedor não podem diferir desses valores. |
| Data da transação | A data em que o dado real de custo da linha da fatura de fornecedor será registrado no projeto. |Nenhum |
| Classe da transação | Selecione **Despesa** para registrar uma fatura de fornecedor para uma categoria de despesa. | O valor **Despesa** indica que a linha da fatura de fornecedor está sendo usada para registrar o valor da fatura de serviços que foram adquiridos como categorias de despesa. |
| Project | O nome do projeto no qual os serviços que estão sendo faturados foram usados. | Este campo é obrigatório e não pode ficar em branco. |
| Tarefa | O nome da tarefa do projeto na qual os serviços que estão sendo faturados foram usados. Este campo estará disponível somente se houver um projeto selecionado. A seleção de uma tarefa do projeto é opcional. | Se este campo estiver em branco, o gerente de projeto poderá corresponder a linha da fatura de fornecedor com as despesas registradas em qualquer tarefa do projeto. Se a linha da fatura de fornecedor não fizer referência a uma linha de subcontrato e esse campo ficar em branco, o dado real de custo criado pela linha da fatura de fornecedor não será vinculado a nenhum valor real de vendas não faturado. Nesse caso, se o faturamento baseado em tarefas estiver configurado, talvez não seja possível faturar os custos para o cliente final. |
| Categoria da transação | A categoria de transação que está sendo faturada. Deve ser criada uma categoria de despesa correspondente para a categoria de transação selecionada. | A combinação dos valores de **Categoria de transação** e **Unidade** será usada como valor padrão ou calculado para o campo **Preço unitário** na linha da fatura de fornecedor. |
| Quantidade | Insira a quantidade que está sendo faturada pelo fornecedor na linha da fatura. |Nenhum|
| Grupo de unidades | Um valor padrão é inserido com base no grupo de unidades da categoria de transação selecionada. | Nenhum |
| Unidade | O valor padrão é unidade base do grupo de unidades selecionado. Você pode alterar esse valor para comprar em qualquer unidade do grupo de unidades. | A combinação dos valores de **Categoria de transação** e **Unidade** será usada como valor padrão ou calculado para o campo **Preço unitário** na linha da fatura de fornecedor. |
| Preço unitário | O preço unitário padrão usa a combinação dos valores de **Categoria de transação** e **Unidade** da lista de preços do projeto aplicável à data da transação da linha da fatura de fornecedor. | Se o preço da lista de preços do projeto aplicável for configurado em uma unidade diferente da unidade na linha da fatura de fornecedor, o sistema usará a conversão de unidades para calcular o preço unitário. |
| Subtotal | Este campo somente leitura será calculado como *Quantidade* &times; *Preço unitário*, se forem inseridos valores nos campos **Quantidade** e **Preço unitário**. Se um ou ambos os campos estiverem em branco, você poderá inserir um valor no campo.| Nenhum |
| Imposto sobre vendas | Insira o valor do imposto sobre venda. | Nenhum |
| Valor total | O valor total da linha da fatura de fornecedor, incluindo impostos. Esse campo é calculado como *Subtotal* + *Imposto sobre vendas*. | Nenhum |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
