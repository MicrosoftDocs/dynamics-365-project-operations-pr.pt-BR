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
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290255"
---
# <a name="developer-notes-for-approvals"></a>Notas do desenvolvedor para Aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations inclui lógica de validação que garante a transição correta do registro através dos estágios de aprovação. As transições de registro corretas garantem que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, como diários e dados reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto, antes de prosseguir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]