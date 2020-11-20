---
title: Configurar os componentes passíveis de cobrança de uma linha de cotação - lite
description: Este tópico fornece informações sobre a configuração de componentes passíveis de cobrança e não passíveis de cobrança em uma linha de cotação com base em projeto.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177092"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Configurar os componentes passíveis de cobrança de uma linha de cotação - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Uma linha de cotação com base em projeto tem o conceito de componentes *incluídos* e componentes *passíveis de cobrança*.

Os componentes incluídos estão sujeitos a:

  - Método de cobrança e divisões do cliente
  - Limites máximos 
  - Configurações de frequência de fatura definidas na linha de cotação com base em projeto

Um subconjunto dos componentes incluídos pode ser marcado como cobrável usando o campo **Tipo de Cobrança**. O campo **Tipo de Cobrança** é um conjunto de opções que permite os seguintes valores no contexto de uma linha de cotação:

  - Passível de Cobrança
  - Não Passível de Cobrança

Os componentes passíveis de cobrança podem ser definidos em tarefas, funções e categorias de transação.

Os encargos são definidos nas tarefas para uma linha de cotação e se aplicam a todas as classes de transação incluídas nessa linha. Se o campo **Incluir Tarefas** estiver definido como **Projeto inteiro** ou tiver sido deixado em branco, a guia **Tarefas Passíveis de Cobrança** não estará disponível.

Os encargos são definidos nas funções para uma linha de cotação e só se aplicam à classe de transação **Tempo**. Se o campo **Incluir Tempo** estiver definido como **Não** na linha de cotação de projeto, a guia **Funções Passíveis de Cobrança** não estará disponível.

Os encargos são definidos em categorias de transação para uma linha de cotação e só se aplicam à classe de transação **Despesa**. Se o campo **Incluir Despesas** estiver definido como **Não** na linha de cotação de projeto, a guia **Categorias Passíveis de Cobrança** não estará disponível.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Atualizar uma tarefa de projeto para passível de cobrança ou não passível de cobrança

Uma tarefa de projeto pode ser passível de cobrança ou não passível de cobrança no contexto de uma linha de cotação com base em projeto, o que torna possível a seguinte configuração:

Se uma linha de cotação com base em projeto incluir **Tempo** e a tarefa **T1**, a tarefa será associada à linha de cotação como passível de cobrança. Se houver uma segunda linha de cotação que inclua **Despesas**, você poderá associar a tarefa **T1** na linha de cotação como não passível de cobrança. O resultado é que todo o tempo registrado na tarefa é passível de cobrança e todas as despesas registradas na tarefa não são passíveis de cobrança.

O tipo de faturamento de uma tarefa pode ser configurado na guia **Tarefas Passíveis de Cobrança** de uma linha de cotação baseada no projeto atualizando o campo **Tipo de Cobrança** na subgrade **Tarefas da Linha de Cotação**. Como alternativa, você pode atualizar o tipo de faturamento de uma tarefa do projeto no campo **Tipo de Cobrança** na subgrade na configuração de faturamento da tarefa de um projeto que mostra as linhas da cotação associadas a uma tarefa.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função para passível de cobrança ou não passível de cobrança

Uma função pode ser passível de cobrança ou não passível de cobrança no contexto de uma linha de cotação com base em projeto específica.

O tipo de faturamento de uma função pode ser configurado na guia **Funções Passíveis de Cobrança** de uma linha da cotação atualizando o campo **Tipo de Faturamento** na subgrade **Funções Passíveis de Cobrança**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação para passível de cobrança ou não passível de cobrança

Uma categoria de transação pode ser passível de cobrança ou não passível de cobrança em uma linha de cotação específica.

O tipo de faturamento de uma transação pode ser configurado na guia **Categorias Passíveis de Cobrança** de uma linha da cotação atualizando o campo **Tipo de Faturamento** na subgrade **Categorias Passíveis de Cobrança**.

### <a name="resolve-chargeability"></a>Resolver os encargos
Uma estimativa ou real criado para o tempo só será considerado passível de cobrança se **Tempo** estiver incluído na linha de cotação e se **Tarefa** e **Função** forem configuradas como passíveis de cobrança na linha de cotação.

Uma estimativa ou real criado para a despesa só será considerado passível de cobrança se **Despesa** estiver incluído na linha de cotação e se **Tarefa** e **Categoria de Transação** forem configuradas como passíveis de cobrança na linha de cotação.

| Inclui Tempo | Inclui Despesa | Tarefas Incluídas | Função | Categoria | Tarefa | Cobrança |
| --- | --- | --- | --- | --- | --- | --- |
| Sim | Sim | Projeto inteiro | Passível de Cobrança | Passível de Cobrança | Não pode ser definido | Cobrança em um tempo real: Passível de Cobrança </br>Tipo de cobrança em uma despesa real: Passível de Cobrança |
| Sim | Sim | Somente tarefas selecionadas | Passível de Cobrança | Passível de Cobrança | Passível de Cobrança | Cobrança em um tempo real: Passível de Cobrança</br>Tipo de cobrança em uma despesa real: Passível de Cobrança |
| Sim | Sim | Somente tarefas selecionadas | Não Passível de Cobrança | Passível de Cobrança | Passível de Cobrança | Cobrança em um tempo real: Não Passível de Cobrança</br>Tipo de cobrança em uma despesa real: Passível de Cobrança |
| Sim | Sim | Somente tarefas selecionadas | Passível de Cobrança | Passível de Cobrança | Não Passível de Cobrança | Cobrança em um tempo real: Não Passível de Cobrança</br> Tipo de cobrança em uma despesa real: Não Passível de Cobrança |
| Sim | Sim | Somente tarefas selecionadas | Não Passível de Cobrança | Passível de Cobrança | Não Passível de Cobrança | Cobrança em um tempo real: Não Passível de Cobrança</br> Tipo de cobrança em uma despesa real: Não Passível de Cobrança |
| Sim | Sim | Somente tarefas selecionadas | Não Passível de Cobrança | Não Passível de Cobrança | Passível de Cobrança | Cobrança em um tempo real: Não Passível de Cobrança</br> Tipo de cobrança em uma despesa real: Não Passível de Cobrança |
| No | Sim | Projeto inteiro | Não pode ser definido | Passível de Cobrança | Não pode ser definido | Cobrança em um tempo real: Não disponível </br>Tipo de cobrança em uma despesa real: Passível de Cobrança |
| No | Sim | Projeto inteiro | Não pode ser definido | Não Passível de Cobrança | Não pode ser definido | Cobrança em um tempo real: Não disponível </br>Tipo de cobrança em uma despesa real: Não Passível de Cobrança |
| Sim | No | Projeto inteiro | Passível de Cobrança | Não pode ser definido | Não pode ser definido | Cobrança em um tempo real: Passível de Cobrança</br>Tipo de cobrança em uma despesa real: Não disponível |
| Sim | No | Projeto inteiro | Não Passível de Cobrança | Não pode ser definido | Não pode ser definido | Cobrança em um tempo real: Não Passível de Cobrança </br>Tipo de cobrança em uma despesa real: Não disponível |
