---
title: Requisições de viagem
description: Este tópico fornece informações sobre requisições de viagem.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f00b5ca2142c4ba5cb523773f1f6dd8f0a055f6f6d474bc2b8e5f775ca0fc739
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994532"
---
# <a name="travel-requisitions"></a>Requisições de viagem

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Uma requisição de viagem lista as despesas que serão incorridas com a finalidade de viagem. Uma requisição de viagem é enviada para análise e pode ser usada para autorizar despesas.

É necessário enviar uma requisição de viagem antes de incorrer em qualquer despesa que será cobrada da organização. Essa obrigação se aplica independentemente de você debitar despesas em um cartão de crédito corporativo, gastar dinheiro que recebeu de um adiantamento ou incorrer em despesas do próprio bolso que serão reembolsadas pela organização.

As requisições e políticas de viagens podem ser usadas para ajudar a gerenciar os gastos da organização. Por exemplo, se a sua organização está trabalhando em um projeto de preço fixo que exige viagens, as despesas de viagem dos membros da equipe do projeto deverão ser incluídas no orçamento do projeto. Ao exigir que as despesas de viagem sejam aprovadas antes de acontecerem, a organização pode ajudar a garantir que o projeto permaneça dentro do orçamento.

## <a name="configuration"></a>Configuração 

As requisições de viagem podem ser configuradas como "obrigatórias" ao habilitar o parâmetro "A pré-autorização da viagem é obrigatória" nos Parâmetros de gerenciamento de despesas. 

## <a name="create-and-submit-a-travel-requisition"></a>Criar e enviar uma requisição de viagem

1. Acesse **Minhas despesas: Requisição de Viagem** e selecione **Nova Requisição de viagem**.
2. Insira uma finalidade e um destino para a requisição.
3. No campo **Descrição da viagem**, insira qualquer informação adicional. 
4. Para cada uma das despesas esperadas, como voo, refeições ou aluguel de carro, crie um item de linha de despesas. Inclua a data estimada, o valor estimado e a moeda de cada despesa. 
5. Quando terminar de adicionar as despesas esperadas, selecione **Salvar**.
6. Quando você estiver pronto para enviar a requisição de viagem, selecione **Fluxo de Trabalho** > **Enviar**.

Você pode exibir suas requisições de viagem aprovadas em **Minhas Despesas: Requisição de Viagem**. 

## <a name="view-available-travel-requisitions"></a>Exibir requisições de viagens disponíveis

Você pode exibir todas as suas requisições de viagem em **Minhas Despesas: Requisições de Viagem**.

## <a name="approve-travel-requisitions"></a>Aprovar requisições de viagem

Selecione a requisição de viagem que deseja aprovar e, em seguida, selecione **Fluxo de Trabalho** > **Aprovar**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Envie um relatório de despesas usando sua requisição de viagem aprovada

1. Crie um novo relatório de despesas e no cabeçalho dele, na lista de requisições de viagem aprovadas, selecione **Mapear para Requisição de viagem**.
2. O campo **Valor da requisição de viagem** é atualizado automaticamente no cabeçalho do relatório de despesas.
3. Adicione cada despesa incorrida para a viagem. Se o campo **Pré-autorizado** estiver habilitado, o valor reconciliado e o valor autorizado para a categoria de despesas específica serão atualizados.

> [!NOTE]
> Quando você mapeia um relatório de despesas para uma requisição de viagem aprovada, o valor da transação não pode ser maior do que o valor autorizado. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]