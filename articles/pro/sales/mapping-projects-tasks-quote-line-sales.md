---
title: Mapear projetos e tarefas para uma linha de cotação baseada em projeto
description: Este tópico fornece informações sobre como mapear projetos e tarefas para uma linha de tarefa baseada em projeto.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272734"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mapear projetos e tarefas para uma linha de cotação baseada em projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Em linhas de cotação baseadas em projeto, você pode mapear as tarefas específicas de um projeto que já está associado a uma linha de cotação.

Quando você mapeia tarefas para uma linha de cotação, os seguintes itens definidos na linha de cotação só se aplicam a essas tarefas:

- Método de cobrança
- Opções de encargos
- Limites máximos
- Clientes

Por exemplo, você pode ter um projeto em que uma fase tem preço fixo e todas as outras fases são tempo e materiais. Nesse caso, você pode associar a primeira fase, e todas as suas tarefas filho, à linha de cotação para essa fase com um método de cobrança de preço fixo. Você pode então associar todas as outras fases à linha de cotação baseada em tempo e materiais.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Associar tarefas a linhas de cotação baseadas em projeto

Você pode associar tarefas a linhas de cotação dos seguintes locais:

- Página **Projeto** > guia **Cobrança de tarefas** (ideal)
- Página **Linha de cotação** > guia **Tarefas cobráveis** 

### <a name="from-the-project-page"></a>Na página Projeto

A página **Projeto** fornece a experiência ideal para associar tarefas a linhas de cotação. Você pode usar esta página para selecionar várias tarefas e associar todas elas, além de suas tarefas filho, à linha de cotação selecionada.

1. Na guia **Geral** de uma linha de cotação baseada em projeto, verifique se o campo **Projeto** está preenchido.
2. No campo **Tarefas incluídas**, selecione **Somente tarefas selecionadas**.
3. Salve a linha de cotação baseada em projeto. Quando o formulário é atualizado, a guia **Tarefas cobráveis** é exibida.
4. Na guia **Geral**, selecione o link para o projeto no campo **Projeto**.
5. Na página **Projetos**, selecione a guia **Cobrança de tarefas**.
6. Na segunda grade, que se aplica à configuração de cobrança de tarefas específicas, selecione uma ou mais tarefas e selecione **Associar linhas de cotação**.
7. Na página da caixa de diálogo que aparece, selecione uma linha de cotação que exibe linhas de cotação baseadas em projeto na cotação.
8. No campo **Tipo de cobrança**, indique se essas tarefas são cobráveis ou não.
9. Marque a caixa de seleção para indicar se a associação deve incluir tarefas filho das tarefas selecionadas. Ao marcar a caixa, você associará as tarefas filho das tarefas selecionadas à linha de cotação.
10. Selecione **OK** para fechar a caixa de diálogo.

### <a name="from-the-quote-line-page"></a>Na página Linha de cotação

Você pode associar tarefas de projeto a linhas de cotação na guia **Tarefas cobráveis** na página **Linha de cotação**.

>[!NOTE]
>O lugar ideal para associar tarefas de projeto a linhas de cotação é na guia **Cobrança de tarefas** na página **Projeto**. Se você associar tarefas na guia **Tarefas cobráveis** na página **Linha de cotação**, você deverá associar manualmente cada projeto.

1. Na guia **Geral** de uma linha de cotação baseada em projeto, verifique se há um projeto selecionado no campo **Projeto**.
2. No campo **Tarefas incluídas**, selecione **Somente tarefas selecionadas**.
3. Salve a linha de cotação baseada em projeto. Quando o formulário é atualizado, a guia **Tarefas cobráveis** é exibida.
4. Na guia **Tarefas cobráveis**, selecione **Adicionar uma tarefa de linha de cotação**.
5. Na página **Tarefa de linha de cotação**, no campo **Tarefas**, selecione a tarefa e no campo **Tipo de cobrança**, selecione **Salve**. 
6. Feche a página. A tarefa selecionada agora é associada à linha de cotação.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Desassociar tarefas de linhas de cotação baseadas em projeto

### <a name="from-the-project-page"></a>Na página Projeto

Este método fornece a experiência ideal para desassociar tarefas de linhas de cotação. Você pode usar esta página para selecionar várias tarefas e desassociar todas elas, além de suas tarefas filho, da linha de cotação selecionada.

1. Na guia **Geral** de uma linha de cotação baseada em projeto, no campo **Projeto**, selecione o link do projeto.
2. Na página **Projetos**, selecione a guia **Cobrança de tarefas**.
3. Na segunda grade, que se aplica à configuração de cobrança de tarefas específicas, selecione uma ou mais tarefas e selecione **Desassociar linhas de cotação**.
4. Na página de diálogo que aparece, selecione uma linha de cotação.
5. Marque a caixa de seleção para indicar se a associação também deve ser removida das tarefas filho das tarefas selecionadas. Ao marcar a caixa, você também desassociará as tarefas filho das tarefas selecionadas à linha de cotação.
6. Selecione **OK**. Uma mensagem de aviso informa que, se você remover essa associação, quaisquer dados reais registrados anteriormente na tarefa podem ser revertidos. 
7. Selecione **OK** para continuar e remover a associação entre a tarefa e a linha de cotação baseada no projeto.

### <a name="from-the-quote-line-page"></a>Na página Linha de cotação

Você pode também desassociar tarefas de projeto a linhas de cotação na guia **Tarefas cobráveis** na página **Linha de cotação**.

1. Na guia **Tarefas cobráveis**, selecione **Excluir uma tarefa de linha de cotação**.
2. Selecione **OK**. Uma mensagem de aviso informa que, se você remover essa associação, quaisquer dados reais registrados anteriormente na tarefa podem ser revertidos. 
3. Selecione **OK** para continuar e remover a associação entre a tarefa e a linha de cotação baseada no projeto.

>[!NOTE]
> Este procedimento não exclui a tarefa do projeto. Ele apenas remove a associação de tarefa da linha de cotação baseada em projeto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]