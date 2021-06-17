---
title: Notas do desenvolvedor para Aprovações
description: Este tópico fornece informações adicionais do desenvolvedor sobre como trabalhar com aprovações.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996777"
---
# <a name="developer-notes-for-approvals"></a>Notas do desenvolvedor para Aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations inclui lógica de validação que garante a transição correta do registro através dos estágios de aprovação. As transições de registro corretas garantem que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, como diários e dados reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto, antes de prosseguir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]