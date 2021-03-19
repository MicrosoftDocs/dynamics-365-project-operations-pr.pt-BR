---
title: Despesas intercompanhia
description: Este tópico fornece informações sobre como usar despesas entre empresas para atribuir as despesas de um funcionário à entidade legal para a qual o trabalho foi executado.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271519"
---
# <a name="intercompany-expenses"></a>Despesas entre empresas

Um trabalhador que é empregado por uma entidade legal em uma organização pode executar trabalho para outra entidade legal na mesma organização. Você pode usar despesas entre empresas para atribuir as despesas de um funcionário à entidade legal para a qual o trabalho foi executado. A entidade legal que emprega o trabalhador é chamada de entidade legal que concede empréstimo. A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal que contrai empréstimo. 

Para que um funcionário possa criar e enviar despesas entre empresas, você deve habilitar as linhas de despesas entre empresas. Na entidade legal de empréstimo, na página **Parâmetros de gerenciamento de despesas**, selecione **Permitir linhas de despesas entre empresas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Lançamento de imposto para despesas entre empresas

[!include [banner](../includes/banner.md)]

Para usar grupos de impostos associados à entidade legal de empréstimo (origem) em vez da entidade legal de empréstimo (destino) em seu relatório de despesas, você deve habilitar a funcionalidade na configuração do imposto sobre vendas de contabilidade. Quando o parâmetro **Entidade legal para lançamento de imposto entre empresas** está definido para **Origem** e **Aplicar regras de tributação de impostos sobre vendas** está definido como **Não**, é utilizada a combinação fiscal para a entidade legal de empréstimo. Quando o mesmo parâmetro for definido como **Destino**, será utilizada a combinação fiscal para entidade legal que contrai empréstimo. Para entidades legais nos Estados Unidos, quando o parâmetro é definido como **Fonte**, o campo **Imposto sobre vendas a receber** também deve ser configurado na nova página **Grupos de lançamentos contábeis**. O mecanismo de contabilidade usará as informações desse campo para a entrada contábil relacionada a impostos.   
O comportamento é consistente para linhas de despesas lançadas com ou sem um projeto.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]