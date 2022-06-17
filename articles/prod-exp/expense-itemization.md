---
title: Discriminação de despesas
description: Este artigo explica como discriminar despesas usando o espaço de trabalho de despesas reformuladas.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920920"
---
# <a name="expense-itemization"></a>Discriminação de despesas

[!include [banner](../includes/banner.md)]

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

As organizações geralmente exigem que os funcionários forneçam um detalhamento das despesas incorridas durante a viagem. Por exemplo, um fólio de hotel pode conter várias linhas detalhadas para tarifa de hospedagem, impostos, estacionamento e outras despesas diversas incorridas todos os dias durante a estadia. Ou uma despesa de refeição pode exigir que você forneça um detalhamento mais granular para café da manhã, almoço ou jantar. Quaisquer que sejam as necessidades da organização, cada categoria de despesa pode ser configurada para refletir as subcategorias ou os itens de linha que compõem uma despesa. Embora a discriminação de itens sempre tenha sido compatível com o **Gerenciamento de despesas**, o espaço de trabalho **Despesas reformuladas** permite uma discriminação de itens mais eficiente quando o recurso **Capacidade de discriminar despesas recorrentes rapidamente** está ativado.  

## <a name="enable-quick-itemization"></a>Habilitar discriminação rápida de itens 

Você pode usar o recurso **Capacidade de discriminar despesas recorrentes rapidamente** para detalhar despesas recorrentes rapidamente, evitando a necessidade de inserir as despesas diárias todas as vezes durante a estadia. Conclua as etapas a seguir para habilitar a discriminação rápida de itens.

1. Acesse o espaço de trabalho **Gerenciamento de Recursos** e, na lista de recursos, localize e selecione **Relatórios de despesas reinventados**. 
2. Selecione **Habilitar agora**. 
3. Na lista de recursos, localize e selecione **Capacidade de discriminar despesas recorrentes rapidamente**.
4. Selecione **Habilitar agora**. 

## <a name="itemization-grid"></a>Grade de discriminação de itens 

Se uma categoria de despesa tiver subcategorias ou componentes diferentes que compõem essa despesa, ela poderá ser discriminada. Para discriminar uma despesa, selecione a linha de despesa no relatório de despesas e, no painel **Detalhes de despesas**, selecione **Ações** > **Discriminar**. O controle deslizante **Discriminação de itens** revela uma grade com campos. A tabela a seguir fornece um exemplo de cada campo na grade e como o campo é renderizado no relatório de despesas. 

|     Campo          |     Description                                                                                  |     Exemplo              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subcategoria    |     A lista de subcategorias configuradas no tipo de categoria de despesa **Hotel**.             |     Tarifa diária do quarto      |
|     Data de Início     |     A data em que o item de despesa foi incorrido pela primeira vez.                                           |     13/09/2021           |
|     Diária     |     O valor incorrido para o item de despesa.                                                    |     200                  |
|     Quantidade       |     O número de vezes que a carga é repetida em um período contínuo.                       |     3                    |

![Discrimine despesas.](media/Itemization%20screen%201.png)

Ao salvar uma discriminação de itens, você verá uma linha individualizada para a quantidade especificada na grade de discriminação de itens. Cada linha começa na data especificada na grade.

![Relatório discriminado por item.](media/Itemization%20screen%202.png)

