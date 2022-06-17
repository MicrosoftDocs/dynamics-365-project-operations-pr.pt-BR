---
title: Relatórios de despesas reprojetados
description: Este artigo fornece informações sobre a experiência reprojetada e reformulada da entrada do relatório de despesas.
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 09322d7a59ae91f64dfa63b00f035178d7ca6444
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920966"
---
# <a name="redesigned-expense-reports"></a>Relatórios de despesas reprojetados

A entrada do relatório de despesas foi reprojetada para simplificar o processo de preenchimento de relatórios de despesas e diminuir o tempo necessário. Veja os principais componentes da nova experiência com despesas:

- Um novo espaço de trabalho de gerenciamento de despesas que permite acessar as despesas do seu delegado.
- Uma nova experiência de correspondência de entrada para mostrar melhor os recibos no nível de cabeçalho e simplificar o processo de anexação de recibos a linhas de despesa.
- Uma nova grade somente leitura que permite exibir muito mais linhas de despesas e colunas adicionais de dados. Agora você pode ver todas as linhas discriminadas e divididas, juntamente com as despesas pai.
- Um painel simplificado para editar despesas.
- Mensagens de erro, aviso e políticas reprojetadas para ajudar a garantir que você tenha o contexto correto para entender qual é o problema e como resolvê-lo. A Microsoft removeu muitas mensagens que apareciam antes que os usuários tivessem a oportunidade de concluir as tarefas e resolver os problemas, como a mensagem de discriminação incompleta.
- Uma nova página para especificar quais campos são exigidos por sua organização, quais campos são opcionais e quais campos não devem ser capturados. Esta página ajudará a reduzir o número de campos que usuários devem definir.
- Uma nova aparência para relatórios de despesas, para que os relatórios não pareçam mais como se tivessem sido projetados para pessoas de contabilidade.

Para ativar a nova experiência, use o workspace **Gerenciamento de recursos** para ativar o recurso **Relatórios de despesas reinventados**. Quando você ativa esse recurso, ocorrem as seguintes ações:

- O espaço de trabalho de despesas existente é substituído pelo novo espaço de trabalho.
- Um novo item de menu para visibilidade do campo de despesas é adicionado.
- Nenhum item de menu existente para os relatórios de despesas (a página existente) ou os campos do relatório de despesas são removidos.
- Fluxos de trabalho e aprovações ainda levam você para a página de relatórios de despesas existentes.

## <a name="new-features"></a>Novos recursos

| Novo recurso | Descrição |
|---|----|
| Visibilidade do campo de despesas | Uma nova página de configuração permite especificar quais campos devem ser desabilitados para uma organização, quais campos devem ser obrigatórios e quais campos são recomendados. |
| Campos obrigatórios | A nova configuração simples permite tornar alguns campos obrigatórios sem precisar usar a estrutura de política. |
| Campos opcionais | Uma segunda página para campos opcionais é adicionada. Dessa forma, os funcionários não sentirão como se tivessem que definir os campos, mas eles podem ser acessados facilmente. |
| Adicionar recibos não anexados | A capacidade de adicionar recibos não anexados ao relatório de despesas é mais visível no espaço de trabalho e no relatório de despesas. |
| Mensagens aprimoradas | Há melhor visibilidade nas linhas de despesas que contêm avisos ou erros. |
| Redução de mensagens na barra de mensagens| O número de mensagens do log de Informações foi diminuído e foi feito um esforço para evitar que mensagens duplicadas aparecessem em muitos casos. |
| Ações comuns agrupadas | A interface foi limpa com a adição de um novo botão de ações para a maioria das ações comuns de nível de linha e a adição de um botão de reticências (...) para cabeçalho e outras ações menos frequentes. |
| Novo espaço de trabalho para aumentar a visibilidade | Um novo espaço de trabalho unifica recursos e links que permitem que os usuários migrem para áreas diferentes. |
| Adicionar despesas e recibos existentes durante a criação da despesa | Ao criar relatórios de despesas, você pode adicionar todas as despesas e recibos selecionados. |
| Calculadora de taxa de câmbio | Foi adicionada uma calculadora de taxa de câmbio que permite calcular a taxa de câmbio para transações do próprio bolso em várias moedas. |
| Salvar e adicionar novas linhas de despesa | Os botões **Salvar** e **Novo** estão disponíveis quando novas despesas são inseridas, para ajudar a inserir rapidamente as linhas de despesas. |
| Melhor visibilidade em linhas divididas e discriminadas | As linhas discriminadas e divididas são adicionadas diretamente à lista de despesas, para aumentar a visibilidade e ajudar a determinar facilmente se há erros de política ou outros erros. |
| Mostrar recibos durante a discriminação | Os recibos podem ser exibidos durante a discriminação. |

A versão inicial é focada em cenários de entrada de despesa. Qualquer revisão de relatório de despesas ou cenário de aprovação continuará a usar a página de entrada de despesa existente.

Os recursos a seguir estão presentes na página existente, mas ainda não estão presentes na nova página. Estes recursos serão reintroduzidos nas próximas versões:

- Aprovações
- Aprovação de contas a pagar e a capacidade de editar a contabilidade
- Vários pontos de entrada
- Integração de requisição de viagem
- Entidade de dados para visibilidade do campo de despesas
- Entrada para despesas diárias
- Fluxo de trabalho do nível da linha
- Suporte para aprovadores provisórios
- Discriminação avançada


[!INCLUDE[footer-include](../includes/footer-banner.md)]