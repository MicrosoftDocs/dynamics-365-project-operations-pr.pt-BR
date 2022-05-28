---
title: Despesas intercompanhia
description: Este tópico fornece informações sobre como usar despesas entre empresas para atribuir as despesas de um funcionário à entidade legal para a qual o trabalho foi executado.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684215"
---
# <a name="intercompany-expenses"></a>Despesas entre empresas

Um trabalhador que é empregado por uma entidade legal em uma organização pode executar trabalho para outra entidade legal na mesma organização. Você pode usar despesas entre empresas para atribuir as despesas de um funcionário à entidade legal para a qual o trabalho foi executado. A entidade legal que emprega o trabalhador é chamada de entidade legal que concede empréstimo. A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal que contrai empréstimo. 

Para que um funcionário possa criar e enviar despesas entre empresas, você deve habilitar as linhas de despesas entre empresas. Na entidade legal de empréstimo, na página **Parâmetros de gerenciamento de despesas**, selecione **Permitir linhas de despesas entre empresas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Lançamento de imposto para despesas entre empresas

[!include [banner](../includes/banner.md)]

Para usar grupos de impostos associados à entidade legal de empréstimo (origem) em vez da entidade legal de empréstimo (destino) em seu relatório de despesas, você deve habilitar a funcionalidade na configuração do imposto sobre vendas de contabilidade. Quando o parâmetro **Entidade legal para lançamento de imposto entre empresas** está definido para **Origem** e **Aplicar regras de tributação de impostos sobre vendas** está definido como **Não**, é utilizada a combinação fiscal para a entidade legal de empréstimo. Quando o mesmo parâmetro for definido como **Destino**, será utilizada a combinação fiscal para entidade legal que contrai empréstimo. Para entidades legais nos Estados Unidos, quando o parâmetro é definido como **Fonte**, o campo **Imposto sobre vendas a receber** também deve ser configurado na nova página **Grupos de lançamentos contábeis**. O mecanismo de contabilidade usará as informações desse campo para a entrada contábil relacionada a impostos.   
O comportamento é consistente para linhas de despesas lançadas com ou sem um projeto.  

## <a name="new-expense-expression-builder"></a>Novo construtor de expressões de despesa

O novo construtor de expressão de despesa aborda problemas com cenários de despesa entre empresas que usam projetos. Esse recurso garante que, ao criar uma despesa entre empresas, a política de despesa seja validada corretamente em relação ao projeto selecionado na linha de despesa e que o relatório de despesa possa ser enviado com êxito.

Para que o recurso construtor de expressão de despesa funcione, ele deve ser ativado. Além disso, a política de despesa que possui uma ID de projeto deve ser configurada.

Se você já configurou políticas que validam a ID do projeto na linha de despesa, essas políticas devem ser desativadas. Você pode então ativar o recurso e reconfigurar as políticas.

Para ativar o recurso, siga as etapas abaixo.

1. Acesse **Workspaces** \> **Gerenciamento de Recursos**.
2. Na lista, selecione **Novo construtor de expressões para abordar problemas em cenários de despesas entre empresas que usam projetos**. Então selecione **Habilitar agora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
