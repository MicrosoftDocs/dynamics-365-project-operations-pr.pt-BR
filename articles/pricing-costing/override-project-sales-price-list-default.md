---
title: Substituir listas de preços de vendas do projeto
description: Este tópico fornece informações sobre a criação de listas de preços de venda personalizadas.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672217"
---
# <a name="override-project-sales-price-lists"></a>Substituir listas de preços de vendas do projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

## <a name="customer-specific-project-price-lists"></a>Listas de preços de projetos específicas do cliente

Os contratos de preços específicos do cliente podem ser configurados como listas de preços do projeto em um registro da conta no Dynamics 365 Project Operations.

Para configurar uma lista de preços de projeto específica do cliente, na área **Vendas**, navegue até o registro da conta.

1. Abra a página de lista **Contas**.
2. Localize e clique duas vezes em um registro de cliente para abrir a página de detalhes da **Conta**.
3. Na guia **Listas de Preços do projeto**, selecione **+ Nova Lista de Preços do Projeto**.
4. Na página **Nova Lista de Preços do Projeto**, selecione uma lista de preços da lista suspensa. Apenas listas de preços que têm o contexto definido como **Vendas** e cuja moeda corresponda à moeda da conta estão incluídas.
5. Nomeie a associação e selecione **Salvar**. Uma lista de preços de projetos específicas do cliente será criada. Esta lista de preços será usada para definir preços de projeto padrão em cotações de projeto ou contratos criados para este cliente, onde a data de criação da cotação ou do contrato do projeto está dentro da data efetiva da lista de preços.

## <a name="custom-pricing-on-project-quotes"></a>Preços personalizados nas cotações do projeto

Nas cotações do projeto, você pode ter o preço do projeto que começa com uma lista de preços padrão do cliente ou dos parâmetros do projeto.

Quando você precisar de preços personalizados para o trabalho relacionado ao projeto em uma cotação específica, poderá obtê-los na entidade associada às listas de preços do projeto.

Conclua as etapas a seguir para configurar o preço de projeto específico da cotação.

1. Abra a cotação do projeto e selecione a guia **Listas de Preços do Projeto**.
2. Na subgrade, selecione **Criar precificação personalizada**.

Todas as listas de preços do projeto anexadas à cotação são copiadas para novas listas de preços. Os nomes das novas listas de preços refletem o nome da cotação com um carimbo de data e hora para quando essas listas de preços foram criadas.

Você pode usar cada uma dessas listas de preços e fazer atualizações nos preços de mão de obra (preço da função) e despesas (preço da categoria). Esses preços serão aplicáveis apenas a esta cotação de projeto.

## <a name="price-lists-on-a-project-contract"></a>Listas de preços em um contrato do projeto

Em um contrato do projeto, o preço do projeto sempre é padronizado como uma lista de preços personalizada com o nome do contrato e o carimbo de data/hora de criação anexado ao nome. Isso ocorre se o contrato foi criado quando a cotação foi ganha ou se o contrato foi criado do zero. Se necessário, você pode remover essa associação à lista de preços personalizada e associar uma lista de preços padrão ao contrato do projeto.

Quando você associa uma lista de preços padrão às listas de preços do projeto na cotação ou contrato, quaisquer alterações feitas nos preços na lista de preços afetarão todas as cotações e contratos que usam a lista de preços.