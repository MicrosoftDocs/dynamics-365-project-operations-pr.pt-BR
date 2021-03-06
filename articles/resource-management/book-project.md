---
title: Reservar para um projeto
description: Este tópico fornece informações sobre como reservar um recurso em um projeto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907865"
---
# <a name="book-to-a-project"></a>Reservar para um projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Há momentos em que um Gerente de projeto ou Gerente de recursos precisará alocar um recurso a um projeto sem um requisito específico definido por um membro genérico da equipe. Isso pode ser realizado de três formas.

- Reservar da grade de membros da equipe
- Reservar no painel de agendamento
- Reservar no formulário **Projeto**

## <a name="book-from-the-team-member-grid"></a>Reservar da grade de membros da equipe

Se a sua organização estiver operando no modo de Alocação de recursos híbrido, o Gerente de projeto pode reservar um recurso diretamente para o projeto ao concluir as seguintes etapas.

1. No projeto, vá para a grade de membros da equipe e selecione **Novo**.
2. Defina o nome da posição e a função do recurso.
3. Selecione o recurso reservável da pesquisa disponível.
4. Depois de selecionar o recurso, defina as seguintes informações de campo para reservar o recurso:

    - Data de Início
    - Data de término
    - Método de alocação
    - Horas, se aplicável
    - Aprovador do projeto

6. Selecione **Salvar e Fechar**

## <a name="book-from-the-schedule-board"></a>Reservar no painel de agendamento

Quando um Gerente de recursos precisa reservar um recurso diretamente para um projeto, é possível usar o quadro de agendamento e os requisitos do projeto. Os requisitos do projeto é um requisito de recurso que está sempre disponível para reserva. Para reservar diretamente em um projeto do quadro de agendamento, execute as seguintes etapas.

1. Navegue até o quadro de agendamento e na página à esquerda, filtre os recursos que está considerando para o requisito.
2. No painel inferior, selecione a guia **Projeto** para exibir uma lista de requisitos do projeto.
3. Arraste o requisito até um recurso e defina as seguintes informações:

    - Data de Início
    - Data de término
    - Status da reserva
    - Método de reserva
    - Duração

## <a name="book-from-the-project-form"></a>Reservar no formulário Projeto

Como Gerente de projeto, talvez seja necessário reservar um recurso para um projeto, mas conhecer apenas os critérios em vez do nome do recurso. Execute as seguintes etapas para usar o assistente de agendamento para encontrar um recurso baseado em quaisquer atributos disponíveis do recurso. 

1. Navegue até o projeto e selecione **Reservar** para abrir o Assistente de Agendamento.
2. Usando os filtros do lado esquerdo do Assistente de Agendamento, restrinja os critérios e selecione **Pesquisar**.
3. Com base nos recursos retornados nos resultados, é possível reservar um recurso.

> [!NOTE]
> Esse método não cria reservas para o recurso. Em vez disso, adiciona o recurso à equipe. Depois que o membro da equipe tiver sido adicionado ao projeto, o gerente do projeto poderá manter reservas ou estender reservas para adicionar as reservas necessárias ao recurso.
