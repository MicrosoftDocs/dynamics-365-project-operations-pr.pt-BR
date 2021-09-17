---
title: Linhas de subcontrato para produtos
description: Este tópico explica como registrar linhas de subcontrato para produtos e usar os diversos campos para registrar compras de produto de fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323672"
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

| Campo | Descrição |
| ----- | ----------- |
| Name | O nome da linha de subcontrato. |
| Descrição | Uma breve descrição de produtos que estão sendo pedidos na linha de subcontrato. |
| Tipo de Linha | Esse valor de campo tem como padrão **Baseado em quantidade**. |
| Método de Cobrança |  O método de cobrança da linha de subcontrato. Uma agenda de fatura com base em marco está disponível para métodos de cobrança de preço fixo. |
| Classe da Transação | Esse valor de campo tem como padrão **Tempo**. Para criar linhas de subcontrato para a compra de produtos, no campo **Classe de Transação**, selecione **Material**. Essa seleção indica que a linha de subcontrato está sendo utilizada para registrar uma compra de uma categoria de produtos ou serviços a serem utilizados em projetos. |
| Selecionar Produto | Selecione se o produto que está sendo adquirido é mantido no catálogo de produtos ou é um produto fora do catálogo. |
| Produto | Selecionar um produto ativo no catálogo. Esse campo só estará disponível quando **Selecionar Produto** estiver definido como **Existente**. |
| Produto Fora do Catálogo | Insira o nome do produto fora do catálogo. Esse campo só estará disponível quando **Selecionar Produto** estiver definido como **Fora do Catálogo**.  |
| Data de Entrega Solicitada | Selecione a data de entrega necessária para os produtos. Essa data também é usada para escolher uma lista de preços das listas de preços de projeto anexadas ao subcontrato. O custo do produto na linha de subcontrato então terá o padrão saído daquela lista de preços. |
| Data de entrega contratada | Selecione a data em que os produtos estão contratualmente acordados para serem entregues.  |
| Quantidade Encomendada | Insira a quantidade do produto que está sendo comprado do fornecedor. Se um Gerente de Projeto ultrapassar essa quantidade, haverá um aviso. |
| Grupo de Unidades | Esse valor é padronizado apenas para produtos do catálogo. Quando **Produto** e **Data de entrega solicitada** estiverem selecionados, o sistema selecionará a lista de preços aplicável com base na data de entrega. Os itens da lista de preços relacionados são consultados para o produto correspondente. Os valores da unidade e do grupo de unidades têm como padrão a configuração no registro do item da lista de preços. |
| Unidade | Esse valor é padronizado para a configuração da unidade no registro do item da lista de preços. Você pode alterar isso para outra unidade, conforme necessário. A combinação de produto e unidade é usada para como o padrão do preço unitário na linha de subcontrato para produtos de catálogo existentes. |
| Preço Unitário | O preço unitário tem como padrão o uso da combinação de produto e unidade dos itens de lista de preços relacionados à lista de preços de projeto aplicável para a data de entrega solicitada da linha de subcontrato.  |
| Subtotal | Esse campo somente leitura será calculado como Quantidade x Preço unitário se ambos os campos tiverem valores inseridos. Se o campo **Quantidade**, o campo **Preço unitário**, ou ambos, estiverem vazios, você poderá inserir um valor no campo.  |
| Imposto sobre Vendas | Insira o valor do imposto sobre vendas. |
| Valor Total | Esse campo calculado mostra o valor total da linha de subcontrato após a inclusão dos impostos. O valor nesse campo é calculado como subtotal + imposto. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
