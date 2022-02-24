---
title: Cancelar entradas de tempo e despesa aprovadas anteriormente
description: Este tópico fornece informações sobre como cancelar uma transação aprovada de tempo e despesa do projeto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
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
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150564"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Cancelar entradas de tempo ou despesa aprovadas anteriormente

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Na versão mais recente do Dynamics 365 Project Service Automation, os aprovadores podem cancelar entradas de tempo ou despesa que eles aprovaram anteriormente.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Cancelar uma entrada de tempo ou despesa aprovadas anteriormente

Siga estas etapas para cancelar uma entrada de tempo ou despesa que foi aprovada anteriormente.

1. Vá para **Projetos** \> **Meu Trabalho** \> **Aprovações**.
2. Na página de lista **Aprovações**, altere a exibição para **Minhas aprovações anteriores**. Uma lista das entradas de tempo e despesa que você aprovou anteriormente é mostrada.
3. Selecione uma ou mais entradas e selecione **Cancelar aprovação**. Você recebe uma mensagem de aviso.
4. Selecione **OK** para cancelar a aprovação.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Compreenda o impacto de cancelar uma aprovação de entrada de tempo ou despesa

Quando uma aprovação é cancelada, há impactos operacionais e financeiros.

### <a name="operational-impact"></a>Impacto operacional

No lado das operações, quando uma aprovação é cancelada, o status do registro é redefinido para **Rascunho** e a aprovação não aparece mais na exibição **Minhas aprovações anteriores**. Em vez disso, a aprovação cancelada aparece na exibição **Entradas de tempo para aprovação** ou **Entradas de despesa para aprovação** se era uma entrada de tempo ou uma entrada de despesa, respectivamente. Além disso, o status da entrada de tempo ou despesa relacionada é alterado para **Enviado**, de modo que a entrada relacionada é consistente com as aprovações que tem um status de **Rascunho**.

Como aprovador, você pode editar alguns dos campos de uma provação que tem um status de **Rascunho**. Esses campos incluem **Tipo de Cobrança** e **Horas Faturáveis para Entradas de Tempo**. Depois de fazer as alterações, é possível aprovar o registro novamente. Se desejar, você pode rejeitar a entrada. Se você rejeitar a aprovação de uma entrada de tempo, o status da entrada será alterado para **Devolvida**. Se você rejeitar a aprovação de uma entrada de despesa, o status será alterado para **Rejeitada**. De modo prático, as entradas devolvidas e rejeitadas se comportam igualmente a uma entrada com o status de **Rascunho**. Um membro da equipe do projeto pode fazer qualquer mudança necessária na entrada e reenviá-la para aprovação, ou excluir completamente a entrada.

### <a name="financial-impact"></a>Impacto financeiro

Um projeto também é afetado financeiramente quando uma aprovação é cancelada. Primeiramente, os dados reais correspondentes de custo e vendas são atualizados da seguinte maneira:

- O status de ajuste é definido como **Ajustado**.
- O status da cobrança é definido como **Cancelado**.

Em seguida, as entradas reversas são criadas na tabela Dados reais. Para criar entradas de reversão, o sistema dados reais originais nos valores de campo. Os únicos valores que não são copiados são os valores de quantidade. Esses valores são revertidos. Os dados reais revertidos são criados para dados reais de **Custo** e **Vendas Não Cobradas**. O campo **Status do Ajuste** nos dados reais revertidos é definido como **Não Ajustável** e o status de cobrança é definido como **Cancelado**.

Depois que as alterações forem feitas, o valor que é registrado como gasto no projeto e na lista de pendências de receita no projeto não será mais contado para os valores representados por esses dados reais.
