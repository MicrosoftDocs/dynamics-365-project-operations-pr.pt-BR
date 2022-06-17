---
title: Estimar vendas e custos do projeto quando um recurso reservável preenche várias funções em um projeto
description: Este artigo explica como usar dimensões de preços para dar suporte a estimativas de preços e custos para um recurso que preenche várias funções em um projeto.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9bb59537aaa75d9003925bec37642a2fa7c9ca22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923450"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimar vendas e custos do projeto quando um recurso reservável preenche várias funções em um projeto 

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - faturamento pro forma, Project Operations para cenários baseados em estoque/produção__ 

As empresas que têm como base projetos frequentemente precisam de um recurso para preencher várias funções em um projeto. Cada função pode ter um preço e um custo diferentes. Isso significa que o mesmo tempo do recurso em um projeto pode ter uma estimativa financeira diferente, dependendo das taxas de custo e cobrança de cada função. Você pode configurar os valores no registro do membro da equipe para o recurso indicado com diferentes substituições em cada uma das tarefas para as quais o membro da equipe está atribuído.

O exemplo a seguir mostra como a substituição simples de um valor permite que um recurso tenha várias funções em um projeto com custos e taxas de cobrança diferentes.

## <a name="create-tasks"></a>Criar tarefas
Para criar tarefas, você precisa adicionar tarefas, bem como tarefas de resumo. Em seguida, você precisa atribuir a tarefa antes de adicionar a duração da tarefa. 

### <a name="add-tasks-and-summary-tasks"></a>Adicionar tarefas e tarefas de resumo
Para adicionar uma tarefa, execute estas etapas.

1. Vamos para **Projetos** e abra o projeto ao qual deseja adicionar tarefas.
2. Selecione **Adicionar nova tarefa**. Dê um nome à tarefa e pressione **Enter**.
3. Insira outro nome de tarefa e pressione **Enter**. Repita isso até que você tenha uma lista completa de tarefas.
3. Para recuar tarefas em tarefas de **Resumo**, selecione os três pontos verticais no nome da tarefa e, em seguida, selecione **Criar subtarefa**. 

  > [!TIP]
  > Para selecionar mais de uma tarefa, selecione uma tarefa, pressione e segure **Ctrl** e selecione outra tarefa.
  >
  > Você também pode escolher **Promover subtarefa** para mover tarefas de debaixo das tarefas de **Resumo**.

### <a name="assign-tasks"></a>Atribuir tarefas

Conclua as etapas a seguir para atribuir tarefas.

1. Na coluna **Atribuído a** de uma tarefa, selecione o ícone de pessoa.
2. Escolha um membro da equipe na lista ou insira um texto para procurar um nome.

### <a name="add-task-duration-and-columns"></a>Adicionar colunas e duração de tarefas

Normalmente, é mais fácil começar a criar seu projeto com duração. Conclua as etapas a seguir para adicionar uma duração de tarefa.

1. Na coluna **Duração** de uma tarefa, digite o número de dias que você acha que levará para realizar a tarefa. Se você quiser usar uma unidade de tempo diferente, digite um número e a palavra **horas**, **semanas** ou **meses**.
2. Se você deseja que sua tarefa apareça como um marco em forma de diamante na exibição **Linha do tempo**, na coluna **Duração**, digite **0 dias**.
3. Pressione **Enter** para ir para o próximo campo **Duração** de tarefa e continue inserindo durações.

  > [!NOTE]
  > Você não pode inserir uma duração para tarefas de resumo.

Você pode adicionar colunas ao seu projeto para fornecer mais detalhes. Para fazer isso, selecione **Adicionar coluna**. 

Para obter mais informações, consulte [Criar um projeto](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar a função e a unidade organizacional para um membro de equipe de projeto genérico
Conclua as etapas a seguir para configurar uma função e unidade organizacional para um membro de equipe genérica.

1. Na página **Tarefas**, selecione a linha **Tarefa** para **Tarefa A**. 
2. Em **Atribuído a**, selecione **Adicionar recurso genérico**. Isso abre a página **Criação Rápida de Membro de Equipe**.
3. Na página **Criação Rápida de Membro de Equipe**, especifique os atributos do membro genérico da equipe que poderá executar essa tarefa.
4. Selecione a função e a unidade organizacional apropriadas e, em seguida, selecione **Salvar e Fechar**. Um membro genérico da equipe é criado e atribuído à tarefa. 
5. Repita as etapas de 1 a 4 para a **Tarefa B**. Contudo, a **Tarefa B** deve ter uma função e unidade organizacional atribuídas ao membro da equipe genérico diferentes da **Tarefa A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Configurar a função e a unidade organizacional para uma tarefa
Conclua as etapas a seguir para configurar uma função e unidade organizacional para uma tarefa.

1. Depois de criar a **Tarefa A**, selecione a tarefa e, em seguida, selecione o ícone **i** para abrir o painel **Detalhes da Tarefa**. 
2. No painel **Detalhes da Tarefa**, role até a parte inferior e selecione **Ver Detalhes** para abrir a página **Detalhes da Tarefa**.
3. Na página **Detalhes da Tarefa**, em **Função** e **Unidade Organizacional**, adicione os valores necessários para executar essa tarefa para o recurso. 

  > [!NOTE]
  > Se você concluir esse cenário usando os dados de demonstração do Project Operations, selecione **Líder de Consultoria** para a função e **Fabrikam US** como unidade organizacional.

4. Selecione a **Tarefa B** e, em seguida, a tarefa.
5. Selecione o ícone **i** para abrir o painel **Detalhes da Tarefa**. 
6. No painel **Detalhes da Tarefa**, role até a parte inferior e selecione **Ver Detalhes** para abrir a página **Detalhes da Tarefa**.
7. Na página **Detalhes da Tarefa**, em **Função** e **Unidade Organizacional**, adicione os valores necessários para um recurso executar essa tarefa. Os valores em **Função** e **Unidade Organizacional** para **Tarefa B** devem ser diferentes daqueles para a **Tarefa A**. 

  > [!NOTE]
  > Se você concluir esse cenário usando os dados de demonstração do Project Operations, selecione **Técnico de Rede** para a função e **Fabrikam US** como unidade organizacional.

8. Salve e feche a página **Detalhes da Tarefa**. 

## <a name="team-member-and-estimates-behavior"></a>Membro da equipe e comportamento de estimativas 
Para entender o comportamento na grade **Membro da Equipe** e as estimativas, conclua as etapas a seguir.

1. Na grade **Membro da Equipe**, selecione os dois membros de equipe genéricos e, em seguida, selecione **Gerar Requisitos**. Isso gerará os requisitos de recursos. 
2. Selecione a linha do membro da equipe para **Líder de Consultoria** e **Reservar**. O quadro da programação é aberto com uma lista de recursos. Selecione um recurso e **Reservar** para reservar o recurso de acordo com esse requisito.
3. Selecione a linha do membro da equipe para **Técnico de Rede** e **Reservar**. O quadro da programação é aberto com uma lista de recursos. Selecione o mesmo recurso selecionado acima e **Reservar** para reservar o recurso de acordo com esse requisito.

### <a name="team-member-grid"></a>Grade Membro da Equipe 

Na grade **Membro da Equipe**, os dois registros de membros de equipe genéricos são excluídos e substituídos por apenas um recurso. Há um conjunto de valores para esse recurso, que é um conjunto de valores padrão para **Função** e **Unidade Organizacional**.

Ao expandir a linha desse registro de membro de equipe, você pode ver atribuições distintas no registro de membro de equipe para as duas tarefas. Cada linha de atribuição tem valores específicos de tarefa para **Função** e **Unidade Organizacional**. 

### <a name="estimates-grid"></a>Grade Estimativas 

Na grade **Estimativas**, as duas atribuições para o mesmo recurso têm preços diferentes. O preço da atribuição para o recurso na **Tarefa A** é definido usando-se o valor de atributo **Função** de **Líder de Consultoria**. O preço da atribuição para o mesmo recurso na **Tarefa B** foi estimado usando o valor do atributo **Função** de **Técnico de Rede**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]