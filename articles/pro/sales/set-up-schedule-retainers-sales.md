---
title: Configurar uma agenda de honorários – lite
description: Este tópico fornece informações sobre como configurar uma agenda de honorários no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181258"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Configurar uma agenda de honorários – lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

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
