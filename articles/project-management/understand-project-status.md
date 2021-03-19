---
title: Entender o status de projeto
description: Este tópico fornece informações sobre o status atribuído a projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286459"
---
# <a name="understand-project-status"></a>Entender o status de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


A seção **Status** na página **Entidade de Projeto** fornece um resumo da integridade de um projeto com base no custo e esforço.


## <a name="status-summary-fields"></a>Campos do resumo do status

- **Status geral do projeto** é um campo editável que mostra o status geral do projeto. Esse campo usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco. 
- O campo **Comentários** permite ao gerente do projeto inserir comentários específicos sobre o status. 
- O campo **Status** atualizado em não é editável. O valor neste campo é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.
- Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da grade de acompanhamento. Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, esses campos serão atualizados como **Adiantado**. Quando a variação de agenda e de custo para o nó raiz for negativa, esses campos serão definidos como **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]