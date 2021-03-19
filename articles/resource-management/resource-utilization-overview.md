---
title: Visão geral da utilização de recurso
description: Este tópico fornece informações sobre a utilização do recurso no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279304"
---
# <a name="resource-utilization-overview"></a>Visão geral da utilização de recurso

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Os recursos podem ter horas trabalhadas faturáveis de destino. Essas horas trabalhadas de destino são definidas como um atributo na função padrão de um recurso ou definidas no registro do recurso reservável individual. Os cálculos de horas trabalhadas se baseiam nas horas reais que os recursos relataram usando entradas de hora aprovadas.

As fórmulas a seguir são usadas para calcular as horas trabalhadas:

  - Horas trabalhadas faturáveis = Horas reais passíveis de cobrança ÷ Capacidade do recurso
  - Horas trabalhadas não faturáveis = Tempo real com ID do tipo de cobrança = Não passível de cobrança, Complementar ou Não disponível ÷ Capacidade do recurso
  - Interno = Tempo real sem contrato de vendas ÷ Capacidade do recurso
  - Capacidade do recurso = Horas de trabalho do recurso – Ausência temporária – Dias de folga

Você pode encontrar a exibição **Horas Trabalhadas do Recurso** no painel **Recursos**.

Cada célula na grade representa o percentual de horas trabalhadas faturáveis do recurso em um período, como dia, semana ou mês. As fórmulas a seguir são usadas para colorir as células:

  - **Verde**: horas trabalhadas faturáveis >= horas trabalhadas de destino do recurso
  - **Amarelo**: horas trabalhadas de destino – 20 <= horas trabalhadas faturáveis < horas trabalhadas de destino
  - **Vermelho**: horas trabalhadas faturáveis < horas trabalhadas de destino – 20

Como a exibição **Horas Trabalhadas do Recurso** é baseada no Painel de Agendamento, você pode usar as funcionalidades de filtragem dele para filtrar seus resultados.

A grade exige que você defina as horas trabalhadas de destino na função ou no recurso individual. Para definir essa configuração, vá para **Recursos** > **Funções de recursos**.

Além disso, uma função padrão deve ser atribuída a cada recurso reservável. Vá para **Recursos** > **Recursos**. Na guia **Project Service**, verifique se uma função do recurso está definida e se o campo **É Padrão** está definido como **Sim**. É possível adicionar outras funções onde **É Padrão** = **Não**. A função onde **É Padrão** = **Sim** é usada para avaliar a utilização do recurso em relação ao destino dessa função.

Na guia **Project Service**, você também pode definir horas trabalhadas de destino individuais para o recurso. O cálculo de horas trabalhadas então usa essas horas trabalhadas de destino para avaliar o destino do recurso em vez do destino da função padrão do recurso.

As horas trabalhadas são mostradas para um recurso, somente se ele tiver tempo passível de cobrança, aprovado durante o período exibido na grade.


[!INCLUDE[footer-include](../includes/footer-banner.md)]