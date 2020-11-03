---
title: Adicionar membros da equipe da grade de membros da equipe
description: Este tópico fornece informações sobre como você pode gerenciar recursos de membros da equipe.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 0f975d295b4c0ccef9827767beabd32ffd761faa
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071306"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Adicionar membros da equipe da grade de membros da equipe

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

O Dynamics 365 Project Operations inclui um painel de Gerente de recursos que fornece uma visão geral da demanda e da utilização do recurso em toda a organização. Você pode usar os gráficos desse painel para visualizar as seguintes informações:

- **Demanda do recurso** : o gráfico **Solicitação de Recurso Ativa** mostra os recursos que foram enviados. Os recursos são agregados pela função ou pelo projeto.
- **Demanda de recurso não enviada** : o gráfico **Demanda de Recurso Não Atribuída** mostra todos os requisitos de recurso que não foram enviados. Este gráfico ajuda os Gerenciadores de recursos a verem a demanda que não está confirmada e pode ser enviada por meio de uma solicitação de recurso.
- **Horas trabalhadas faturáveis para a semana passada** : o gráfico **Horas trabalhadas por Função** mostra a porcentagem das horas trabalhadas faturáveis por função de dados reais da organização em relação às suas horas trabalhadas faturáveis de destino por função.

    > [!NOTE]
    > Para disponibilizar o gráfico **Horas Trabalhadas por Função** , crie um trabalho que execute o fluxo de trabalho **UpdateRoleUtilization**. Esse trabalho recorrente é executado a cada sete dias para calcular as horas trabalhadas faturáveis para os sete dias anteriores. Os resultados são agregados por função.

## <a name="manage-project-team-members"></a>Gerenciar membros da equipe do projeto

Os gerentes de projeto podem usar o painel do Gerente de recursos para gerenciar os recursos em projetos. Por exemplo, eles podem adicionar um membro da equipe diretamente a um projeto e reservar um membro da equipe para atender aos requisitos de recurso que foram capturados por um recurso genérico.

### <a name="add-a-team-member-directly-to-a-project"></a>Adicionar um membro da equipe diretamente a um projeto

Para adicionar um membro da equipe diretamente a um projeto, no formulário **Projetos** , na guia **Equipe** , selecione **Novo**. A caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto** é exibida. Nessa caixa de diálogo, você pode executar estas tarefas:

- **Reservar um recurso nomeado** : no campo **Recurso Reservável** , selecione o nome do recurso. Em seguida, selecione a função, defina o período e selecione um método de alocação. O recurso nomeado que você selecionou é adicionado ao projeto usando o método de alocação selecionado e o calendário de recursos.
- **Adicionar um recurso genérico** : deixe o campo **Recurso reservável** em branco, selecione a função, defina o período e selecione o método de alocação de preferência. Um recurso genérico é adicionado à equipe como espaço reservado. O espaço reservado contém o padrão de demanda usado para reservar recursos nomeados na equipe. O requisito é feito de acordo com o calendário do projeto.
- **Adicionar um recurso nomeado à equipe sem consumir capacidade do recurso** : no campo **Recurso Reservável** , selecione um recurso. Selecione o período e, em seguida, **Nenhum** como o método de alocação. O recurso é adicionado à equipe, mas a capacidade do recurso não é consumida por meio de uma reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservar um membro da equipe para atender aos requisitos de um recurso genérico

Em Project Operations, você pode reservar um recurso genérico em uma equipe de projeto. Também é possível especificar a função, a capacidade necessária e como essa capacidade é distribuída. No requisito do recurso, é possível especificar atributos que são associados ao recurso genérico. Esses atributos incluem habilidades necessárias, além da unidade organizacional e dos recursos de preferência.

Execute as seguintes etapas para especificar as habilidades necessárias em um recurso genérico para um desenvolvedor.

1. No formulário **Projetos** , na guia **Equipe** , selecione **Novo** para reservar um recurso genérico.
2. Na exibição **Todos os Membros da Equipe** , na coluna **Requisito de Recurso** , selecione o link de modo a adicionar habilidades necessárias para o recurso genérico.
3. No formulário **Requisito de Recurso** que é exibida, na grade **Habilidades** , selecione as reticências ( **...** ) e, em seguida, **Adicionar Novas Características de Requisito** para adicionar as habilidades necessárias para seu desenvolvedor.
4. No formulário de diálogo **Criação Rápida: Característica de Requisito** , no campo **Característica** , selecione a habilidade necessária.
5. No campo **Valor de classificação** , selecione o nível de proficiência para essa habilidade. 
6. No campo **Requisito de Recurso** , defina o requisito para dar origem a recursos, partindo de unidades organizacionais ou, até mesmo, de recursos nomeados. Ao concluir, selecione **Salvar**.
7. No formulário **Requisito de Recurso** , selecione **Reservar** para atender ao requisito de recurso. Você também pode selecionar o recurso genérico na grade **Todos os Membros da Equipe** e selecione **Reservar**.

    > [!NOTE]
    > Neste exemplo, há mais de 40 horas necessárias, mas nenhuma hora reservada, pois os recursos genéricos não têm reservas. Além disso, não há horas atribuídas, pois o recurso genérico foi adicionado diretamente à equipe em vez de ser adicionado por meio da atribuição de tarefas.

    No formulário **Assistente de Agendamento** , é possível filtrar os recursos disponíveis pelos requisitos que são especificados no requisito de recurso. Os recursos são classificados de acordo com os parâmetros de classificação que são especificados no Quadro de Agendamento.

   Alguns dos filtros usados com mais frequência são:

    - **Características com uma classificação** : filtre por habilidades, certificações e outras qualidades do recurso, além de classificações de proficiência.
    - **Funções** : filtre por funções padrão que são atribuídas a recursos reserváveis.
    - **Unidades organizacionais** : filtre recursos reserváveis pelas unidades organizacionais às quais eles são atribuídos.

8. Se não estiver satisfeito com os resultados da pesquisa inicial de requisito, você poderá alterar os critérios de filtro. Expanda o painel **Filtrar Exibição** à esquerda e selecione **Pesquisar** para encontrar recursos adicionais. Para alterar como os resultados são classificados, selecione **Classificar**.
9. Selecione recursos de acordo com a demanda que é especificada no requisito, conforme indicado no topo da grade. Você pode limpar a seleção das células na grade e deixar a capacidade do recurso em aberto. Somente um recurso por vez pode ser selecionado como reservado.
10. Selecione **Reservar** para reservar o recurso selecionado e deixar o Quadro de Agendamento em aberto, de modo que você possa selecionar recursos adicionais. Como alternativa, selecione **Reservar e Sair** para reservar o recurso selecionado e fechar o Quadro de Agendamento.
11. Retorne à exibição **Todos os Membros da Equipe**. Na grade, observe que o recurso genérico foi substituído pelo recurso nomeado, e as 40 horas são listadas como reservadas para esse recurso.

    > [!NOTE]
    > Nenhuma hora atribuída é mostrada, pois foram reservadas diretamente na equipe. Elas não foram reservadas usando a atribuição de tarefas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Atribuir recursos genéricos a tarefas e gerar requisitos de recurso

No Project Operations, você pode criar tarefas e atribuir recursos genéricos a elas. Desse modo, a demanda do recurso pode ser representada pelos espaços reservados enquanto você estima sua agenda e seus números financeiros. É possível gerar requisitos para recursos genéricos e atendê-los.

1. No formulário **Projetos** , na guia **Agendar** , selecione **Adicionar** para criar uma tarefa.
2. No campo **Recursos** , selecione o símbolo **Seletor de Recursos**. O Seletor de Recursos aparece e mostra membros da equipe existentes para o projeto.
3. Digite o novo nome do novo recurso genérico e selecione **Criar**.
4. Na caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto** exibida, no campo **Função** , selecione a função para o recurso genérico. 
5. No campo **Unidade de Recursos** , selecione a unidade organizacional para o recurso genérico. Em seguida, selecione **Salvar**. O membro da equipe genérico agora é atribuído à tarefa.

   Na guia **Equipe** , você verá o novo membro da equipe genérico. Observe que ele tem apenas horas atribuídas. Essas horas são a soma de todas as tarefas que são atribuídas ao membro da equipe genérico. O membro da equipe genérico não tem as horas exigidas nem um requisito de recurso.

6. Agora você pode atribuir o membro da equipe genérico a outras tarefas usando o Seletor de Recursos.

   Ao terminar de atribuir o recurso genérico às tarefas, você poderá gerar um requisito para o recurso genérico.

7. Na guia **Equipe** , selecione o recurso genérico e selecione **Gerar Requisito**. Quando o requisito for gerado, o membro da equipe genérico terá horas exigidas e um link para o requisito de recurso.

  Após reserva de um recurso nomeado, o recurso genérico é removido da equipe e substituído pelo recurso nomeado. Na guia **Agendar** , as atribuições de recurso genérico são removidas e substituídas pelo recurso nomeado.

  > [!NOTE]
  > Esse comportamento ocorre apenas quando um recurso é totalmente reservado para o requisito de recurso genérico. Quando um recurso nomeado substitui parcialmente o requisito de recurso genérico ou vários recursos nomeados substituem o requisito de recurso genérico, este permanece atribuído à tarefa.

O Project Operations não atribui ambos os recursos à tarefa, pois esse comportamento geraria uma agenda menos previsível. Neste exemplos simples, é fácil dividir as horas igualmente entre dois recursos. No entanto, em cenários mais complexos que envolvem várias tarefas e vários recursos, o PSA teria que supor como deve alocar as reservas que são recebidas para vários recursos em várias tarefas.

Portanto, nesses cenários, o Gerente de projeto é responsável por analisar as várias reservas e atribuí-las conforme a necessidade. Para alocar as reservas, o Gerente de projeto atribui as tarefas dos recursos genéricos aos recursos nomeados e usa a exibição **Reconciliação** para garantir que a alocação funcione com as reservas.

### <a name="edit-a-resource-requirement"></a>Editar um requisitos de recurso

Depois que um requisito de recurso tiver sido criado, um Gerente de projeto ou Gerente de recursos pode querer editar os detalhes para refinar os critérios de pesquisa quando o Quadro de Agendamento é usado. Para editar o requisito de recurso, siga estas etapas.

1. No formulário **Projetos** , na guia **Equipe** , selecione o link para qualquer requisito em um recurso genérico.
2. No formulário **Requisição de recurso** exibido, insira as informações de campo necessárias

   No formulário **Requisição de recurso** , o Gerente de projeto ou o Gerente de recursos também pode definir habilidades, funções, preferências de recursos e a unidade organizacional preferida.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Atualizar reservas do recurso depois que ele é reservado em um projeto

Depois de adicionar um recurso genérico ou nomeado a uma equipe de projeto, você pode alterar as reservas do recurso.

1. No formulário **Projetos** , na guia **Equipe** , selecione um membro da equipe e, por fim, selecione **Manter Registros**.
 
   O Quadro de Agendamento aparece e mostra as reservas do membro da equipe do projeto. Expanda o registro do membro da equipe para exibir as horas que foram reservadas em relação a esse projeto e outros projetos que estão consumindo a capacidade do membro da equipe.

2. Selecione e arrastre a reserva para estendê-la ou encurtá-la. Uma caixa de diálogo **Criar Reserva de Recursos** aparece e permite ajustar a reserva.
3. Clique com o botão direito do mouse na reserva. É possível usar o menu de atalho para concluir as seguintes ações:

    - Alterar o status da reserva
    - Editar a reserva
    - Substituir um recurso na equipe do projeto

### <a name="change-the-booking-status"></a>Alterar o status da reserva

Você pode alterar qualquer status de reserva padrão ou personalizada.

Os seguintes status são incluídos no Project Operations:

- **Cancelado** : cancela uma reserva do recurso e libera a capacidade do recurso.
- **Reserva fixa** : consome a capacidade de um recurso. Geralmente, uma reserva tem esse status quando você abre **Manter Reservas** na grade **Todos os Membros da Equipe** no formulário **Projetos**.
- **Reserva Flexível** : adiciona um recurso a uma equipe, mas não consome a capacidade do recurso. Esse status indica que o recurso foi reservado para trabalho potencial, mas ainda tem capacidade caso ele seja necessário em outros trabalhos. Na exibição da disponibilidade geral do recurso, as reservas flexíveis têm um status diferente de reservas fixas.
- **Proposto** : representa uma proposta do Gerente de recursos ou do Gerente de projeto para um recurso. As propostas não consomem a capacidade de um recurso, e o recurso não é adicionado à equipe do projeto. Para fazer uma reserva fixa do recurso na equipe, o Gerente de projeto deve aceitar a proposta.

### <a name="submit-resource-requests"></a>Enviar solicitações de recurso

As solicitações de recurso são usadas para transmitir a demanda, ou requisito de recurso, que deve ser atendida por um Gerente de recursos. Para um recurso genérico que já está na equipe, você pode enviar uma solicitação de recurso diretamente. Uma solicitação de recurso pode ser atendida de duas maneiras:

- O Gerente de recursos atende à solicitação diretamente. Nesse caso, o recurso genérico é substituído por uma reserva fixa que tem um recurso nomeado.
- O Gerente de recursos propõe um recurso para o Gerente de projeto, e o Gerente de projeto aprova ou rejeita o recurso proposto.

#### <a name="direct-fulfillment-of-resource-requests"></a>Atendimento direto das solicitações de recurso

Quando um requisito de recurso é gerado, um Gerente de projeto pode enviar uma solicitação de recurso para um recurso genérico selecionando o recurso e **Enviar Solicitação**. Os comentários sobre o recurso podem ser fornecidos ao Gerente de recursos que está atendendo à solicitação. Depois que a solicitação é enviada, o campo **Status** do membro da equipe é alterado para **Enviado**. Quando o Gerente de recursos atende à solicitação, o membro da equipe genérico é substituído pelo recurso nomeado na grade **Todos os Membros da Equipe**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Usar uma proposta de recurso para solicitações de recurso

Em vez de reservar diretamente um recurso em uma solicitação de recurso, um Gerente de recursos pode propor um recurso ao Gerente de projeto. Um Gerente de recursos pode usar essa opção quando uma correspondência exata para os requisitos não estiver disponível. Quando um Gerente de recursos propõe um recurso, o Gerente de projeto vê se o campo **Status** para o membro da equipe genérico foi alterado para **Precisa de Revisão**.

É possível exibir o recurso proposto junto com uma visualização do efeito da reserva da proposta. 

1. Clique duas vezes no membro da equipe com status de **Precisa de revisão**. 
2. Selecione a guia **Recursos Propostos**.
3. Selecione **Aceitar Todas as Propostas** para aceitar todos os recursos propostos ou **Rejeitar Todas as Propostas** para rejeitá-las. Se você aceitar os recursos propostos, eles serão reservados fixamente no projeto como membros da equipe e substituirão os recursos genéricos.

> [!NOTE]
> Você deve aceitar ou rejeitar todos os recursos propostos. Não é possível aceitá-los ou rejeitá-los parcialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituir um recurso na equipe do projeto

Às vezes, o Gerente de projeto deve substituir um membro da equipe registrado em um projeto.

1. No formulário **Projetos** , na guia **Equipe** , selecione o recurso que precisa de um substituto e selecione **Manter Reservas**.
2. Expanda o recurso para exibir os projetos aos quais ele está atribuído.
3. Clique com o botão direito do mouse no projeto e selecione **Substituir Recurso**.
4. Se você souber o recurso que deseja substituir para o recurso atual, selecione ou digite o nome e selecione **Reatribuir**.

Ou, se você precisar procurar um recurso, execute as seguintes etapas.

1. Selecione **Localizar Substituição**.

   O Assistente de Agendamento retorna uma lista de substitutos disponíveis. No Assistente de Agendamento, você ainda pode filtrar os recursos disponíveis para localizar um substituto adequado.

2. Para substituir o recurso, selecione o recurso desejado e, em seguida, **Substituto**.   

   As reservas e atribuições são substituídas pelo novo recurso.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Reconciliar reservas e atribuições do membro da equipe

Para membros da equipe, reservas e atribuições são livremente combinadas. Em outras palavras, os recursos podem ter atribuições, mas nenhuma reserva, ou podem ter reservas, mas nenhuma atribuição. De maneira ideal, reservas e atribuições devem ser alinhadas para que os recursos tenham capacidade confirmada para executar as atribuições de tarefa. No entanto, as reservas podem ser baseadas na disponibilidade e as durações das tarefas podem ser alteradas conforme o projeto continua. Portanto, a livre combinação de reservas e atribuições proporciona flexibilidade.

O Project Operations tem uma guia **Reconciliação** que permite aos Gerentes de projeto reconciliar reservas dos membros da equipe e suas atribuições para equipes de projeto.

A guia **Reconciliação** mostra reservas e atribuições até o nível da atribuição de tarefas individual para cada membro da equipe. Ela mostra horas em células que representam períodos, desde meses até dias.

A guia também mostra um total líquido geral para o projeto com uma coluna de total.

Para cada recurso, a guia calcula a diferença entre as reservas do membro da equipe e um valor acumulado das atribuições de tarefas do membro da equipe. O ideal é que essa diferença seja 0 (zero). Em outras palavras, não deve haver diferença entre as reservas e as atribuições. As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:

- **Falta de reserva** : ocorre quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, um Gerente de projeto pode querer corrigir essa condição estendendo as reservas do recurso para cobrir o déficit.
- **Reservas em excesso** : ocorrem quando um recurso é reservado para o projeto, mas não é atribuído a tarefas. Essa condição pode ser aceitável nos casos onde o recurso foi reservado para o projeto antes da atribuição da tarefa. No entanto, em outros casos, o recurso não foi planejado para ser atribuído a tarefas. Nesses casos, o Gerente de projetos deve considerar o cancelamento das reservas do recurso, para que a capacidade possa ser usada em outro projeto.

Em alguns casos, quando você exibe a hora em um nível mais alto do que o nível de dia (por exemplo, o nível de mês), é possível ver uma diferença líquida de zero para um recurso. Em outras palavras, reservas = atribuições. No entanto, se você exibir a hora no nível de semana, será possível ver que há atribuições de zero horas e reservas de 40 horas na primeira semana, mas as atribuições de 40 horas e reservas de zero horas na segunda semana. De modo geral, as reservas e atribuições são reconciliadas, mas elas diferem de uma semana para a outra.

Ao exibir tempo em níveis mais altos, as células na guia **Reconciliação** têm um indicador para informar que há diferenças em níveis mais baixos. Clique duas vezes em uma célula para ampliar e exibir a diferença. É possível clicar com o botão direito do mouse para reduzir. Ao selecionar um recurso e depois selecionar **Próxima diferença** na barra de ferramentas da grade, você pode ir para a próxima diferença entre reservas e atribuições para esse recurso. Selecione **Diferença anterior** para voltar. Também é possível desativar o indicador de diferença e o comportamento da navegação em **Configurações**.

Se você tiver atribuições de tarefa para um recurso, mas nenhuma reserva, na guia **Reconciliação** no formulário **Projetos** , selecione a falta de reserva e depois selecione **Estender Reserva**. A caixa de diálogo **Estender Reserva** aparece e mostra a reserva que é necessária para suprir a falta do recurso. A caixa de diálogo também mostra as reservas existentes do recurso em todos os projetos ou outras entidades que podem ser agendadas. Se você selecionar **OK** a fim de criar a reserva para o recurso, independentemente da disponibilidade desse recurso, é possível haver reservas em excesso.

O Gerente de projeto ou o Gerente de recursos pode usar o Quadro de Agendamento para gerenciar situações em que um recurso é reservado em excesso além de sua capacidade.
