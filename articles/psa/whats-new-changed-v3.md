---
title: Novidades ou alterações no Project Service Automation versão 3
description: Este artigo inclui informações sobre o que há de novo e o que foi alterado no Project Service Automation versão 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d076e270f426131119eab097e7f359c228edb51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926578"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Novidades ou alterações no Project Service Automation versão 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]



Este artigo inclui informações sobre as alterações feitas na UI (interface do usuário), nas funcionalidades e na terminologia do Project Service Automation entre a versão 2 ou 1 e a versão 3.

## <a name="project-scheduling"></a>Agendamento de projetos
O agendamento de projetos, que era conhecido como WBS (estrutura de detalhamento de trabalho) nas versões anteriores, foi renomeado para Agendar, e pode ser acessado clicando na guia **Agendar**. 

![Agendamento de projetos.](media/psa-schedule-01.png)

A agenda agora tem uma nova superfície de interação moderna e acessível. No entanto, o mecanismo de agendamento subjacente do Project Service Automation não foi alterado. Os botões de controle na faixa de opções da grade da agenda permitem interagir com a agenda de maneira semelhante à versão anterior do Project Service Automation. Outras alterações à agenda incluem:

- **Gráfico de Gantt** - O gráfico de Gantt não está mais presente. Uma nova visualização de Gantt será oferecida em uma atualização futura.
- **Cabeçalhos de coluna** - Você pode ocultar os cabeçalhos das colunas na grade clicando no indicador para baixo ao lado do título da coluna. 
- **Colunas** - É possível exibir colunas ocultas clicando em **Adicionar coluna**. 
- **Categoria da transação** - Uma pesquisa por **Categoria da transação** foi adicionada à grade da agenda e será exibida por padrão. 
 
## <a name="project-templates"></a>Modelos de projeto
As alterações a seguir foram realizadas na funcionalidade de modelo do projeto.

### <a name="create-a-project-template"></a>Criar um modelo de projeto 
Você pode criar um modelo de projeto na versão 3 de maneira semelhante à das versões anteriores do Project Service Automation. O modelo pode conter apenas uma agenda, e ela pode incluir atribuições, mas elas não são obrigatórias. Se a agenda tiver atribuições, elas poderão ser somente para recursos genéricos. É possível gerar requisitos de recurso para recursos genéricos, mas eles não poderão ser reservados com recursos reais no modelo. Não é possível reservar um recurso real para uma equipe em um modelo. 

### <a name="create-a-template-from-an-existing-template"></a>Criar um modelo com base em um modelo existente
Ao criar um modelo de projeto com base em um modelo existente no Project Service Automation versão 3, ocorre o seguinte: 

- A agenda do projeto de origem é copiada no modelo. 
- Os recursos genéricos são copiados para a equipe e todas as atribuições de recursos genéricos também são copiadas. Os requisitos para os recursos genéricos não são copiados. 

### <a name="create-a-template-from-an-existing-project"></a>Criar um modelo com base em um projeto existente
Ao criar um modelo de projeto com base em um projeto existente, ocorre o seguinte: 

- A agenda do projeto de origem é copiada no modelo. 
- Os recursos genéricos são copiados para a equipe e todas as atribuições de recursos genéricos são preservadas. Os requisitos para os recursos genéricos não são copiados.    
- Os recursos nomeados, atribuídos ou não atribuídos, são removidos da equipe e substituídos por recursos genéricos.
- As informações do cliente são removidas, se houver. 
- As referências às cotações e aos contratos são removidas, se houver. 

### <a name="create-a-project-from-a-template"></a>Criar Projeto a Partir do Modelo
Ao criar um projeto com base em um modelo no Project Service Automation versão 3, ocorre o seguinte:

- A agenda, a equipe e as atribuições são copiadas para o novo projeto.   
- A data de início é a data da cópia ou a data selecionada pelo usuário.   
- Para os membros de equipe genéricos com requisitos de recurso no modelo, os requisitos não são copiados nem gerados automaticamente. Será necessário gerá-los. 

## <a name="copy-a-project"></a>Copiar um projeto
Ao copiar um projeto com base em um modelo no Project Service Automation versão 3, ocorre o seguinte: 

- A data de início estimada é copiada, mas pode ser alterada.  
- A agenda e as tarefas do projeto são copiadas. 
- Os recursos genéricos e suas atribuições são copiados. Os requisitos de recurso para os recursos genéricos não são copiados. Você deverá gerá-los novamente. 
- Os recursos reais e suas atribuições não são copiados. Em vez disso, eles são substituídos por recursos genéricos. 
- Os dados reais não são copiados para o novo projeto. 

## <a name="move-a-scheduled-project"></a>Mover um projeto agendado
Ao mover o agendamento de um projeto existente, ocorre o seguinte: 

- As datas da tarefa são movidas automaticamente para corresponder ao período da movimentação. 
- Os recursos genéricos atribuídos são preservados.   
- Se tiverem sido gerados antes de o projeto ser movido, os requisitos do recurso genérico continuarão aos mesmos e não serão gerados de novo automaticamente. Você deverá gerá-los novamente para refletir as novas atribuições devido à movimentação da tarefa. 
- As atribuições de recursos reais são alteradas para corresponder à movimentação de datas da tarefa. As reservas de recursos reais não são alteradas. Você deverá alterar as reservas usando a exibição de reconciliação. 
- Os recursos da equipe com reservas, mas sem atribuições, não são alterados. 
- Os dados reais não são movidos. 

## <a name="estimates"></a>Estimativas
As estimativas foram divididas em duas guias, **Atribuição de recurso** e **Estimativas**. A guia **Atribuição de recurso** contém as estimativas de esforço e mostra as atribuições do recurso para as tarefas em uma exibição em fases de tempo. Você pode editar as estimativas com base no que foi gerado pelo mecanismo de agendamento.

![Guia Atribuições de recursos mostrando estimativas de esforço e atribuições do recurso para as tarefas.](media/resource-assignments-tab-02.png)

A guia **Estimativas** mostra os valores de custo e vendas das atribuições do recurso. Os valores são somente leitura. Agora, a definição de custo e preço de vendas é derivada das atribuições do membro da equipe na agenda. Isso significa que, se houver uma tarefa sem nenhuma atribuição, ela será exibida sob o bucket não atribuído. Isso também significa que, sem **função**, que é uma dimensão de precificação padrão, não haverá nenhuma estimativa de custo ou vendas se houver um cliente ou um contrato/uma cotação associado ao projeto. 

![Guia Estimativas mostrando valores de custo e venda.](media/estimates-tab-03.png)
  
A categoria também tem suporte em tarefas na exibição de agenda. O agrupamento por categoria na exibição em fases de tempo das estimativas fornecerá uma experiência melhor, especialmente quando você tiver estimativas de despesa em seu projeto. As estimativas de despesa são inseridas usando uma grade em uma guia separada. 

As estimativas de despesa podem ser inseridas na grade da guia **Estimativas de despesas**. 

![Guia Estimativas de despesas mostrando a grade de estimativas de despesas.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Gerenciamento de recursos
No Project Service Automation versão 3, com a nova interface do usuário Cliente Unificado e as alterações nos relacionamentos entre reservas e atribuições, a definição da equipe de um projeto com recursos genéricos ou reais foi alterada significativamente em comparação às versões 2 e 1. Entretanto, os conceitos de recursos reserváveis, **real** e **genérico**, permanecem iguais, assim como os membros da equipe, os requisitos, as atribuições e as reservas.   

![Usando o seletor de recursos.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Atribuir um recurso reservável real 
No Project Service Automation versão 3, as reservas e as atribuições de tarefas não estão tão interligadas quanto nas versões anteriores do Project Service Automation. Você pode usar a grade de equipe para reservar um membro da equipe **real**, de modo semelhante ao mercado.

Usando o seletor de recursos na agenda, você pode selecionar o membro da equipe criado na exibição de equipe e, em seguida, atribuir tarefas a ele. É possível continuar a atribuir tarefas aos recursos, mesmo depois de suas reservas. Use a guia **Reconciliação** para reconciliar membros da equipe que possuem diferenças nas reservas e atribuições.

O seletor de recursos mostrará os membros da equipe para o projeto. Você também pode usar o seletor de recursos para pesquisar e exibir outros recursos reserváveis que não fazem parte da equipe do projeto. Você pode atribuí-los a uma tarefa, e ele passarão a fazer parte da equipe do projeto. Você deverá reservá-los usando a guia **Painel de agendamento** ou a guia **Reconciliação**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Atribuir um recurso genérico reservável a uma tarefa e uma equipe de projeto e, em seguida, preencher com um recurso real por meio do Painel de agendamento 
No Project Service Automation versão 3, a funcionalidade para gerar uma equipe não é usada para recursos genéricos. Em vez disso, você pode criar e atribuir diretamente um recurso genérico com base na agenda, digitando o nome da posição do recurso genérico na célula de recurso da agenda. Ou pode selecionar o ícone de recurso na célula e, em seguida, usando o seletor de recursos, digitar o nome do recurso genérico que deseja criar. Isso abrirá um painel de criação rápida que permite definir a função e a unidade organizacional do membro da equipe de recurso genérico. Depois de criar o recurso, ele será atribuído à tarefa e você poderá continuar a atribuir esse recurso genérico a outras tarefas na agenda.    
 
Quando tiver atribuído o recurso a todas as tarefas apropriadas, você poderá gerar um requisito de recurso e, depois, atendê-lo fazendo a reserva diretamente no **Painel de agendamento** ou enviando uma solicitação de recurso. Também é possível adicionar recursos genéricos diretamente à grade de membro da equipe. 

Os recursos genéricos são adicionados à equipe do projeto sem nenhum requisito de recurso e com as datas de início/término do projeto até que o requisito de recursos seja gerado. Para gerar um requisito, selecione o recurso genérico e clique em **Gerar**. O link de requisito é exibido e as horas necessárias serão preenchidas com as horas atribuídas. Você pode clicar no link para abrir e atualizar o requisito.
  
Quando a reserva for concluída e tiver sido totalmente atendida por um recurso nomeado, o recurso genérico será substituído pelo recurso nomeado e a atribuição na agenda será atualizada com o recurso nomeado. 

Os recursos propostos para os requisitos agora são armazenados em uma guia, em vez de uma seção separada.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Vários recursos nomeados atendendo a um recurso genérico
Quando um requisito é atendido com vários recursos, o recurso genérico permanece na equipe e atribuído à tarefa. Os membros da equipe nomeados que são reservados não são atribuídos como parte da posição. O gerente de projeto pode atribuir o trabalho, conforme apropriado, aos recursos reais.  A exibição **Reconciliação** fornece um detalhamento das reservas entre vários recursos para diversas atribuições de tarefa. Isso não é feito automaticamente porque, em cenários mais complicados, como um em que você tem um pacote de tarefas compondo o requisito, a maneira como o gerente de projeto quer fazer a atribuição deve ser considerada. Como o sistema não pode entender a intenção, as suposições provavelmente serão diferentes das pretensões e um resultado incorreto ou imprevisível será obtido. O resultado previsível é que o recurso genérico permaneça atribuído até que o gerente de projeto atribua deliberadamente os recursos usando a exibição **Reconciliação**.

### <a name="reconciliation"></a>Reconciliação
A guia **Reconciliação** mostra as reservas e todas as atribuições de cada membro da equipe do projeto. A exibição mostra as horas em células que podem representar pontos no tempo, desde meses até dias. Essa exibição permite que os gerentes de projeto reconciliem as reservas dos membros da equipe e suas atribuições para a equipe do projeto. Isso é útil porque as reservas e as atribuições de tarefa não estão rigidamente combinadas, o que permite uma maior flexibilidade ao planejar um projeto. 

![Guia Reconciliação mostrando as reservas e as atribuições dos membros da equipe do projeto.](media/resource-reconciliation-tab-06.png)

Para cada recurso, a exibição calcula a diferença entre as reservas de um membro da equipe e o valor acumulado das atribuições de tarefas desse membro e exibe as duas diferenças a seguir, que podem ocorrer com reservas e atribuições em um projeto: 

- **Falta de reserva** – As faltas de reserva ocorrem quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, um gerente de projeto pode corrigir essa condição estendendo as reservas do recurso para cobrir o déficit. 
- **Reservas em excesso** – As reservas em excesso ocorrem quando um recurso é reservado para o projeto, mas não é atribuído a tarefas.  Essa condição pode ser aceitável se, por exemplo, o recurso tiver sido reservado antes da atribuição de tarefas. Entretanto, em outros casos, talvez não haja um plano de atribuição do recurso, e o gerente de projeto pode considerar o cancelamento das reservas do recurso para permitir que a capacidade seja usada em outro projeto. 

Quando você tem atribuições de tarefas para um recurso, mas nenhuma reserva (uma falta de reserva), é possível selecionar a falta de reserva agregada e clicar em **Estender reserva**. Aqui, é possível verificar a reserva necessária para resolver a falta do recurso e sua disponibilidade. 
 
## <a name="time-and-expense"></a>Tempo e despesa
Esta seção inclui informações sobre as mudanças de tempo, despesas e aprovações no Project Service Automation versão 3. Como parte da solução Dynamics 365 Project Service Automation, o recurso **Entrada de hora** foi atualizado para aproveitar a estrutura da Interface Unificada. Isso permite a entrega de uma interface de usuário consistente e uniforme que segue um design responsivo para uma exibição ideal em qualquer tamanho de tela ou dispositivo. 

### <a name="landing-page"></a>Página de aterrissagem
A experiência de entrada de hora personalizada não extensível foi preterida na versão 3. Em vez disso, agora há uma experiência de grade nativa extensível e acessível. Você pode acessar a funcionalidade de entrada de hora usando o mapa do site à esquerda. Com essa mudança, você não poderá mais inserir horas para uma semana de uma só vez. Em vez disso, deverá criar uma entrada de hora para cada dia na grade. Após a criação de algumas entradas de tempo, os usuários poderão criar entradas de tempo em massa com a função **Copiar** explicada mais adiante neste artigo. 

![Página de aterrissagem de entrada de hora.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Criar novas entradas de hora 
Clique em **Novo** na faixa de opções para abrir uma página de criação rápida de entrada de hora, na qual você deve inserir a duração em minutos, horas ou dias. Para fazer isso, basta começar a digitar h, m ou d juntamente com a quantidade.  

![Criação rápida de entrada de hora.](media/quick-create-time-entry-08.png)

Os campos de pesquisa são apoiados por exibições do sistema. Por exemplo, depois de inserir informações sobre o projeto, o campo **Tarefa do projeto** é definido, por padrão, com a exibição de **Minhas tarefas de projeto abertas**. Para criar entradas de hora para as tarefas que não foram atribuídas ao usuário, clique em **Alterar exibição** na pesquisa e selecione **Todas as tarefas de projeto ativas**. Depois de a entrada de hora ser criada e exibida na grade, você pode editar todos os valores de linha diretamente na grade.  

### <a name="bulk-createcopy"></a>Criar/copiar em massa 
Após criar algumas entradas de hora, é possível usar a funcionalidade de cópia para criar entradas de hora adicionais em massa. Clique em **Copiar** para abrir a caixa de diálogo **Copiar**. Em **Do período: Data de Início**, defina o intervalo de datas do qual os períodos de tempo devem ser copiados. Em **Até o período: Data de Início**, especifique a data em que as entradas devem ser criadas. Clique em **Copiar** para copiar as entradas de hora no dia da semana correspondente indicado em **Até o período**. Por exemplo, a entrada de hora de segunda-feira da semana passada será copiada na segunda-feira da semana indicada em **Até o período**. 

![Copiar entradas de hora em massa.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importar dados 
As atribuições e o Exchange seguem o mesmo padrão da interface do usuário, o que permite que o usuário especifique o intervalo de datas quando as reservas precisam ser importadas. Dessa maneira, você deve selecionar explicitamente as reservas que devem ser copiadas nas entradas de hora de **Rascunho**. Na versão 3, não é mais possível ver o padrão de entradas de hora **Sugerido** na grade e no calendário.  

### <a name="change-in-calendar-control"></a>Alteração no controle de calendário
Na versão 3, deixamos o controle de calendário personalizado e passamos a usar o Calendário UC para exibir as entradas de hora da semana. Nesse calendário, você pode visualizar dia, semana e mês. 

> [!NOTE]
> Uma limitação do Calendário é que esse controle não oferece suporte a ações em itens de calendário individuais. Por exemplo, você não poderá selecionar um ou mais itens de calendário e enviar ou excluir esses itens. Ao clicar em um item de calendário, a página de entidade **Entrada de hora** será aberta para realizar ações adicionais. 

### <a name="extensibility"></a>Extensibilidade do 
**Capturar dados em campos personalizados apenas de entidades de entrada de hora e despesa** - A entrada de hora usar uma grade editável, uma grade somente leitura e controles de calendário da plataforma. Todos esses controles são nativos e, por isso, oferecem suporte a personalizações. No Project Service Automation versão 3, você pode adicionar outros campos personalizados, configurar campos de pesquisa e apoiá-los com exibições personalizadas. Também é possível definir uma lógica de negócios personalizada com base em valores selecionados de campos personalizados.  

**Capturar dados em campos personalizados de entradas de hora e despesa e propagá-los por entidades que suportam o fluxo de envio e aprovação** - O processamento típico de entradas de hora é exibido no diagrama a seguir.

![Processo de fluxo de entrada de tempo.](media/process-time-entries-10.png)

Se os requisitos de negócios estipularem que as entidades de hora e despesa devem capturar as dimensões de preço personalizadas e propagar os valores definidos por um recurso de hora e entrada na dimensão de preço personalizada para todas as entidades na imagem anterior, consulte [Configurar campos personalizados como dimensões de preço](set-up-pricing-dimensions.md).

Para dar suporte aos requisitos de negócios nos quais as entidades de hora e despesa devem capturar as dimensões personalizadas que não são de preço e propagar os valores, você pode usar a configuração de dimensões de preço e indicar as dimensões personalizadas como dimensões de preço sem custo ou taxa de cobrança. Outro cenário seria a adição de um campo personalizado para cada uma das entidades usando o mesmo nome de campo em todas as entidades. Plug-ins personalizados podem ser criados para relacionar os registros nas entidades que estão participando do fluxo de envio/aprovação usando as entidades de origem e conexão da transação.  

### <a name="delegate-time-and-expense-entry"></a>Delegar entradas de hora e despesa
A plataforma Common Data Service não oferece suporte à representação de um usuário por outro, o que significa que, no Project Service Automation versão 3, não há suporte para a entrada delegada de hora e despesa. No entanto, parceiros e clientes utilizaram uma solução alternativa para habilitar o suporte a experiências de entrada de hora delegada na versão 3. Essa solução é apenas uma alternativa, e não uma solução completa. Por isso, é importante entender suas limitações e usar essa abordagem somente se as limitações forem aceitáveis. 

> [!IMPORTANT]
> Essas informações só devem ser consideradas como uma sugestão diretriz para a implementação personalizada por um parceiro/cliente. A equipe do produto não oferecerá suporte formal para essa funcionalidade por meio de nenhum de nossos canais de suporte.

### <a name="customization-details"></a>Detalhes da personalização 
A personalização permite que você adicione um **Recurso reserva** para criar e editar experiências, o que possibilita que um usuário atue como delegado, alterando o campo **Reserva de recursos** para outro usuário para o qual as entradas de hora e despesa precisam ser registradas. As etapas a seguir abordam a delegação da entrada de hora. Essas mesmas informações se aplicam à delegação da entrada de despesa. 
 
1.  Certifique-se de que o usuário delegado possua acesso de segurança global para os projetos e as tarefas dos projetos. 
1.  Como **Recurso reservável**, que é um campo na entidade **Entrada de hora**, não é exibido na página **Criação rápida**, é necessário adicioná-lo.

    -ou-

    Crie uma exibição personalizada, que inclua a coluna **Recurso reservável**, para exibir somente as entradas de hora criadas para o recurso. Publique as personalizações no designer de módulo de aplicativo para que essa exibição apareça sob **Exibir seletor** na página **Entradas de hora**. Existem dois plug-ins que tratam da configuração do gerenciador para entradas de hora que não são do projeto:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Crie um plug-in para substituir o campo **Gerente** pelo gerente do usuário atribuído no campo **Recurso reservável**. Use o mesmo **Estágio de execução** que o plug-in OOB (fora de banda) (pré-validação) e use uma **Ordem de execução** que seja superior à dos plug-ins OOB (maior que 1). Isso garantirá que o plug-in personalizado seja executado depois do plug-ins OOB.  
 
### <a name="end-user-experience"></a>Experiência do usuário final
1.  Ao criar uma entrada de hora na página de criação rápida, insira os detalhes do Projeto e da Tarefa do projeto e, em seguida, selecione o usuário no campo **Recurso reservável** para o qual as entradas de hora devem ser registradas. 
2.  Por padrão, esse campo usa como padrão o usuário conectado; entretanto, considerando que o usuário substituiu esse campo, a entrada de hora agora será criada para o **Recurso reservável** escolhido.
3.  Quando você envia as entradas de hora que criou para esses registros, elas são colocadas em fila para o aprovador do projeto, conforme esperado. 
4.  Quando você recupera as entradas de hora do outro usuário, elas são retornadas em um estado de **Rascunho**, com o campo **Recurso reservável** definido para outro usuário. 
5.  Opcionalmente, você pode alternar para exibição personalizada para filtrar as entradas de tempo hora do outro usuário. 
 
### <a name="limitations"></a>Limitações
As funcionalidades **Copiar** e **Importar** funcionam apenas no contexto do usuário que está conectado. Isso significa que não é possível copiar ou importar entradas de hora que tenham sido criadas para o usuário conectado como recurso reservável.

As entradas de hora que não são para um projeto serão encaminhadas para aprovação para o gerente do recurso reservável apenas se a etapa 4 da seção **Detalhes da personalização** acima tiver sido concluída. Caso contrário, as entradas de hora que não são de projeto do outro usuário serão encaminhadas incorretamente para o gerente do usuário conectado. 

### <a name="other-changes"></a>Outras alterações 
A funcionalidade **Reservas e Tarefas** foi removida. 

## <a name="multidimensional-pricing"></a>Precificação multidimensional
Para maximizar a flexibilidade e atender a diferentes requisitos de negócios, o Project Service Automation versão 3 oferece suporte à aplicação discreta de conjuntos de dimensão de precificação para as taxas de custo e cobrança. Os valores de dimensão podem ser definidos como padrão e, em seguida, propagados no processo de definição de custo e preço, desde a criação do perfil até a entrada de horas e os dados reais do projeto. A configuração específica do cliente e sua modificação ou extensão utilizam a infraestrutura de personalização padrão.

O Project Service Automation é fornecido com um conjunto padrão de dimensões de precificação, funções e unidades de recurso, e ele permite a configuração de preços e custos para cada combinação de função e unidade organizacional.

Para os clientes do Project Service Automation que desejam continuar usando esses campos prontos para uso como dimensões de precificação na versão 3, não haverá nenhuma alteração relevante. Você pode continuar usando o Project Service Automation. No entanto, se precisar definir o preço ou os custos de seus recursos usando outros atributos adicionais, a versão 3 permite adicionar suas próprias dimensões de precificação personalizadas ao Project Service Automation. A extensão das dimensões de precificação personalizadas é uma experiência de configuração complicada. 

## <a name="quotes-and-contracts"></a>Cotações e contratos
No Project Service Automation versão 3, os aspectos de configuração e gerenciamento de cotações e contratos foram alterados. As seções a seguir incluem informações mais detalhadas.

### <a name="set-up-chargeability-options"></a>Configurar opções de encargos
Nas versões 1 e 2, a configuração de encargos para funções e categorias de cotações e contratos específicos era feita usando a exibição **Encargos**, que estava na navegação superior de uma linha de cotação ou uma linha de contrato. Esse também era o local em que você podia configurar os preços para essas funções e categorias de encargos.

A partir da versão 3, a configuração de opções de encargos por função e categoria de despesa será feita no nível da linha de cotação ou contrato. A configuração de preços é separada da configuração de encargos. É possível encontrar **Funções passíveis de cobrança** e **Categorias passíveis de cobrança** como guias das páginas **Linha de cotação** e **Linha de contrato** sem ter de usar a navegação superior.

![Funções passíveis de cobrança.](media/chargeable-12.png)
 
A configuração de Funções passíveis de cobrança e Categorias passíveis de cobrança também utiliza o controle de grade editável pronto para uso. Para cada função e cada categoria, as opções com suporte para o tipo de cobrança durante a fase de cotação e contratação permanecem inalteradas em relação às versões anteriores como **Passível de cobrança** e **Não passível de cobrança**. **Complementar** não é um tipo suportado durante a fase de cotação ou contratação. **Complementar** tem suporte apenas durante a aprovação de horas ou despesas.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Criar e editar precificação personalizada para uma cotação e um contrato de projeto do Project Service Automation
Nas versões 1 e 2, o uso de uma lista de preços personalizada para cotações e contratos específicos era feito por meio de **Editar preços** na exibição **Encargos**. A exibição **Encargos** estava localizada na navegação superior de uma linha de cotação ou uma linha de contrato. Esse também era o local em que você podia configurar as opções de encargos para as categorias de despesas e funções.

A partir da versão 3, a criação e o uso de uma lista de preços de projeto personalizada em uma cotação ou um contrato de projeto do Project Service Automation foram separados da configuração de encargos. A cotação e os contratos de projeto do Project Service Automation têm uma nova guia, chamada **Lista de preços de projetos**. Essa guia mostra uma exibição associada de todas as Listas de preços do projeto que foram anexadas à cotação ou ao contrato do projeto do Project Service Automation. Para criar uma lista de preços personalizada com base em uma lista de preços existente que já está associada a uma cotação ou um contrato do projeto, clique em **Criar precificação personalizada**. Isso criará uma cópia de todas as listas de preços associadas e as anexará à cotação ou ao contrato. Agora, é possível abrir a lista de preços e editar o preço da categoria da função ou da despesa, de modo que essas alterações de preço sejam aplicadas apenas a essa cotação ou a esse contrato. 
  
A imagem a seguir é anterior à criação das listas de preços personalizadas.

![Antes das listas de preços personalizadas.](media/before-custom-price-lists-13.png)

A imagem a seguir é posterior à criação das listas de preços personalizadas.

![Depois das listas de preços personalizadas.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Um pequeno atraso pode ocorrer entre você clicar em **Criar precificação personalizada** e a lista de preços personalizada ser criada. É recomendável atualizar a grade, em vez de clicar várias vezes. Uma lista de preços personalizada será criada se o nome da lista de preços associada tiver o nome da cotação ou o nome do contrato do projeto anexado a ele.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
