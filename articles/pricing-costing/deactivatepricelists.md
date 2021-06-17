---
title: Desativar listas de preços
description: Este tópico explica como desativar ou remover listas de preços antigas ou não utilizadas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001322"
---
# <a name="deactivate-price-lists"></a>Desativar listas de preços 

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Para remover listas de preços antigas ou não utilizadas do Dynamics 365 Project Operations, há duas etapas que você deve concluir. 

1. Remova ou exclua a lista de preços de páginas específicas.
2. Desative ou exclua a lista de preços das listas de preços ativas na página **Lista de Preços**.

>[!IMPORTANT]
> Você deve concluir as duas etapas para remover totalmente uma lista de preços. Apenas executar a etapa 2, que é excluir ou desativar diretamente a lista de preços da exibição Listas de Preços Ativas, não é suficiente. Você também deve excluir a associação desta lista de preços de todos os locais mencionados na etapa 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Exclua a lista de preços de páginas específicas
1. Para excluir uma lista de preços do Project Operations, vá para as seguintes páginas:  

      - Página **Parâmetros do projeto** > guia **Listas de Preços**
      - Página **Unidade Organizacional** > grade **Listas de Preços**
      - Página **Conta** > grade **Listas de Preços do Projeto**
      - Página **Cotações do Projeto** > grade **Listas de Preços do Projeto**: Isso se aplica a todas as cotações de projetos ativos.
      - Página **Contratos do Projeto** > grade **Listas de Preços do Projeto**: Isso se aplica a todos os contratos de projetos ativos.

 2. Para cada página, você precisa selecionar a lista de preços que deseja excluir e, em seguida, selecionar **Excluir**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Exclua ou desativa a lista de preços da página Listas de Preços
 
1. Para excluir uma lista de preços das listas de preços ativas, vá para **Vendas** > **Clientes** > **Lista de Preços**. 
2. Selecione a lista de preços que deseja excluir e escolha **Excluir**. Se a lista de preços for referenciada em qualquer transação existente, você não poderá excluí-la. Se isso acontecer, você pode desativar a lista de preços para que ela não apareça em nenhuma visualização. 
3. Para desativar a lista de preços, selecione a lista de preços novamente e escolha **Desativar**.   
