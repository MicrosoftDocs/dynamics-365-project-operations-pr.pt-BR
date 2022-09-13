---
title: Ativar e revisar uma cotação de projeto
description: Este artigo fornece informações sobre como ativar e revisar cotações no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410310"
---
# <a name="activate-and-revise-a-project-quote"></a>Ativar e revisar uma cotação de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os recursos de ativação e revisão ajudam você a acompanhar o controle de versão para cotações baseadas em projeto durante as fases de estimativa e negociação. Quando um rascunho de uma cotação é ativado, ele se torna somente leitura.

Os recursos de ativação e revisão permitem que você execute as seguintes tarefas:

- Ganhe ou perca cotações somente após a ativação.
- Revise uma cotação para fazer alterações na cotação existente ou criar uma nova versão.

> [!NOTE]
> Depois que o recurso de ativação e revisão de cotações estiver habilitado, ele não poderá ser desabilitado.

Para ativar a capacidade de ativar e revisar cotações baseadas em projeto, siga estas etapas:

1. Vá para **Configurações** \> **Parâmetros**.
1. Abra o registro **Parâmetros**.
1. No Painel de Ação, na guia **Controle de Recursos**, selecione **Habilitar ativação e revisão de cotações**.
1. Na caixa de diálogo de confirmação, selecione **OK**.
1. Após alguns momentos, atualize o navegador. Os recursos de ativação e revisão agora devem estar disponíveis. Você saberá que esses recursos foram habilitados se o botão **Habilitar ativação e revisão de cotações** não aparecer mais no Painel de Ação.

## <a name="activating-a-quote"></a>Ativar uma cotação

Após habilitar o recurso de ativação e revisão de cotações, os botões **Fechar cotação como ganha** e **Fechar cotação como perdida** no Painel de Ação não ficam disponíveis para cotações de projeto de rascunho. Eles ficam disponíveis somente após a ativação de uma cotação.

A ativação representa o estágio no processo de cotação em que você deseja evitar mais alterações na cotação. Neste estágio, a cotação é enviada para revisão interna ou para o cliente.

Os botões **Fechar cotação como ganha** e **Fechar cotação como perdida** no Painel de Ação ficam disponíveis para cotações ativadas. Dependendo do resultado da revisão interna ou do cliente, você pode usar um desses botões para fechar uma cotação ativada. Você pode fazer negociações e alterações em cotações ativadas selecionando **Revisar cotação**.

## <a name="revising-a-quote"></a>Revisar uma cotação

Se você precisar fazer alterações em uma cotação ativada, selecione **Revisar cotação**. A cotação é fechada, e o código de motivo **revisado** é usado. Uma cotação será criada com a mesma ID e um número de revisão incrementado. Todos os detalhes da cotação original são copiados para a nova cotação. A nova cotação está com status de rascunho e pode ser editada conforme necessário.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
