---
title: Conjuntos de aprovações
description: Este artigo explica como trabalhar com conjuntos de aprovações, solicitações e subconjuntos dessas operações.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524902"
---
# <a name="approval-sets"></a>Conjuntos de aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

A aprovação define as solicitações de aprovação do grupo em subconjuntos menores de operações. Esse agrupamento permite que as aprovações sejam processadas por projeto, em uma ordem específica, e permite novas tentativas e sequenciamento. O agrupamento das solicitações de aprovação aumenta a confiabilidade e a capacidade de rastreamento do processamento de aprovações para grandes volumes de aprovações.

Os conjuntos de aprovação indicam o estado geral de processamento de seus registros relacionados. Quando um registro de aprovação é processado usando um conjunto de aprovações, o registro passa de **Enviado** para **Aprovado**, e não estará mais vinculado ao conjunto de aprovações. Se um registro falhar quando for enviado para aprovação, o registro permanecerá em um status de **Enviado** e o conjunto de aprovações é marcado como reprovado. O conjunto de aprovações registra a mensagem de erro da falha.

## <a name="processing-approvals-and-approval-sets"></a>Processando aprovações e conjuntos de aprovação
As aprovações que estão na fila para processamento são visíveis na exibição **Processando Aprovações**. O sistema processa todas as entradas várias vezes de forma assíncrona, incluindo uma nova tentativa de aprovação se as tentativas anteriores falharem.

O campo **Tempo de Vida do Conjunto de Aprovações** registra o número de tentativas restantes para processar o conjunto antes de ser marcado como falha.

Os conjuntos de aprovações são processados por meio da ativação periódica com base em um **Fluxo da Nuvem** chamado **Project Service – Agendar Recorrentemente Conjuntos de Aprovações do Projeto**. Ele é encontrado na **Solução** chamada **Project Operations**. 

Verifique se o fluxo está ativado realizando as etapas a seguir.

1. Como administrador, entre em [flow.microsoft.com](https://powerautomate.microsoft.com).
2. No canto superior direito, alterne para o ambiente que você usa para o Dynamics 365 Project Operations.
3. Selecione **Soluções** para listar as soluções instaladas no ambiente.
4. Na lista de soluções, selecione **Project Operations**.
5. Altere o filtro de **Todos** para **Fluxos da Nuvem**.
6. Verifique se o fluxo **Project Service – Agendar Recorrentemente Conjuntos de Aprovações do Projeto** está definido como **Ativado**. Caso contrário, selecione o fluxo e **Ativar**.
7. Verifique se o processamento ocorre a cada cinco minutos revisando a lista **Trabalhos do Sistema** na área **Configurações** do ambiente do Dataverse do Project Operations.

## <a name="failed-approvals-and-approval-sets"></a>Aprovações e conjuntos de aprovações com falha
A exibição **Aprovações Reprovadas** lista todas as aprovações que exigem intervenção do usuário. Abra os logs do conjunto de aprovações associados para identificar a causa da falha.
Selecionar **Tentar novamente** adiciona à contagem de tempo de vida do conjunto de aprovação, move o conjunto de aprovação de volta para um status de **Em processamento** e tenta processar os registros restantes.

## <a name="configure-approval-sets"></a>Configurar conjuntos de aprovação

### <a name="enable-the-approval-sets-feature"></a>Habilite o recurso de conjuntos de Aprovação
Antes de ativar o recurso Conjuntos de aprovações, verifique se não há aprovações sendo processadas atualmente. Depois que esse recurso é habilitado, a ação não pode ser desfeita.

- Vá para a página **Parâmetros do projeto** e selecione **Controle de Recursos** > **Habilitar Aprovações Modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurando o limite assíncrono 
Quando os conjuntos de aprovação são criados, o processamento passa para o segundo plano quando o número selecionado de registros para aprovação excede o limite indicado. Use o campo **Limite Assíncrono** para configurar quando o processamento de aprovação deve ser executado de forma síncrona ou assíncrona. Selecione um dos seguintes valores:

  - Zero: todas as solicitações devem ser processadas de forma assíncrona. 
  - Números maiores que zero: as aprovações são processadas de forma assíncrona apenas quando o número de aprovações enviadas excede esse valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
