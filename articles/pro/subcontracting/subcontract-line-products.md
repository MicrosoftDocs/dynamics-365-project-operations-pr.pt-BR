---
title: Linhas de subcontrato para produtos
description: Este tópico explica como registrar linhas de subcontrato para produtos e usar os diversos campos para registrar compras de produto de fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cda2db2b6beafb943738b35857d091f7ad17390d
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558533"
---
# <a name="subcontract-lines-for-products"></a>Linhas de subcontrato para produtos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Um subcontrato no Dynamics 365 Project Operations pode ter uma linha de subcontrato para produtos. Essas linhas permitem que um Gerente de Projeto compre produtos de fornecedores que ele poderá usar nas tarefas do projeto.

Conclua as etapas a seguir para criar uma linha de subcontrato para produtos no Project Operations.

1. Na página de navegação, selecione **Subcontratos** e abra o subcontrato com o qual deseja trabalhar. 
2. Na guia **Linhas de Subcontrato**, selecione **+ Novo** para criar uma nova linha de subcontrato.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Material** e insira ou selecione a informação de campo necessária. 
4. Selecione **Salvar**.

A tabela a seguir fornece informações sobre os campos na página **Linha de subcontrato** e na página **Criação Rápida** à medida que elas forem relevantes para a compra de produtos.

| Campo | Descrição | Impacto funcional|
| ----- | ----------- | ----------- |
| Name | Nome da linha do subcontrato para ajudar na identificação. |Isso será exibido como a primeira coluna em todas as pesquisas baseadas em linhas de subcontrato.
| Descrição | Uma breve descrição de produtos que estão sendo pedidos na linha de subcontrato. | Nenhum(a) |
| Tipo de Linha | Esse campo tem um valor padrão **Baseado em quantidade**. |Nenhum(a) |
| Método de Cobrança | Este é um conjunto de opções que representa os dois principais modelos de contratação com suporte do Project Operations: **Preço Fixo** e **Tempo e Material**. | Com base no método de cobrança selecionado, uma agenda de faturamento baseada em etapas é disponibilizada para linhas de subcontrato com o método de cobrança Preço Fixo. |
| Classe da Transação |Esse campo tem um valor padrão **Tempo**. Para criar linhas de subcontrato para a compra de produtos, defina o campo **Classe da Transação** como **Material**.  | Isso indica que a linha do subcontrato está sendo utilizada para registrar a compra de produtos a serem utilizados nos projetos. |
| Selecionar Produto | Selecione se o produto que está sendo adquirido é mantido no catálogo de produtos ou é um produto fora do catálogo. |Nenhum(a) |
| Produto | Selecionar um produto ativo no catálogo. Esse campo só estará disponível quando **Selecionar Produto** estiver definido como **Existente**. |A combinação de **Produto** e **Unidade** será usada como o padrão ou será calculada para o preço unitário da linha do subcontrato.
| Produto Fora do Catálogo | Insira o nome do produto fora do catálogo. Esse campo só estará disponível quando **Selecionar Produto** estiver definido como **Fora do Catálogo**.  |O preço de compra não será preenchido automaticamente para produtos fora do catálogo.|
| Data de Entrega Solicitada | Insira a data de entrega necessária para os produtos.| Essa data também é usada para escolher uma lista de preços das listas de preços de projeto anexadas ao subcontrato. O custo do produto na linha de subcontrato então terá o padrão saído daquela lista de preços. |
| Data de entrega contratada | Insira a data em que os produtos estão contratualmente previstos para serem entregues.  |Nenhum(a)|
| Quantidade Encomendada | Insira a quantidade do produto que está sendo comprado do fornecedor.| Isso será usado para mostrar avisos quando um gerente de projeto estiver extrapolando esta quantidade.|
| Grupo de Unidades | Esse valor é padronizado apenas para produtos do catálogo. |Quando **Produto** e **Data de entrega solicitada** estiverem selecionados, o sistema selecionará a lista de preços aplicável com base na data de entrega. Os itens da lista de preços relacionados são consultados para o produto correspondente. Os valores da unidade e do grupo de unidades têm como padrão a configuração no registro do item da lista de preços. |
| Unidade | Este valor usa como padrão a unidade configurada no registro do item da lista de preços. Você pode alterar isso para outra unidade, conforme necessário.| A combinação de produto e unidade é usada para como o padrão do preço unitário na linha de subcontrato para produtos de catálogo existentes. |
| Preço Unitário | O preço unitário tem como padrão o uso da combinação de produto e unidade dos itens de lista de preços relacionados à lista de preços de projeto aplicável para a data de entrega solicitada da linha de subcontrato.  |Nenhum(a) |
| Subtotal | Esse campo somente leitura será calculado como Quantidade x Preço unitário se ambos os campos tiverem valores inseridos. Se o campo **Quantidade**, o campo **Preço unitário**, ou ambos, estiverem vazios, você poderá inserir um valor no campo.  |Nenhum(a) |
| Imposto sobre Vendas | Insira o valor do imposto sobre vendas. |Nenhum(a) |
| Valor Total | Esse campo calculado mostra o valor total da linha de subcontrato após a inclusão dos impostos. O valor nesse campo é calculado como Subtotal + Imposto. |Nenhum(a) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
