---
title: Relatórios de despesas reinventados
description: Este tópico fornece informações sobre a experiência reprojetada e reformulada para a entrada de relatórios de despesas.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122779"
---
# <a name="expense-reports-reimagined"></a>Relatórios de despesas reinventados

A entrada de relatório de despesas foi reprojetada para simplificar o processo e diminuir o tempo necessário para concluir um relatório. Veja os principais componentes da nova experiência com despesas:

- Um novo espaço de trabalho de gerenciamento de despesas que permite acessar as despesas do seu delegado.
- Uma nova experiência de correspondência de entrada para mostrar melhor os recibos no nível de cabeçalho e simplificar o processo de anexação de recibos a linhas de despesa.
- Uma nova grade somente leitura que permite exibir muito mais linhas de despesas e colunas adicionais de dados. Agora você pode ver todas as linhas discriminadas e divididas, juntamente com as despesas pai.
- Um painel simplificado para editar despesas.
- Mensagens de erro, aviso e políticas reprojetadas para ajudar a garantir que você tenha o contexto correto para entender qual é o problema e como resolvê-lo. Removemos muitas mensagens que apareciam antes que os usuários pudessem concluir suas tarefas e resolver os problemas.
- Uma nova página para especificar os campos obrigatórios, os campos opcionais e os campos que não devem ser incluídos. Esta página ajuda a reduzir o número de campos que devem ser definidos.
- Uma nova aparência para relatórios de despesas, para que os relatórios não pareçam mais como se tivessem sido projetados para pessoas de contabilidade.

Para ativar a nova experiência, use o espaço de trabalho **Gerenciamento de recursos** para ativar o recurso **Relatórios de despesas reformulados**. Quando você ativa esse recurso, ocorrem as seguintes ações:

- O espaço de trabalho de despesas existente é substituído pelo novo espaço de trabalho.
- Um novo item de menu para visibilidade do campo de despesas é adicionado.
- Nenhum item de menu existente para os relatórios de despesas (a página existente) ou os campos do relatório de despesas são removidos.
- Fluxos de trabalho e aprovações ainda levam você para a página de relatórios de despesas existentes.

## <a name="getting-started-video-for-new-users"></a>Vídeo de introdução para novos usuários

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

O [vídeo Experiência de despesas Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (mostrado acima) está incluído na [playlist do Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) disponível no YouTube.

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
| Melhor visibilidade em linhas divididas e discriminadas | As linhas discriminadas e divididas são adicionadas diretamente à lista de despesas, para aumentar a visibilidade e ajudar a determinar facilmente se há erros. |
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
