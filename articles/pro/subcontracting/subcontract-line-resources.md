---
title: Recursos de linha de subcontrato
description: Este tópico explica como especificar os recursos dedicados que são fornecidos pelo fornecedor para uma linha de subcontrato específica por tempo.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323357"
---
# <a name="subcontract-line-resources"></a>Recursos de linha de subcontrato

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

No Dynamics 365 Project Operations, um fornecedor pode especificar recursos que serão usados para fornecer a capacidade do recurso que está sendo adquirido na linha de subcontrato por tempo.

## <a name="create-subcontract-line-resources"></a>Criar recursos de linha de subcontrato

Para criar recursos de linha de subcontrato, conclua as etapas a seguir.

1. No painel de navegação, selecione **Subcontratos** e abra o subcontrato com o qual deseja trabalhar.
2. Abra a linha de subcontrato para o horário em que deseja especificar os recursos do fornecedor.
3. Na guia **Recursos de Linha de Subcontrato**, na subgrade, selecione **+ Novo Recurso de Linha de Subcontrato**.
4. Na página **Novo Marco da Linha de Subcontrato**, insira as informações necessárias e selecione **Salvar e Fechar**.

A tabela a seguir explica os campos do recurso de linha de subcontrato.

| Campo |  Descrição |
| ----- | ------------ |
| Recurso Reservável | Selecione um recurso reservável do tipo "Trabalhador contratado" que deseja usar como o recurso na linha de subcontrato. Se você ainda não criou um recurso reservável para o trabalhador contratado, deixe esse campo vazio. Um recurso reservável é criado quando você salva o registro.  |
| Contact | Se o campo **Recurso Reservável** está vazio, você pode criar seu recurso de linha de subcontrato de um contato existente. Use a pesquisa para exibir a lista de contatos ativos no sistema. Selecione um contato para o fornecedor deste subcontrato. O contato selecionado é validado quando você salva o registro. Se o contato que você selecionou não for um contato válido, seu registro não será salvo. Se não houver recurso reservável para o contato selecionado, o sistema criará um recurso reservável para o contato selecionado antes de criar o recurso de linha de subcontrato. |
| Usuário | Se o campo **Recurso Reservável** estiver vazio, você poderá criar um recurso de linha de subcontrato ao selecionar um usuário ativo. Use a pesquisa para exibir a lista de usuários ativos no sistema. Se não houver recurso reservável para o usuário selecionado, o sistema criará um recurso reservável para o usuário selecionado antes da criação do recurso de linha de subcontrato. |
| Data de Início | A data de início da atribuição do trabalhador subcontratado. Se este recurso for reservado para um período anterior a esse intervalo de datas, ocorrerá um aviso. |
| Data de Término | A data de conclusão da atribuição do trabalhador subcontratado. Se este recurso for reservado para um período posterior a esse intervalo de datas, ocorrerá um aviso. |
| Esforço | O número total de horas de esforço que o trabalhador subcontratado gastará nesta linha de subcontrato. Se este recurso for reservado além do esforço ao qual estão alocados neste subcontrato, ocorrerá um aviso. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
