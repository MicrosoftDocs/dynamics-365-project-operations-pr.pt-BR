---
title: Comprar materiais sem estoque ou categorias de compras usando uma fatura de fornecedor pendente
description: Este artigo explica como registrar faturas de fornecedores pendentes.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921978"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Comprar materiais sem estoque ou categorias de compras usando uma fatura de fornecedor pendente

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

À medida que uma empresa adquire materiais sem estoque ou categorias de compras para um projeto, os custos podem ser registrados imediatamente no projeto. 

Por exemplo, a Contoso Robotics US está executando um projeto de renovação de equipamentos e precisa de licenças de software. Essas licenças são adquiridas de um fornecedor terceirizado.  Usando o Dynamics 365 Finance, o funcionário de contas a pagar registra um documento de fatura de fornecedor pendente e atribui os custos de licença diretamente ao projeto de renovação de equipamentos. 

> [!IMPORTANT]
> Antes de usar a funcionalidade descrita neste artigo, revise e aplique as configurações necessárias. Para obter mais informações, consulte [Habilitar materiais sem estoque e faturas de fornecedor pendentes](configure-materials-nonstocked.md) e [Usar categorias de compras com ordens de compra do projeto e faturas de fornecedor pendentes](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publicar uma fatura de fornecedor pendente relacionada ao projeto 

As faturas de fornecedor pendentes podem ser registradas na página **Faturas de fornecedor pendentes** (**Contas a pagar** > **Faturas** > **Faturas de fornecedor pendentes**). Conclua as seguintes etapas para postar uma fatura de fornecedor pendente relacionada ao projeto:

1. Vá para **Contas a pagar** > **Faturas** e selecione **Nova**. 
1. No campo **Conta de fatura**, selecione um fornecedor e, no campo **Número**, insira a identificação de fatura do fornecedor.
1. Adicione uma linha à fatura do fornecedor e, no campo **Número do item**, selecione o item sem estoque que foi comprado do fornecedor. Como alternativa, no campo **Categoria de compras**, selecione a categoria de compras que foi comprada do fornecedor.   
1. Adicione a quantidade que foi comprada. O sistema preenche o preço unitário com base na configuração de preço do item sem estoque. 
1. Verifique o valor total e outros detalhes necessários na linha.
1. Nos detalhes da linha, na guia **Projeto**, selecione a ID do projeto no qual esse item será registrado.
1. Opcional: selecione o número da atividade e atualize a categoria do projeto e a propriedade da linha.
1. Lance a fatura de fornecedor pendente. Quando a fatura é lançada, o sistema registra as seguintes informações:
    
    - O valor do saldo do fornecedor.
    - O valor do imposto.
    - O custo do projeto é registrado na conta de integração de aquisições.
    - A transação de custo real do projeto no Dataverse.  Esta transação é posteriormente processada usando o [diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md). A postagem deste diário move o valor da conta de integração de aquisições para a conta de custo do projeto. 
    - Compras que são faturadas para o cliente do projeto usando o método de cobrança de tempo e materiais. Além disso, transações de vendas não faturadas são criadas para as compras no Dataverse. A lista de preços do produto no Dataverse é usada para os preços de venda e os valores das transações de vendas não faturadas.
