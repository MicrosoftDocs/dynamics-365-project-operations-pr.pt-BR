---
title: Visão geral das estruturas de detalhamento de trabalho
description: Uma estrutura de detalhamento de trabalho (WBS) é uma descrição do trabalho que será feito para um projeto. É uma hierarquia de tarefas que representa o entendimento da equipe do projeto da composição do trabalho, e do tamanho, custo e duração de cada componente ou tarefa.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eddaf8a868845bde11c8bb7bc04f63777d628cf4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369407"
---
# <a name="work-breakdown-structures-overview"></a>Visão geral das estruturas de detalhamento de trabalho

[!include [banner](../includes/banner.md)]

Uma estrutura de detalhamento de trabalho (WBS) é uma descrição do trabalho que será feito para um projeto. É uma hierarquia de tarefas que representa o entendimento da equipe do projeto da composição do trabalho, e do tamanho, custo e duração de cada componente ou tarefa. Uma WBS tem três objetivos maiores:

-   Descrever os detalhes ou composição do trabalho nas tarefas.
-   Agendar o trabalho do projeto.
-   Estimar o custo de cada tarefa.

O nível de detalhe em uma WBS depende do nível de precisão necessário nas estimativas e o nível de rastreamento necessário comparado a essas estimativas. Projetos com baixa tolerância para erros na agenda ou custo geralmente precisam de uma WBS mais detalhada, e rastreamento diligente de progresso do trabalho e custo comparado com WBS. Esse tipo de projeto é comum nas empresas de construção e engenharia. 

Em contraste, projetos em empresas como mídia e propaganda, software e infraestrutura de TI tendem a ser diferente e a produtividade é relativa à experiência e competência do indivíduo realizando a tarefa. Portanto, essas empresas usam uma WBS para obter uma aproximação do tamanho de um projeto, não para rastrear o progresso desse projeto em detalhe. 

Criar uma WBS é um processo intenso, geralmente realizado em um longo período, e requer colaboração e informações de muitas pessoas. Este tópico descreve como você pode usar os aprimoramentos da WBS para atender aos seus requisitos de estimativa e rastreamento.

## <a name="prerequisites-for-creating-a-wbs"></a>Pré-requisitos para criar uma WBS
Para criar uma WBS, você deve ser capaz de criar uma agenda de trabalho e estimar o custo do trabalho.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Pré-requisitos para criar uma agenda de trabalho

Para usar as funcionalidades de agendamento com sucesso dos recursos da WBS, conclua a configuração a seguir:

1.  Configurar um calendário padrão e um calendário de projeto:
    1.  Clique em **Gerenciamento de projetos e contabilidade** &gt; **Configuração** &gt; **Parâmetros de gerenciamento de projetos e contabilidade** &gt; **Agendamento**. No campo **Calendário padrão**, especifique um calendário padrão. Esse será o calendário padrão para qualquer novo projeto criado.
    2.  Você pode mudar o calendário padrão para um projeto específico. Clique na página de detalhes do projeto e, em seguida, na Guia Rápida **Equipe do projeto e agendamento**, atualize o campo **Calendário de agendamento** selecionando outro calendário.

2.  Configure os dias úteis e o horário comercial. O calendário que você define como o calendário padrão para seu projeto será usado na WBS para determinar as informações a seguir:

-   Dias úteis e feriados
-   O número de horas no horário comercial em um dia

Para configurar os dias úteis e horário comercial para um calendário, ou para criar um novo calendário, clique em **Administração da empresa** &gt; **Comum** &gt; **Calendários**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Pré-requisitos para estimar o custo de trabalho

Para usar as funcionalidades de estimativa de custo por completo da WBS, você deve configurar os custos e preços de vendas para trabalhadores, categorias de trabalho, despesas, tarifas e itens.

-   Para configurar preço de custo e vendas de trabalho, despesas e categorias de tarifa, clique em **Gerenciamento de projetos e contabilidade** &gt; **Configuração** &gt; **Preços**.
-   Para configurar o custo e preço de vendas de itens, use a página **Contratos comerciais** para cada item na página de lista **Produtos lançados** no Gerenciamento de informações de produto.

## <a name="creating-a-wbs"></a>Criando uma WBS
Criar uma WBS envolve três atividades:

1.  **Detalhamento de trabalho** – Cria um detalhamento de trabalho em pedaços gerenciáveis ou tarefas.
2.  **Agenda de trabalho** – Estima o tempo necessário para concluir uma tarefa, definir interdependências de tarefa e selecionar o início e fim das datas da tarefa.
3.  **Estimativa de custo** – Estima custos para cada tarefa.

As seções a seguir abordam como as funcionalidades da WBS podem ajudar com cada uma dessas atividades.

### <a name="work-decomposition"></a>Detalhamento do trabalho

Criar um detalhamento ou decomposição de trabalho geralmente é a primeira etapa do processo de criar uma WBS. A funcionalidade da WBS oferece suporte às bases de criação para detalhamento ou decomposição de trabalho. 

**Tarefa raiz do projeto** A tarefa raiz do projeto é a tarefa de resumo de nível superior de um projeto. Todas as outras tarefas do projeto são criadas nele. O nome da tarefa raiz sempre é definido para o nome do projeto. O esforço, as datas e a duração do nó raiz resumem os valores para as tarefas abaixo da tarefa raiz. Você não pode modificar as propriedades do nó raiz ou excluí-las.

**Resumo ou tarefas de contêiner** Uma tarefa de resumo é uma tarefa que tem subtarefas ou tarefas constituintes nela. Uma tarefa resumo não tem nenhum esforço de trabalho nem custo próprio. Em vez disso, o esforço de trabalho e custo de uma tarefa de resumo são a soma do esforço de trabalho e custo de suas tarefas constituintes. A data de início mais anterior das tarefas-membro é usada como data de início da tarefa de resumo, e a data de término mais posterior das tarefas-membro é usada como a data final. Você pode modificar o nome de uma tarefa de resumo, mas você não pode modificar as propriedades de agendamento para esforço, datas e duração. Se você excluir uma tarefa de resumo, todas as respectivas tarefas de membro também serão excluídas. 

**Tarefas de nó folha** Uma tarefa de nó folha representa o pacote de trabalho mais detalhado do projeto. Um nó folha tem um esforço estimado, um número planejado de recursos, datas de início e de término e uma a duração. 

Você pode concluir as operações de hierarquia a seguir para habilitar a criação de uma hierarquia de trabalho ou detalhamento para um projeto. 

**Nova tarefa** Qualquer nova tarefa criada é adicionada automaticamente ao nó raiz e um número da WBS é atribuído automaticamente à tarefa. O número da WBS representa o nível da tarefa na hierarquia. Para tarefas no primeiro nível sob a tarefa raiz do projeto, um esquema de numeração 1, 2, 3... é usado. Para tarefas que estão sob o primeiro nível, um esquema de numeração 1.1, 1.2, 1.3... é usado. Para cada nível adicionado no nível anterior, uma nova série de números com ponto é adicionada. 

Atualmente, você não pode personalizar os números da WBS. 

**Tarefa de recuo** Quando você recua uma tarefa, ela se torna filha da tarefa que a precede. O número da WBS da nova tarefa filho é recalculado automaticamente com base no número da WBS de seu novo pai. A tarefa pai agora é um resumo ou tarefa contêiner e, portanto, torna-se um acúmulo de suas tarefas constituintes. 

> [!NOTE] 
> Quando você recua tarefas sob uma tarefa que era um nó folha antes da operação de recuo, a tarefa de resumo recém-criada perde suas próprias datas, esforço e número de recursos. Agora, ele usa um resumo dos valores de suas novas tarefas membro. 

**Recuar tarefa para a esquerda** Quando você recua uma tarefa para a esquerda, não é mais uma tarefa constituinte de seu pai. O número da WBS da tarefa é recalculado automaticamente para refletir o novo nível da tarefa na hierarquia. O esforço, o custo e as datas da tarefa pai anterior são recalculados para excluir essa tarefa. 

**Mova para cima e Mova para baixo** Quando você clica em **Mover para baixo** e **Mover para baixo**, você altera a posição de uma tarefa na hierarquia de seu pai. A posição de uma tarefa não afeta o esforço, o custo, as datas ou a duração da tarefa. No entanto, o número da WBS da tarefa é recalculado automaticamente para refletir a nova posição da tarefa.

### <a name="schedule-estimation"></a>Agendar estimativa

A estimativa do agendamento geralmente é a segunda etapa na criação de uma WBS. Como prática recomendada, você deve concluir a estimativa do agendamento depois de criar as tarefas. A página **Estrutura de detalhamento de trabalho** em Finanças tem duas seções. O painel superior destina-se à estimativa do agendamento, e o painel inferior inclui uma guia **Custos e receitas estimados** que você pode usar para estimativa de custos. 
**Dependências de tarefas** Em uma WBS, você pode criar um relacionamento predecessor entre as tarefas. Quando os valores predecessores são atribuídos a tarefas, a tarefa pode ser iniciada apenas depois que todas suas tarefas predecessoras tiverem sido concluídas. A data de início planejada da tarefa é automaticamente definida para a data mais recente de todas as suas predecessoras. 

**Agendamento de tarefas** Os seguintes fatores determinam a programação das tarefas do nó folha:

-   Antecessores
-   Esforço
-   O número de recursos
-   Datas de início e término

A data de início de uma tarefa de nó folha que não possui predecessoras é automaticamente definida para a data de início do agendamento do projeto. A duração de uma tarefa de nó folha é sempre calculada como o número de dias úteis entre as datas de início e término. 

*<strong><em>Regras de agendamento</em></strong>* Quando a assistência de agendamento automática está ativada, as seguintes regras se aplicam ao agendamento de tarefas para tarefas de nó folha:

-   As datas de início e término de uma tarefa devem ser dias úteis, de acordo com o calendário de agendamento do projeto.
-   A data de início de uma tarefa que tem predecessoras é definida automaticamente para data de término mais recente de suas predecessoras.
-   O esforço para uma tarefa é calculado automaticamente da seguinte forma:

Número de pessoas × Duração × Número de horas em u m dia de trabalho comum no calendário do projeto. 

Em alguns casos, talvez você queira desconsiderar essas regras. Você pode desativar o agendamento automático para evitar que o Financeiro configure ou corrija automaticamente quaisquer propriedades das tarefas do nó folha. Quando você insere informações para uma tarefa que causa uma violação de qualquer regra de agendamento, um ícone de erro de agendamento é mostrado para a tarefa. Se você não quiser que erros de programação sejam exibidos, clique em **Erros de programação são mostrados** para desligar o recurso. 

> [!NOTE] 
> Os valores de um resumo ou tarefa de contêiner continuam a ser calculados como a soma dos valores das tarefas constituintes, independentemente da assistência ao agendamento automático estar ligada ou desligada. 

**Corrigindo erros de programação** Quando a assistência de agendamento automático está ativada, não é provável que ocorram erros de agendamento. No entanto, se você desativar a assistência de agendamento automático e ligá-la novamente mais tarde, ícones de erro de agendamento podem aparecer na WBS. 

**Corrigindo erros de agendamento por tarefa** Quando você clica duas vezes no ícone de erro de agendamento para uma tarefa específica, uma caixa de diálogo exibe todos os erros de agendamento para essa tarefa. Você pode decidir quais erros de agendamento corrigir para a tarefa. 

**Corrigindo todos os erros de programação** Se você deseja que o Financeiro corrija todos os erros de agendamento na WBS, no Painel de Ação, clique em **Corrigir todas as discrepâncias de programação**. 

> [!NOTE] 
> Este recurso pode causar modificações significativas na WBS. Os erros são corrigidos na seguinte ordem:

1.  O esforço estimado em todas as tarefas é modificado para que seja igual à capacidade definida no calendário do projeto.
2.  A data de início de cada tarefa é modificada para que a tarefa comece depois que todas as tarefas predecessoras forem concluídas.
3.  A data de início de cada tarefa é modificada para remover lacunas nas datas de início das tarefas predecessoras.

### <a name="cost-estimation"></a>Estimativa de custo

Como foi mencionado anteriormente neste documento, você insere a estimativa de custo para cada tarefa de nó folha usando a guia **Custos e receitas estimados** no painel inferior da página **Estrutura de detalhamento de trabalho**. 

> [!NOTE] 
> Você não pode modificar a estimativa de custo para um resumo ou tarefa de contêiner. A estimativa de custo para uma tarefa de resumo é igual à soma da estimativa de custo de suas tarefas de nó folha. O custo total estimado para cada tarefa é calculado como a soma dos valores de custo estimados para os seguintes tipos de transação:

-   Trabalho
-   Item ou material
-   Despesas

Um tipo de transação **Taxa** é usado para estimar a receita baseada em taxas. Este tipo de transação não possui um componente de custo e, portanto, não é considerado quando os custos são estimados. 

O tipo de transação **Em conta** é usado para registrar o valor de vendas contratado em um tipo de projeto de valor fixo. Este tipo de transação também não é considerado quando os custos são estimados. 

Ao estimar os custos de mão de obra, material e despesas de cada tarefa, você deve atribuir uma categoria de projeto ao custo estimado. 

**Estimando custos de mão de obra** Para cada tarefa de nó folha, você atribui um esforço de trabalho em horas e uma categoria padrão. Portanto, quando você configura uma programação para uma tarefa, a estimativa de custo de mão de obra para essa tarefa é automaticamente adicionada à categoria padrão de mão de obra. Esta estimativa de custo é exibida na guia **Custos e receitas estimados** na grade **Detalhes da linha** para essa tarefa. Se você precisar de mais estimativas de custo de mão de obra, pode adicioná-las nesta guia. Se você aumentar ou diminuir as horas na estimativa de custo de mão de obra, a programação da tarefa será recalculada automaticamente. 

**Estimando despesas e custos de material** A guia **Custos e receitas estimados** também permite estimar despesas e custos de material para uma tarefa, se você precisar de estimativas. 

O custo e preço de venda para cada linha de estimativa de mão de obra ou despesa são baseados na configuração que é definida para cada categoria nas tabelas de preços em **Gestão e contabilidade de projetos** &gt; **Configuração** &gt; **Preços**. Para itens, custo e preço de vendas são adicionados por padrão do item ou acordos comerciais na página de lista **Produtos lançados** no gerenciamento de informação de produtos.

## <a name="tracking-progress-on-the-wbs"></a>Acompanhamento do progresso na WBS
Alguns setores acompanham o andamento de um projeto em relação a uma WBS em um nível muito granular, enquanto outros acompanham o andamento em um nível mais alto da WBS. Esta seção descreve como você pode usar o rastreamento da WBS para os requisitos do seu projeto. 

Finanças tem três visões para a WBS de um projeto: a visão de planejamento, visão de rastreamento de esforço e visão de rastreamento de custos.

### <a name="planning-view"></a>Visão de planejamento

A visualização de Planejamento exibe a estimativa planejada ou de linha de base da programação e as informações de custo. Embora não haja recursos para rastrear a versão e a linha de base para uma WBS do projeto, os valores nesta exibição têm a intenção de representar a versão da linha de base. As seções Estimativa de cronograma e Estimativa de custo deste tópico descrevem essa visão e como ela é usada para criar uma WBS.

### <a name="effort-tracking-view"></a>Exibição de Acompanhamento de Esforço

A exibição Acompanhamento de esforço mostra o acompanhamento de progresso para tarefas na WBS. Ela compara as horas de esforço reais acumuladas para uma tarefa com as horas de esforço planejadas. As fórmulas a seguir fornecem os valores na visualização de rastreamento de esforço:

-   Porcentagem de progresso = Esforço real até o momento ÷ Esforço planejado para a tarefa
-   Esforço restante (também conhecido como estimativa para completar \[ETC\]) = Esforço planejado - esforço real até a data
-   Estimativa ao término (EAT) = Esforço restante + Esforço real até o momento
-   Variação de esforço projetada = Esforço planejado – EAT

A visualização de rastreamento de esforço exibe uma projeção da variação de esforço para a tarefa, com base em se EAC é mais ou menos do que o esforço planejado:

-   Se a EAT for maior do que o esforço planejado, a projeção é de que a tarefa levará mais tempo do que foi planejado e está atrasada.
-   Se a EAT for menor do que o esforço planejado, a projeção é de que a tarefa levará menos tempo do que foi planejado e está adiantada.

**Replanejamento do esforço do gerente de projeto** Ocasionalmente, o gerente de projeto ou outra pessoa que está acompanhando o andamento de um projeto terá que revisar as estimativas originais de uma tarefa. A tarefa pode estar se movendo mais rápido ou mais devagar do que o inicialmente previsto por vários motivos. Por exemplo, o escopo foi reduzido ou os trabalhadores têm menos experiência do que o planejado originalmente. Projeções são a percepção do gerente de projeto de estimativas, com base no estado atual em um projeto. Em geral, você não deve mudar o número de linha de base, porque uma linha de base representa um documento publicado para o agendamento de projeto e estimativa de custo que todos os participantes no projeto concordaram com. 

Gerentes de projetos pode modificar o esforço em tarefas de duas maneiras:

-   Modifique o esforço restante que é definido automaticamente para atualizar o esforço restante real na tarefa.
-   Modifique a porcentagem de progresso que é definida automaticamente para atualizar o progresso real na tarefa.

Ambas abordagens causam o recálculo de ETC, EAT, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAT, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e sua variação de esforço projetado é atualizado. 

**Esforço modificado em tarefas de resumo** Você pode modificar o esforço em tarefas de resumo ou contêiner. Independentemente de você modificar esses valores usando o esforço restante ou a porcentagem de progresso nas tarefas de resumo, os cálculos ocorrem automaticamente na ordem a seguir:

1.  A EAT, a ETC e a porcentagem de progresso na tarefa são calculadas.
2.  A nova EAT é distribuída até as tarefas filho na mesma proporção em que o valor da EAT original.
3.  O novo EAT em cada tarefa de nó folha é calculado.
4.  O esforço restante e a porcentagem de progresso são recalculados para todas as tarefas filho afetadas, com base no novo valor de EAT. A variação de esforço das tarefas também é recalculada.
5.  O EAT das tarefas de resumo também é recalculado a partir dos nós folha.

Clique **Expandir para o nível** na visão Rastreamento de esforço para definir o nível no qual rastrear e manter sua WBS. A WBS é automaticamente expandida para esse nível na exibição de rastreamento de esforço sempre que você a abre.

### <a name="cost-tracking-view"></a>Exibição Acompanhamento de custo

A visão Rastreamento de custo exibe o rastreamento do consumo de custo para uma tarefa. Nesta visão, o custo real gasto em uma tarefa até o momento é comparado ao custo planejado da tarefa. As fórmulas a seguir fornecem os valores na visualização de rastreamento de custo:

-   Porcentagem de custo consumido = Custo real até o momento ÷ Custo planejado para a tarefa
-   Custo até a conclusão (CTC) = Custo planejado – Custo real até o momento
-   Estimativa completa (EAT) = CTC + Custo real até a data
-   Variação de custo projetada = Custo planejado – EAT

A visualização de rastreamento de custo exibe uma projeção da variação de custo para a tarefa, com base em se EAC é mais ou menos do que o custo planejado:

-   Se a EAT for maior do que o custo planejado, a projeção é de que a tarefa use mais dinheiro do que foi planejado e está acima do orçamento.
-   Se a EAT for menor do que o custo planejado, a projeção é de que a tarefa use menos dinheiro do que foi planejado e está abaixo do orçamento.

**Replanejamento de custo do gerente de projeto** Os gerentes de projeto devem usar o CTC para revisar a estimativa de custo original de uma tarefa. O gerente de projeto pode modificar o valor CTC para o custo necessário para concluir a tarefa. Se você modificar o valor de CTC, o CTC, EAT da tarefa e a porcentagem de custo consumido e a variação de custo projetada em uma tarefa são recalculados. A EAT, a ETC e a porcentagem de custo consumido nas tarefas de resumo também são recalculadas e sua variação de custo projetado é atualizado. 

> [!NOTE] 
> Quando você revisa o esforço para uma tarefa de WBS na exibição de rastreamento de esforço, o CTC, EAT da tarefa, a porcentagem de custo consumido e a variação de custo projetada são recalculados na exibição de rastreamento de custo. No entanto, as revisões de custo não afetam os valores na visão Rastreamento de esforço, porque o custo por tipo de transação (mão de obra, material ou despesa) ou categoria de projeto não é revisado. 

**Revisão de projeção de custos em tarefas de resumo** Você pode revisar os custos em tarefas de resumo e os cálculos ocorrem automaticamente na seguinte ordem:

1.  O EAT, CTC e porcentagem do custo consumido na tarefa são recalculados.
2.  A nova EAT é distribuída até as tarefas filho na mesma proporção em que a EAT original nas tarefas.
3.  O novo EAT para cada tarefa é calculado.
4.  O CTS e a porcentagem de custo consumido são recalculados para as tarefas filho afetadas, com base no valor EAT. A variação de custo das tarefas também é recalculada.
5.  O EAT para todas as tarefas de resumo é recalculado com base nessa alteração.

Clique **Expandir para o nível** na visão Rastreamento de custo para definir o nível no qual rastrear e manter sua WBS. A WBS é expandida para esse nível na exibição de rastreamento de Custo sempre que você a abre.

### <a name="earned-value-management"></a>Gerenciamento de valor agregado

Você pode usar o método de valor agregado (EVM) para controlar o andamento de um projeto. Você pode visualizar as métricas de valor agregado no Centro de Funções do gerente de projeto. O componente do gráfico de valor agregado mostra os valores divididos em fases do valor planejado e do custo real. O valor ganho na data atual é mostrado como um ponto. Os dados divididos em fases para o valor agregado não estão disponíveis no momento. 

A fase de tempo no gráfico de valor agregado é exibida por semana ou por mês. Esta seção descreve os três pilares do EVM: valor planejado, valor agregado e custo real. 

**Valor planejado** A teoria EVM afirma que o gráfico do valor planejado representa a taxa em que a equipe do projeto planejou ganhar valor no projeto. 

O departamento de finanças usa a regra de ganho 0:100 ao criar o valor planejado. Sob esta regra, o valor da tarefa é postado na tarefa a partir de sua data de término. Nenhum valor é postado até que a tarefa seja 100% concluída. 

Em Gerenciamento e contabilidade de projeto, você insere a data de término dos nós folha e o custo planejado para eles. Quando o gráfico do valor planejado é exibido por semana, o valor planejado é resumido por semana para todas as tarefas do nó folha para a duração do projeto. 

**Valor agregado** A teoria EVM afirma que o gráfico do valor agregado representa a taxa em que a equipe do projeto está ganhando realmente valor no projeto. 

O departamento de finanças usa a regra de ganho 0:100 ao criar o valor recebido. Sob esta regra, o valor da tarefa é postado na tarefa a partir de sua data de término. Nenhum valor é postado até que a tarefa seja 100% concluída. 

Quando o valor agregado é calculado, a porcentagem de progresso de cada tarefa é considerada. De acordo com a regra de ganho de 0:100, apenas as tarefas concluídas em um determinado período são consideradas para o cálculo do valor agregado no final desse período. O valor agregado no projeto é calculado para todas as tarefas que foram concluídas quando o gráfico é criado. 

> [!NOTE] 
> Atualmente, o sistema de rastreamento de WBS não possui estruturas de dados para armazenar porcentagens históricas de progresso em cada tarefa. Portanto, o valor agregado pode ser relatado apenas a partir do momento em que o cubo é processado. Processe o cubo regularmente para atualizar os dados de valor agregado que são mostrados no Centro de Funções. 

**Custo real** A teoria EVM afirma que o gráfico de custo real representa a taxa na qual o dinheiro está sendo gasto no projeto. 

As transações lançadas em um projeto são usadas para traçar a linha de custo real. Os custos são resumidos por data. Esses dados são então usados para representar graficamente os custos reais por semana ou por mês no gráfico de valor agregado.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Como usar os conceitos de valor planejado, valor agregado e custo real

**Variação de cronograma** Durante o planejamento, você cria uma previsão de trabalho em uma linha do tempo. Portanto, o valor planejado é a taxa na qual os planejadores do projeto pensaram que o trabalho seria concluído no projeto. Depois que um projeto está em andamento, o trabalho é concluído e o projeto ganha valor. Ao comparar o valor planejado com o valor agregado, você pode ver como o trabalho em um projeto está progredindo. O resultado dessa comparação é chamado de variação de cronograma. 

Se o valor planejado para um período for maior do que o valor agregado, a quantidade de trabalho que foi feito em um projeto é menor do que o planejado. Portanto, o projeto está atrasado. Como o valor planejado e o valor agregado são expressos em termos monetários, o tempo de atraso no projeto também recebe um valor monetário. 

Se o valor planejado para um período for menor do que o valor agregado, a quantidade de trabalho que foi feito em um projeto é maior do que o planejado. Portanto, o projeto está adiantado. Esse prazo de entrega também recebe um valor monetário.

**Variação de custo** Como o valor agregado usa o preço de custo como multiplicador, o valor agregado indica o custo do trabalho realizado em um projeto. Conforme o projeto avança, o log de transações fornece um registro do dinheiro que é realmente gasto naquele projeto. Ao comparar o valor ganho com o custo real, você pode ver a quantidade de dinheiro que está sendo gasta em comparação com o valor que é ganho. O resultado dessa comparação é chamado de variação de custo. 

Se o custo real gasto em um período for maior do que o valor ganho, mais dinheiro foi gasto do que ganho. Portanto, o projeto está acima do orçamento. 

Se o custo real gasto em um período for menor do que o valor ganho, mais dinheiro foi ganho do que gasto. Portanto, o projeto está abaixo do orçamento.

## <a name="wbs-templates"></a>Modelos da WBS
Você pode usar a funcionalidade de modelos da WBS para criar modelos padrão para projetos. Se os projetos que sua empresa oferece envolvem muito trabalho repetível, você deve considerar a criação de um modelo de WBS. 

Você pode criar um modelo de WBS a partir da WBS de um projeto existente, de modo que o conhecimento e as melhores práticas reunidas durante o planejamento desse projeto possam ser reutilizados em projetos semelhantes no futuro. No entanto, às vezes, pode não fazer sentido salvar toda a WBS como um modelo. Portanto, você também pode criar modelos de partes da WBS para um projeto.

### <a name="saving-a-projects-wbs-as-a-template"></a>Salvar a WBS de um projeto como um modelo

Depois de criar um modelo, você pode importá-lo para uma nova WBS do projeto no nó raiz ou em qualquer tarefa na WBS do projeto.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importando um modelo da WBS para a WBS de um projeto

Quando você importa tarefas, as tarefas no modelo são organizadas com base na data de início da tarefa sob a qual foram importadas. Durante a importação, os relacionamentos do predecessor nas tarefas de modelo são usados para calcular as datas de início das tarefas importadas. O calendário de trabalho padrão do projeto de destino é aplicado para computar as datas de término das tarefas importadas, de forma que os dias úteis e as horas de trabalho padrão definidas no calendário de trabalho do projeto atual sejam retidos. 

Valores de custo e preços de venda nas linhas de estimativa são aplicados para garantir que os preços que são específicos para o projeto ou contrato de projeto tenham datas válidas.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Diferenças entre a WBS de um projeto e um modelo de WBS

-   As tarefas nos modelos de WBS não têm datas de início e término.

Os dias úteis e não úteis não estão definidos para os modelos de WBS.

-   Os modelos de WBS sempre usam o calendário de agendamento que é configurado como o calendário padrão para todos os projetos.

O calendário de programação padrão é usado apenas para descobrir as horas em um dia de trabalho padrão.

-   Os relacionamentos do predecessor não são copiados para um modelo de WBS.

Como os modelos de WBS não têm datas, a lógica da data de início baseada na data de término de um predecessor não é necessária.

-   Uma linha de estimativa de custo de mão de obra é criada automaticamente quando uma tarefa é criada em um modelo de WBS. O preço de venda e o valor do custo são copiados do trabalhador selecionado.

Despesas e custos de itens podem ser criados manualmente, assim como na WBS de um projeto.

-   Erros de programação são exibidos quando há desvios da seguinte fórmula:

Esforço = Número de recursos × Duração × Número de horas em um dia de trabalho padrão 

Você pode corrigir todos os erros de programação ao mesmo tempo clicando em **Corrigir todos os erros de agendamento**. 

Como alternativa, você pode corrigir erros de agendamento individualmente clicando no ícone de aviso para cada tarefa.





[!INCLUDE[footer-include](../includes/footer-banner.md)]