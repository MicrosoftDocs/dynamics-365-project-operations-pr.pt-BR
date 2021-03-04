---
title: Configurar uma agenda de honorários
description: Este tópico fornece informações sobre como configurar uma agenda de honorários no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596358"
---
# <a name="set-up-a-retainer-schedule"></a>Configurar uma agenda de honorários

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As agendas de honorários são configuradas na página **Contrato do Projeto** no Dynamics 365 Project Operations.

1. Na página **Contrato do Projeto**, na guia **Adiantamentos e Honorários**, selecione **Configurar agenda de honorários**.
2. Na página da caixa de diálogo que é aberta, os campos listados na tabela a seguir são mostrados. A tabela dá uma ideia de como os valores inseridos impactam ou influenciam a agenda de honorários que será criada.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| Cliente do Contrato do Projeto | O cliente do contrato que será cobrado por este honorário ou adiantamento. | Se você tiver vários clientes no contrato e precisar faturar cada um deles por um valor específico de honorário ou adiantamento, crie manualmente uma fatura para cada cliente. |
| Início da Agenda de Honorários | Insira a data de início da agenda de honorários. | Esta data pode não ser a data em que o primeiro honorário ou adiantamento foi criado. A data em que o primeiro honorário ou adiantamento é criado, também é influenciada pela frequência da fatura. |
| Fim da Agenda de Honorários | Insira a data de término da agenda de honorários. | Esta data pode não ser a data em que o último honorário ou adiantamento foi criado. A data em que o último honorário ou adiantamento foi criado, também é influenciada pela frequência da fatura. |
| Número de Honorários a Serem Criados | Quando você insere o número de honorários a serem criados, o sistema usa a data de início e a frequência para criar o número neste campo. | Quando este campo é atualizado manualmente, o sistema ignora o valor no campo **Fim da Agenda de Honorários** e em vez disso cria o número específico de honorários ou adiantamentos. |
| Frequência da Fatura | A frequência com que o aplicativo criará honorários ou adiantamentos. | Este valor influencia diretamente no número de honorários e adiantamentos e nas datas de criação. |
| Valor Total | O valor total é o valor dividido nos pagamentos de honorário e adiantamento individual que serão criados. | Não há impacto posterior para esse campo. |