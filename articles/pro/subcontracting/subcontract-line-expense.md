---
title: Linhas de subcontrato para categorias de despesa
description: Este tópico explica como registrar linhas de subcontrato para despesas e usar os campos para registrar a compra de tempo de fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323807"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Linhas de subcontrato para categorias de despesa

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Um subcontrato no Dynamics 365 Project Operations pode ter uma linha para categorias de despesas. As linhas de subcontrato para categorias de despesa permitem que um Gerente de Projeto compre categorias de serviços ou produtos de fornecedores que podem ser cobrados de um projeto.

Para criar uma linha de subcontrato para categorias de despesas no Project Operations, conclua as etapas a seguir.

1. No painel de navegação, selecione **Subcontratos** e abra o subcontrato com o qual deseja trabalhar.
2. Na guia **Linhas de Subcontrato**, selecione **Novo** para criar uma nova linha.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Despesa** e insira ou selecione qualquer outra informação de campo necessária.

A tabela a seguir fornece informações sobre os campos na página de detalhes **Linha de subcontrato** e na página **Criação Rápida**.

| **Campo** |  **Descrição** |
| ----------| ---------------- |
| Name | O nome da linha de subcontrato. |
| Descrição | Uma breve descrição das categorias de serviço ou produto que estão sendo adquiridas na linha de subcontrato. |
| Tipo de Linha | Esse campo tem um valor padrão **Baseado em quantidade**.  |
| Método de Cobrança | O método de cobrança da linha de subcontrato. Com base no método de cobrança da linha, uma agenda de faturamento baseada em marcos está disponível para o método de cobrança de preço fixo.  |
| Classe da Transação | Esse campo tem um valor padrão **Tempo**. Para criar linhas de subcontrato para a compra de produtos, defina o campo **Classe de Transação** como **Despesa**. O valor desse campo indica que a linha de subcontrato está sendo utilizada para registrar uma compra de uma categoria de produtos ou serviços a serem utilizados em projetos. |
| Categoria da Transação | Selecione a categoria de transação. |
| Data de Início Solicitada | A data em que as categorias de compra devem ser disponibilizadas pelo fornecedor. O início solicitado é usado para escolher uma lista de preços das listas de preços de projeto anexadas ao subcontrato. O custo da categoria na linha de subcontrato tem seu padrão na lista de preços. |
| Término solicitado | A data em que as categorias de compra não são mais necessárias. Essa data chama um aviso quando um gerente de projeto associa essa linha de subcontrato a estimativas de despesas específicas nos projetos com data posterior à essa. |
| Quantidade Encomendada | A quantidade da categoria que está sendo comprada do fornecedor. Quando um gerente de projeto ultrapassar a quantidade adquirida, haverá um aviso.  |
| Grupo de Unidades | Esse valor de campo é padronizado com base no grupo de unidades padrão configurado para a categoria selecionada. |
| Unidade | Esse valor de campo é padronizado com base na unidade padrão configurada para a categoria selecionada. A combinação de categoria e unidade é usada para definir o preço unitário na linha de subcontrato. |
| Preço Unitário | O valor do campo de preço unitário tem como padrão a combinação da categoria e da unidade dos preços da categoria relacionados à lista de preços do projeto que é aplicável ao início solicitado da linha de subcontrato.  |
| Subtotal | Esse campo somente leitura é calculado automaticamente como o preço unitário da quantidade se os valores da quantidade e do preço unitário forem inseridos. Se um ou ambos os campos estiverem vazios, você poderá inserir manualmente um valor nesse campo.  |
| Imposto sobre Vendas | Insira o valor do imposto sobre venda.  |
| Valor Total | O valor total da linha de subcontrato, incluindo impostos. Esse campo é calculado como subtotal + imposto sobre vendas.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
