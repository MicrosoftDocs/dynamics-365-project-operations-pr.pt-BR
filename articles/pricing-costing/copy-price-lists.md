---
title: Copiar listas de preços
description: Este tópico fornece informações sobre como copiar listas de preços no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67a69d521ac0a5632371138bd4fbb9dd00fe34ee
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181483"
---
# <a name="copy-price-lists"></a>Copiar listas de preços

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Você pode criar cópias de listas de preços no Dynamics 365 Project Operations. Por exemplo, você pode criar listas de preços para o próximo ano usando uma lista de preços do ano atual.  Ou você pode copiar uma lista de preços para taxas de fatura e preços de venda das listas de preços para custo. 

Para fazer uma cópia da lista de preços, conclua as etapas a seguir.

1. Abra a lista de preços da qual deseja fazer uma cópia e selecione **Copiar**.
2. Insira todas as informações necessárias para copiar a lista de preços. A tabela a seguir mostra as considerações a serem observadas ao inserir informações.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| Nome | O nome da lista de preços de origem com **-copy** acrescentado. | A lista de preços inclui esse valor em todas as páginas de listagem e opções de lista suspensa. |
| Contexto | Insira o contexto que deseja para a lista de preços de destino. | Uma lista de preços com o contexto definido como **Custo** é usada para consultar o preço de estimativas e dados reais de custo. Uma lista de preços com o contexto definido como **Vendas** é usada para consultar o preço de estimativas e dados reais de venda. Somente as listas de preços cujo contexto está definido como **Vendas** podem ser anexadas a uma lista de preços de projeto para um cliente, cotações ou contrato. |
| Data de Início | A data de início do período em que a lista de preços entra em vigor. | Junto com **Data de Término**, esse campo será usado para determinar qual lista de preços é aplicável a determinada estimativa ou linha de dados reais. |
| Data de Término | A data de término do período em que a lista de preços entra em vigor. | Junto com **Data de Início**, esse campo será usado para determinar qual lista de preços é aplicável a determinada estimativa ou linha de dados reais. |
| Moeda | A moeda da lista de preços de origem. Isso pode ser alterado. | Quando isso é alterado, todas as linhas de preços resultantes para itens de mão de obra, despesas e itens do catálogo de produtos são convertidas na moeda da lista de preços de destino durante a cópia. |
| Unidade de Tempo | A moeda da lista de preços de origem. Isso pode ser alterado. | Quando isso é alterado, todas as linhas de preços resultantes para itens de mão de obra são convertidos na unidade da lista de preços de destino durante a cópia. A conversão da configuração da unidade para a unidade de tempo da lista de preços de origem e a unidade de tempo da lista de preços de destino é usada. |
| Descrição | Uma descrição da lista de preços de origem com **-copy** acrescentado. É um campo de texto e permite que você tenha uma descrição de várias linhas da lista de preços. | Esse campo é mostrado nas exibições **Associadas** na lista de preços em várias entidades que possuem listas de preços relacionadas. |

3. Salve a lista de preços. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Atualizar uma lista de preços aplicando uma marcação a todos os preços

1. Nas guias **Função**, **Categoria** e **Item da Lista de Preços** de uma lista de preços, é possível selecionar **Atualizar Preços** para aplicar uma marcação a todos os preços na subgrade. 
2. Na página de diálogo aberta, insira uma marcação. Você também pode inserir uma porcentagem de marcação negativa para diminuir os preços em uma determinada porcentagem. 
3. Selecione **OK** na página de diálogo e, em seguida, verifique se os preços na subgrade refletem as alterações feitas.
