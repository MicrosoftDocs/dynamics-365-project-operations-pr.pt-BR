---
title: Definir calendários de projeto
description: Este tópico fornece informações sobre como aplicar um modelo de calendário a um projeto para rastrear a agenda do projeto.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998982"
---
# <a name="define-project-calendars"></a>Definir calendários de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Para criar e gerenciar um projeto, você deve aplicar um modelo de calendário ao projeto. O modelo de calendário define os seguintes atributos de projeto:

- Horas de trabalho, incluindo horário de início e término
- Dias úteis
- Exceções de calendário, como dias não úteis

O modelo de calendário aplicado a um projeto é uma cópia do modelo de calendário definido nas configurações da sua organização.

> [!NOTE]
> Se você alterar o modelo de calendário, essas alterações não se propagarão para as horas de trabalho do projeto. Para alterar as horas de trabalho do projeto, um novo modelo deve ser aplicado.

Para criar um modelo de calendário para sua organização, existem dois requisitos principais:

- Defina as horas de trabalho desejadas do modelo usando um recurso reservável novo ou existente.
- Crie um novo modelo de calendário e associe o modelo ao recurso reservável.

**Defina as horas de trabalho do modelo**

1. Vá para **Recursos** \> **Recursos**.
2. Crie um novo recurso para fazer referência no modelo de calendário ou selecione um recurso existente.
3. Selecione a guia **Horas de Trabalho** do recurso e complete as instruções em [Definir horas de trabalho para um recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar as regras de calendário.

**Criar um novo modelo de calendário**

1. Acesse **Configurações** \> **Modelo de Calendário**.
2. Selecione **Novo** e insira um nome, uma descrição e um recurso de modelo.

> [!NOTE]
> Quando um recurso é referenciado em um modelo de calendário, uma cópia do calendário do recurso é associada ao modelo de calendário. Se as horas de trabalho do modelo copiado mudarem, essas alterações não serão propagadas no modelo de calendário.

Agora é possível associar o modelo de trabalho a um modelo de calendário de projeto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

