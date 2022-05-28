---
title: Configurar componentes passíveis de uma linha de contrato do projeto
description: Este tópico fornece informações sobre componentes incluídos, passíveis de cobrança e não passíveis de cobrança nas linhas do contrato.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bd419e189cd063f1cb2a1f0ecd3cd6450de0996b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586606"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Configurar componentes passíveis de uma linha de contrato do projeto

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Uma linha de contrato com base em projeto tem o conceito de componentes incluídos, passíveis de cobrança e não passíveis de cobrança.

Os componentes incluídos estão sujeitos ao método de cobrança, divisões do cliente, limites que não devem ser excedidos e configurações de frequência de fatura definidas na linha do contrato com base no projeto.

Um subconjunto dos componentes incluídos pode ser marcado como passível de cobrança atualizando o campo **Tipo de Cobrança**.

Os componentes passíveis de cobrança podem ser definidos em funções e categorias de transação.

Para uma linha de contrato de projeto, os encargos definidos em uma função só se aplica à classe de transação **Tempo**. Se **Incluir Tempo** estiver configurado como **Não** em uma linha de contrato de projeto, a guia **Funções passíveis de cobrança** não estará disponível.

Os encargos são definidos em categorias de transação para uma linha de contrato do projeto e só se aplicam à classe de transação **Despesa**. Se **Incluir Despesas** estiver configurado como **Não** em uma linha de contrato de projeto, a guia **Categorias Passíveis de Cobrança** não estará disponível.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função para passível de cobrança ou não passível de cobrança

Uma função pode ser passível de cobrança ou não passível de cobrança em linha de contrato com base em projeto específica.

Na guia **Funções passíveis de cobrança** de uma linha de contrato baseada no projeto, na subgrade **Categorias Passíveis de Cobrança**, no campo **Tipo de Faturamento**, atualize o tipo de faturamento de uma função.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação para passível de cobrança ou não passível de cobrança

Uma categoria de transação pode ser passível de cobrança ou não passível de cobrança em uma linha de contrato com base em projeto específica.

Na guia **Categorias Passíveis de Cobrança** de uma linha de contrato baseada no projeto, na subgrade **Categorias Passíveis de Cobrança** no campo **Tipo de Faturamento**, atualize o tipo de faturamento de uma transação.

### <a name="resolve-chargeability"></a>Resolver os encargos

Uma estimativa ou real criado para o tempo só será considerado passível de cobrança se o tempo estiver incluído na linha do contrato e se a função for configurada como passível de cobrança na linha do contrato.

Uma estimativa ou real criado para despesa só será considerado passível de cobrança se a despesa estiver incluída na linha do contrato e se a categoria de transação for configurada como passível de cobrança na linha do contrato.

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
