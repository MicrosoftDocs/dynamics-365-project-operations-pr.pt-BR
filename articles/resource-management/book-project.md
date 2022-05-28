---
title: Reservar para um projeto
description: Este tópico fornece informações sobre como reservar um recurso em um projeto.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b47ae8cb38be6d29804aec8b069e6a8aec0ffb70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591345"
---
# <a name="book-to-a-project"></a>Reservar para um projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

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
    - Duration
   
   > [!NOTE]
   > No momento, o Dynamics 365 Project Operations não dá suporte ao painel de agendamento.   

## <a name="book-from-the-project-form"></a>Reservar no formulário Projeto

Como Gerente de projeto, talvez seja necessário reservar um recurso para um projeto, mas conhecer apenas os critérios em vez do nome do recurso. Execute as seguintes etapas para usar o assistente de agendamento para encontrar um recurso baseado em quaisquer atributos disponíveis do recurso. 

1. Navegue até o projeto e selecione **Reservar** para abrir o Assistente de Agendamento.
2. Usando os filtros do lado esquerdo do Assistente de Agendamento, restrinja os critérios e selecione **Pesquisar**.
3. Com base nos recursos retornados nos resultados, é possível reservar um recurso.

> [!NOTE]
> Esse método não cria reservas para o recurso. Em vez disso, adiciona o recurso à equipe. Depois que o membro da equipe tiver sido adicionado ao projeto, o gerente do projeto poderá manter reservas ou estender reservas para adicionar as reservas necessárias ao recurso.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
