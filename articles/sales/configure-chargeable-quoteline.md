---
title: Configurar os componentes passíveis de cobrança de uma linha de cotação baseada em projeto
description: Este tópico fornece informações sobre componentes incluídos, passíveis ou não passíveis de cobrança em linhas de cotação baseadas em projeto.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 251d0013b445d2f7d17fbe1908f0db2e05cfc2670ac667deb363c98f608a2aef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003982"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Configurar os componentes passíveis de cobrança de uma linha de cotação baseada em projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Uma linha de cotação baseada em projeto pode ter componentes incluídos e componentes passíveis de cobrança.

Os componentes incluídos estão sujeitos ao método de faturamento, divisões do cliente, limites que não devem ser excedidos e configurações de frequência de fatura definidas na linha de cotação baseada em projeto.
Um subconjunto dos componentes incluídos podem ser marcados como passíveis de cobrança usando **Tipo de Cobrança**. É possível selecionar uma das seguintes opções no campo **Tipo de Cobrança** no contexto de uma linha de cotação:

   - Passível de Cobrança
   - Não Passível de Cobrança

Os componentes passíveis de cobrança podem ser definidos em funções e categorias de transação.

Os encargos definidos em funções de uma linha de cotação de projeto aplicam-se apenas à classe de transação **Hora**. Se uma linha de cotação de projeto tiver **Incluir Hora** = **Não**, a guia **Funções Passíveis de Cobrança** não estará disponível.

Os encargos definidos em categorias de transação de uma linha de cotação de projeto aplicam-se apenas à classe de transação **Despesa**. Se uma linha de cotação de projeto tiver **Incluir Despesas** = **Não**, a guia **Categorias Passíveis de Cobrança** não estará disponível.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função para passível de cobrança ou não passível de cobrança
Uma função pode ser passível ou não passível de cobrança em uma linha de cotação baseada em projeto. O tipo de cobrança em uma função pode ser configurado na guia **Funções Passíveis de Cobrança** de uma linha de cotação baseada em projeto. Para fazer isso, atualize **Tipo de Cobrança** na subgrade **Funções Passíveis de Cobrança**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação para passível de cobrança ou não passível de cobrança
Uma categoria de transação pode ser passível ou não passível de cobrança em uma linha de cotação baseada em projeto. O tipo de cobrança em uma transação pode ser configurado na guia **Categorias Passíveis de Cobrança** de uma linha de cotação baseada em projeto. Para fazer isso, atualize o campo **Tipo de Cobrança** na subgrade **Categorias Passíveis de Cobrança**. 

## <a name="resolve-chargeability"></a>Resolver os encargos

Uma estimativa ou dado real criado para a hora será considerado como passível de cobrança se a hora estiver incluída na linha de cotação e se a função estiver configurada como passível de cobrança.
Uma estimativa ou dado real criado para uma despesa será considerado como passível de cobrança se a despesa estiver incluída na linha de cotação e se a categoria de transação estiver configurada como passível de cobrança na linha de cotação. A seguinte tabela mostra como os encargos são predefinidos em cada dado real. Os padrões são baseados nos componentes incluídos e o tipo de cobrança configurado na linha de cotação.

| Inclui hora | Inclui despesa | Função | Categoria | Tarefa |
| --- | --- | --- | --- | --- |
| Sim | Sim | Passível de Cobrança | Passível de Cobrança | Cobrança em um tempo real: Passível de Cobrança </br>Tipo de cobrança em uma despesa real: Passível de Cobrança |
| Sim | Sim | Não Passível de Cobrança | Passível de Cobrança | Cobrança em um tempo real: Não Passível de Cobrança </br>Tipo de cobrança em uma despesa real: Passível de Cobrança |
| Sim | Sim | Não Passível de Cobrança | Não Passível de Cobrança | Cobrança em um tempo real: Não Passível de Cobrança </br>Tipo de cobrança em uma despesa real: Não Passível de Cobrança |
| No | Sim | Não pode ser definido | Passível de Cobrança | Cobrança em um tempo real: Não disponível </br>Tipo de cobrança em uma despesa real: Passível de Cobrança |
| No | Sim | Não pode ser definido | Não Passível de Cobrança | Cobrança em um tempo real: Não disponível </br>Tipo de cobrança em uma despesa real: Não Passível de Cobrança |
| Sim | No | Passível de Cobrança | Não pode ser definido | Cobrança em um tempo real: Passível de Cobrança </br>Tipo de cobrança em uma despesa real: Não disponível |
| Sim | No | Não Passível de Cobrança | Não pode ser definido | Cobrança em um tempo real: Não Passível de Cobrança </br> Tipo de cobrança em uma despesa real: Não disponível |


[!INCLUDE[footer-include](../includes/footer-banner.md)]