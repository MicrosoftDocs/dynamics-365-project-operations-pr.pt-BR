---
title: Gerenciar listas de preços de projeto em cotações de projeto - lite
description: Este tópico fornece informações sobre como trabalhar com listas de preço do projeto em cotações. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d48da44f382e329a978a8ceee59c354d009f2114
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273004"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Gerenciar listas de preços de projeto em cotações de projeto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

As cotações do projeto são desenvolvidas para oferecer suporte a listas de preços de venda com várias datas de vigência. Com o Dynamics 365 Project Operations, uma nova entidade associada chamada **Listas de preços do projeto** é adicionada. Esta entidade tem um relacionamento de 1 para muitos com uma cotação de projeto.

As listas de preços do projeto são usadas para definir o preço das transações de tempo e despesas em um projeto. Quando uma cotação tem uma ou mais listas de preços de projeto, essas listas de preços são usadas para definir o preço de estimativas de tempo e despesas e dados efetivos em projetos que estejam associados à cotação por meio da linha de cotação.

Quando não houver listas de preços de projeto em uma cotação de projeto, você receberá uma mensagem de aviso. A mensagem informa que, como não há listas de preços do projeto, o trabalho e as despesas estimados e reais do projeto não serão avaliados. Em vez disso, eles terão preço zero (0) para os valores de venda.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Associar ou desassociar uma lista de preços de projeto em uma cotação de projeto

Para criar ou selecionar uma lista de preços específica para estimar o trabalho e despesas baseadas no projeto, conclua as seguintes etapas.

1. Na cotação, selecione a guia **Preço do projeto** e, na subgrade, selecione **+ Adicionar nova lista de preços de projeto**.
2. Na página de criação rápida, selecione uma lista de preços. A lista suspensa mostra todas as listas de preços que têm o contexto definido como **Vendas** e a moeda corresponde à moeda da cotação.
4. Insira uma descrição para a associação da lista de preços do projeto e selecione **Salvar e fechar**.

Uma associação de lista de preço do projeto é criada.

Você pode repetir este processo se precisar associar mais de uma lista de preços do projeto à cotação do projeto. Crie várias listas de preços do projeto apenas se houver datas de vigência diferentes em cada uma das listas de preços do projeto associadas.

> [!NOTE]
> O Project Operations não é compatível com sobreposição da efetividade de data das listas de preços do projeto. Se houver várias listas de preços de projeto para uma transação com determinada data, o preço dessa transação será definido como zero (0).
Para remover uma associação de lista de preços do projeto, selecione a lista de preços do projeto e selecione **Excluir lista de preços do projeto da cotação**. A lista de preços é removida das listas de preços do projeto da cotação, mas a própria lista de preços não é excluída. Apenas a associação à cotação é excluída.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Configure listas de preços de projeto padrão em uma cotação

As listas de preços do projeto podem ser configuradas como padrão em uma cotação do projeto. Essa configuração garante que todas as cotações em sua organização sempre comecem com uma lista de preços padrão para aquele período de preços.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Configurar padrão organizacional para listas de preço do projeto

1. Vá para **Configurações** > **Geral** > **Parâmetros**.
2. Na página da lista **Parâmetros ativos**, localize o registro e clique duas vezes para abri-lo. 
3. Na página **Parâmetros**, selecione a guia **Lista de preços**. Você pode ver que a lista de listas de preços padrão é exibida. Esta é uma lista de custos padrão e listas de preços de venda. Ao ter uma lista de preços de venda associada aqui para cada moeda em que você vende, você garantirá que essa lista de preços de venda seja padronizada em qualquer cotação que você criar para clientes que realizem transações nessa moeda.

### <a name="set-up-customer-specific-project-price-lists"></a>Configure listas de preços do projeto específicas do cliente

As listas de preços do projeto específicas do cliente também podem ser configuradas quando você negociar um contrato de preços principal com seus clientes.

Para configurar uma lista de preços do projeto específica do cliente, conclua as etapas a seguir.

1. Na area **Vendas**, selecione **Clientes**.
2. Na lista de suas contas ativas, selecione e abra o registro do cliente para o qual você possui uma lista de preços especial.
3. Na guia **Listas de preços do projeto**, você pode criar uma nova associação de lista de preços para ter a lista de preços do projeto que é específica para este cliente.

## <a name="create-custom-pricing-on-a-project-quote"></a>Criar preços personalizados em uma cotação de projeto

Depois de ter listas de preços de projeto padrão organizacionais e específicas do cliente, suas cotações de projeto serão criadas automaticamente com essas associações de lista de preços do projeto. No entanto, em certos casos, talvez você precise criar preços personalizados para uma cotação de projeto específica. 

1. Em **Cotação de projeto**, na guia **Lista de preços do projeto**, verifique na subrade se nenhum registro específico da lista de preços está selecionado.
2. Selecione **Criar preços personalizados**. Isso fará cópias de todas as listas de preços padrão atualmente associadas à cotação e associará essas cópias à cotação. As atuais associações a listas de preços padrão serão removidas. O vendedor pode então começar a fazer edições nos preços dessas cópias. Esses preços alterados serão aplicáveis apenas a esta cotação de projeto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]