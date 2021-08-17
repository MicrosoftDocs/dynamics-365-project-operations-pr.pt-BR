---
title: Comprar materiais sem estoque usando uma fatura de fornecedor pendente
description: Este tópico explica como registrar faturas de fornecedores pendentes.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009022"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Comprar materiais sem estoque usando uma fatura de fornecedor pendente

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Como uma empresa adquire materiais não estocados para um projeto, os custos podem ser logo registrados no projeto. 

Por exemplo, a Contoso Robotics US está realizando um projeto de renovação de equipamentos e precisa de licenças de software. Essas licenças são adquiridas de um fornecedor terceirizado.  Usando o Dynamics 365 Finance, o administrador de contas a pagar registra um documento de fatura do fornecedor pendente e atribui os custos da licença diretamente ao projeto de renovação do equipamento. 

> [!IMPORTANT]
> Antes de usar a funcionalidade descrita neste tópico, revise e aplique as configurações necessárias. Para obter mais informações, consulte [Habilitar materiais não estocados e faturas de fornecedores pendentes](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publicar uma fatura de fornecedor pendente relacionada ao projeto 

As faturas de fornecedor pendentes podem ser registradas na página **Faturas de fornecedor pendentes** (**Contas a pagar** > **Faturas** > **Faturas de fornecedor pendentes**). Conclua as seguintes etapas para postar uma fatura de fornecedor pendente relacionada ao projeto:

1. Acesse **Contas a pagar** > **Faturas** e selecione **Novo**. 
2. No campo **Conta da fatura**, selecione um fornecedor e, no campo **Número**, insira a identificação da fatura do fornecedor.
3. Adicione uma linha à fatura do fornecedor e, no campo **Número de item**, selecione o item não estocado adquirido do fornecedor. 

    > [!NOTE]
    > As linhas da fatura do fornecedor baseadas em uma categoria de compras não podem ser registradas no projeto. 
    
5. Adicione a quantidade comprada. O sistema preencherá o preço unitário com base na configuração de preço do item não estocado. 
6. Verifique o valor total e outros detalhes necessários na linha.
7. Nos detalhes da linha, na guia **Projeto**, selecione a ID do projeto em que este item será gravado.
8. Opcionalmente, selecione o número da atividade e atualize a categoria do projeto e a propriedade da linha.
9. Poste a fatura de fornecedor pendente. Quando a fatura for postada, o sistema registrará:
    
    - O valor do saldo do fornecedor.
    - O valor do imposto.
    - O custo do projeto é registrado na conta de integração de aquisições.
    - A transação real do projeto no Dataverse. Esta transação é posteriormente processada usando o [diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md). A postagem deste diário move o valor da conta de integração de aquisições para a conta de custo do projeto.
