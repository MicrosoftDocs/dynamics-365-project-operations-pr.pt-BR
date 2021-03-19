---
title: Definir calendários de projeto
description: Este tópico fornece informações sobre como usar um calendário de projeto para controlar o cronograma do projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286954"
---
# <a name="define-project-calendars"></a>Definir calendários de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Para criar uma agenda de projeto, crie um modelo de calendário de projeto que defina o número de horas de trabalho por dia e todos os feriados comerciais. Para criar um modelo de calendário de projeto, associe um modelo de trabalho ao campo **Modelo de calendário** do projeto. Siga estas etapas para criar um modelo de trabalho.

1. No painel de navegação à esquerda, selecione **Recursos**. 
2. Na página de lista **Recursos**, abra um registro de usuário e selecione **Mostrar Horas de Trabalho**.

  > [!NOTE]
  > Certifique-se de permitir pop-ups na página do navegador. Isso permite ver as horas de trabalho definidas para o recurso.
  
3. Na guia **Exibição Mensal**, selecione **Configurar**. Uma lista de três opções é exibida: 

  - Nova Agenda Semanal
  - Agenda de Trabalho para Um Dia
  - Folga

4. Selecione **Nova Agenda Semanal** e defina as opções para essa agenda de recurso. Você pode definir uma agenda semanal recorrente, parâmetros de hora diários, feriados comerciais e muito mais.
5. Defina um intervalo de datas, selecione **Salvar** e **Fechar**. 
6. Volte para a página de lista **Recursos** e selecione o recurso para o qual você definiu as horas de trabalho. 
7. Selecione **Definir Calendário como** para definir o modelo de trabalho. 
8. Na caixa de diálogo **Modelo de Trabalho**, insira um nome para o modelo de trabalho e selecione **Aplicar**. 

Agora é possível associar o modelo de trabalho a um modelo de calendário de projeto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]