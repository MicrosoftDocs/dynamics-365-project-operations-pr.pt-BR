---
title: Considerações de atualização para Aprovações Modernas
description: O tópico abrange os pontos que os administradores devem considerar ao habilitar a funcionalidade de Aprovações Modernas.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578372"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Considerações de atualização para Aprovações Modernas 

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Como parte do ciclo de lançamentos 1 de abril de 2022, a funcionalidade Aprovações Modernas será habilitada por padrão. Essa funcionalidade melhora a confiabilidade da lógica de aprovação e garante que você possa determinar o motivo, caso a lógica de aprovação falhe.

Como parte dessa alteração, as mudanças de status de aprovações de projetos são atualizadas. O status agora passa diretamente de **Enviado** para **Aprovado**. **Pendente** não é mais um status de aprovações. Para determinar se uma aprovação está pendente, verifique se a aprovação faz parte de um conjunto de aprovações e revise o estado do conjunto de aprovações em anexo.

## <a name="before-you-upgrade"></a>Antes de atualizar

Antes de atualizar para Aprovações Modernas, verifique se não há aprovações pendentes. Aprovações Modernas não usa o status **Pendente**. Portanto, as aprovações ainda marcadas como **Pendente** após a atualização não serão processadas.

## <a name="after-you-upgrade"></a>Após a atualização

Depois de atualizar para Aprovações Modernas, um administrador deve validar se o fluxo da nuvem que processa aprovações foi habilitado.

1. Entre em [flow.microsoft.com](https://flow.microsoft.com)
2. No canto superior direito da página, alterne seu ambiente para o ambiente que você atualizou.
3. Selecione **Soluções** para listar as soluções instaladas no ambiente.
4. Na lista de soluções, selecione **Project Operations** ou **Project Service**.
5. Altere o filtro de **Todos** para **Fluxos da Nuvem**.
6. Verifique se a opção **Project Service – Agendar Recorrentemente Conjuntos de Aprovações do Projeto** está definida como **Ativado**. Caso contrário, selecione o fluxo e **Ativar**.
7. A cada cinco minutos, verifique se o processamento está ocorrendo, revisando a lista **Trabalhos do Sistema** na área **Configurações**.

## <a name="short-term-rollback"></a>Reversão de curto prazo

Se você não conseguir absorver as alterações ou se encontrar um problema grave com esse recurso, poderá reverter temporariamente para o fluxo de aprovação original executando as seguintes etapas:
1. Entre no seu ambiente e confirme se não há aprovações pendentes.
2. Vá para **Configurações** > **Parâmetros do Projeto**.
3. Selecione **Controle de Recursos** e **Aprovações Modernas** para desativar o recurso.

## <a name="removing-the-feature-flag"></a>Remoção do sinalizador de recurso

Na atualização do ciclo 2 de outubro de 2022, a capacidade de desativar esse recurso será removida.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
