---
title: Gerenciar recursos
description: Este tópico fornece informações sobre como você pode gerenciar recursos.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b067f900fa49bba04536b49600dbe80a2167f707
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997812"
---
# <a name="manage-resources"></a>Gerenciar recursos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Dynamics 365 Project Service Automation inclui um painel de gerente de recursos que fornece uma visão geral visual da demanda e horas trabalhadas do recurso em toda a organização. Você pode usar os gráficos desse painel para visualizar as seguintes informações:

- **Demanda do recurso** – o gráfico **Solicitação de Recurso Ativa** mostra os recursos que foram enviados. Os recursos são agregados pela função ou pelo projeto.
- **Demanda de recurso não enviada** – o gráfico **Demanda de Recurso Não Atribuída** mostra todos os requisitos de recurso que não foram enviados. Ele ajuda os gerenciadores de recursos a verem a demanda que não está confirmada e pode ser enviada por meio de uma solicitação de recurso.
- **Horas trabalhadas faturáveis para a semana passada** – o gráfico **Horas trabalhadas por Função** mostra a porcentagem das horas trabalhadas faturáveis por função de dados reais da organização em relação às suas horas trabalhadas faturáveis de destino por função.

    > [!NOTE]
    > Para disponibilizar o gráfico **Horas Trabalhadas por Função**, crie um trabalho que execute o fluxo de trabalho UpdateRoleUtilization. Esse trabalho recorrente é executado a cada sete dias para calcular as horas trabalhadas faturáveis para os sete dias anteriores. Os resultados são agregados por função.

## <a name="manage-project-team-members"></a>Gerenciar membros da equipe do projeto

Os gerentes de projeto podem usar o painel do gerente de recursos para gerenciar os recursos em projetos. Por exemplo, eles podem adicionar um membro da equipe diretamente a um projeto e reservar um membro da equipe para atender aos requisitos de recurso que foram capturados por um recurso genérico.

### <a name="add-a-team-member-directly-to-a-project"></a>Adicionar um membro da equipe diretamente a um projeto

Para adicionar um membro da equipe diretamente a um projeto, na página **Projetos**, na guia **Equipe**, selecione **Novo**. A caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto** é exibida. Nessa caixa de diálogo, você pode executar estas tarefas:

- **Reservar um recurso nomeado** – no campo **Recurso Reservável**, selecione o nome do recurso. Em seguida, selecione a função, defina o período e selecione um método de alocação. O recurso nomeado que você selecionou é adicionado ao projeto usando o método de alocação selecionado e o calendário de recursos.
- **Adicionar um recurso genérico** – deixe o campo **Recurso reservável** em branco, selecione a função, defina o período e selecione o método de alocação de preferência. Um recurso genérico é adicionado à equipe como um espaço reservado de modo a manter o padrão de demanda que é usado para reservar recursos nomeados na equipe. O requisito é feito de acordo com o calendário do projeto.
- **Adicionar um recurso nomeado à equipe sem consumir capacidade do recurso** – no campo **Recurso Reservável**, selecione um recurso. Em seguida, selecione o período e **Nenhum** como o método de alocação. O recurso é adicionado à equipe, mas a capacidade do recurso não é consumida por meio de uma reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservar um membro da equipe para atender aos requisitos de um recurso genérico

No PSA, você pode reservar um recurso genérico em uma equipe de projeto, bem como especificar a função, a capacidade necessária e como essa capacidade é distribuída. No requisito do recurso, é possível especificar atributos que são associados ao recurso genérico. Esses atributos incluem habilidades necessárias, além da unidade organizacional e dos recursos de preferência.

Siga estas etapas para especificar as habilidades necessárias em um recurso genérico para um desenvolvedor.

1. Na página **Projetos**, na guia **Equipe**, selecione **Novo** para reservar um recurso genérico.

    ![Recurso genérico reservado na equipe](media/Resource-Management-image9.png)

2. Na exibição **Todos os Membros da Equipe**, na coluna **Requisito de Recurso**, selecione o link de modo a adicionar habilidades necessárias para o recurso genérico.

    ![Link do requisito](media/Resource-Management-image10.png)

3. Na página **Requisito de Recurso** que é exibida, na grade **Habilidades**, selecione as reticências (**...**) e, em seguida, **Adicionar Novas Características de Requisito** para adicionar as habilidades necessárias para seu desenvolvedor.

    ![Comando Adicionar Novas Características de Requisito](media/Resource-Management-image11.png)

4. Na caixa de diálogo **Criação Rápida: Característica de Requisito** que é exibida, no campo **Característica**, selecione a habilidade necessária. Em seguida, no campo **Valor de classificação**, selecione o nível de proficiência para essa habilidade. Por fim, no campo **Requisito de Recurso**, defina o requisito para dar origem a recursos, partindo de unidades organizacionais ou, até mesmo, de recursos nomeados. Ao concluir, selecione **Salvar**.

    ![Caixa de diálogo Criação Rápida: Característica de Requisito](media/Resource-Management-image12.png)

5. Na página **Requisito de Recurso**, selecione **Reservar** para atender ao requisito de recurso.

    ![Botão Reservar na página Requisito de Recurso](media/Resource-Management-image13.png)

    Você também pode selecionar o recurso genérico na grade **Todos os Membros da Equipe** e selecione **Reservar**.

    ![Botão Reservar acima da grade Todos os Membros da Equipe](media/Resource-Management-image14.png)

    > [!NOTE]
    > Neste exemplo, há mais de 40 horas necessárias, mas nenhuma hora reservada, pois os recursos genéricos não têm reservas. Além disso, não há horas atribuídas, pois o recurso genérico foi adicionado diretamente à equipe. Ele não foi adicionado usando a atribuição de tarefas.

    Na página **Assistente de Agendamento**, é possível filtrar os recursos disponíveis pelos requisitos que são especificados no requisito de recurso. Os recursos são classificados de acordo com os parâmetros de classificação que são especificados no Quadro de Agendamento.

    ![Página Assistente de Agendamento](media/Resource-Management-image15.png)

    Veja a seguir alguns filtros que são usados frequentemente:

    - **Características com uma classificação** – filtre por habilidades, certificações e outras qualidades do recurso, além de classificações de proficiência.
    - **Funções** – filtre por funções padrão que são atribuídas a recursos reserváveis.
    - **Unidades organizacionais** – filtre recursos reserváveis pelas unidades organizacionais às quais eles são atribuídos.

6. Se não estiver satisfeito com os resultados da pesquisa inicial de requisito, você poderá alterar os critérios de filtro. Expanda o painel **Filtrar Exibição** à esquerda e selecione **Pesquisar** para encontrar recursos adicionais.

    ![Painel Filtrar Exibição](media/Resource-Management-image16.png)

7. Para alterar como os resultados são classificados, selecione **Classificar**.

    ![Comando Classificar](media/Resource-Management-image17.png)

8. Selecione recursos de acordo com a demanda que é especificada no requisito, conforme indicado no topo da grade. Você pode limpar a seleção das células na grade e deixar a capacidade do recurso em aberto. Somente um recurso por vez pode ser selecionado como reservado.

9. Selecione **Reservar** para reservar o recurso selecionado e deixar o Quadro de Agendamento em aberto, de modo que você possa selecionar recursos adicionais. Como alternativa, selecione **Reservar e Sair** para reservar o recurso selecionado e fechar o Quadro de Agendamento.

    ![Recurso a ser reservado](media/Resource-Management-image19.png)

    Você recebe uma notificação sobre as horas reservadas. Os indicadores de demanda mostram quanto do requisito de reserva foi atendido e quanto ainda falta. Também é possível ver o quanto é consumido da capacidade do recurso selecionado. Selecione **Expandir** para exibir mais detalhes sobre reservas do recurso.

9. Retorne à exibição **Todos os Membros da Equipe**. Na grade, observe que o recurso genérico foi substituído pelo recurso nomeado, e as 40 horas são listadas como reservadas para esse recurso.

    ![Grade Todos os Membros da Equipe atualizada](media/Resource-Management-image20.png)

    > [!NOTE]
    > Nenhuma hora atribuída é mostrada, pois foram reservadas diretamente na equipe. Elas não foram reservadas usando a atribuição de tarefas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Atribuir recursos genéricos a tarefas e gerar requisitos de recurso

No PSA, você pode criar tarefas e atribuir recursos genéricos a elas. Desse modo, a demanda do recurso pode ser representada pelos espaços reservados enquanto você estima sua agenda e seus números financeiros. É possível gerar requisitos para recursos genéricos e atendê-los.

1. Na página **Projetos**, na guia **Agendar**, selecione **Adicionar** para criar uma tarefa.

    ![Nova tarefa criada](media/Resource-Management-image21.png)

2. No campo **Recursos**, selecione o símbolo **Seletor de Recursos**. O Seletor de Recursos aparece e mostra membros da equipe existentes para o projeto.

    ![Seletor de Recursos](media/Resource-Management-image22.png)

3. Digite o novo nome do novo recurso genérico e selecione **Criar**.

    ![Nome de um novo recurso genérico inserido](media/Resource-Management-image23.png)

4. Na caixa de diálogo **Criação Rápida: Membro da Equipe do Projeto** exibida, no campo **Função**, selecione a função para o recurso genérico. No campo **Unidade de Recursos**, selecione a unidade organizacional para o recurso genérico. Em seguida, selecione **Salvar**.

    ![Caixa de diálogo Criação Rápida: Membro da Equipe do Projeto](media/Resource-Management-image24.png)

    O membro da equipe genérico agora é atribuído à tarefa.

    ![Membro da equipe genérico atribuído à tarefa](media/Resource-Management-image25.png)

    Na guia **Equipe**, você verá o novo membro da equipe genérico. Observe que ele tem apenas horas atribuídas. Essas horas são a soma de todas as tarefas que são atribuídas ao membro da equipe genérico. O membro da equipe genérico ainda não tem horas exigidas nem um requisito de recurso.

    ![Membro da equipe genérico na guia Equipe](media/Resource-Management-image26.png)

5. Agora você pode atribuir o membro da equipe genérico a outras tarefas usando o Seletor de Recursos.

    ![Membro da equipe genérico no Seletor de Recursos](media/Resource-Management-image27.png)

    Ao terminar de atribuir o recurso genérico às tarefas, você poderá gerar um requisito para o recurso genérico.

5. Na guia **Equipe**, selecione o recurso genérico e selecione **Gerar Requisito**.

    ![Comando Gerar Requisito](media/Resource-Management-image28.png)

    Quando o requisito for gerado, o membro da equipe genérico terá horas exigidas e um link para o requisito de recurso.

    ![Link Requisito de recurso](media/Resource-Management-image29.png)

    Após reserva de um recurso nomeado, o recurso genérico é removido da equipe e substituído pelo recurso nomeado.

    ![Recurso genérico substituído pelo recurso nomeado](media/Resource-Management-image30.png)

    Na guia **Agendar**, as atribuições de recurso genérico são removidas e substituídas pelo recurso nomeado.

    ![Atribuições de recurso genérico substituídas pelo recurso nomeado na guia Agendar](media/Resource-Management-image31.png)

    > [!NOTE]
    > Esse comportamento ocorre apenas quando um recurso é totalmente reservado para o requisito de recurso genérico. Quando um recurso nomeado substitui parcialmente o requisito de recurso genérico ou vários recursos nomeados substituem o requisito de recurso genérico, este permanece atribuído à tarefa.

    Na ilustração a seguir, uma tarefa de 80 horas foi planejada para uma duração de cinco dias (16 horas por dia por cinco dias) e atribuída ao recurso genérico denominado **Funcional**.

    ![Tarefa de oitenta horas e cinco dias para o recurso genérico Funcional](media/Resource-Management-image32.png)

    Quando você gera o requisito, é para 80 horas por cinco dias.

    ![Requisito gerado para 80 horas por cinco dias](media/Resource-Management-image33.png)

    Como os recursos disponíveis funcionam somente oito horas por dia, dois recursos são necessário para atender ao requisito.

    ![Segundo recurso](media/Resource-Management-image35.png)

    Na guia **Equipe**, agora é possível ver que o recurso genérico não tenha horas exigidas, mas as horas atribuídas ainda aparecem com os dois recursos nomeados que compõem o atendimento.

    ![Dois recursos nomeados na guia Equipe](media/Resource-Management-image36.png)

    Na guia **Agendar**, o recurso genérico permanece atribuído à tarefa.

    ![Recursos genéricos na guia Agendar](media/Resource-Management-image37.png)

O PSA não atribui ambos os recursos à tarefa, pois esse comportamento geraria uma agenda menos previsível. Neste exemplos simples, é fácil dividir as horas igualmente entre dois recursos. No entanto, em cenários mais complexos que envolvem várias tarefas e vários recursos, o PSA teria que supor como deve alocar as reservas que são recebidas para vários recursos em várias tarefas.

Portanto, nesses cenários, o gerente de projeto é responsável por analisar as várias reservas e atribuí-las conforme a necessidade. Para alocar as reservas, o gerente de projeto atribui as tarefas dos recursos genéricos aos recursos nomeados e usa a exibição **Reconciliação** para garantir que a alocação funcione com as reservas.

### <a name="edit-a-resource-requirement"></a>Editar um requisitos de recurso

Depois que um requisito de recurso tiver sido criado, um gerente de projeto ou gerente de recursos pode querer editar os detalhes para refinar os critérios de pesquisa quando o Quadro de Agendamento é usado. Para editar o requisito de recurso, siga estas etapas.

1. Na página **Projetos**, na guia **Equipe**, selecione o link para qualquer requisito em um recurso genérico.
2. Na página **Requisito de Recurso** que é exibida, você pode atualizar vários atributos. Veja alguns exemplos:

    - Nome
    - Data Inicial
    - Data Final
    - Duração
    - Tipo de Recurso

Na página **Requisito de Recurso**, o gerente de projeto ou gerente de recursos também pode definir as seguintes informações:

- Habilidades
- Funções
- Preferências de recurso
- Unidades organizacionais preferenciais

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Atualizar reservas do recurso depois que ele é reservado em um projeto

Depois de adicionar um recurso genérico ou nomeado a uma equipe de projeto, você pode alterar as reservas do recurso.

1. Na página **Projetos**, na guia **Equipe**, selecione um membro da equipe e, por fim, selecione **Manter Registros**.

    ![Quadro de Agendamento aberto para o membro da equipe selecionado](media/Resource-Management-image40.png)

    O Quadro de Agendamento aparece e mostra as reservas do membro da equipe do projeto. Expanda o registro do membro da equipe para exibir as horas que foram reservadas em relação a esse projeto e outros projetos que estão consumindo a capacidade do membro da equipe.

2. Selecione e arrastre a reserva para estendê-la ou encurtá-la. Uma caixa de diálogo **Criar Reserva de Recursos** aparece e permite ajustar a reserva.

    ![Caixa de diálogo Criar Reserva de Recursos](media/Resource-Management-image41.png)

3. Clique com o botão direito do mouse na reserva. É possível usar o menu de atalho para concluir as seguintes ações:

    - Alterar o status da reserva.
    - Editar a reserva.
    - Substituir um recurso na equipe do projeto.

### <a name="change-the-booking-status"></a>Alterar o status da reserva

Você pode alterar qualquer status de reserva padrão ou personalizada.

![Comando Alterar Status](media/Resource-Management-image42.png)

Os seguintes status são incluídos no PSA:

- **Cancelado** – esse status cancela uma reserva do recurso e libera a capacidade do recurso.
- **Reserva Fixa** – esse status consome a capacidade de um recurso. Geralmente, uma reserva tem esse status quando você abre **Manter Reservas** na grade **Todos os Membros da Equipe** na página **Projetos**.
- **Reserva Flexível** – esse status adiciona um recurso a uma equipe, mas não consome a capacidade do recurso. Ele indica que o recurso foi reservado para trabalho potencial, mas ainda tem capacidade se for necessário para outros trabalhos. Na exibição da disponibilidade geral do recurso, as reservas flexíveis têm um status diferente de reservas fixas.
- **Proposto** – esse status representa uma proposta do gerente de recursos ou gerente de projeto para um recurso. As propostas não consomem a capacidade de um recurso, e o recurso não é adicionado à equipe do projeto. Para fazer uma reserva fixa do recurso na equipe, o gerente de projeto deve aceitar a proposta.

### <a name="submit-resource-requests"></a>Enviar solicitações de recursos

As solicitações de recurso são usadas para transmitir a demanda (requisito de recurso) que deve ser atendida por um gerente de recursos. Para um recurso genérico que já está na equipe, você pode enviar uma solicitação de recurso diretamente. Uma solicitação de recurso pode ser atendida de duas maneiras:

- O gerente de recursos atende à solicitação diretamente. Nesse caso, o recurso genérico é substituído por uma reserva fixa que tem um recurso nomeado.
- O gerente de recursos propõe um recurso para o gerente de projeto, e o gerente de projeto aprova ou rejeita o recurso proposto.

#### <a name="direct-fulfillment-of-resource-requests"></a>Atendimento direto das solicitações de recurso

Quando um requisito de recurso é gerado, um gerente de projeto pode enviar uma solicitação de recurso para um recurso genérico selecionando o recurso e **Enviar Solicitação**.

![Botão Enviar Solicitação](media/Resource-Management-image45.png)

Os comentários sobre o recurso podem ser fornecidos ao gerente de recursos que está atendendo à solicitação. Depois que a solicitação é enviada, o campo **Status** do membro da equipe é alterado para **Enviado**.

![Inserindo comentários opcionais](media/Resource-Management-image46.png)

Quando o gerente de recursos atende à solicitação, o membro da equipe genérico é substituído pelo recurso nomeado na grade **Todos os Membros da Equipe**.

![Membro da equipe genérico substituído pelo recurso nomeado na grade Todos os Membros da Equipe](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Usar uma proposta de recurso para solicitações de recurso

Em vez de reservar diretamente um recurso em uma solicitação de recurso, um gerente de recursos pode propor um recurso ao gerente de projeto. Um gerente de recursos pode usar essa opção quando uma correspondência exata para os requisitos não está disponível. Quando um gerente de recursos propõe um recurso, o gerente de projeto vê se o campo **Status** para o membro da equipe genérico foi alterado para **Precisa de Revisão**.

![Status do membro da equipe genérico alterado para Precisa de Revisão](media/Resource-Management-image48.png)

Para exibir o recurso proposto com uma visualização do efeito da reserva da proposta, clique duas vezes no membro da equipe que tem um status de **Precisa de Revisão**. Em seguida, selecione a guia **Recursos Propostos**.

![Guia Recursos Propostos](media/Resource-Management-image49.png)

Selecione **Aceitar Todas as Propostas** para aceitar todos os recursos propostos ou **Rejeitar Todas as Propostas** para rejeitá-las. Se você aceitar os recursos propostos, eles serão reservados fixamente no projeto como membros da equipe e substituirão os recursos genéricos.

> [!NOTE]
> Você deve aceitar ou rejeitar todos os recursos propostos. Não é possível aceitá-los ou rejeitá-los parcialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituir um recurso na equipe do projeto

Às vezes, o gerente de projeto deve substituir um membro da equipe registrado em um projeto.

1. Na página **Projetos**, na guia **Equipe**, selecione o recurso que precisa de um substituto e selecione **Manter Reservas**.
2. Expanda o recurso para exibir os projetos aos quais ele está atribuído.

    ![Recurso expandido para mostrar projetos atribuídos](media/Resource-Management-image50.png)

3. Clique com o botão direito do mouse no projeto e selecione **Substituir Recurso**.
4. Se você souber o recurso que deseja substituir para o recurso atual, selecione ou digite o nome e selecione **Reatribuir**.

    ![Especificando um recurso substituto](media/Resource-Management-image51.png)

    Se preferir, siga estas etapas para procurar um recurso:

    1. Selecione **Localizar Substituição**.

        ![Procurando um recurso substituto](media/Resource-Management-image52.png)

        O Assistente de Agendamento retorna uma lista de substitutos disponíveis. No Assistente de Agendamento, você ainda pode filtrar os recursos disponíveis para localizar um substituto adequado.

        ![Lista de substitutos disponíveis](media/Resource-Management-image53.png)

    2. Para substituir o recurso, selecione o recurso desejado e, em seguida, **Substituto**.

        ![Recurso substituto selecionado](media/Resource-Management-image54.png)

    As reservas e atribuições são substituídas pelo novo recurso.

    ![Reservas e atribuições substituídas pelo novo recurso](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Reconciliar reservas e atribuições do membro da equipe

Para membros da equipe, reservas e atribuições são livremente combinadas. Em outras palavras, os recursos podem ter atribuições, mas nenhuma reserva, ou podem ter reservas, mas nenhuma atribuição. De maneira ideal, reservas e atribuições devem ser alinhadas para que os recursos tenham capacidade confirmada para executar as atribuições de tarefa. No entanto, as reservas podem ser baseadas na disponibilidade e as durações das tarefas podem ser alteradas conforme o projeto continua. Portanto, a livre combinação de reservas e atribuições proporciona flexibilidade.

O PSA tem uma guia **Reconciliação** que permite aos gerentes de projeto reconciliar reservas dos membros da equipe e suas atribuições para equipes de projeto.

![Guia Reconciliação](media/Resource-Management-image56.png)

A guia **Reconciliação** mostra reservas e atribuições até o nível da atribuição de tarefas individual para cada membro da equipe. Ela mostra horas em células que representam períodos, desde meses até dias.

A guia também mostra um total líquido geral para o projeto com uma coluna de total.

Para cada recurso, a guia calcula a diferença entre as reservas do membro da equipe e um valor acumulado das atribuições de tarefas do membro da equipe. O ideal é que essa diferença seja 0 (zero). Em outras palavras, não deve haver diferença entre as reservas e as atribuições. As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:

- **Falta de reserva** – a falta de reserva ocorre quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, um gerente de projeto pode querer corrigir essa condição estendendo as reservas do recurso para cobrir o déficit.
- **Reservas em excesso** – ocorrem quando um recurso é reservado para o projeto, mas não é atribuído a tarefas. Essa condição pode ser aceitável nos casos onde o recurso foi reservado para o projeto antes da atribuição da tarefa. No entanto, em outros casos, o recurso não foi planejado para ser atribuído a tarefas. Nesses casos, o gerente de projetos deve considerar o cancelamento das reservas do recurso, para que a capacidade possa ser usada em outro projeto.

Em alguns casos, quando você exibe tempo em um nível mais alto do que o nível de dia (por exemplo, o nível de mês), é possível ver uma diferença líquida de zero para um recurso (em outras palavras, reservas = atribuições). No entanto, se você exibir o tempo no nível de semana, será possível ver que há atribuições de zero horas e reservas de 40 horas na primeira semana, mas as atribuições de 40 horas e reservas de zero horas na segunda semana. De modo geral, as reservas e atribuições são reconciliadas, mas elas diferem de uma semana para a outra.

Ao exibir tempo em níveis mais altos, as células na guia **Reconciliação** têm um indicador para informar que há diferenças em níveis mais baixos. Ao clicar duas vezes em uma célula, você pode ampliar para exibir a diferença. É possível clicar com o botão direito do mouse para reduzir. Ao selecionar um recurso e usar o controle **Próxima diferença** na barra de ferramentas da grade, você pode ir para a próxima diferença entre reservas e atribuições para esse recurso. Você pode usar o controle **Diferença anterior** para voltar. Também é possível desativar o indicador de diferença e o comportamento da navegação em **Configurações**.

![Indicador de diferença](media/Resource-Management-image57.png)

Se você tiver atribuições de tarefa para um recurso, mas nenhuma reserva, na página **Projetos**, na guia **Reconciliação**, selecione a falta de reserva e, em seguida, **Estender Reserva**. A caixa de diálogo **Estender Reserva** aparece e mostra a reserva que é necessária para suprir a falta do recurso. Ela também mostra as reservas existentes do recurso em todos os projetos ou outras entidades que podem ser agendadas. Se você selecionar **OK** a fim de criar a reserva para o recurso, independentemente da disponibilidade desse recurso, é possível haver reservas em excesso.

![Caixa de diálogo Estender Reserva](media/Resource-Management-image58.png)

O gerente de projeto ou o gerente de recursos pode usar o Quadro de Agendamento para gerenciar situações em que um recurso é reservado em excesso além de sua capacidade.


[!INCLUDE[footer-include](../includes/footer-banner.md)]