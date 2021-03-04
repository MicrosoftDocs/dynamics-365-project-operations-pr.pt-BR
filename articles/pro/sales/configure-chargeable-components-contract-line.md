---
title: Configurar componentes passíveis de cobrança de uma linha de contrato baseada em projeto - lite
description: Este tópico fornece informações sobre como adicionar componentes passíveis de cobrança às linhas de contrato no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513865"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Configurar componentes passíveis de cobrança de uma linha de contrato baseada em projeto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Uma linha de contrato com base em projeto tem componentes *incluídos* e componentes *passíveis de cobrança*.

Os componentes incluídos são componentes que estão sujeitos a:

  - Método de cobrança e divisões do cliente
  - Limites máximos 
  - Configurações de frequência de fatura definidas na linha de contrato com base em projeto

Um subconjunto dos componentes incluídos pode ser marcado como cobrável usando o campo **Tipo de Cobrança**. O campo **Tipo de Cobrança** é um conjunto de opções que permite os seguintes valores no contexto de uma linha de contrato:

  - Passível de Cobrança
  - Não Passível de Cobrança

Os componentes passíveis de cobrança podem ser definidos em tarefas, funções e categorias de transação.

Os encargos são definidos nas tarefas para uma linha de contrato do projeto e se aplicam a todas as classes de transação incluídas na linha. Se o campo **Incluir Tarefas** em uma linha de contrato estiver em branco ou definido como **Projeto inteiro**, a guia **Tarefas passíveis de cobrança** não estará disponível.

Os encargos definidos em funções para uma linha de contrato do projeto só se aplicam à classe de transação **Tempo**. Se o campo **Incluir Tempo** em uma linha de contrato estiver definido como **Não**, a guia **Funções passíveis de cobrança** não estará disponível.

Os encargos são definidos em categorias de transação para uma linha de contrato do projeto e só se aplicam à classe de transação **Despesa**. Se o campo **Incluir Despesas** estiver definido como **Não**, a guia **Categorias Passíveis de Cobrança** não estará disponível.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Atualizar uma tarefa de projeto como passível de cobrança ou não passível de cobrança

Uma tarefa de projeto pode ser passível de cobrança ou não passível de cobrança em uma linha de contrato específica, o que torna possível a seguinte configuração:

Se uma linha de contrato com base em projeto incluir **Tempo** e uma determinada tarefa, **T1** estará associado a ela como passível de cobrança. Se houver uma segunda linha de contrato que inclua **Despesa**, você poderá associar a tarefa T1 na linha de contrato como não passível de cobrança. O resultado é que todo o tempo registrado na tarefa é passível de cobrança e todas as despesas não são passíveis de cobrança.

O tipo de faturamento de uma tarefa pode ser configurado na guia **Tarefas Passíveis de Cobrança** da linha do contrato atualizando o campo **Tipo de Cobrança** na subgrade de tarefas da linha do contrato. Como alternativa, você pode atualizar o campo **Tipo de Cobrança** na subgrade da tarefa Configuração de Faturamento de um projeto que mostra as linhas de contrato associadas a uma tarefa.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Atualizar uma função como passível de cobrança ou não passível de cobrança

Uma função pode ser passível de cobrança ou não passível de cobrança em uma linha de contrato específica.

O tipo de cobrança de uma função pode ser configurado na guia **Funções Passíveis de Cobrança** de uma linha de contrato. Para fazer isso, atualize o campo **Tipo de Cobrança** na subgrade **Funções Passíveis de Cobrança**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação como passível de cobrança ou não passível de cobrança

Uma categoria de transação pode ser passível de cobrança ou não passível de cobrança em uma linha de contrato específica.

O tipo de cobrança de uma transação pode ser configurado na guia **Categorias Passíveis de Cobrança** de uma linha de contrato com base em projeto. Para fazer isso, atualize o campo **Tipo de Cobrança** na subgrade **Categorias Passíveis de Cobrança**.

### <a name="resolve-chargeability"></a>Resolver os encargos

Uma estimativa ou real criado para o tempo só será considerada passível de cobrança se **Tempo** estiver incluído na linha de contrato e se **Tarefa** e **Função** estiverem configuradas como passíveis de cobrança na linha de contrato.

Uma estimativa ou real criado para despesa só será considerado passível de cobrança se **Despesa** estiver incluída na linha de contrato e se as categorias **Tarefa** e **Transação** estiverem configuradas como passíveis de cobrança na linha de contrato.


| Inclui Tempo | Inclui Despesa | Inclui Tarefas | Função           | Categoria       | Tarefa                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Sim           | Sim              | Projeto inteiro | Passível de Cobrança     | Passível de Cobrança     | Cobrança em um Tempo real: **Passível de Cobrança** </br> Tipo de cobrança em Despesa real: **Passível de Cobrança**           |
| Sim           | Sim              | Tarefas selecionadas | Passível de Cobrança     | Passível de Cobrança     | Cobrança em um Tempo real: **Passível de Cobrança** </br> Tipo de cobrança em Despesa real: **Passível de Cobrança**           |
| Sim           | Sim              | Tarefas selecionadas | Não Passível de Cobrança | Passível de Cobrança     | Cobrança em um Tempo real: **Não Passível de Cobrança** </br> Tipo de cobrança em Despesa real: **Passível de Cobrança**       |
| Sim           | Sim              | Tarefas selecionadas | Passível de Cobrança     | Passível de Cobrança     | Cobrança em um Tempo real: **Não Passível de Cobrança** </br> Tipo de cobrança em Despesa real: **Não Passível de Cobrança** |
| Sim           | Sim              | Tarefas selecionadas | Não Passível de Cobrança | Passível de Cobrança     | Cobrança em um Tempo real: **Não Passível de Cobrança** </br> Tipo de cobrança em Despesa real: **Não Passível de Cobrança** |
| Sim           | Sim              | Tarefas selecionadas | Não Passível de Cobrança | Não Passível de Cobrança | Cobrança em um Tempo real: **Não Passível de Cobrança** </br> Tipo de cobrança em Despesa real: **Não Passível de Cobrança** |
| No            | Sim              | Projeto inteiro | Não pode ser definido   | Passível de Cobrança     | Cobrança em um Tempo real: **Não disponível**</br>Tipo de cobrança em Despesa real: **Passível de Cobrança**          |
| No            | Sim              | Projeto inteiro | Não pode ser definido   | Não Passível de Cobrança | Cobrança em um Tempo real: **Não disponível**</br> Tipo de cobrança em Despesa real: **Não Passível de Cobrança**     |
| Sim           | No               | Projeto inteiro | Passível de Cobrança     | Não pode ser definido   | Cobrança em um Tempo real: **Passível de Cobrança** </br> Tipo de cobrança em Despesa real: **Não disponível**        |
| Sim           | No               | Projeto inteiro | Não Passível de Cobrança | Não pode ser definido   | Cobrança em um Tempo real: **Não Passível de Cobrança** </br>Tipo de cobrança em Despesa real: **Não disponível**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]