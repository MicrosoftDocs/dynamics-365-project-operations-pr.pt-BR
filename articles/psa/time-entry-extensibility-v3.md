---
title: Personalizar entrada de hora semanal
description: Este tópico fornece informações sobre como implementar regras de negócios personalizadas que são compatíveis com as práticas de uma organização.
author: stsporen
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cc395e77e987dac062251ef87fcf8295305178e2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071515"
---
# <a name="customize-weekly-time-entry"></a>Personalizar entrada de hora semanal 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

No Microsoft Dynamics 365 Project Service Automation versão 3.3, a Microsoft incluiu uma grade moderna que permite que os recursos do projeto insiram a hora rapidamente por até uma semana por vez. A nova grade de entrada de hora semanal pode mostrar totais de entradas por data, linha ou semana. Os recursos podem fazer cópias das entradas de hora dentro da semana e também copiar em massa das semanas anteriores. Os personalizadores de sistema podem personalizar a exibição adicionando campos, adicionando pesquisas a outras entidades e implementando regras de negócios personalizadas para oferecer suporte às práticas da organização.

A entrada de hora e a nova grade de hora semanal são acessadas por meio do mapa do site. A experiência de entrada de hora personalizada não extensível que fazia parte das versões anteriores do PSA foi substituída pela grade de entrada de hora semanal extensível e também por uma experiência alternativa na grade e no calendário somente leitura. Por causa dessa alteração, os usuários podem inserir a hora em valores semanais.

## <a name="page-layout"></a>Layout de página
A nova grade de entrada de hora semanal é um controle personalizado que possui uma barra de ferramentas e duas seções principais, **Dimensões** e **Duração**. A barra de ferramentas inclui um botão que se aplica somente a esse controle personalizado para a grade de entrada de hora. Por outro lado, os botões no Painel de Ação, na parte superior da página, se aplicam aos três tipos de controles compatíveis com a entrada de hora: o controle de entrada de hora semanal, o controle somente leitura e o controle de calendário.

### <a name="dimensions"></a>Dimensões
A seção **Dimensões** mostra, como títulos de colunas, todas as dimensões em que o tempo pode ser inserido. As seguintes dimensões têm suporte predefinido:

- Projeto
- Tarefa do Projeto
- Função
- Digite
- Status da Entrada

A seção **Dimensões** não permite a edição em linha. Esta seção é apoiada por uma exibição que permite que campos personalizados sejam adicionados à grade de entrada de hora semanal. Para obter informações sobre como adicionar campos personalizados, consulte a seção "Extensibilidade" posteriormente neste tópico.

### <a name="duration"></a>Duração
A seção Duração mostra os dias da semana como cabeçalhos de colunas. Esta seção permite a edição em linha. Após a criação de uma linha de entrada de hora com dimensões apropriadas, os usuários podem inserir rapidamente, em linha, a quantidade de tempo que passaram nessas dimensões.

## <a name="create-a-new-time-entry"></a>Criar uma entrada de hora
Para criar uma entrada de hora na grade de entrada de hora, selecione **Novo**. A caixa de diálogo **Criação rápida de entrada de hora** é exibida. Nessa caixa de diálogo, os usuários podem selecionar a data de entrada de hora e inserir dados para as dimensões **Projeto** , **Tarefa do Projeto** , **Função** e **Duração** em minutos, horas ou dias digitando **h** , **m** ou **d** , juntamente com o número. Os usuários também podem inserir uma descrição e comentários que podem ser compartilhados externamente para a entrada de hora. Quando os usuários salvam suas alterações, os valores inseridos nas dimensões aparecem na seção **Dimensões**. As informações de duração que eles inseriram no campo **Duração** aparecem na data em que a entrada de hora foi criada.

Os campos de pesquisa são apoiados por exibições do sistema. Por exemplo, depois que um usuário entra em um projeto, o campo **Tarefa do Projeto** é definido como **Copiar** por padrão. Para criar entradas de hora para tarefas que não são atribuídas a um usuário, selecione **Alterar Exibição** na caixa de diálogo de pesquisa e selecione a exibição **Todas as Tarefas de Projeto Ativas**.

## <a name="edit-a-time-entry"></a>Editar uma entrada de hora
Os detalhes de alguns campos na página de entrada de hora, como **Descrição** e **Comentários Externos** , não são mostrados na grade de entrada de hora semanal. Em vez disso, um pequeno indicador triangular aparece nas células de duração que possuem esses detalhes adicionais. Selecione a célula e, em seguida, selecione **Editar detalhes** para exibir os dados no painel **Edição rápida**. Para editar ou atualizar os detalhes de uma entrada de hora específica que não faz parte da grade de entrada de hora semanal, os usuários devem abrir o painel **Edição rápida**.

## <a name="copy-a-time-entry-row"></a>Copiar uma linha de entrada de hora
Após a criação da primeira linha de entrada, os usuários podem selecionar **Copiar linha** para copiar a linha inteira para uma nova linha. Quando uma linha é copiada dessa maneira, as dimensões e as durações também são copiadas. Os usuários também podem selecionar **Editar linha** para atualizar valores e durações de dimensão em linha na seção **Duração**.

## <a name="open-a-time-entry"></a>Abrir uma entrada de hora
Para oferecer suporte à entrada ideal e rápida nos campos mais importantes, a grade de entrada de hora semanal mostra um subconjunto de dimensões e durações de tempo selecionadas. Para exibir todos os detalhes de uma entrada de hora única, em **Editar entrada** , selecione **Abrir**.

## <a name="submit-a-time-entry"></a>Enviar uma entrada de hora
Os usuários podem enviar uma entrada de hora única ou um grupo de entradas de hora selecionando um bloco de células ou uma linha de entrada de hora inteira e, em seguida, selecionando **Enviar**. As entradas de hora enviadas são exibidas como pendentes de aprovação na página **Aprovação** dos aprovadores. Depois que as entradas de hora são enviadas com êxito, elas não podem ser editadas.

## <a name="recall-a-time-entry"></a>Recuperar uma entrada de hora
Você pode recuperar entradas de hora que você enviou. Você pode recuperar uma única entrada de hora, um bloco de entradas de hora ou uma linha inteira de entradas de hora. As entradas de hora recuperadas estão disponíveis para recursos para edição.

## <a name="time-entry-status"></a>Status da entrada de hora
Novas entradas de hora recebem automaticamente um status de **Rascunho**. Quando uma entrada de hora é enviada, o status é atualizado para **Enviado**. Quando uma entrada de hora enviada é aprovada, o status é atualizado para **Aprovado**. Se uma entrada de hora for rejeitada, o status será atualizado para **Devolvido** , e a entrada ficará disponível para correção e reenvio. Somente as entradas de hora com status de **Rascunho** podem ser excluídas.

## <a name="view-rejection-comments"></a>Exibir comentários de rejeição
Quando uma entrada de hora é rejeitada por um aprovador, este pode adicionar comentários de rejeição para ajudar o recurso a entender o motivo da rejeição. Para exibir os comentários de rejeição para uma entrada de hora, selecione **Abrir entrada**. Os comentários de rejeição serão mostrados na linha do tempo. Na linha do tempo, o recurso pode responder aos comentários de rejeição antes de reenviar a entrada.

## <a name="copy-week"></a>Copiar semana
Após a criação de algumas entradas de hora, os usuários podem selecionar **Copiar semana** para criar entradas de hora adicionais em massa. A caixa de diálogo **Copiar** é exibida. Na seção **Do período** , use os campos **Data de Início** e **Data de Término** para definir o intervalo de datas que será usado para copiar as entradas. Na seção **Até o período** no campo **Data de início** , especifique a data usada para criar as entradas de hora. Em seguida, selecione **Copiar**. Para a data especificada no período de "término", é criada uma cópia das entradas de hora para o dia da semana correspondente no período de "início". Por exemplo, a entrada de hora de segunda-feira da semana passada é copiada na segunda-feira da semana especificada como o período de "término".

## <a name="import"></a>Importar
O mesmo processo básico é usado para importar reservas, atribuições e trocas. Os usuários podem especificar o intervalo de que as reservas são importadas. Em seguida, eles devem selecionar explicitamente as reservas que devem ser copiadas nas entradas de hora de rascunho. Na versão anterior, as entradas de hora sugeridas apareceram na grade e no calendário e foram perdidas quando a sessão foi atualizada.

## <a name="extensibility"></a>Extensibilidade do 
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Adicionar campos personalizados com pesquisas a outras entidades
Existem três etapas principais para adicionar um campo personalizado à grade de entrada de hora semanal.

1.  Adicione o campo personalizado à caixa de diálogo de criação rápida.
2.  Configure a grade para mostrar o campo personalizado.
3.  Inclua o campo personalizado no fluxo de tarefas de edição de linha ou no fluxo de tarefas de edição de células, conforme apropriado.

Você também deve se certificar de que o novo campo tenha as validações necessárias no fluxo de tarefas de edição de linha ou célula. Como parte dessa etapa, você deve bloquear o campo, com base no status da entrada de hora.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adicionar o campo personalizado à caixa de diálogo de criação rápida
Você deve adicionar o campo personalizado à caixa de diálogo Criação rápida de entrada de hora, para que os usuários possam inserir um valor quando adicionarem entradas de hora usando o botão **Novo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grade para mostrar o campo personalizado
Existem duas maneiras de adicionar um campo personalizado à grade de entrada de hora semanal. A primeira opção é personalizar a exibição **Minhas Entradas de Hora Semanais** e adicionar o campo personalizado a ela. Você pode escolher a posição e o tamanho do campo personalizado na grade editando essas propriedades na exibição.

A segunda opção é criar uma exibição de entrada de hora personalizada e configurá-la como a exibição padrão. Essa exibição deve conter os campos **Descrição** e **Comentários Externos** , além das colunas que você deseja ter na grade. Você pode escolher a posição, o tamanho e a ordem de classificação padrão da grade editando essas propriedades na exibição. Em seguida, configure o controle personalizado dessa exibição para que seja um controle **Grade de Entrada de Hora**. Adicione esse controle à exibição e selecione-o para Web, telefone e tablet. Em seguida, configure os parâmetros para a grade de entrada de hora semanal. Defina o campo **Data de Início** como **msdyn_date** , defina o campo **Duração** como **msdyn_duration** e defina o campo **Status** como **msdyn_entrystatus**. Para a exibição padrão, o campo **Lista de Status somente Leitura** é definido como **192350002,192350003,192350004** , o campo **Fluxo de Tarefas de Edição de Linha** é definido como **msdyn_timeentryrowedit** e o campo **Fluxo de Tarefas de Edição de Célula** é definido como **msdyn_timeentryedit**. Você pode personalizar esses campos para adicionar ou remover o status somente leitura ou usar uma experiência baseada em tarefas (TBX) diferente para edição de linhas ou células. Esses campos devem estar limitados a um valor estático.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Adicionar o campo personalizado no fluxo de tarefas de edição apropriado
As páginas de TBX usadas para edição podem ser encontradas em **Processos**. As páginas padrão são **Project Service – Edição da Linha da Entrada de Hora** e **Project Service – Edição da Entrada de Hora**. É possível editar essas páginas padrão ou criar páginas de TBX personalizadas.

> [!NOTE] 
> Ambas as opções removerão alguma filtragem predefinida em entidades **Projeto** e **Tarefa do Projeto** , para que todas as exibições de pesquisa das entidades fiquem visíveis. Com a predefinição, apenas as exibições de pesquisa relevantes são visíveis.

Você deve determinar o fluxo de tarefas apropriado para o campo personalizado. Provavelmente, se você adicionou o campo na grade, ele deve estar na linha de fluxo de tarefas de edição que é usado para campos que se aplicam a toda a linha de entradas de hora. Se o campo personalizado tiver um valor exclusivo todos os dias, como um campo personalizado para **Hora de término** , ele deverá estar no fluxo de tarefas de edição de célula.

Para adicionar o campo personalizado a um fluxo de tarefas, arraste um elemento **Campo** para a posição apropriada na página e defina suas propriedades. Defina a propriedade **Fonte** como **Entrada de Hora** e defina a propriedade **Campo de Dados** como o campo personalizado. A propriedade **Campo** especifica o nome para exibição na página de TBX. Selecione **Aplicar** para salvar suas alterações no campo. Em seguida, selecione **Atualizar** para salvar suas alterações na página.

Para usar uma nova página de TBX personalizada, crie um processo. Defina a categoria como **Fluxo do Processo Empresarial** , defina a entidade como **Entrada de Hora** e defina o tipo de processo de negócios como **Executar processo como fluxo de tarefas**. Em **Propriedades** , a propriedade **Nome da página** deve ser definida como o nome para exibição da página. Adicione todos os campos relevantes à página de TBX. Salve e ative o processo e depois atualize a propriedade de controle personalizado para o fluxo de tarefas relevante para o valor de **Nome** no processo.

### <a name="add-new-option-set-values"></a>Adicionar novos valores do conjunto de opções
Para adicionar valores do conjunto de opções a um campo predefinido, abra a página de edição do campo e, em **Tipo** , selecione **Editar** próximo ao conjunto de opções. Em seguida, adicione uma nova opção que tenha um rótulo e cor personalizados. Se você deseja adicionar um novo status de entrada de hora, o campo predefinido é chamado de **Status da Entrada** , não **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar um novo status de entrada de hora como somente leitura
Para designar um novo status de entrada de hora como somente leitura, adicione o novo valor de entrada de hora (o número, não o rótulo) à propriedade **Lista de Status somente Leitura**. A parte editável da grade de entrada de hora será bloqueada para as linhas que têm o novo status.
Em seguida, adicione regras de negócios para bloquear todos os campos nas páginas de TBX **Edição da Linha de Entrada de Hora** e **Edição da Entrada de Hora**. É possível acessar as regras de negócios dessas páginas, abrindo o editor de fluxo do processo empresarial da página e selecionando **Regras de Negócios**. Você pode adicionar o novo status à condição nas regras de negócios existentes ou adicionar uma nova regra de negócios para o novo status.

### <a name="add-custom-validation-rules"></a>Adicionar regras de validação personalizadas
Existem dois tipos de regras de validação que você pode adicionar à experiência da grade de entrada de hora semanal: • Regras de negócios no lado do cliente que funcionam em caixas de diálogo de criação rápida e em páginas de TBX • Validações de plug-ins no lado do servidor que se aplicam a todas as atualizações de entrada de hora

#### <a name="business-rules"></a>Regras de negócios
Use regras de negócios para bloquear e desbloquear campos, inserir valores padrão nos campos e definir validações que requerem informações apenas do registro de entrada de hora atual. Você pode acessar as regras de negócios para uma página de TBX, abrindo o editor de fluxo do processo empresarial da página e selecionando **Regras de Negócios**. Você pode editar as regras de negócios existentes ou adicionar uma nova regra de negócios. Para validações ainda mais personalizadas, você pode usar uma regra de negócios para executar o JavaScript.

#### <a name="plug-in-validations"></a>Validações de plug-in
Você deve usar validações de plug-in para quaisquer validações que exijam mais contexto do que o disponível em um registro de entrada de hora único ou para as validações que deseja executar nas atualizações em linha na grade. Para concluir a validação, crie um plug-in personalizado na entidade **Entrada de Hora**.

> [!IMPORTANT] 
> Atualmente, um problema conhecido nas páginas de TBX impede os usuários de corrigir informações e selecionar novamente Concluído quando uma atualização falha na validação de plug-in. Como solução alternativa, configure validações de regra de negócios para evitar essa situação o máximo possível.
