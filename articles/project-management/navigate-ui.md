---
title: Navegando pela interface do usuário
description: Este tópico fornece informações sobre o gerenciamento de projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961815"
---
# <a name="navigating-the-user-interface"></a>Navegando pela interface do usuário

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

## <a name="overview"></a>Visão Geral

O formulário principal do projeto é separado em várias guias. Cada guia representa um nível diferente de detalhe dentro do projeto.

- **Resumo** : fornece uma descrição do projeto e agrega o desempenho planejado e real do projeto.

    ![Guia Resumo e seus campos](media/navigation7.png)

- **Tarefas** : fornece os detalhes sobre a estrutura de detalhamento de trabalho representada por uma visualização em grade, visualização em painel e um gantt.

    ![Guia Tarefa e seus campos](media/navigation8.png)

- **Equipe**: fornece detalhes sobre os participantes do projeto. O esforço atribuído a cada membro da equipe também é resumido nesta visualização.

    ![Guia Equipe e seus campos](media/navigation9.png)

- **Atribuições de recursos**: fornece uma visão baseada em tempo do esforço para cada recurso em um projeto.

    ![Guia Atribuições de recursos e seus campos](media/navigation10.png)

- **Reconciliação de recursos** : fornece uma visão baseada no tempo das diferenças entre as atribuições de cada recurso nomeado e suas reservas.

    ![Guia Reconciliação de recursos e seus campos](media/navigation11.png)

- **Estimativas** : fornece uma visão baseada no tempo das estimativas de custo e vendas de um projeto.

    ![Guia Estimativas e seus campos](media/navigation12.png)

- **Rastreamento** : fornece uma visualização que mostra o progresso das tarefas na estrutura analítica do trabalho em relação a esforço, custo e vendas.

    ![Guia Rastreamento e seus campos](media/navigation13.png)

- **Vendas** : fornece links diretos para cotações e contratos associados ao projeto.

- **Estimativas de despesas**: fornece uma grade que define as despesas do projeto com base nas categorias de despesas organizacionais.

    ![Guia Estimativas de despesas e seus campos](media/navigation14.png)

## <a name="grid-controls"></a>Controles de grade

A seguir, veja uma visão geral dos controles comuns encontrados nas várias guias de planejamento do projeto.

### <a name="refresh"></a>Atualizar

**Atualizar**: recupera os dados mais recentes do servidor se ocorrer alguma alteração após o carregamento da grade.

![Botão Atualizar](media/navigation7.png)

### <a name="group-by"></a>Agrupar por

**Agrupar por**: atualiza o agrupamento das linhas na grade para indicar recursos, funções ou categorias com base nas necessidades do usuário.

![Botão Agrupar por](media/navigation6.png)

### <a name="previousnext"></a>Anterior/Próximo

**Anterior**/**Próximo**: atualiza os períodos de tempo visíveis nas grades baseadas no tempo.

![Botões Anterior e Próximo](media/navigation2.png)

### <a name="timescale"></a>Escala de tempo

**Escala de tempo**: altere a agregação dos dados baseados no tempo entre dias, semanas, meses e anos.

![Botão Escala de tempo](media/navigation3.png)

### <a name="expand"></a>Expandir

**Expandir**: renderiza a grade visível em tela inteira, facilitando a visualização de funções adicionais.

![Botão Expandir](media/navigation4.png)

### <a name="time-phase-by"></a>Tempo baseado em

**Tempo baseado em**: atualize o agrupamento das linhas na grade para refletir as estimativas de custo para estimativas de vendas. Esse controle também aplica-se ao script de estimativa e à grade de rastreamento.

![Botão Tempo baseado em](media/navigation0.png)

### <a name="add-column"></a>Adicionar coluna

**Adicionar coluna**: permite ao usuário definir as colunas visíveis na grade. Somente colunas de funcionalidade predefinida podem ser adicionadas às grades no formulário **Planejamento de projeto**.

![Botão Adicionar coluna](media/navigation5.png)
