---
title: Configurar políticas de despesas
description: Você pode configurar políticas de despesas que seus funcionários devem seguir ao inserir e enviar relatórios de despesas e requisições de viagem no Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650080"
---
# <a name="set-up-expense-policies"></a>Configurar políticas de despesas

[!include [banner](../includes/banner.md)]

Você pode definir políticas que seus funcionários devem seguir ao inserir e enviar relatórios de despesas e requisições de viagem.         
A implementação de políticas de despesas pode ajudá-lo a gerenciar as despesas de forma eficaz.         

Por exemplo, você pode definir uma política para despesas com hotel na cidade de Nova York, informando que a despesa por noite não pode exceder USD 250.       
Se um funcionário enviar um relatório de despesas ou uma requisição de viagem em que a taxa de hospedagem exceda esse valor, o sistema notificará o        
funcionário de que o valor da política para a despesa foi excedido. Você pode configurar a mensagem que o funcionário receberá quando        
definir a política.      
        
É possível definir três tipos de políticas:         
        
- Aviso: permite que o funcionário envie um relatório de despesas ou uma requisição de viagem, mas a despesa será marcada para todos os aprovadores e        
  para relatórios posteriores.        

- Erro: exige que o funcionário revise as despesas para estar em conformidade com a política antes de enviar o relatório de despesas ou a requisição de viagem.       
 
 - Justificativa: exige que o funcionário ou um gerente insira uma justificativa por exceder o valor da política antes de enviar o relatório de despesas ou a requisição de viagem.        

## <a name="policy-tips"></a>Dicas de políticas
Veja a seguir algumas sugestões que podem ajudá-lo na criação de novas políticas para o gerenciamento de despesas. 
* As políticas entram em vigor e não terão efeito se a política for criada com uma data posterior à data em que a despesa ocorreu. Por exemplo, se você estiver criando uma nova política hoje para impor uma despesa máxima de refeição de US$ 50, quaisquer despesas existentes inseridas até ontem não serão verificadas em relação a esta política.
* Ao criar uma política para uma categoria de despesas que pode ser discriminada, considere adicionar uma condição para o tipo de linha de despesas. Algumas políticas, como exigir um recibo, podem não fazer sentido para linhas discriminadas e devem ser aplicadas apenas à linha de cabeçalho ou a uma linha não detalhada. 
* As políticas de gerenciamento de despesas são avaliadas em relação à entidade de origem por padrão. Para cenários intercompanhia, você pode definir a política a ser avaliada em relação à entidade de destino (entidade que toma o empréstimo). Para executar as políticas em relação à entidade de destino, ative o recurso "Avaliar a Política de despesa em relação à entidade legal que toma o empréstimo" no espaço de trabalho **Gerenciamento de Recursos**.

## <a name="when-to-evaluate-policies"></a>Quando avaliar as políticas

Nos parâmetros de gerenciamento de despesas, você pode escolher avaliar as políticas de gerenciamento de despesas quando uma linha for salva ou quando um relatório de despesas for enviado. Se você optar por avaliar quando uma linha for salva, isso garante que os usuários terão uma visibilidade antecipada do que precisam fazer para preencher o relatório de despesas de uma vez. Caso contrário, você pode atrasar a avaliação da política e economizar tempo validando no final, durante o envio para o fluxo de trabalho.
