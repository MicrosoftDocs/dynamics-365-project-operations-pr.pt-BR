---
title: Gerenciar a lista de pendências de cobrança
description: Este tópico fornece informações sobre como exibir e trabalhar com a lista de pendências de cobrança no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c3752abd26e760d27320d2b86079d84a967d53cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287719"
---
# <a name="manage-the-billing-backlog"></a>Gerenciar a lista de pendências de cobrança

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations tem duas exibições dedicadas para ajudar você a usar e a gerenciar a lista de pendências de cobrança. Elas são **Etapas de preço fixo** e **Lista de pendências de cobrança de hora e materiais**. Para selecionar uma exibição, na área **Vendas** do Project Operations, na página de navegação à esquerda, selecione **Cobrança**. Os links da lista de pendências de cobrança são armazenados ali.

## <a name="fixed-price-milestones"></a>Etapas de Preço Fixo

Esta exibição lista todas as etapas de preço fixo em todas as linhas de contrato do projeto no sistema. Uma ou várias etapas podem ser marcados como **Pronto para Faturamento** ou **Não Pronto para Faturamento** desta exibição. Quando você marca uma etapa como **Pronto para Faturamento**, a etapa fica disponível para uma fatura de rascunho.

Quando as linhas de contrato de vários clientes têm um método de faturamento de preço fixo, uma etapa é criada para cada cliente na linha de contrato. O usuário cria uma etapa e essa etapa é dividida em clientes = registros de etapa específicos internamente, de acordo com a divisão percentual de faturamento definida para cada cliente na linha do contrato. Na exibição **Etapas de preço fixo**, você verá registros de etapas individuais específicas do cliente. Cada um desses registros de etapa pode ser marcado como **Pronto para Faturamento** separadamente desta exibição. Quando uma ou mais das divisões de etapa relacionadas são marcadas como **Pronto para Faturamento**, o cabeçalho muda para um status **Em Andamento** a partir de **Não Iniciado**. Quando todas as divisões de etapa tiverem sido faturadas, o status de etapa do cabeçalho se tornará **Concluído**.

Uma etapa em uma fatura de rascunho é mostrada nesta exibição com um status de cobrança **Fatura do Cliente Criada**. Quando a fatura de rascunho é confirmada, o status de cobrança neste registro é atualizado para **Fatura Postada**. Não é recomendável atualizar este valor de status usando código personalizado. O Project Operations não funcionará corretamente se esses valores de status forem atualizados com código personalizado.

## <a name="time-and-material-billing-backlog"></a>Registros Acumulados de Hora e Material

Esta exibição lista todos os dados efetivos de vendas não faturados que não foram faturados em todos os contratos de projeto no sistema. Um ou vários dados efetivos de vendas não cobrados podem ser marcados como **Pronto para Faturamento** ou **Não Pronto para Faturamento** desta exibição. Marcar um dado efetivo de venda não cobrada como **Pronto para Faturamento** o disponibiliza para ser colocado em uma fatura de rascunho.

Dados efetivos de vendas não cobradas com **Limite Máximo** com o status **Com Falha** não podem ser marcados como **Pronto para Faturamento**. Se esses dados efetivos precisarem ser marcados como tal, redefina o status em outros dados efetivos na linha do contrato que estejam comprometidos e, em seguida, avalie o status **Limite Máximo**.

No caso de linhas de contrato de vários clientes que têm um método de faturamento de tempo e material, quando o tempo e as despesas são aprovados, um dado efetivo de vendas não cobradas é criado para cada cliente na linha de contrato de acordo com a divisão percentual de faturamento definida para cada cliente no linha de contrato. Na exibição **Lista de pendências de cobrança de hora e materiais**, você verá esses dados efetivos individuais de vendas não cobradas específicas do cliente. Cada um desses registros de dados efetivos de vendas não cobradas pode ser marcado como **Pronto para Faturamento** separadamente desta exibição.

Um dado efetivo de vendas não cobradas em uma fatura de rascunho é mostrado nesta exibição com um **Status de Cobrança** de **Fatura do Cliente Criada**. Quando a fatura de rascunho é confirmada, o status de cobrança neste registro é atualizado para **Fatura do Cliente**. Não é recomendável atualizar este valor de status, quando ele está neste estado, usando código personalizado. O Project Operations não funcionará corretamente quando esses valores de status forem atualizados com código personalizado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]