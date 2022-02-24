---
title: Configurar os componentes passíveis de cobrança de uma linha de cotação
description: Este tópico fornece informações sobre a configuração de componentes passíveis de cobrança e não passíveis de cobrança em uma linha de cotação com base em projeto.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858279"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurar os componentes passíveis de cobrança de uma linha de cotação 

_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma, Project Operations para cenários com base em recursos/sem estoque_

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

Uma tarefa de projeto pode ser passível de cobrança ou não passível de cobrança no contexto de uma linha de cotação com base em projeto, o que torna possível a seguinte configuração.

Se uma linha de cotação com base em projeto incluir **Tempo** e a tarefa **T1**, a tarefa será associada à linha de cotação como passível de cobrança. Se houver uma segunda linha de cotação que inclua **Despesas**, você poderá associar a tarefa **T1** na linha de cotação como não passível de cobrança. O resultado é que todo o tempo registrado na tarefa é passível de cobrança e todas as despesas registradas na tarefa não são passíveis de cobrança.

O tipo de faturamento de uma tarefa pode ser configurado na guia **Tarefas Passíveis de Cobrança** de uma linha de cotação baseada no projeto atualizando o campo **Tipo de Cobrança** na subgrade **Tarefas da Linha de Cotação**. Como alternativa, você pode atualizar o tipo de faturamento de uma tarefa do projeto no campo **Tipo de Cobrança** na subgrade na configuração de faturamento da tarefa de um projeto que mostra as linhas da cotação associadas a uma tarefa.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função para passível de cobrança ou não passível de cobrança

Uma função pode ser passível de cobrança ou não passível de cobrança no contexto de uma linha de cotação com base em projeto específica.

O tipo de faturamento de uma função pode ser configurado na guia **Funções Passíveis de Cobrança** de uma linha da cotação atualizando o campo **Tipo de Faturamento** na subgrade **Funções Passíveis de Cobrança**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação para passível de cobrança ou não passível de cobrança

Uma categoria de transação pode ser passível de cobrança ou não passível de cobrança em uma linha de cotação específica.

O tipo de faturamento de uma transação pode ser configurado na guia **Categorias Passíveis de Cobrança** de uma linha da cotação atualizando o campo **Tipo de Faturamento** na subgrade **Categorias Passíveis de Cobrança**.

### <a name="resolve-chargeability"></a>Resolver os encargos
Uma estimativa ou dados reais criados para tempo serão considerados passíveis de cobrança se:

   - **Tempo** estiver incluído na linha da cotação.
   - **Função** for configurada como passível de cobrança na linha da cotação.
   - **Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha da cotação. 

Se esses três itens forem verdadeiros, a **Tarefa** também será configurada como passível de cobrança. 

Uma estimativa ou dados reais criados para despesas são considerados passíveis de cobrança se: 

   - **Despesa** estiver incluída na linha da cotação.
   - **Categoria da transação** estiver configurado como passível de cobrança na linha da cotação.
   - **Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha da cotação.

Se esses três itens forem verdadeiros, a **Tarefa** também será configurada como passível de cobrança. 

Uma estimativa ou dados reais criados para material serão considerados passíveis de cobrança se:

   - **Materiais** estiver incluído na linha da cotação.
   - **Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha da cotação.

Se esses dois itens forem verdadeiros, a **Tarefa** também deverá ser configurada como passível de cobrança. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inclui Tempo</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inclui Despesa</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Inclui Materiais</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Tarefas Incluídas</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Função</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Categoria</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tarefa</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impacto de encargos</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Projeto Inteiro </p>
            </td>
            <td width="65" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="70" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em uma despesa real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em um material real: Passível de Cobrança </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="70" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="65" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em uma despesa real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em um material real: Passível de Cobrança </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="65" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em uma despesa real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em um material real: Passível de Cobrança </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="70" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em um material real: <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em um material real: <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Somente tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: <strong>Não Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em despesa real: <strong>Não Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em um material real: Passível de Cobrança </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Projeto Inteiro </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Passível de Cobrança</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: <strong>Não disponível</strong>
                </p>
                <p>
Tipo de cobrança em uma despesa real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em um material real: Passível de Cobrança </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Projeto Inteiro </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: <strong>Não disponível</strong>
                </p>
                <p>
Tipo de cobrança em despesa real: <strong>Não passível de cobrança</strong>
                </p>
                <p>
Tipo de cobrança em um material real: Passível de Cobrança </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Projeto Inteiro </p>
            </td>
            <td width="65" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="70" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em despesa real: <strong>Não disponível</strong>
                </p>
                <p>
Tipo de cobrança em um material real: Passível de Cobrança </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Projeto Inteiro </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: <strong>Não passível de cobrança</strong>
                </p>
                <p>
Tipo de cobrança em despesa real: <strong>Não disponível</strong>
                </p>
                <p>
Tipo de cobrança em um material real: Passível de Cobrança </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Projeto Inteiro </p>
            </td>
            <td width="65" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="70" valign="top">
                <p>
Passível de Cobrança </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em uma despesa real: Passível de Cobrança </p>
                <p>
Tipo de cobrança em material real: <strong>Não disponível</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Projeto Inteiro </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Não Passível de Cobrança</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Cobrança em um tempo real: <strong>Não passível de cobrança</strong>
                </p>
                <p>
Tipo de cobrança em despesa real: <strong>Não passível de cobrança</strong>
                </p>
                <p>
Tipo de cobrança em material real: <strong>Não disponível</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
