---
title: Configurar componentes passíveis de cobrança de uma linha de contrato baseada em projeto
description: Este tópico fornece informações sobre como adicionar componentes passíveis de cobrança às linhas de contrato no Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d18e56f29457151e07636b67ff8d9b184bf5014ef0ceeef9bb9d322672be4335
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003442"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurar componentes passíveis de cobrança de uma linha de contrato baseada em projeto

_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma, Project Operations para cenários com base em recursos/sem estoque_

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

Uma estimativa ou dados reais criados para tempo são considerados passíveis de cobrança se:

   - **Tempo** estiver incluído na linha de contrato.
   - **Função** estiver configurado como passível de cobrança na linha do contrato.
   - **Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha do contrato.
 
 Se esses três itens forem verdadeiros, a tarefa será configurada como passível de cobrança. 

Uma estimativa ou dados reais criados para despesas são considerados passíveis de cobrança se:

   - **Despesa** está incluído na linha de contrato
   - **Categoria da transação** estiver configurado como passível de cobrança na linha do contrato
   - **Tarefas Incluídas** estiver configurado como **Tarefa selecionada** na linha do contrato
  
 Se esses três itens forem verdadeiros, a **Tarefa** será configurada como passível de cobrança. 

Uma estimativa ou dados reais criados para material são considerados passíveis de cobrança se:

   - **Materiais** estiver incluído na linha de contrato
   - **Tarefas Incluídas** estiver configurado como **Tarefas selecionadas** na linha do contrato

Se esses dois itens forem verdadeiros, a **Tarefa** será configurada como passível de cobrança. 

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
Cobrança em um tempo real: <strong>Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em uma despesa real: <strong>Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em um material real: <strong>Passível de Cobrança</strong>
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
Cobrança em um tempo real: <strong>Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em uma despesa real: <strong>Passível de Cobrança</strong>
                </p>
                <p>
Tipo de cobrança em um material real: <strong>Passível de Cobrança</strong>
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
