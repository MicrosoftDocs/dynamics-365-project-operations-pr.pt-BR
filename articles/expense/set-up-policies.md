---
title: Definir políticas de despesas
description: Você pode definir políticas de despesas que seus funcionários devem seguir ao inserir e enviar relatórios de despesas e requisições de viagem.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001862"
---
# <a name="define-expense-policies"></a>Definir políticas de despesas

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Você pode definir políticas que seus funcionários devem seguir ao inserir e enviar relatórios de despesas e requisições de viagem.         
A implementação de políticas de despesas pode ajudá-lo a gerenciar as despesas de forma eficaz.         

Por exemplo, você pode definir uma política para despesas com hotel na cidade de Nova York, informando que a despesa por noite não pode exceder USD 250.       
Se um funcionário enviar um relatório de despesas ou uma requisição de viagem em que a taxa de hospedagem exceda esse valor, o sistema notificará o         
funcionário de que o valor da política para a despesa foi excedido. Você pode configurar a mensagem que o funcionário receberá quando        
definir a política.      
        
É possível definir três tipos de políticas:         
        
- **Aviso**: permite que o funcionário envie um relatório de despesas ou uma requisição de viagem, mas a despesa será marcada para todos os aprovadores e         
  para relatórios posteriores.        

- **Erro**: exige que o funcionário revise as despesas para estar em conformidade com a política antes de enviar o relatório de despesas ou a requisição de viagem.        
 
 - **Justificativa**: exige que o funcionário ou um gerente insira uma justificativa por exceder o valor da política antes de enviar o relatório de despesas ou a requisição de viagem.        

## <a name="policy-tips"></a>Dicas de políticas
Veja a seguir algumas sugestões que podem ajudá-lo na criação de novas políticas para o gerenciamento de despesas: 

- As políticas têm data de efetivação, o que significa que uma política não entrará em vigor se for criada com uma data posterior à data em que a despesa ocorreu. Por exemplo, você cria uma nova política hoje para impor uma despesa máxima com refeição de USD 50. Quaisquer despesas existentes inseridas até ontem não serão verificadas em relação a essa política.
- Ao criar uma política para uma categoria de despesas que pode ser discriminada, considere adicionar uma condição para o tipo de linha de despesas. Algumas políticas, como exigir um recibo, podem não fazer sentido para linhas discriminadas. Nessa situação, a política é aplicada apenas à linha de cabeçalho ou a uma linha não discriminada. 
- As políticas de gerenciamento de despesas são avaliadas em relação à entidade de origem por padrão. Para cenários intercompanhia, você pode definir a política a ser avaliada em relação à entidade de destino (entidade que toma o empréstimo). Para executar as políticas em relação à entidade de destino, ative o recurso **Avaliar a Política de despesa em relação à entidade legal que toma o empréstimo** no espaço de trabalho **Gerenciamento de Recursos**.

## <a name="when-to-evaluate-policies"></a>Quando avaliar as políticas

Nos parâmetros de gerenciamento de despesas, você pode escolher avaliar as políticas de gerenciamento de despesas quando uma linha for salva ou quando um relatório de despesas for enviado. Se você optar por avaliar quando uma linha for salva, os usuários terão uma visibilidade antecipada do que precisam fazer para preencher o relatório de despesas de uma vez. Caso contrário, você pode atrasar a avaliação da política e economizar tempo validando no final, durante o envio para o fluxo de trabalho.


[!INCLUDE[footer-include](../includes/footer-banner.md)]