---
title: Agendamentos de fatura em linhas de cotação baseada em projeto
description: Este tópico fornece informações sobre a criação de programações de faturas e marcos para linhas de cotação.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 506de5217de48814d6b8f03a10c7c8648c575198
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278269"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Agendamentos de fatura em linhas de cotação baseada em projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Uma linha de cotação baseada em projeto oferece a capacidade de expressar uma programação de fatura. Isso é opcional durante a fase de cotação porque o aplicativo não suporta o faturamento de um projeto quando ele está vinculado a uma linha de cotação. O faturamento só é permitido após a cotação ser ganha. O único impacto posterior da criação de uma programação de fatura durante a fase de cotação é que essa programação de fatura é copiada para a linha do contrato com base no projeto. Se você não criar uma programação de fatura durante a fase de cotação, poderá fazê-lo na linha do contrato baseado em projeto.

No geral, o objetivo das programações de faturas é permitir a criação automática de faturas preliminares para uma linha de contrato baseada em projeto. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Crie uma programação de fatura de tempo e material para uma linha de cotação baseada em projeto

Quando o método de faturamento para uma linha de cotação baseada em projeto é Tempo e material, o sistema gera uma programação de fatura baseada em data. Para gerar automaticamente uma programação de fatura com base em data, conclua as etapas a seguir.

1. Vamos para **Configurações** > **Frequências de fatura** e configure uma frequência de fatura.
2. Na página **Citações**, abra a cotação do projeto e na guia **Resumo**, defina uma data de entrega solicitada.
3. Abra a linha de cotação de tempo e material para a qual você precisa criar uma programação de faturamento com base em data. 
4. Na guia **Agendamento de fatura**, selecione valores nos campos **Início de faturamento** e **Frequência de fatura**. 
5. Na subgrade, selecione **Gerar Agenda de Faturas**.
6. O aplicativo gera o agendamento de faturamento com os campo **Data de execução da fatura**, **Data de corte da transação**, e **Status de execução** definidos da seguinte maneira:

    - **Data de execução da fatura** é definido com a data ditada com base na frequência da fatura.
    - **Data limite da transação** é definido para o dia anterior à **Data de execução da fatura**.
    - **Status de execução** é automaticamente definido para **Não executar**. Quando o trabalho de criação automática de fatura for executado para uma determinada data de execução da fatura, ele atualizará este campo para **Execução com sucesso** ou **Falha na execução**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Crie uma programação de fatura de preço fixo para uma linha de cotação baseada em projeto

Quando a linha de cotação baseada em projeto tem um método de faturamento **Fixo**, o sistema cria uma programação de faturamento baseada em marcos. Conclua as etapas a seguir para gerar automaticamente essa programação para um conjunto fixo de marcos que são igualmente distribuídos para o período do calendário.

1. Vamos para **Configurações** > **Frequências de fatura** e configure uma frequência de fatura.
2. Na página **Citações**, abra a cotação do projeto e na guia **Resumo**, defina uma data de entrega solicitada.
3. Abra a linha de cotação de preço fixo para a qual você precisa criar um cronograma de marcos. 
4. Na guia **Agendamento de fatura**, selecione valores nos campos **Início de faturamento** e **Frequência de fatura**. 
5. Na subgrade, selecione **Gerar Etapas Periódicas**.
6. O aplicativo gera a programação de faturamento com um nome de marco, data e valor.

    - O nome da etapa é definido com a data ditada com base na frequência da fatura.
    - O nome da data é definido com a data ditada com base na frequência da fatura.
    - O valor do marco é calculado dividindo o valor da cotação na linha de cotação baseada no projeto pelo número de marcos, conforme determinado pela frequência e início do faturamento e datas de entrega solicitadas.
    - Se a linha de Cotação também tiver um valor de imposto estimado, esse valor será dividido entre cada marco igualmente ao gerar marcos periódicos.

### <a name="manually-create-milestones"></a>Criar etapas manualmente

Os marcos de preço fixo também podem ser gerados manualmente quando não são divididos periodicamente. Para criar uma etapa manualmente:

Abra a linha de cotação de preço fixo para a qual você precisa criar um marco. Na guia **Programação de Faturas**, na subgrade, selecione **+ Criar novo marco de linha de cotação** e insira as informações necessárias com base na tabela a seguir.

| **Campo** | **Local** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Nome da etapa | Criação rápida | O nome da etapa. | Isso é propagado para o marco da linha do contrato do projeto e para a fatura |
| Tarefa do Projeto | Criação rápida | Se o marco estiver vinculado à tarefa do projeto, você pode usar esta referência para adicionar lógica customizada e definir o status do marco com base no status da tarefa. | O aplicativo não tem nenhum impacto downstream dessa referência a uma tarefa. |
| Data da etapa | Criação rápida | Defina a data em que o processo de criação automática de nota fiscal deve procurar o status deste marco para considerá-lo para o faturamento. | Isso é propagado para o marco da linha do contrato do projeto e para a fatura. |
| Status da fatura | Criação rápida | Quando um marco é criado, este status é sempre definido como **Não está pronto para faturamento**. | Isso é propagado para o marco da linha do contrato do projeto e para a fatura. |
| Valor da Linha | Criação rápida | Quantidade ou valor da etapa que será faturada ao cliente. | Isso é propagado para o marco da linha do contrato do projeto e para a fatura. |
| Imposto | Criação rápida | Valor do imposto que será aplicado ao marco. | Isso é propagado para o marco da linha do contrato do projeto e para a fatura. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]