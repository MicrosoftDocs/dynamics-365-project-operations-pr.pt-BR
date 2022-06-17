---
title: Relatórios de despesas reinventados (contém vídeo)
description: Este artigo explica a experiência reprojetada e reformulada da entrada do relatório de despesas.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c74b4b70722af72bc66dba0662813c29d3d1df04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930258"
---
# <a name="expense-reports-reimagined"></a>Relatórios de despesas reinventados

A entrada de relatório de despesas foi reprojetada para simplificar o processo e diminuir o tempo necessário para concluir um relatório. Veja os principais componentes da nova experiência com despesas:

- Um novo espaço de trabalho de gerenciamento de despesas que permite acessar as despesas do seu delegado.
- Uma nova experiência de correspondência de entrada para mostrar melhor os recibos no nível de cabeçalho e simplificar o processo de anexação de recibos a linhas de despesa.
- Uma nova grade somente leitura que permite visualizar muito mais linhas de despesas e outras colunas de dados. Agora você pode ver todas as linhas discriminadas e divididas, juntamente com as despesas pai.
- Um painel simplificado para editar despesas.
- Mensagens de erro, aviso e políticas reprojetadas para ajudar a garantir que você tenha o contexto correto para entender qual é o problema e como resolvê-lo. Removemos muitas mensagens que apareciam antes que os usuários pudessem concluir suas tarefas e resolver os problemas.
- Uma nova página para especificar os campos obrigatórios, os campos opcionais e os campos que não devem ser incluídos. Esta página ajuda a reduzir o número de campos que devem ser definidos.
- Uma nova aparência para relatórios de despesas, para que os relatórios não pareçam mais como se tivessem sido projetados para pessoas de contabilidade.

Para ativar a nova experiência, use o espaço de trabalho **Gerenciamento de recursos** para ativar o recurso **Espaço de trabalho reinventado para relatórios de despesas**. Quando você ativa esse recurso, ocorrem as seguintes ações:

- O espaço de trabalho de despesas existente é substituído pelo novo espaço de trabalho.
- Um novo item de menu para visibilidade do campo de despesas é adicionado.
- Nenhum item de menu existente para os relatórios de despesas (a página existente) ou os campos do relatório de despesas são removidos.
- Fluxos de trabalho e aprovações ainda levam você para a página de relatórios de despesas existentes.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Novos recursos

| Novo recurso | Descrição |
|---|----|
| Visibilidade do campo de despesas | Uma nova página de configuração permite que você especifique quais campos devem ser desabilitados para uma organização. Você também pode especificar quais campos devem ser obrigatórios e quais campos são recomendados. |
| Campos obrigatórios | A nova configuração simples permite tornar alguns campos obrigatórios sem precisar usar a estrutura de política. |
| Campos opcionais | Uma segunda página para campos opcionais é adicionada. Dessa forma, os funcionários não sentirão como se tivessem que definir os campos, mas eles podem ser acessados facilmente. |
| Adicionar recibos não anexados | A capacidade de adicionar recibos não anexados ao relatório de despesas é mais visível no espaço de trabalho e no relatório de despesas. |
| Mensagens aprimoradas | Há melhor visibilidade nas linhas de despesas que contêm avisos ou erros. |
| Redução de mensagens na barra de mensagens| O número de mensagens do log de Informações foi diminuído e foi feito um esforço para evitar que mensagens duplicadas aparecessem em muitos casos. |
| Ações comuns agrupadas | A interface foi limpa com a adição de um novo botão de ações para a maioria das ações comuns de nível de linha e a adição de um botão de reticências (...) para cabeçalho e outras ações menos frequentes. |
| Novo espaço de trabalho para aumentar a visibilidade | Um novo espaço de trabalho unifica recursos e links que permitem que os usuários migrem para áreas diferentes. |
| Adicionar despesas e recibos existentes durante a criação da despesa | Ao criar relatórios de despesa, você pode adicionar todas as despesas ou selecionar despesas não anexadas. As despesas não anexadas são as despesas que foram importadas do cartão de crédito corporativo ou despesas que foram criadas manualmente pelo usuário, mas não foram anexadas a um relatório de despesa.|
| Calculadora de taxa de câmbio | Foi adicionada uma calculadora de taxa de câmbio que permite calcular a taxa de câmbio para transações do próprio bolso em várias moedas. |
| Salvar e adicionar novas linhas de despesa | Os botões **Salvar** e **Novo** estão disponíveis quando novas despesas são inseridas, para ajudar a inserir rapidamente as linhas de despesas. |
| Melhor visibilidade em linhas divididas e discriminadas | As linhas discriminadas e divididas são adicionadas diretamente à lista de despesas, para aumentar a visibilidade e ajudar a determinar facilmente se há erros. |
| Veja os detalhes da subcategoria em linhas discriminadas | As linhas discriminadas de uma despesa pai mostram os rótulos de subcategoria no relatório de despesas. A discriminação permite que você revise os detalhes granulares rapidamente.|
|Discriminar despesas recorrentes por item rapidamente | O espaço de trabalho de despesas reinventado oferece a capacidade de detalhar as despesas recorrentes rapidamente, adicionando a subcategoria, a data de início e a quantidade. A quantidade refere-se ao número de vezes que a carga é repetida em um período contínuo. |
| Mostrar recibos durante a discriminação | Os recibos podem ser exibidos durante a discriminação. |
| Seleção de adiantamento em dinheiro | Selecione um ou mais adiantamentos em dinheiro para cumprir uma única transação de despesa. |
| Saldo de adiantamento em dinheiro | Revise o saldo de adiantamento em dinheiro em tempo real ao criar uma entrada de despesa em adiantamentos em dinheiro aprovados e pagos. |

A versão inicial é focada em cenários de entrada de despesa. Qualquer revisão de relatório de despesas ou cenário de aprovação continuará a usar a página de entrada de despesa existente.


Os recursos a seguir não são compatíveis com o espaço de trabalho reformulado dos relatórios de Despesas, mas estão planejados para versões futuras: 

- Integração de requisição de viagem
- Entrada de despesas diária
- Suporte para aprovadores provisórios
- Capacidade de exibir o histórico do fluxo de trabalho


[!INCLUDE[footer-include](../includes/footer-banner.md)]
