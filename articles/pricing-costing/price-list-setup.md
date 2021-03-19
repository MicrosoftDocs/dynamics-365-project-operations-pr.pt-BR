---
title: Configurar listas de preços
description: Este tópico fornece informações sobre como configurar listas de preços de venda e de custo.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 34ee7bb157426507ec7ca8c031f5cb552e85099b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275479"
---
# <a name="set-up-price-lists"></a>Configurar listas de preços

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As listas de preços no Dynamics 365 Project Operations representam um catálogo de taxas. As taxas expressam custos, vendas e taxas de cobranças. Se a lista de preços expressar taxas de custo ou taxas de vendas e cobranças, o contexto da lista de preços será **Vendas** ou **Custo**.

As extensões a seguir são específicas do Project Operations e são aplicadas a listas de preços do Dynamics 365 Sales.

- **Contexto**: este campo tem os valores compatíveis **Custo** e **Vendas**. O valor **Compra** não é compatível. Defina o contexto como **Custo** para criar uma lista de preços de custo ou definir o contexto **Vendas** para uma lista de preços de venda. As listas de preços de custo resolvem o preço do tipo de custo em registros de estimativa e dados reais. As listas de preços de venda resolvem o preço em registros estimados e de dados reais de tipos de vendas faturadas e não faturadas.
- **Unidade de tempo**: esta é a unidade de tempo padrão do preço configurado na tabela **Preço da Função** relacionada para essa lista de preços.
- **Entidade da Lista de Preços**: este é o campo oculto pelo Project Operations para diferenciar listas de preços específicas para cotações ou contratos daquelas que são padrão e globalmente aplicáveis.

## <a name="price-list-header"></a>Cabeçalho da lista de preços

A tabela a seguir inclui os campos na guia **Geral** de uma lista de preços que é exclusiva do Project Operations ou contém alterações significativas no comportamento de listas de preços em Vendas.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Nome | Guia **Geral** e formulários de **Criação Rápida** | A entidade da lista de preços. | A lista de preços é exibida com esse valor em todas as páginas da lista e opções suspensas.|
| Contexto | Guia **Geral** e formulários de **Criação Rápida** | Este campo pode ser definido como **Custo** ou **Vendas**. | Uma lista de preços definida como **Custo** é usada para consultar o preço de estimativas e dados reais de custo. Uma lista de preços definida como **Vendas** é usada para consultar o preço de estimativas e dados reais de venda. Somente as listas de preços cujo contexto está definido como **Vendas** podem ser anexadas a listas de preços do projeto para clientes, cotações do projeto e contratos do projeto. |
| Data de Início | Guia **Geral** e formulários de **Criação Rápida** | A data de início do período em que a lista de preços entra em vigor. | Com o campo **Data de Término**, esse campo será usado para determinar qual lista de preços é aplicável a determinada estimativa ou linha de dados reais. |
| Data de Término | Guia **Geral** e formulários de **Criação Rápida** | A data de término do período em que a lista de preços entra em vigor. | Com o campo **Data de Início**, esse campo será usado para determinar qual lista de preços é aplicável a determinada estimativa ou linha de dados reais. |
| Moeda | Guia **Geral** e formulários de **Criação Rápida** | Este campo é usado para definir a moeda como padrão em cada função, categoria ou linha de item da lista de preços relacionada a essa lista de preços. | Nas listas de preços de **Vendas**, as funções, categorias ou linhas do item da lista de preços não podem ser criadas em outra moeda. Nas listas de preços de **Custo**, é possível criar uma linha de preço de função em qualquer moeda. A moeda definida aqui é usada como padrão. A configuração do usuário relacionada aos preços da função pode substituir esse valor para permitir a configuração da taxa de custo de mão de obra em qualquer moeda. As taxas de custo da categoria e os custos do item da lista de preços podem ser configurados apenas na moeda definida aqui. |
| Unidade de Tempo | Guia **Geral** e formulários de **Criação Rápida** | Este campo é usado para definir a unidade de tempo como padrão em cada linha de função relacionada a essa lista de preços. | O valor deste campo é usado apenas na configuração de preço da função relacionada. Nas listas de preços de **Custo** e **Vendas**, é possível criar uma linha de preço de função em qualquer unidade de tempo. A unidade de tempo definida aqui é usada como padrão. A configuração do usuário relacionada aos preços da função pode substituir esse valor para permitir a configuração da taxa de custo e de cobrança de mão de obra em qualquer unidade de tempo. |
| Descrição | Guia **Geral** e formulários de **Criação Rápida** | Este campo permite fornecer uma descrição de várias linhas da lista de preços. | Esse campo é mostrado nas exibições **Associadas** na lista de preços em várias entidades que possuem listas de preços relacionadas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]