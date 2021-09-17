---
title: Conjuntos de aprovações
description: Este tópico explica como trabalhar com conjuntos de aprovações, solicitações e os subconjuntos dessas operações.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323222"
---
# <a name="approval-sets"></a>Conjuntos de aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

A aprovação define as solicitações de aprovação do grupo em subconjuntos menores de operações. Esse agrupamento permite que as aprovações sejam processadas por projeto, em uma ordem específica, e permite novas tentativas e sequenciamento. O agrupamento das solicitações de aprovação aumenta a confiabilidade e a capacidade de rastreamento do processamento de aprovações para grandes volumes de aprovações.

Os conjuntos de aprovação indicam o estado geral de processamento de seus registros relacionados. Quando um registro de aprovação é processado usando um conjunto de aprovações, o registro passa de **Enviado** para **Aprovado**, e não estará mais vinculado ao conjunto de aprovações. Se um registro falhar quando for enviado para aprovação, o registro permanecerá em um status de **Enviado** e o conjunto de aprovações é marcado como reprovado. O conjunto de aprovações registra a mensagem de erro da falha.

## <a name="processing-approvals-and-approval-sets"></a>Processando aprovações e conjuntos de aprovação
As aprovações que estão na fila para processamento são visíveis na exibição **Processando Aprovações**. O sistema processa todas as entradas várias vezes de forma assíncrona, incluindo uma nova tentativa de aprovação se as tentativas anteriores falharem.

O campo **Tempo de Vida do Conjunto de Aprovações** registra o número de tentativas restantes para processar o conjunto antes de ser marcado como falha.

## <a name="failed-approvals-and-approval-sets"></a>Aprovações e conjuntos de aprovações com falha
A exibição **Aprovações Reprovadas** lista todas as aprovações que exigem intervenção do usuário. Abra os logs do conjunto de aprovações associados para identificar a causa da falha.
Selecionar **Tentar novamente** adiciona à contagem de tempo de vida do conjunto de aprovação, move o conjunto de aprovação de volta para um status de **Em processamento** e tenta processar os registros restantes.

## <a name="configure-approval-sets"></a>Configurar conjuntos de aprovação

### <a name="enable-the-approval-sets-feature"></a>Habilite o recurso de conjuntos de Aprovação
Antes de ativar o recurso Conjuntos de aprovações, verifique se não há aprovações sendo processadas atualmente.

- Vá para a página **Parâmetros do projeto** e selecione **Controle de Recursos** > **Habilitar Aprovações Modernas**.

### <a name="turn-off-the-approval-sets-feature"></a>Desativar o recurso de conjuntos de Aprovação
Antes de desativar o recurso Conjuntos de aprovações, verifique se não há aprovações sendo processadas atualmente.

- Vá para a página **Parâmetros do Projeto** e selecione **Controle de Recursos** > **Desativar Aprovações Modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurando o limite assíncrono 
Quando os conjuntos de aprovação são criados, o processamento passa para o segundo plano quando o número selecionado de registros para aprovação excede o limite indicado. Use o campo **Limite Assíncrono** para configurar quando o processamento de aprovação deve ser executado de forma síncrona ou assíncrona. Selecione um dos seguintes valores:

  - Zero: todas as solicitações devem ser processadas de forma assíncrona. 
  - Números maiores que zero: as aprovações são processadas de forma assíncrona apenas quando o número de aprovações enviadas excede esse valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
