---
title: Notas do desenvolvedor para Aprovações
description: Este artigo fornece informações adicionais do desenvolvedor sobre como trabalhar com aprovações.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924738"
---
# <a name="developer-notes-for-approvals"></a>Notas do desenvolvedor para Aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations inclui lógica de validação que garante a transição correta do registro através dos estágios de aprovação. As transições de registro corretas garantem que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, como diários e dados reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto, antes de prosseguir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]