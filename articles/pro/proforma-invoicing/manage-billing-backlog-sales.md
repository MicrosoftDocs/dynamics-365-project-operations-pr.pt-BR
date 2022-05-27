---
title: Gerenciar lista de pendências de cobrança do projeto
description: Este tópico fornece informações sobre as várias visualizações disponíveis para uso ao gerenciar o backlog de cobrança em projetos.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3a90d50fcca8824db10594352cbd1e204665c53
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578127"
---
# <a name="manage-project-billing-backlog"></a>Gerenciar lista de pendências de cobrança do projeto 

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

O Dynamics 365 Project Operations tem exibições dedicadas para ajudar a gerenciar a lista de pendências de cobrança. Para gerenciar a lista de pendências de cobrança, selecione os links na área **Vendas**, em **Cobrança**. 

As seguintes exibições estão disponíveis:

- Honorários e Adiantamentos
- Adiantamentos e Honorários Disponíveis
- Etapas de Preço Fixo
- Registros Acumulados de Cobrança de Produtos
- Registros Acumulados de Hora e Material

## <a name="retainers-and-advances"></a>Honorários e Adiantamentos

A exibição **Honorários e Adiantamentos** lista todos os honorários e adiantamentos em todos os contratos de projeto no sistema. Depois que um honorário ou adiantamento é faturado, o valor do adiantamento é disponibilizado para uso.

## <a name="available-retainers-and-advances"></a>Adiantamentos e Honorários Disponíveis

A exibição **Honorários e Adiantamentos Disponíveis** lista todos os honorários e adiantamentos disponíveis em todos os contratos de projeto no sistema. Depois que um honorário ou adiantamento é faturado, o valor do adiantamento é disponibilizado para uso e é adicionado à lista. Depois que o valor do honorário ou adiantamento for totalmente usado, ele será removido da lista.

## <a name="fixed-price-milestones"></a>Etapas de Preço Fixo

A exibição **Etapas de Preço Fixo** lista todas as etapas de preço fixo em todas as linhas de contrato do projeto no sistema. Uma ou várias etapas podem ser marcadas como **Pronto para faturamento** ou **Não pronto para faturamento** desta exibição. Marcar uma etapa como **Pronto para faturamento** disponibiliza-a para ser colocada em uma fatura de rascunho.

Quando linhas de contrato de vários clientes têm um método de cobrança de preço fixo, uma etapa é criada para cada cliente na linha de contrato. Uma etapa pode ser criada e dividida em registros de etapas individuais específicos do cliente. Essa divisão é interna e segue a divisão de porcentagem de cobrança definida para cada cliente na linha do contrato. Na exibição **Etapas de Preço Fixo**, você verá os registros de etapas individuais específicos do cliente. Cada um desses registros de etapa pode ser marcado como **Pronto para Faturamento** separadamente desta exibição. Quando uma ou mais das divisões de etapas relacionadas são marcadas como **Pronto para Faturamento**, o status do cabeçalho é atualizado para **Em Progresso** de **Não Iniciado**. Quando todas as divisões de etapas são faturadas, o status de etapa do cabeçalho é atualizado para **Concluído**.

Uma etapa em uma fatura de rascunho é mostrada nesta exibição com um status de cobrança **Fatura do Cliente Criada**. Quando a fatura de rascunho é confirmada, o status da cobrança no registro é atualizado para **Fatura do Cliente Postada**. Não atualize este valor de status usando código personalizado. O Project Operations não funciona corretamente quando esses valores de status são atualizados com código personalizado.

## <a name="product-billing-backlog"></a>Registros Acumulados de Cobrança de Produtos

A exibição **Lista de Pendências de Cobrança do Produto** lista todas as linhas de contrato baseadas em produto em todos os contratos de projeto no sistema. Uma ou várias linhas de contrato baseadas em produto podem ser marcadas como **Pronto para Faturamento** ou **Não Pronto para Faturamento** desta exibição. Marcar uma linha de contrato baseada em produto como **Pronto para Faturamento** disponibiliza-a para ser colocada em uma fatura de rascunho.

Uma linha de contrato baseada em produto que está em uma fatura de rascunho é mostrada nesta exibição com um status de cobrança **Fatura do Cliente Criada**. Quando a fatura de rascunho é confirmada, o status de cobrança neste registro é atualizado para **Fatura do Cliente**. Não atualize este valor de status usando código personalizado. O Project Operations não funciona corretamente quando esses valores de status são atualizados com código personalizado.

## <a name="time-and-material-billing-backlog"></a>Registros Acumulados de Hora e Material

A exibição **Lista de Pendências de Cobrança de Hora e Materiais** lista todos os valores reais de vendas não cobrados em todos os contratos de projeto no sistema que não foram faturados. Um ou vários dados efetivos de vendas não cobrados podem ser marcados como **Pronto para Faturamento** ou **Não Pronto para Faturamento** desta exibição. Marcar um dado efetivo de venda não cobrada como **Pronto para Faturamento** o disponibiliza para ser colocado em uma fatura de rascunho.

Dados reais não cobrados com um status **NTE (Limite Máximo)** de **Falhou** não podem ser marcados como **Pronto para Faturamento**. Se for necessário marcar os dados reais como **Pronto para Faturamento**, redefina o status em outros dados reais na linha do contrato que foram confirmados. Depois, reavalie o status **NTE (limite máximo)**.

Se as linhas de contrato de vários clientes tiverem um método de cobrança de horas e materiais, quando a hora e as despesas forem aprovadas, um dado real de vendas não cobradas será criado para cada cliente na linha do contrato de acordo com a divisão percentual de cobrança definida para cada um dos clientes. Na exibição **Lista de Pendências de Cobrança de Hora e Materiais**, você verá esses dados reais de vendas não cobradas específicos do cliente. Cada um desses registros de dados efetivos de vendas não cobradas pode ser marcado como **Pronto para Faturamento** separadamente desta exibição.

Um dado real de vendas não cobradas que está em uma fatura de rascunho é mostrado nesta exibição com um status de cobrança **Fatura do Cliente Criada**. Quando a fatura de rascunho é confirmada, o status de cobrança neste registro é atualizado para **Fatura do Cliente**. Não atualize este valor de status usando código personalizado. O Project Operations não funciona corretamente quando esses valores de status são atualizados com código personalizado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
