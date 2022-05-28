---
title: Gerenciar listas de preços do projeto em contratos do projeto
description: Este tópico fornece informações sobre como gerenciar listas de preços do projeto em contratos do projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ad0e260fde65cf3eb32539fbcdb7101796cb53b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600498"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Gerenciar listas de preços do projeto em contratos do projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os contratos do projeto no Dynamics 365 Project Operations são elaborados para oferecer suporte a listas de preços de venda de várias datas efetivas em um contrato. No Project Operations, há uma nova entidade associada chamada **Listas de Preços do Projeto**. Essa entidade tem um relacionamento um-para-muitos com um contrato do projeto.

As listas de preços de projetos são usadas para determinar o preço de transações de tempo, material e despesas em um projeto. Quando um contrato tem uma ou mais listas de preço de projeto, elas são usadas para definir o preço de tempo, material, estimativas de despesas e dados reais em projetos associados ao contrato por meio da linha de contrato.

Quando não há listas de preços de projeto em um contrato de projeto, verá uma mensagem de aviso de que não há listas de preços de projeto e as estimativas, o trabalho de projeto real, materiais e despesas registradas não serão precificadas. Não haverá preço para os valores de venda.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Associar ou desassociar uma lista de preços do projeto em um contrato do projeto

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Crie ou associe uma lista de preços específica para estimar o trabalho, o material e as despesas com base no projeto

1. No contrato do projeto, selecione a guia **Listas de Preços do Projeto**.
2. Na subgrade, selecione **+ Adicionar Nova Lista de Preços do Projeto**.
3. No controle deslizante **Criação Rápida**, selecione uma lista de preços. 

  A lista suspensa mostra todas as listas de preços que têm o contexto definido como **Vendas**, no qual a moeda da lista de preços corresponde à moeda do contrato.
  
4. Insira uma descrição para a associação da lista de preços do projeto, selecione **Salvar** e, em seguida, feche o controle deslizante **Criação Rápida**.

   Uma associação de lista de preço do projeto é criada.
   
5. Repita as etapas 1 a 4 para associar mais de uma lista de preços do projeto ao contrato do projeto. Crie várias listas de preços do projeto apenas se houver data de validade diferente em cada uma das listas de preços de projeto associadas.

> [!NOTE]
> O Project Operations não suporta sobreposição da data efetiva das listas de preço do projeto. Se houver várias listas de preços do projeto para uma transação com uma determinada data, o preço dessa transação será definido como zero.

### <a name="remove-a-project-price-list-association"></a>Remover uma associação da lista de preços do projeto

- Selecione a lista de preços do projeto e, em seguida, escolha **Excluir Lista de Preços do Projeto do Contrato** na subgrade. 

  A lista de preços é removida das listas de preços do projeto no contrato. A própria lista de preços não será excluída. Apenas a associação ao contrato será excluída.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Configurar padronização automática de listas de preços do projeto em um contrato

Uma lista de preços de projeto pode ser configurada como a lista de preços de projeto padrão. Esta configuração garante que todos os contratos em sua organização sempre comecem com uma lista de preços de projeto padrão para aquele período de preços.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Configure o padrão organizacional para listas de preços de projetos

1. Vá para **Configurações** > **Geral** e selecione **Parâmetros**.
2. Na página da lista **Parâmetros Ativos**, selecione e clique duas vezes no registro para abri-lo. Ao clicar duas vezes, certifique-se de não clicar em um valor de campo que seja um hiperlink. 
3. Na página **Parâmetros Ativos**, selecione a guia **Lista de Preços**. Uma subgrade mostra listas de preços padrão. Esta é uma lista de custos padrão e listas de preços de venda. Ter uma lista de preços de **Vendas** associada aqui para cada moeda em que você vende garante que a lista de preços de venda seja o padrão em qualquer contrato que você criar para clientes que realizam transações nessa moeda.

### <a name="set-up-a-customer-specific-project-price-list"></a>Configurar uma lista de preços do projeto específica do cliente

Você também pode configurar listas de preços do projeto específica do cliente quando tiver negociado um acordo principal de preços com seus clientes.

1. Vá para **Vendas** > **Clientes**.
2. Na lista de contas ativas, selecione o cliente para o qual possui uma lista de preços especial.
3. Selecione o registro do cliente para abri-lo e selecione a guia **Listas de Preços do Projeto**. Uma subgrade mostra listas de preços de projetos específicas para este cliente. 
4. Crie uma nova associação de lista de preços aqui para ter uma lista de preços de projeto específica para este cliente.

## <a name="custom-pricing-on-a-project-contract"></a>Preços personalizados em um contrato do projeto

Depois de ter listas de preços de projeto padrão organizacionais e específicas do cliente, seus contratos de projeto serão criados com essas associações de lista de preços de projeto automaticamente. No entanto, as listas de preços do projeto em um contrato do projeto são sempre copiadas com a data e o nome do contrato anexados a elas. Os gerentes de conta e de projeto podem então começar a fazer edições nos preços dessas cópias. Esses preços alterados serão aplicáveis apenas a este contrato do projeto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
