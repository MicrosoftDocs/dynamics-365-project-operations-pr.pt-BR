---
title: Notas do desenvolvedor para Aprovações
description: Este tópico fornece informações adicionais do desenvolvedor sobre como trabalhar com aprovações.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579706"
---
# <a name="developer-notes-for-approvals"></a>Notas do desenvolvedor para Aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations inclui lógica de validação que garante a transição correta do registro através dos estágios de aprovação. As transições de registro corretas garantem que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, como diários e dados reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto, antes de prosseguir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]