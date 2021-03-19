---
title: Criar agendas de faturas em uma linha de contrato baseada em projeto - lite
description: Este tópico fornece informações sobre como criar agendas de faturas e etapas.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4706a2a711efa7d176030deaa33b65bca28d8498
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273364"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Criar agendas de faturas em uma linha de contrato baseada em projeto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Você pode anexar uma agenda de faturas em uma linha de contrato baseada em projeto. O faturamento só é permitido depois que o contrato é ganho para criar um contrato de projeto. As agendas de faturas permitem que faturas de rascunho para uma linha de contrato baseada em projeto sejam criadas automaticamente. Se você pretende sempre criar faturas manualmente, pode ignorar a criação de agendas de faturas em uma linha de contrato com base em projeto ou em uma linha de contrato.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Criar uma hora e uma agenda de faturas de material para uma linha de contrato baseada em projeto

Quando uma linha de contrato baseada em projeto tem um método de cobrança de hora e material, você pode criar uma agenda de faturas baseada em data. Para gerar automaticamente uma programação de fatura com base em data, conclua as etapas a seguir.

1. Acesse **Configurações** > **Frequências de Fatura** para configurar a frequência da fatura.
2. Abra o contrato do projeto e, na guia **Resumo**, defina a data de entrega solicitada.
3. Abra a linha de contrato de horas e materiais para a qual você deseja criar uma agenda de faturas com base em data. 
4. Na guia **Agenda de Faturas**, selecione uma data de início da cobrança e a frequência da fatura. 
5. Na subgrade, selecione **Gerar Agenda de Faturas**.

    O sistema gera a agenda de faturas com as seguintes informações de campo:

    - **Data de Execução da Fatura** é definida com a data com base na frequência da fatura.
    - **Data Limite da Transação** é definida para o dia anterior à **Data de Execução da Fatura**.
    - **Status de execução** é automaticamente definido para **Não executar**. Quando o trabalho de criação de fatura automática for executado para determinada **Data de Execução da Fatura**, este campo será atualizado para **Execução Bem-sucedida** ou **Falha na Execução**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Criar uma agenda de faturas de preço fixo para uma linha de contrato baseada em projeto

Quando uma linha de contrato baseada em projeto tem um método de cobrança de preço fixo, você pode criar uma agenda de faturas com base em etapas. Conclua as etapas a seguir para gerar automaticamente uma agenda de faturas com base em etapas para um conjunto fixo de etapas que são distribuídas igualmente para o período do calendário.

1. Acesse **Configurações** > **Frequências de Fatura** para configurar a frequência da fatura.
2. Abra o contrato do projeto e, na guia **Resumo**, defina a data de entrega solicitada.
3. Abra a linha de contrato de preço fixo na qual você precisa criar uma agenda de etapas. 
4. Na guia **Agenda de Faturas (Etapas de Cobrança)**, selecione a data de início da cobrança e a frequência da fatura. 
5. Na subgrade, selecione **Gerar Etapas Periódicas**.

    O sistema gera a agenda de faturas com as informações de etapas a seguir.

    - **Nome da Etapa** é definido com a data ditada com base na frequência da fatura.
    - **Data da Etapa** é definida com a data ditada com base na frequência da fatura.
    - **Valor da Etapa** é calculado dividindo o valor do contrato na linha do contrato baseada no projeto pelo número de etapas, conforme determinado por frequência, início da cobrança e datas de entrega solicitadas.
    - Se a linha do contrato tiver um valor no campo **Valor Estimado do Imposto**, este campo também será rateado para cada etapa igualmente ao gerar etapas periódicas.

As etapas de cobrança devem ser iguais ao valor contratado da linha de contrato baseada em projeto. Se elas não forem iguais, ocorrerá um erro. Você pode corrigir esse erro verificando se as etapas de cobrança totalizam o valor contratado da linha, criando, editando ou excluindo etapas. Após a conclusão das alterações, atualize a página.

### <a name="manually-create-milestones"></a>Criar etapas manualmente

Etapas de preço fixo podem ser geradas manualmente quando não são divididas periodicamente. Para criar uma etapa manualmente, conclua as etapas a seguir.

1. Abra a linha de contrato de preço fixo na qual você deseja criar uma etapa. 
2. Na guia **Agenda de Faturas**, na subgrade, selecione **+ Criar nova etapa de linha de contrato**.
3. No formulário **Criação de Etapa**, insira as informações necessárias com base na tabela a seguir. 

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Nome da Etapa | Criação Rápida | Campo de texto para o nome da etapa. | Este campo está incluído na etapa da linha do contrato do projeto e na fatura. |
| Tarefa do Projeto | Criação Rápida | Se a etapa estiver associada a uma tarefa do projeto, use esta referência para adicionar lógica personalizada e definir o status da etapa com base no status da tarefa. | Não há impacto derivado dessa referência em uma tarefa. |
| Data da Etapa | Criação Rápida | A data em que o processo de criação automática de fatura deve buscar o status desta etapa para considerá-la para o faturamento. | Isso é incluído na etapa da linha do contrato do projeto e na fatura. |
| Status da Fatura | Criação Rápida | Quando a etapa é criada, este status é sempre definido como **Não está pronto para faturamento** ou **Não iniciado**. | Isso é incluído na etapa da linha do contrato do projeto e na fatura. |
| Valor da Linha | Criação Rápida | A quantidade ou valor da etapa que será faturada para o cliente. | Este campo é incluído na etapa da linha do contrato do projeto e na fatura. |
| Imposto | Criação Rápida | O valor do imposto aplicado na etapa. | Isso é incluído na etapa da linha do contrato do projeto e na fatura. |

4. Selecione **Salvar e Fechar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]