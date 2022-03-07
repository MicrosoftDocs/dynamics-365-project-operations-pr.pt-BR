---
title: Entrada de despesa (lite)
description: Este tópico fornece informações sobre como trabalhar com entrada de despesa em uma implantação lite.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 48bf86a5cee475708f93462dc154e21b36240023f0a94cf31c49e9a096951736
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007807"
---
# <a name="expense-entry-lite"></a>Entrada de despesa (lite)

_**Aplica-se a:** Implantação lite - gerenciar faturamento pro forma_

Básico ou lite, o gerenciamento de despesas é o recurso usado para registrar despesas simples. Você pode registrar despesas em um projeto e, em seguida, o aprovador do projeto revisará e aprovará essas despesas.

Para obter mais informações sobre recursos de despesas no Dynamics 365 Project Operations, consulte [Visão geral de despesas](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Capturar uma despesa básica

Você pode capturar as despesas para que você possa enviá-las para o aprovador.

1. Vá para **Despesas** e selecione **Novo**.
2. Na página **Nova Despesa**, insira as informações de despesas obrigatórias e selecione **Salvar**.

## <a name="submit-a-basic-expense"></a>Enviar uma despesa básica

Quando tiver capturado todas as suas despesas e estiver pronto para aprová-las, você deve enviá-las.

1. Vá para **Despesas** e selecione uma despesa. Ou, selecione todas as despesas usando a caixa de seleção no cabeçalho.
2. Selecione **Enviar**. O sistema processa as entradas selecionadas e depois cria solicitações de aprovação de despesas.

## <a name="add-an-attachment"></a>Adicionar um anexo

Você pode ter que fornecer documentação adicional sobre sua despesa ao aprovador. Você pode anexar um recibo na linha do tempo da entrada de despesa. Selecione **Editar** e na **Linha do tempo**, selecione o ícone de clipe de papel para anexar o recibo.

## <a name="recall-a-basic-expense"></a>Recuperar uma despesa básica

Ao enviar uma despesa por engano, é possível recuperá-la. O tempo necessário para recuperar uma entrada de despesa depende do estágio de aprovação.  Se o aprovador ainda não tiver aprovado a entrada, a recuperação poderá ser executada imediatamente. No entanto, se a entrada já tiver sido aprovada, o aprovador receberá uma solicitação para aprovar a recuperação e reverter as transações.

1. Vá para **Despesas** e, na lista de despesas, selecione a despesa que deseja recuperar.
2. Selecione **Recuperar**. Se a entrada de despesa não tiver sido aprovada, o sistema a recuperará imediatamente. Se a entrada de despesa já tiver sido aprovada, uma solicitação de recuperação será criada para notificar o aprovador que você deseja reverter a despesa. O aprovador confirmará se a reversão poderá ser feita e a entrada será retornada.

## <a name="delete-a-basic-expense"></a>Excluir uma despesa básica

As despesas que ainda não foram enviadas podem ser excluídas. Para excluir uma despesa que já foi enviada, é necessário antes recuperá-la.

## <a name="see-also"></a>Consulte também

- [Visão geral de aprovações](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]