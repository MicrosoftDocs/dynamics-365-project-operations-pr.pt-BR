---
title: Gerenciar estimativas de receita
description: Este tópico fornece informações sobre como trabalhar com estimativas de receita para projetos.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013833"
---
# <a name="manage-revenue-estimates"></a>Gerenciar estimativas de receita

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Você pode criar, calcular, lançar, reverter ou eliminar estimativas de receita. Você pode fazer isso manualmente ou usando um processo periódico. Este tópico fornece informações sobre como trabalhar com estimativas de receita para projetos.

### <a name="manage-revenue-estimates-manually"></a>Gerenciar estimativas de receita manualmente

No projeto de estimativa de receita de preço fixo ou na página **Consulta de estimativa** (**Gerenciamento e contabilidade de projeto** > **Relatórios e consultas** > **Consultas de estimativas e relatórios**), selecione **Estimativas**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Gerenciar estimativas de receita usando um processo periódico

Acesse **Gerenciamento e contabilidade de projeto** > **Atividades Periódicas** > **Estimativas** e selecione o processo correspondente.

## <a name="create-a-revenue-estimate"></a>Crie uma estimativa de receita

Conclua as etapas a seguir para criar uma estimativa de receita. 

1. Acesse **Gerenciamento e contabilidade de projeto** > **Atividades Periódicas** > **Estimativas**.
2. Selecione **Novo**. Na página **Criação de estimativa**, selecione os seguintes parâmetros:

   - **Código do período**: esse código determina a frequência com que as estimativas são lançadas.
   - **Data da estimativa**: a data em que a estimativa é processada.
   - **Contínua**: marque essa caixa de seleção para criar estimativas somente se as estimativas foram lançadas no período anterior ou se a estimativa é a primeira estimativa que foi criada. Se não for selecionada, as estimativas serão criadas mesmo se as estimativas não foram lançadas no período anterior.
   - **Custo para concluir o método**: defina como estimar o trabalho restante do projeto. Para obter mais informações, consulte [Custo para concluir os métodos](cost-complete-methods.md).
   - **Método de conclusão**: selecione um método de conclusão entre as seguintes opções:
     - **Automático**: a porcentagem de conclusão é calculada automaticamente e com base nas linhas de custo incluídas no cálculo. O modelo de custo define as linhas de custo que são incluídas.
     - **Manual**: a porcentagem de conclusão é igual à porcentagem de conclusão da última estimativa. Depois que a estimativa for criada, você poderá alterar o **Cálculo manual** na página **Estimativas**.
     - **Do modelo de custo**: uma combinação dos métodos automático e manual. Essa opção é definida automática ou manualmente, dependendo do valor padrão no modelo de custo.
   - **Modelo de previsão**: selecione um modelo de previsão para a estimativa.
   - **Imprimir lista de estimativa**: crie e exiba uma lista de orçamentos. A lista contém o status da função atual. Você pode imprimir qualquer aviso sobre a estimativa no relatório. As seguintes condições fazem com que avisos sejam exibidos na lista de estimativas:
     - Uma porcentagem de conclusão maior que 100%.
     - Uma porcentagem de conclusão menor que 0%.
     - Um valor negativo na coluna **Para concluir**.
     - Uma estimativa sem valor de contrato correspondente.
     - Uma estimativa sem estimativa de custo anexada.
   - **Mostrar Infolog**: selecione esta opção para receber uma mensagem que contenha informações sobre os projetos de estimativa que foram processados quando o trabalho foi executado.


## <a name="post-wip-or-accruals"></a>Lançar WIP ou acúmulos

Depois que as estimativas forem avaliadas, elas serão mantidas, diminuídas ou aumentadas. Você poderá, então, lançar o WIP quando trabalhar com o princípio de avaliação **Contrato concluído** ou lançar os acúmulos quando trabalhar com o princípio de avaliação **Porcentagem concluída**.
  
O status do período de estimativa mudará de **Criado** para **Lançado**.

## <a name="reverse-wip-or-accruals"></a>Reverter WIP ou acúmulos

Use a opção de reversão para creditar WIP ou acúmulos já lançados e, em seguida, crie estimativas para o período.

> [!NOTE]
> Para reverter um período que está entre outros períodos, reverta os períodos de estimativa necessários e, em seguida, lance-os novamente. Como todos os períodos subsequentes dependem das estimativas do período anterior, não pule nenhum período.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Elimine o projeto previsto e conclua o projeto

A etapa final no processo de estimativa é eliminar o projeto previsto e encerrar o projeto de preço fixo quando a porcentagem de conclusão atingir 100%.

Quando você executa a eliminação, ocorrerá o seguinte:

- Para um projeto de preço fixo com um contrato concluído, os valores de WIP são eliminados das contas de saldo e lançados nas contas de lucros e perdas.
- Para um projeto de preço fixo com uma porcentagem concluída, os acúmulos são removidos das contas de lucros e perdas.

A estimativa mudará o status para **Eliminado**.

> [!NOTE]
> Em casos especiais, a porcentagem pode ultrapassar 100%. Quando isso acontecer, reduza a porcentagem de conclusão usando o método **Definir custo a ser concluído como zero** para atingir 100%.

## <a name="reverse-elimination"></a>Reverter eliminação

1. Acesse **Gerenciamento e contabilidade de projeto** > **Atividades Periódicas** > **Estimativas** > **Reverter eliminação**. 
2. No Painel de Ações, na guia **Processo**, no grupo **Manter**, selecione **Estimativa**. 
3. Selecione **Reverter eliminação**.

Use esta página para reverter todas as eliminações com uma data de estimativa especificada e com um status de estimativa de **Eliminado**. O status da transação será alterado depois que você selecionar os campos apropriados.

Isso também alterará automaticamente o status do projeto para **Em andamento** se o estágio do projeto estiver definido como concluído. O status da estimativa do período do projeto será aletrado de volta para **Lançado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]