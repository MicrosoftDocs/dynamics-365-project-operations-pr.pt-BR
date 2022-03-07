---
title: Gerenciar lista de pendências de cobrança
description: Este tópico fornece informações sobre como exibir e trabalhar com a lista de pendências de cobrança no Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2e839c1f32248fff6d97271796666b5031f66490ccd98574045b770100bf379f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991067"
---
# <a name="manage-billing-backlog"></a>Gerenciar lista de pendências de cobrança

_ **Aplicável a:** Project Operations para cenários baseados em recursos/sem estoque

O Dynamics 365 Project Operations tem exibições dedicadas para ajudar a gerenciar a lista de pendências de cobrança. Para gerenciar a lista de pendências de cobrança, selecione os links na área **Vendas**, em **Cobrança**. 

As seguintes exibições estão disponíveis:

- Honorários e Adiantamentos
- Adiantamentos e Honorários Disponíveis
- Etapas de Preço Fixo
- Registros Acumulados de Hora e Material

## <a name="retainers-and-advances"></a>Honorários e Adiantamentos

A exibição **Honorários e Adiantamentos** lista os honorários e adiantamentos em todos os contratos do projeto. Depois que um honorário ou adiantamento é faturado, o valor do adiantamento é disponibilizado para uso.

## <a name="available-retainers-and-advances"></a>Adiantamentos e Honorários Disponíveis

A exibição **Adiantamentos e Honorários Disponíveis** lista todos os honorários e adiantamentos em todos os contratos do projeto. Depois que um honorário ou adiantamento é faturado, o valor do adiantamento é disponibilizado para uso e é adicionado à lista. Depois que o valor do honorário ou do adiantamento é totalmente usado, ele é removido da lista.

## <a name="fixed-price-milestones"></a>Etapas de Preço Fixo

A exibição **Etapas de Preço Fixo** lista todas as etapas de preço fixo em todas as linhas de contrato do projeto. A partir desta exibição, uma ou várias etapas podem ser marcadas como **Pronto para faturamento** ou **Não pronto para faturamento**. Marcar uma etapa como **Pronto para faturamento** disponibiliza-a para ser colocada em uma fatura de rascunho.

Quando linhas de contrato de vários clientes têm um método de cobrança de preço fixo, uma etapa é criada para cada cliente na linha de contrato. Uma etapa pode ser criada e dividida em registros de etapas individuais específicos do cliente. Essa divisão é interna e segue a divisão de porcentagem de cobrança definida para cada cliente na linha do contrato. Na exibição **Etapas de Preço Fixo**, você verá os registros de etapas individuais específicos do cliente. Cada um desses registros de etapa pode ser marcado como **Pronto para Faturamento** separadamente desta exibição. Quando uma ou mais das divisões da etapa relacionada são marcadas como **Pronto para faturamento**, o status do cabeçalho será atualizado para **Em andamento** a partir de **Não Iniciado**. Quando todas as divisões da etapa são faturadas, o status da etapa do cabeçalho é atualizado para **Concluído**.

Uma etapa em uma fatura de rascunho é mostrada nesta exibição com um status de cobrança **Fatura do Cliente Criada**. Quando a fatura de rascunho é confirmada, o status da cobrança no registro é atualizado para **Fatura do Cliente Postada**. 

> [!NOTE] 
> Não atualize este valor de status usando código personalizado. O Project Operations não funciona corretamente quando esses valores de status são atualizados com código personalizado.

## <a name="time-and-material-billing-backlog"></a>Registros Acumulados de Hora e Material

A exibição **Lista de Pendências de Cobrança de Hora e Materiais** lista todos os valores reais de vendas não cobrados em todos os contratos de projeto no sistema que não foram faturados. Um ou vários dados efetivos de vendas não cobrados podem ser marcados como **Pronto para Faturamento** ou **Não Pronto para Faturamento** desta exibição. Marcar um dado efetivo de venda não cobrada como **Pronto para Faturamento** o disponibiliza para ser colocado em uma fatura de rascunho.

Dados reais não cobrados com um status **NTE (Limite Máximo)** de **Falhou** não podem ser marcados como **Pronto para Faturamento**. Se os valores reais precisarem ser marcados como **Pronto para Faturamento**, redefina o status em outros valores reais na linha do contrato que estão comprometidos e, em seguida, reavalie o status **NTE (limite máximo)**.

Se as linhas de contrato de vários clientes tiverem um método de cobrança de horas e materiais, quando a hora e as despesas forem aprovadas, um dado real de vendas não cobradas será criado para cada cliente na linha do contrato de acordo com a divisão percentual de cobrança definida para cada um dos clientes. Na exibição **Lista de Pendências de Cobrança de Hora e Materiais**, você verá esses dados reais de vendas não cobradas específicos do cliente. Cada um desses registros de dados efetivos de vendas não cobradas pode ser marcado como **Pronto para Faturamento** separadamente desta exibição.

Um valor real de vendas não faturadas que está em um rascunho de fatura é mostrado nesta exibição com um status de faturamento de **Fatura do Cliente Criada**. Quando a fatura de rascunho é confirmada, o status de cobrança neste registro é atualizado para **Fatura do Cliente**. 

> [!NOTE] 
> Não atualize este valor de status usando código personalizado. O Project Operations não funciona corretamente quando esses valores de status são atualizados com código personalizado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
