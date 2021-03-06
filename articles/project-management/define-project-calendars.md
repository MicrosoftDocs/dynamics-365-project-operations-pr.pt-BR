---
title: Definir calendários de projeto
description: Este tópico fornece informações sobre como usar um calendário de projeto para controlar o cronograma do projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897977"
---
# <a name="define-project-calendars"></a>Definir calendários de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

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
