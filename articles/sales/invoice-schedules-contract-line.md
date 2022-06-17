---
title: Criar uma agenda de faturas em uma linha de contrato baseada em projeto
description: Este artigo fornece informações sobre como criar agendas e etapas de fatura em linhas de contrato.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 490a61b67f54bdad95ecfce905191c381dddc85b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914986"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Criar uma agenda de faturas em uma linha de contrato baseada em projeto 

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Você pode criar uma agenda de faturas para uma linha de contrato baseada em projeto. O faturamento só será permitido depois que o contrato for ganho e você estiver criando um contrato de projeto. Uma agenda de faturas permite que faturas de rascunho para uma linha de contrato baseada em projeto sejam criadas automaticamente. No entanto, se você só criar faturas manualmente, poderá ignorar a criação de agendas de faturas em linhas do contrato.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Criar uma agenda de fatura de hora e material para uma linha de contrato

Quando uma linha de contrato baseada em projeto tem um método de cobrança de hora e material, você pode criar uma agenda de faturas baseada em data. Para gerar automaticamente uma programação de fatura com base em data, conclua as etapas a seguir.

1. Vá para **Configurações** > **Frequências de fatura** e configure uma frequência de fatura.
2. Vá para o registro do contrato do projeto e na guia **Resumo**, no campo **Data de Entrega Solicitada**, selecione uma data.
3. Abra a linha de contrato **Hora e Material** para a qual você está criando a agenda de faturas baseada em data. 
4. Na guia **Agenda de Faturas**, selecione a data inicial de cobrança e a frequência de fatura.
5. Na subgrade, selecione **Gerar Agenda de Faturas**. A agenda de faturas é gerada com os campos **Data de Execução da Fatura**, **Data de Corte da Transação** e **Status de Execução** definidos da seguinte maneira:

    - **Data de Execução da Fatura**: esta data é ditada pela frequência da fatura.
    - **Data de Corte da Transação**: o dia anterior à data de execução da fatura.
    - **Status de Execução**: automaticamente definido como **Não Executado**. Quando o trabalho de criação de fatura automática for executado para determinada data de execução da fatura, este campo será atualizado para **Execução Bem-sucedida** ou **Falha na Execução**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Crie uma agenda de faturas de preço fixo para uma linha de contrato

Quando a linha de contrato tem um método de cobrança fixa, você pode criar uma agenda de faturas baseada em etapas. 

> [!NOTE]
> As etapas não poderão ser criadas em uma linha de contrato se não houver projeto mapeado para a linha de contrato.

Conclua as etapas a seguir para gerar uma agenda de faturas baseada em etapas para um conjunto fixo de etapas igualmente distribuídas para o período do calendário.

1. Vá para **Configurações** > **Frequências de fatura** e configure uma frequência de fatura.
2. Vá para o registro do contrato do projeto e na guia **Resumo**, no campo **Data de Entrega Solicitada**, selecione uma data.
3. Abra a linha de contrato **Preço Fixo** para a qual você está criando a agenda de etapas. Na guia **Etapas de Cobrança**, selecione a data inicial de cobrança e a frequência de fatura. 
4. Na subgrade, selecione **Gerar Etapas Periódicas**. A agenda de faturas é gerada com os campos **Nome da Etapa**, **Data da Etapa** e **Valor da Etapa** definidos da seguinte forma:

    - **Nome da Etapa**: esse nome é ditado pela frequência da fatura.
    - **Data da Etapa**: esta data é ditada pela frequência da fatura.
    - **Valor da Etapa**: este valor é calculado dividindo o valor do contrato na linha do contrato pelo número de etapas, conforme determinado pela frequência, início da cobrança e datas de entrega solicitadas.

    Se a linha do contrato tiver um valor no campo **Valor estimado do imposto**, esse campo também será distribuído para cada etapa igualmente ao gerar etapas periódicas.

As etapas de cobrança devem ser iguais ao valor contratado da linha do contrato. Caso contrário, você receberá um erro na página **Linha do Contrato**. Você pode corrigir o erro verificando se as etapas de cobrança totalizam o valor contratado da linha, criando, editando ou excluindo etapas. Depois que as alterações forem feitas, atualize a página para remover o erro.

### <a name="manually-create-milestones"></a>Criar etapas manualmente

Você pode gerar manualmente etapas de preço fixo quando elas não são divididas periodicamente. Conclua as etapas a seguir para criar manualmente uma etapa.

1. Abra a linha de contrato de preço fixo para a qual você está criando uma etapa. Na guia **Agenda de Faturas**, na subgrade, selecione **+ Criar nova etapa da linha de contrato**. 
2. Na página **Criação de Etapa**, insira as informações necessárias com base na tabela a seguir.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Nome da Etapa | Criação Rápida | Campo de texto para o nome da etapa. | Isso é transferido para a etapa de linha do contrato do projeto e a fatura. |
| Tarefa do Projeto | Criação Rápida | Se a etapa estiver vinculada à tarefa do projeto, use esta referência para adicionar lógica personalizada para definir o status da etapa com base no status da tarefa. | O aplicativo não tem impacto downstream dessa referência a uma tarefa. |
| Data da Etapa | Criação Rápida | Defina a data em que o processo de criação automática de nota fiscal deve procurar o status deste marco para considerá-lo para o faturamento. | Isso é transferido para a etapa de linha do contrato do projeto e a fatura. |
| Status da Fatura | Criação Rápida | Quando uma etapa é criada, este status é sempre definido como **Não Pronto para Faturamento** ou **Não Iniciado**. | Isso é transferido para a etapa de linha do contrato do projeto e a fatura. |
| Valor da Linha | Criação Rápida | Quantidade ou valor da etapa que será faturada ao cliente. | Isso é transferido para a etapa de linha do contrato do projeto e a fatura. |
| Imposto | Criação Rápida | O valor do imposto aplicado na etapa. | Isso é transferido para a etapa de linha do contrato do projeto e a fatura. |

3. Selecione **Salvar e Fechar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]