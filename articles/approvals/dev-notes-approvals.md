---
title: Notas do desenvolvedor para Aprovações
description: Este tópico fornece informações adicionais do desenvolvedor sobre como trabalhar com aprovações.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483934"
---
# <a name="developer-notes-for-approvals"></a>Notas do desenvolvedor para Aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations inclui lógica de validação que garante a transição correta do registro através dos estágios de aprovação. As transições de registro corretas garantem que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, como diários e dados reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto, antes de prosseguir.
