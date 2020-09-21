---
title: Alocação de recursos para projetos
description: Este tópico fornece informações sobre a alocação de recursos para projetos.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749011"
---
# <a name="project-resourcing"></a>Alocação de recursos para projetos

[!include [banner](../includes/banner.md)]

Este tópico fornece informações sobre a alocação de recursos para projetos.

Um desafio para gerentes de projeto e de recursos durante o estágio de planejamento do projeto é a alocação de recursos, em que eles devem determinar e reservar o recurso correto para trabalhar em um projeto. No Dynamics 365 Finance, a funcionalidade de alocação de recursos para projetos permite definir funções que são tratadas como recursos temporários que podem ser reservados para um compromisso específico ou parte de um compromisso. Esse tipo de alocação de recursos permite que os gerentes de projeto e de recursos concluam as seguintes tarefas:

- Definir uma função que tenha as competências necessárias, para que seja fácil corresponder os recursos.
- Usar funções para definir uma agenda de compromissos inicial baseada em recursos reservados.
- Estimar os custos e determinar um orçamento inicial, com base nas funções e recursos atribuídos a um projeto.
- Usar funções para estimar o número de reservas de recursos necessárias para cada compromisso.
- Estimar o número de recursos necessários para todo o ciclo de vida de um projeto.
- Elaborar uma estrutura de detalhamento de trabalho (WBS) usando as atribuições iniciais de recursos.

[![Ciclo de vida do projeto](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

À medida que continua o planejamento do projeto, os recursos planejados podem ser substituídos por pessoas da equipe. O gerente de projeto também pode voltar e atualizar as reservas de recursos durante qualquer estágio do projeto.

## <a name="set-up-project-resources"></a>Configurar recursos do projeto
Você deve configurar um calendário e associá-lo a um funcionário ou colaborador. O calendário é usado para agendar o projeto e o horário de trabalho dos recursos reservados para o projeto. Durante a configuração do calendário, os gerentes de projeto podem fazer o nivelamento de recursos como parte da otimização de recursos. Com base na agenda do calendário, podem ser colocadas restrições aos recursos. Você pode configurar um calendário na página **Calendários**.

Ao configurar um funcionário como recurso do projeto, você pode selecionar entre os funcionários que trabalham na empresa para a qual você está configurando os recursos. Você também pode selecionar funcionários de outras empresas em sua organização. Esses funcionários são conhecidos como recursos intercompanhia.

Os procedimentos a seguir explicam como configurar um funcionário como um recurso de projeto na sua empresa e como configurar um recurso de projeto intercompanhia.

### <a name="set-up-a-worker-as-a-project-resource"></a>Configurar um funcionário como um recurso do projeto

1. Na página **Funcionários**, na lista **Funcionários**, selecione o funcionário que você está adicionando como um recurso de projeto e abra o registro dele.
2. No Painel de ação, selecione **Projeto** &gt; **Configuração** &gt; **Configuração do projeto**.
3. Selecione um calendário e feche a página.

Você também pode especificar projetos padrão para um recurso como um tipo de atribuição prévia. As atribuições prévias podem ser usadas quando o gerente de recursos ou de projeto sabe com antecedência em quais projetos o recurso estará trabalhando. As atribuições prévias também podem ser baseadas na solicitação de um patrocinador ou cliente do projeto. Para fazer a atribuição prévia de um projeto, na página **Atribuir projetos**, na guia **Projetos**, na lista **Projetos pendentes**, selecione o projeto apropriado.

### <a name="set-up-an-intercompany-resource"></a>Configurar um recurso intercompanhia

Ao configurar um funcionário como um recurso intercompanhia, você deve concluir a configuração na empresa que faz e na que toma o empréstimo.

**Na empresa que faz o empréstimo**

1. No Finance, verifique se a empresa que faz o empréstimo está selecionada e conclua o procedimento da seção anterior, "Configurar um funcionário como um recurso do projeto".
2. Na página **Contabilidade intercompanhia**, selecione **Novo**.
3. No campo **ID de entidade legal**, selecione a empresa que faz o empréstimo. Preencha os campos restantes conforme apropriado e, em seguida, selecione **Salvar**.
4. Na página **Preço de transferência**, selecione **Novo**.
5. No campo **Entidade legal que toma o empréstimo**, selecione a empresa apropriada.
6. Para emprestar à empresa que toma o empréstimo apenas o recurso que você criou no início desta seção, no campo **Recurso**, selecione o nome do recurso que você criou. Para colocar todos os recursos da empresa que faz o empréstimo à disposição da empresa que o toma, deixe o campo **Recurso** em branco.
7. Na página **Parâmetros de gerenciamento e contabilidade de projeto**, na guia **Intercompanhia**, defina a opção **Habilitar quadro de horários e agendamento de recursos intercompanhia** como **Sim**.

**Na empresa que toma o empréstimo**

- Na página **Lista de recursos**, no filtro de pesquisa, insira o nome do recurso que você criou para a empresa que faz o empréstimo para verificar se o nome está incluído na lista de recursos para a empresa que o toma.

## <a name="manage-resource-competencies"></a>Gerenciar as competências dos recursos
As competências dos recursos são uma parte essencial do gerenciamento de recursos. Elas podem ser usadas como base para determinar os recursos que têm o equilíbrio correto entre habilidades, formação, certificação e experiência em projetos. Você deve configurar essas informações para cada recurso e atualizá-las regularmente. Dessa forma, é possível maximizar as habilidades quando as competências de recursos específicos são correspondidas durante a atribuição de recursos do projeto.

[![Exemplos de habilidades, certificações, formação e experiência em projetos](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Os procedimentos a seguir explicam como configurar algumas das competências para um recurso.

Para configurar as competências de um funcionário, você pode usar a página de lista **Funcionários** em Recursos Humanos ou a página de lista **Recursos** em Gerenciamento e contabilidade de projeto. Para os procedimentos a seguir, a página de lista **Funcionários** em Recursos Humanos é usada.

### <a name="set-up-competencies-certificates"></a>Configurar competências: certificados

1. Na página de lista **Funcionários**, selecione a linha para a qual o funcionário deseja adicionar informações sobre certificados.
2. No Painel de ações, na guia **Funcionário**, no grupo **Competências**, selecione **Certificados**.
3. Selecione **Novo** e, no campo **Tipo de certificado**, selecione **PMP**.
4. No campo **Data de início**, selecione **01/10/2015** e **Salvar**.

### <a name="set-up-competencies-skills"></a>Configurar competências: habilidades

1. Na página de lista **Funcionários**, certifique-se de que o funcionário que você usou no procedimento anterior ainda está selecionado. Então, no Painel de ações, na guia **Funcionário**, no grupo **Competências**, selecione **Habilidades**.
2. Selecione **Novo**.
3. No campo **Habilidade**, selecione **Gerenciamento de projetos**.
4. No campo **Nível**, selecione **5 Especialista**.
5. No campo **Data do nível**, selecione **14/01/2014**.
6. No campo **Anos de experiência**, digite **10**.
7. Selecione **Salvar** e feche a página.

## <a name="create-a-new-project"></a>Criar um novo projeto
1. Na página **Gerenciamento de projetos**, selecione **Novo projeto** e insira estes valores:

    - **Tipo de projeto:** Tempo e material
    - **Nome do projeto:** Atualização do XYZ fase 2
    - **Grupo de projeto:** TM\_WIP
    - **ID do contrato de projeto:** 00000002

2. Selecione **Criar projeto**.

### <a name="assign-a-resource-to-a-project"></a>Atribuir um recurso a um projeto

1. Na página **Funcionários**, na lista **Funcionários**, selecione o registro do funcionário para o qual você anteriormente configurou as competências e abra o registro dele.
2. No Painel de ações, na guia **Projeto**, no grupo **Configuração**, selecione **Atribuir projetos**.
3. Na página **Atribuições de projetos de validação de recursos**, na guia **Projetos**, no campo **Adicionar o projeto aos projetos selecionados**, filtre pelo projeto **Atualização do XYZ fase 2**.
4. No painel **Projetos pendentes**, selecione um projeto e, em seguida, selecione o botão de seta para adicioná-lo ao painel **Projetos selecionados**.

Você também pode atribuir categorias a um recurso conforme sua necessidade. O tipo de categoria é **Custo** ou **Receita**. O tipo de categoria é determinado por sua organização. Se nenhuma categoria for atribuída a um recurso, o Finance procurará a categoria padrão nos preços por hora para custo e receita.

### <a name="set-up-project-resource-and-role-characteristics"></a>Configurar as características da função e recurso do projeto

Um gerente de projeto pode usar a funcionalidade de alocação de recursos do projeto para criar as funções necessárias para o projeto. As funções podem ser usadas se os recursos confirmados ainda forem desconhecidos quando os estiverem sendo reservados. As funções podem ser reservadas temporariamente como recursos planejados, para que você possa continuar as etapas de planejamento do projeto.

[![Exemplo de uma função](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Cenário:** a Contoso foi contratada para concluir um projeto de tempo e material que tem um termo de abertura aprovado. O gerente de projeto júnior ainda está preenchendo o escopo do projeto. O gerente de recursos está no momento identificando recursos específicos que serão reservados para trabalhar no novo projeto. Devido à natureza crítica do projeto, o patrocinador dele solicitou um gerente de projeto sênior como uma das funções. O gerente de recursos deve encontrar o novo recurso e definir a função no sistema, caso o gerente de projeto júnior precise das informações do recurso durante o planejamento do projeto.

As etapas a seguir mostram como o gerente de recursos pode configurar a função de gerente de projeto sênior e associar características de recursos a ela. Posteriormente, a função poderá ser usada para pesquisar recursos disponíveis que correspondam às competências de recursos necessárias.

1. Na página **Configurar funções**, selecione **Novo** e insira estes valores:

    - **ID da função:** Gerente de projeto sênior
    - **Descrição:** Gerente de projeto sênior

2. Selecione **Criar**.
3. Selecione a função **Gerente de projeto sênior** e, em seguida, **Configurar características**.
4. No campo **Tipo de característica**, selecione **Habilidade**.
5. No campo **Características disponíveis**, insira a habilidade para pesquisar.
6. No campo **Tipo de característica**, selecione **Certificado**.
7. No campo **Características disponíveis**, insira o tipo de certificado para pesquisar.

### <a name="assign-a-project-resource-to-a-project"></a>Atribuir um recurso a um projeto

1. Na página **Todos os projetos**, selecione o projeto **Atualização do XYZ fase 2**.
2. Na guia **Equipe do projeto e agendamento**, selecione **Adicionar**.
3. No campo **Função**, selecione **Membro da equipe**.
4. Selecione **Reservar do calendário**.
5. Na página **Disponibilidade do recurso**, selecione **Configurações de exibição**.
6. Na página **Ajustar configurações de exibição**, insira os seguintes valores:

    - **Formato da exibição do intervalo de datas:** Dia
    - **Exibir descrições de disponibilidade:** Sim
    - **Exibir capacidade restante:** Sim

7. Na lista de recursos, selecione um recurso.
8. Selecione **Reserva fixa** e **Capacidade total**.


### <a name="assign-a-resource-to-a-default-role"></a>Atribuir um recurso a uma função padrão

Para ajudar os gerentes de projeto ou de recursos, é possível se aprofundar mais nos recursos que podem ser reservados para um projeto. Você pode associar uma função padrão a um recurso existente ou a um recurso recém-adquirido. Por exemplo, quando Daniel foi contratado, ele tinha a experiência e as habilidades para preencher a função de analista de negócios. O gerente de recursos atribuiu essa função como a função padrão de Daniel. Portanto, o gerente de recursos adicionou Daniel a um grupo de analistas de negócios que estão disponíveis para trabalhar em projetos.

Durante a reserva de recursos, os gerentes de projeto podem filtrar os recursos de função que estão disponíveis para trabalhar em projetos. Eles podem usar essas informações como um critério ao realizar análises de decisão de vários critérios durante o preenchimento de recursos. Eles também podem adicionar outras características de recurso ao filtro para pesquisar recursos que tenham habilidades, formação e experiência específicas para um determinado projeto.

**Cenário:** um projeto aprovado foi iniciado e a função de gerente de projeto sênior foi reservada como um recurso planejado durante o estágio de planejamento do projeto. O gerente de recursos agora encontrou um recurso para ocupar a função de gerente de projeto sênior.

1. Na página **Lista de recursos**, selecione **Daniel Goldschmidt**.
2. Na página **Função do recurso**, selecione **Novo** e insira estes valores:

    - **Efetivo:** insira a data atual.
    - **Expiração:** insira **Nunca**.
    - **Função:** insira **Gerente de projeto sênior**.

3. Selecione **Salvar** e feche a página.
4. Na guia **Competências**, adicione a habilidade **ProjectMgmt** e o certificado **PMP**.

## <a name="set-up-role-based-pricing"></a>Configurar o preço baseado em função
Todos os preços de custo, venda e transferência podem ser configurados para funções.

1. Na página **Preço de venda (hora)**, selecione **Novo** e insira uma data de início.
2. Na coluna **Função**, selecione uma função.
3. Na coluna **Preço**, insira um preço para a função de recurso selecionada.

## <a name="form-a-project-team"></a>Formar uma equipe de projeto
Para usar as funções que foram configuradas anteriormente em um projeto, um gerente de projeto deve associar as funções ao projeto. Várias funções podem ser atribuídas a um projeto. Para evitar confusão, essas funções são automaticamente rotuladas durante a reserva. Por exemplo, se o gerente de projeto precisa de três engenheiros de software, três funções de engenheiro de software com os rótulos **engenheiro de software 1**, **engenheiro de software 2** e **engenheiro de software 3** serão geradas automaticamente. Se as características da função foram definidas anteriormente para a função, elas são aplicadas como um filtro durante as pesquisas de um recurso. Características adicionais podem ser adicionadas conforme necessário para refinar ainda mais a pesquisa.

As configurações de exibição também podem ser personalizadas para exibir melhor a disponibilidade de recursos. Existem opções para mostrar a disponibilidade horária, diária, semanal, mensal, trimestral e anual. Também há uma opção para mostrar a capacidade disponível e restante dos recursos. Essa opção é útil para gerenciamento de horas, ao estimar o tempo disponível para atividades ou disponibilidade de recursos.

O gerente de projeto pode selecionar uma função na página e, em seguida, se houver um recurso disponível que atenda ao requisito, selecionar para reservar um recurso para preencher a função. Observe que os recursos não precisam ser reservados nesse ponto do estágio de planejamento. Ao criar uma WBS, você pode substituir funções por recursos de equipe para o projeto. Se as funções forem substituídas por recursos de equipe na WBS, a configuração do recurso atualiza automaticamente o agendamento e a lista da equipe do projeto.

[![Lista da equipe do projeto que inclui funções e recursos reais](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

O gerente de projeto tem várias opções para reservar um recurso para um projeto, como **Capacidade restante**, **Capacidade total**, **Porcentagem de capacidade** e **Especificar horas**. Essas opções de reserva podem ser canceladas a qualquer momento se as atribuições de recursos forem alteradas. Dois tipos de reserva são compatíveis:

- **Reserva fixa**: a reserva de recurso foi aprovada e confirmada para trabalhar no compromisso pelo período especificado.
- **Reserva flexível**: a reserva de recurso foi configurada para tentar trabalhar no compromisso pelo período especificado.

O seguinte procedimento explica como criar uma equipe de projeto.

### <a name="create-a-project-team"></a>Criar uma equipe de projeto

1. Na página de lista **Todos os projetos**, selecione um projeto e, em seguida, **Editar**.
2. Na guia **Equipe do projeto e agendamento**, no campo **Data de término do agendamento**, insira a data de início do agendamento mais um mês. Por exemplo, se a data de início do agendamento for 24 de junho de 2017 (24/06/2017), insira **24/07/2017**.
3. Selecione **Adicionar**.
4. No painel **Adicionar funções ao projeto**, no campo **Função**, selecione **Gerente de projeto sênior**.
5. Selecione **Competências necessárias**.
6. Na página **Escolher características**, as características que você configurou anteriormente para a função de gerente de projeto sênior são selecionadas por padrão. Selecione **OK**.
7. Na página **Adicionar funções ao projeto**, no campo **Número de recursos**, digite **1**.
8. No campo **Recurso**, a pesquisa mostra todos os recursos que possuem as competências necessárias. Selecione **Daniel Goldschmidt** e, em seguida, **Criar**.
9. Na página **Projeto**, selecione **Adicionar**.
10. No painel **Adicionar funções ao projeto**, no campo **Função**, selecione **Membro da equipe**. No campo **Número de recursos**, insira **5**.
11. Selecione **Criar**.
12. Na página **Projetos**, selecione **Preencher recurso**.

## <a name="resource-capacity-synchronization"></a>Sincronização da capacidade dos recursos
Os processos de sincronização de recursos ajudam a garantir que as informações do calendário e do calendário base se encaixem no agendamento de recursos do projeto. Se o calendário for alterado, os processos farão as atualizações necessárias no agendamento dos recursos do projeto. Os processos também ajudam a melhorar o desempenho, porque as informações dos recursos do calendário são sincronizadas com antecedência. Portanto, as atualizações nas informações de agendamento de recursos ocorrem mais rapidamente. Recomendamos que você agende os processos em lote, em vez de um de cada vez. Caso contrário, existe o risco de alguém se esquecer das datas inclusivas da última sincronização das informações. Se não forem usadas datas inclusivas, podem ocorrer lacunas durante a sincronização de datas.

![Sincronização de calendário](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizar acúmulos de capacidade dos recursos

O processo de sincronização foi projetado para sincronizar todas as informações do calendário de recursos. Essas informações incluem informações básicas do calendário sobre quaisquer alterações na tabela de capacidade do calendário de recursos do projeto. Se novos recursos forem adicionados ao projeto, a sincronização ajudará a garantir que as informações atualizadas do calendário estejam disponíveis. Essa sincronização pode ser feita a qualquer momento.

É recomendável usar atualização em lote. As opções estão disponíveis durante a sincronização das reservas de capacidade.

1. Selecione **Gerenciamento e contabilidade de projeto** &gt; **Periódico** &gt; **Sincronização de capacidade** &gt; **Sincronizar acúmulos de capacidade de recursos**.
2. Defina as opções na tabela a seguir.

    | Opção      | Descrição |
    |-------------|-------------|
    | Código de período | Opcionalmente, selecione o código de intervalo de datas do razão geral para definir as datas de início e de término do processo de sincronização para os acúmulos de capacidade de recursos. |
    | Data de Início  | Insira a data de início do processo de sincronização para os acúmulos de capacidade de recursos. |
    | Data de término    | Insira a data de término do processo de sincronização para os acúmulos de capacidade de recursos. |

[![Processo de sincronização](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Configurar funções em modelos de WBS
Os gerentes de projeto podem configurar modelos de WBS que podem ser aplicados ao criar uma WBS para novos projetos. Os gerentes de projeto podem adicionar funções ao criar um modelo. Use o procedimento a seguir para atribuir uma função a um modelo de WBS.

1. Selecione **Gerenciamento e contabilidade de projetos** &gt; **Configuração** &gt; **Projetos** &gt; **Modelos de estrutura de detalhamento de trabalho**.
2. Selecione **Detalhes** para um modelo de WBS selecionado.
3. Selecione uma tarefa na lista e, em seguida, no campo **Função**, selecione uma função para atribuir à tarefa.

### <a name="work-with-a-wbs"></a>Trabalhar com uma WBS

Você pode criar uma nova WBS ou copiar uma WBS de um modelo de WBS existente. Um gerente de projeto pode gerenciar facilmente os recursos atribuindo funções a novas tarefas na WBS. As funções podem ser substituídas após a aquisição de um recurso ou após a identificação de um recurso confirmado para trabalhar na tarefa. Essa flexibilidade permite que os gerentes de projeto realizem as seguintes tarefas:

- Identificar o número de recursos necessários para os pacotes de trabalho da WBS.
- Estimar os custos do projeto.
- Determinar um orçamento preliminar.
- Estimar a duração da atividade, com base em funções e recursos.
- Desenvolver alguns planos de gerenciamento de projeto, com base nas informações de projeto disponíveis.

Outras opções foram adicionadas à WBS para usar melhor a funcionalidade de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Atribuições de recursos</td>
<td>Visualize os recursos atribuídos, as datas, o número de horas e tipo de reserva para tarefas na WBS.</td>
</tr>
<tr class="even">
<td>Gerar equipe automaticamente</td>
<td>Adicione recursos planejados automaticamente usando funções associadas a uma tarefa. O Finance sugere automaticamente recursos planejados usando análise de decisão de vários critérios baseada em funções. Depois que as funções e o esforço (horas) forem definidos para as tarefas em uma WBS, e depois que a estrutura for liberada, selecione <strong>Gerar equipe automaticamente</strong>. O número necessário de recursos planejados é adicionado à WBS e à guia <strong>Equipe do projeto e agendamento</strong>.</td>
</tr>
<tr class="odd">
<td>Recurso (lista suspensa)</td>
<td>Na página <strong>Abrir formulário de atribuição de recursos</strong>, você pode selecionar recursos para reserva fixa ou flexível, com base na duração especificada. Você pode ajustar as configurações de exibição para ver e definir a duração das atividades dos recursos. Você pode selecionar e atribuir recursos no nível do pacote de trabalho usando as seguintes opções:
<ul>
<li><strong>Aceitar</strong>: confirmar as alterações no recurso atribuído a uma tarefa.</li>
<li><strong>Cancelar</strong>: cancelar as alterações no recurso atribuído a uma tarefa.</li>
<li><strong>Atribuir automaticamente</strong>: um recurso da equipe disponível que possui uma função correspondente é automaticamente selecionado e atribuído à tarefa selecionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na página **Todos os projetos**, selecione o projeto **Atualização do XYZ fase 2**.
2. Selecione **Planejar** &gt; **Atividades** &gt; **Estrutura de detalhamento de trabalho**.
3. Selecione **Nova** para adicionar as seguintes atividades de nível um à WBS:

    - Iniciando
    - Planejamento
    - Executando
    - Monitoramento e controle
    - Fechar

4. Defina as datas e o esforço (horas), conforme mostrado na ilustração a seguir.

    [![Definir as datas e o esforço](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selecione a linha de tarefa **Iniciando** e, em seguida, no campo **Função**, selecione **Gerente de projeto sênior**.
6. Selecione **Publicar**.
7. Na mesma linha, no campo **Recurso**, selecione **Daniel Goldschmidt** e, em seguida, **Aceitar**.
8. Selecione a linha de tarefa **Planejamento** e, em seguida, no campo **Função**, selecione **Analista de negócios**.
9. Selecione **Publicar** e, em seguida, **Gerar equipe automaticamente**.
10. Na caixa de mensagem que é exibida, selecione **Sim**.
11. No campo **Recurso**, verifique se o valor é **Analista de negócios 1**.
12. Para o recurso **Analista de negócios 1**, abra a pesquisa e selecione **Iniciar atribuições de recursos**. Em seguida, selecione um funcionário para a tarefa.
13. Selecione **Atribuição flexível** &gt; **Capacidade total**.

    > [!NOTE] 
    > Você não recebe um aviso de que o recurso especificado agora é o 2, porque o número de recursos permanece 1.

14. Na página **Estrutura de detalhamento de trabalho**, valide a atribuição de recursos na WBS e selecione **Salvar**.

## <a name="resource-fulfillment-for-planned-resources"></a>Preenchimento de recursos para recursos planejados
Um gerente de projeto pode planejar as funções de recursos necessárias para um projeto. O gerente de recursos verá esses recursos planejados como solicitações na página **Preenchimento de recursos** e pode atribuir recursos reais.

1. Na página **Todos os projetos**, selecione o projeto **Atualização do XYZ fase 2**.
2. Selecione **Projeto** e selecione **Editar**.
3. Na guia **Equipe do projeto e agendamento**, selecione **Adicionar**.
4. Na caixa de diálogo **Adicionar funções**, selecione a função **Desenvolvedor de software**.
5. Selecione **Criar** e feche a página do projeto.
6. Na página **Preenchimento de recurso**, selecione **Desenvolvedor de software 1** para o **Projeto de atualização do XYZ fase 2**.
7. Selecione um funcionário e, em seguida, **Atribuir**.
8. Verifique se a linha de **Desenvolvedor de software 1** foi removida para o **Projeto de atualização do XYZ fase 2**.
9. Na guia **Equipe do projeto e agendamento**, para o projeto **Atualização do XYZ fase 2**, verifique se o funcionário que você selecionou na etapa anterior foi adicionado como **Desenvolvedor de software**.

## <a name="requests-for-project-resources"></a>Solicitações de recursos do projeto
A funcionalidade de agendamento de recursos do projeto permite apenas que os gerentes de recursos distribuam recursos de equipe em compromissos ou projetos. Para ativar essa funcionalidade, conclua as seguintes tarefas ou verifique se elas foram concluídas:

- Configurar sequências numéricas.
- Configurar fluxos de trabalho de gerenciamento e contabilidade de projeto.
- Habilite fluxos de trabalho de solicitação de recursos.

Após a conclusão das tarefas anteriores, você poderá concluir as seguintes tarefas conforme necessário:

- Criar uma solicitação de recurso a partir de um recurso em equipe com reserva flexível.
- Monitorar as solicitações de recursos.
- Preencher solicitações de recursos.
- Solicitar um recurso de equipe de uma WBS.
- Reservar recursos para um projeto sem ter uma solicitação de um recurso de equipe.

## <a name="monitor-project-teams"></a>Monitorar equipes de projeto
1. Na página **Todos os projetos**, selecione o link da **ID do projeto** para o projeto **Atualização do XYZ fase 2**.
2. Na FastTab **Equipe do projeto e agendamento**, verifique se os recursos do projeto listados estão corretos.
