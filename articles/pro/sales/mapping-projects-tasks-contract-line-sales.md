---
title: Mapear projetos e tarefas para uma linha de contrato baseada em projeto - lite
description: Este tópico fornece informações sobre como adicionar e remover projetos e tarefas para uma linha de contrato.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4737f9870904bfc7adac11b8e2aa13bb8c610ca3
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858034"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Mapear projetos e tarefas para uma linha de contrato baseada em projeto 

_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma, Project Operations para cenários com base em recursos/sem estoque_

Em linhas de contrato baseadas em projeto, você pode mapear tarefas específicas em um projeto para a linha de contrato.

Quando você mapeia tarefas específicas para uma linha de contrato, o método de cobrança, as opções de cobrança, os limites de NTE (limite máximo) e os clientes definidos na linha de contrato serão aplicáveis apenas a essas tarefas específicas.

Se você tiver um cenário em que uma fase de um projeto, por exemplo a fase de protótipo, tiver preço fixo e todas as outras fases forem de tempo e materiais, você poderá associar a fase de protótipo e todas as tarefas filho associadas à linha de contrato para essa fase com um método de cobrança de preço fixo.

Todas as outras fases da estrutura de detalhamento de trabalho (WBS) podem ser associadas à linha do contrato baseada em tempo e materiais.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Associar tarefas a linhas de contrato baseadas em projeto

As tarefas podem ser associadas a linhas de contrato na guia **Tarefas Cobráveis** na página **Linha de Contrato** ou na guia **Cobrança de Tarefas** na página **Projeto**.

### <a name="from-the-contract-line-page"></a>Na página Linha de contrato

Conclua as etapas a seguir para associar as tarefas do projeto à linha de contrato na guia **Tarefas Cobráveis** da página **Linha de Contrato**.

1. Na guia **Geral** de uma linha de contrato baseada em projeto, verifique se o campo **Projeto** está preenchido.
2. No campo **Tarefas Incluídas**, selecione **Apenas Tarefas Selecionadas**.
3. Salve suas alterações. O formulário será atualizado e a guia **Tarefas Cobráveis** ficará visível.
4. Selecione a guia **Tarefas Cobráveis** e, na subgrade, selecione **Adicionar uma Tarefa da Linha de Contrato**.
5. Na página **Tarefas da Linha de Contrato**, na lista suspensa **Tarefas**, selecione a tarefa. 
6. Insira as informações no campo **Tipo de Cobrança** e selecione **Salvar e Fechar**. A tarefa selecionada está associada à linha do contrato.

> [!NOTE]
> Esta não é a experiência ideal para associar tarefas do projeto a linhas de contrato. Cada projeto precisará ser associado manualmente nesta experiência. A forma preferencial é na guia **Cobrança de Tarefas** na página **Projeto**.

### <a name="from-the-project-page"></a>Na página Projeto

Este é o método ideal para associar tarefas a linhas de contrato. Você pode selecionar várias tarefas e associar todas elas e as tarefas filho à linha de contrato selecionada. Conclua as etapas a seguir para associar tarefas à linha de contrato da página **Projeto**.

1. Na guia **Geral** de uma linha de contrato baseada em projeto, verifique se o campo **Projeto** está preenchido.
2. No campo **Tarefas Incluídas**, selecione **Apenas Tarefas Selecionadas**.
3. Salve a linha de contrato baseada em projeto. O formulário será atualizado e a guia **Tarefas Cobráveis** ficará visível. Isso é somente para fins de verificação.
4. Na guia **Geral** da linha de contrato baseada em projeto, no campo **Projeto**, selecione o link do projeto.
5. Na página **Projeto**, selecione a guia **Configuração de Cobrança da Tarefa**.
6. Há duas grades. Uma grade é para linhas de contrato que se aplicam ao projeto inteiro. A segunda grade se aplica à configuração de cobrança de tarefas específicas. Na segunda grade, selecione uma ou mais tarefas e, em seguida, **Associar Linhas de Contrato**.
7. Na página da caixa de diálogo que for aberta, selecione uma linha de contrato no menu suspenso.
8. Use o menu suspenso **Tipo de Cobrança** para marcar as tarefas como cobráveis ou não cobráveis.
9. Marque a caixa de seleção para indicar se a associação também deve incluir tarefas filho das tarefas selecionadas. Marcar a caixa também associará as tarefas filho das tarefas selecionadas à linha de contrato.
10. Selecione **OK** para fechar a caixa de diálogo.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Desassociar tarefas de linhas de contrato baseadas em projeto

### <a name="from-the-contract-line-page"></a>Na página Linha de contrato

Conclua as etapas a seguir para desassociar tarefas do projeto da linha de contrato na guia **Tarefas Cobráveis** da página **Linha de Contrato**.

1. Na guia **Tarefas Cobráveis**, selecione **Excluir uma Tarefa da Linha de Contrato**.
2. Uma mensagem de aviso indica que a remoção dessa associação pode resultar na reversão de dados reais anteriormente registrados na tarefa. Selecione **OK** na caixa de diálogo para remover a associação entre a tarefa e a linha de contrato baseada em projeto. 

> [!NOTE]
> Isso não exclui a tarefa do projeto. Isso remove a associação de tarefa da linha de contrato baseada em projeto.

### <a name="from-the-project-page"></a>Na página Projeto

Esta é a experiência ideal para desassociar tarefas de linhas de contrato. Você pode selecionar várias tarefas e desassociar todas elas e as tarefas filho da linha de contrato selecionada. Conclua as etapas a seguir para desassociar tarefas da linha de contrato.

1. Na guia **Geral** da linha de contrato baseada em projeto, no campo **Projeto**, clique no link do projeto.
2. Na página **Projeto**, selecione a guia **Configuração de Cobrança da Tarefa**.
3. Existem duas grades na página. Uma grade é para linhas de contrato que se aplicam ao projeto inteiro e a segunda se aplica à configuração de cobrança de tarefas específicas. Na segunda grade, selecione uma ou mais tarefas e, em seguida, **Desassociar Linhas de Contrato**.
4. Na página da caixa de diálogo que for aberta, selecione uma linha de contrato no menu suspenso.
5. Marque a caixa de seleção para indicar se a associação também deve ser removida de tarefas filho das tarefas selecionadas. Marcar a caixa também desassociará as tarefas filho das tarefas selecionadas da linha de contrato.
6. Selecione **OK**. Uma mensagem de aviso indica que a remoção dessa associação pode resultar na reversão de dados reais anteriormente registrados na tarefa. Selecione **OK** na caixa de diálogo de aviso para remover a associação entre a tarefa e a linha de contrato baseada em projeto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
