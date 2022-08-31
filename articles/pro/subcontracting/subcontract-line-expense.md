---
title: Linhas de subcontrato para categorias de despesa
description: Este artigo explica como registrar linhas de subcontrato para despesas e usar os campos para registrar a compra de tempo de fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261826"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Linhas de subcontrato para categorias de despesa

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Um subcontrato no Dynamics 365 Project Operations pode ter uma linha para categorias de despesas. As linhas de subcontrato para categorias de despesa permitem que um Gerente de Projeto compre categorias de serviços ou produtos de fornecedores que podem ser cobrados de um projeto.

Para criar uma linha de subcontrato para categorias de despesas no Project Operations, conclua as etapas a seguir.

1. No painel de navegação, selecione **Subcontratos** e abra o subcontrato com o qual deseja trabalhar.
2. Na guia **Linhas de Subcontrato**, selecione **Novo** para criar uma nova linha.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Despesa** e insira ou selecione qualquer outra informação de campo necessária.

A tabela a seguir fornece informações sobre os campos na página de detalhes **Linha de subcontrato** e na página **Criação Rápida**.

| **Campo** | **Descrição** | **Impacto funcional** |
| --- | --- | --- |
| Name | Nome da linha do subcontrato para ajudar na identificação. | Isso será exibido como a primeira coluna em todas as pesquisas baseadas em linhas de subcontrato. |
| Descrição | Uma breve descrição das categorias de despesas que estão sendo compradas na linha do subcontrato. | Nenhum(a) |
|Tipo de Linha | Esse campo tem um valor padrão **Baseado em quantidade**. |Nenhum(a) |
| Método de Cobrança | Este é um conjunto de opções que representa os dois principais modelos de contratação com suporte do Project Operations: **Preço Fixo** e **Tempo e Material**. | Uma agenda de faturamento baseada em etapas é disponibilizada para linhas de subcontrato se o método de cobrança Preço Fixo for selecionado. |
| Classe da Transação | Esse campo tem um valor padrão **Tempo**. Para criar linhas de subcontrato para a compra de produtos, defina o campo **Classe da Transação** como **Despesa**.  | Isso indica que a linha do subcontrato está sendo utilizada para registrar a compra de uma categoria de despesas a ser utilizada nos projetos. |
| Categoria da Transação | Mostra uma lista de categorias de transações ativas no sistema. |Nenhum(a) |
| Data de Início Solicitada | Insira a data em que as categorias de compra devem ser disponibilizadas pelo fornecedor. | O início solicitado é usado para escolher uma lista de preços de projeto nas listas de preços de projeto anexadas ao subcontrato. O custo da categoria na linha do subcontrato vem dessa lista de preços. |
| Término solicitado | Insira a data em que as categorias de compra não sejam mais necessárias. | Isso será usado para mostrar avisos quando um gerente de projeto estiver associando esta linha de subcontrato a estimativas de despesas específicas no projeto que sejam necessárias após esta data. |
| Quantidade Encomendada | Quantidade da categoria sendo comprada do fornecedor. | Isso será usado para mostrar avisos quando um gerente de projeto estiver extrapolando esta quantidade.|
| Grupo de Unidades | O valor padrão é baseado no grupo de unidades padrão configurado para a categoria selecionada. |Nenhum(a) |
| Unidade | O padrão é baseado na unidade padrão configurada para a categoria selecionada.  | A combinação de **Categoria** e **Unidade** será usada como o padrão ou será calculada para o preço unitário da linha do subcontrato.  |
| Preço Unitário | O valor padrão usa a combinação de **Categoria** e **Unidade** dos preços da categoria relacionados à lista de preços do projeto, que é aplicável para o início solicitado da linha do subcontrato. |Nenhum(a) |
| Subtotal | Este é um campo somente leitura calculado como Quantidade X Preço unitário, se os valores de quantidade e preço unitário forem inseridos. Se um ou ambos os campos estiverem em branco, você poderá inserir um valor no campo. |Nenhum(a) |
| Imposto sobre Vendas | Insira o valor do imposto sobre venda. |Nenhum(a) |
| Valor Total | O valor total da linha de subcontrato, incluindo impostos. Esse campo é calculado como Subtotal + Imposto. |Nenhum(a) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
