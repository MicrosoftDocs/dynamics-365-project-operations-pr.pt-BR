---
title: Despesas com diárias
description: Este artigo fornece informações sobre como trabalhar com despesas com diárias.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923174"
---
# <a name="per-diem-expenses"></a>Despesas com diárias

> [!IMPORTANT] 
> A funcionalidade descrita neste artigo está disponível para usuários específicos como parte de uma versão preliminar.

Um pagamento de diária é um subsídio diário fixo e predeterminado que uma empresa paga a seus funcionários para hospedagem (hotéis), refeições e despesas eventuais que esses funcionários incorrem ao viajar a trabalho. A empresa paga esse subsídio aos funcionários em vez de pagar as despesas de viagem reais. Os funcionários podem usar o subsídio de diária de **Despesas eventuais/Outros** para cobrir gorjetas, serviço de quarto, lavanderia ou lavagem a seco em reuniões de negócios importantes. A taxa de diária pode variar, dependendo se o empregador opta por reembolsar o custo combinado de hospedagem e refeições ou apenas o custo de refeições e despesas eventuais.

As taxas de diária podem ser baseadas na época do ano, no local da viagem ou em ambos. Ao criar uma regra de diária, você pode especificar que uma porcentagem da taxa de diária será retida caso um funcionário receba refeições ou serviços de cortesia. Você também pode definir um número mínimo e um número máximo de horas para aplicação da taxa de diária à viagem de um funcionário.

A diária é calculada como o subsídio total oferecido por dia menos a redução de despesas com refeições (custo das refeições de cortesia) que são fornecidas ao funcionário.

## <a name="configure-per-diems"></a>Configurar diárias

Para configurar despesas com diárias, siga estas etapas.

1. Vá para **Gerenciamento de despesas** \> **Configuração** \> **Geral** \> **Parâmetros de gerenciamento de despesas**.
2. Na guia **Diária**, no campo **Calcular redução de refeições por**, selecione como devem ser calculadas as diárias:

    - **Tipo de refeição por viagem** – Calcular a diária com base no tipo de refeição inserida (café da manhã, almoço ou jantar) e na redução de despesas com refeições especificada para cada tipo de refeição para o subsídio de diária durante a viagem.
    - **Tipo de refeição por dia** – Calcular a diária com base no tipo de refeição inserida e na redução de despesas com refeições especificada para cada tipo de refeição para o subsídio de diária por dia.
    - **Número de refeições por dia** – Calcular a diária com base no número de refeições inseridas por dia e na redução de despesas com refeições para o número de refeições fornecidas a cada dia.

3. Vá para **Gerenciamento de despesas** \> **Configuração** \> **Cálculos e códigos** \> **Localizações por dia**.
4. Adicione os locais onde as diárias podem ser usadas.
5. Para cada local adicionado, na guia **Diárias**, selecione a taxa de diária e a moeda válidas entre as datas de início e de término específicas para hospedagem, refeições e outras despesas. Para configurar as taxas de diária e as moedas, vá para **Gerenciamento de despesas** \> **Configuração** \> **Cálculos e códigos** \> **Diárias**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Diárias na interface de despesas reformulada

O recurso de diária tem suporte no espaço de trabalho **Gerenciamento de Despesas** reformulado do Microsoft Dynamics 365 Finance versão 10.0.25 e posterior.

Para habilitar diárias, siga estas etapas.

1. No espaço de trabalho **Gerenciamento de Recursos**, localize e selecione o recurso **Relatórios de Despesas Reinventados** na lista e selecione **Habilitar agora**.
2. Localize e selecione o recurso **Interface reinventada do relatório de despesas com diárias** na lista e selecione **Habilitar agora**.

## <a name="how-the-feature-works"></a>Como o recurso funciona

Esta seção fornece exemplos de três cenários de configuração. Para cada exemplo, o campo **Calcular redução de refeições por** está definido com um valor diferente. Para todos os três exemplos, o valor total a pagar é igual, até que a redução de despesas com refeições seja aplicada. Depois desse momento, o valor total a pagar é diferente em cada exemplo.

Para criar a despesa com diárias usada nos três exemplos, siga estas etapas.

1. Vá para **Espaços de Trabalho** \> **Gerenciamento de Despesas**.
2. Selecione **Novo relatório de despesas** ou selecione um relatório de despesas existente.
3. Adicione uma nova despesa. No campo **Categoria**, selecione **Diária**. Selecione o local e as datas de início e de término de sua viagem. A diária para hospedagem, refeições e despesas eventuais (outras despesas) é calculada com base no subsídio diário definido para o local selecionado.

    Por exemplo, você seleciona **Redmond (USA)** como local. O subsídio diário para esse local é de 150 dólares americanos (USD 150) para hospedagem, USD 75 para refeições e USD 5 para despesas eventuais. A data de início é 10 de janeiro e a data de término é 14 de janeiro. Portanto, a duração selecionada é de cinco dias quando a configuração selecionada é de dias corridos com hora, e o período selecionado começa e termina às 12h00 nas datas de início e término. Seguem os cálculos:

    - Valor total a pagar = 5 × (150 + 75 + 5) = 5 × 230 = USD 1.150
    - Refeição e parte eventual do valor total = 5 × (75 + 5) = USD 400

Se café da manhã, almoço e jantar foram fornecidos durante a viagem, essas refeições devem ser contabilizadas como uma redução de despesas com refeições.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemplo 1: Diária em que as reduções de despesas com refeições são baseadas no tipo de refeição por viagem

Neste exemplo, a redução de despesas com refeições é de 30% para café da manhã, 30% para almoço e 40% para jantar. Na página **Parâmetros de gerenciamento de despesas**, o campo **Calcular redução de refeições por** é definido como **Tipo de refeição por viagem**. Aqui estão os cálculos caso tenham sido fornecidos três cafés da manhã, dois almoços e nenhum jantar ao funcionário:

- Redução de despesas com refeições = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112,50
- Refeições e despesas eventuais = 400 – 112,50 = USD 287,50
- Valor total a pagar = Subsídio total – Redução de despesas com refeições = 1.150 – 112,50 = USD 1.037,50

![Despesa com diárias em que a redução de despesas com refeições é baseada no tipo de refeição por viagem.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemplo 2: Diária em que as reduções de despesas com refeições são baseadas no tipo de refeição por dia

Neste exemplo, a redução de despesas com refeições é de 30% para café da manhã, 30% para almoço e 40% para jantar. Na página **Parâmetros de gerenciamento de despesas**, o campo **Calcular redução de refeições por** é definido como **Tipo de refeição por dia**. Nesse caso, na grade **Refeições**, na caixa de diálogo **Editar despesa**, limpe as caixas de seleção para indicar quais refeições foram fornecidas a você durante a viagem.

Por exemplo, aqui estão os cálculos caso tenha sido fornecido café da manhã nos três primeiros dias da viagem:

- Redução diária de despesas com refeições para cada um dos três primeiros dias = 75 × 30% = USD 22,50
- Total da redução de despesas com refeições = 3 × 22,50 = USD 67,50
- Refeições e despesas eventuais para os dias 1 a 3 = 75 – 22,50 = USD 57,50
- Total de refeições e despesas eventuais = Soma de refeições e despesas eventuais nos cinco dias = 400 – 67,50 = USD 332,50
- Valor total a pagar = Valor total – Redução de despesas com refeições = 1.150 – 67,50 = USD 1.082,50

![Despesa com diárias em que a redução de despesas com refeições é baseada no tipo de refeição por dia.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemplo 3: Diária em que as reduções de despesas com refeições são baseadas no número de refeições por dia

Neste exemplo, a redução de despesas com refeições é calculada com base no número de refeições fornecidas por dia (ou seja, o campo **Calcular redução de refeições por** na página **Parâmetros de gerenciamento de despesas** é definido como **Número de refeições por dia**). Na grade **Refeições**, na caixa de diálogo **Editar despesa**, limpe as caixas de seleção para indicar quais refeições foram fornecidas.
Neste caso, a redução de despesas com refeições é baseada apenas no número de refeições fornecidas e não no tipo de refeição (Café da manhã/almoço/jantar) fornecida.

Aqui estão os cálculos de diárias quando o subsídio diário é de USD 150 para hospedagem, USD 75 para refeições e USD 5 para despesas eventuais:

- **Valor total a pagar** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1.150
- **Uma refeição:** redução de despesas com refeições = 20% = USD 15
- **Duas refeições:** redução de despesas com refeições = 50% = USD 37,50
- **Três refeições:** redução de despesas com refeições = 100% = USD 75

Seguem os cálculos do **subsídio para refeições e despesas eventuais**, que inclui USD 5 para despesas eventuais:

- Dia 1 - Duas refeições fornecidas = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Dia 2 - Duas refeições fornecidas = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Dia 3 - Uma refeição fornecida = (75 – 15) + 5 = 60 + 5 = USD 65
- Dia 4 - Nenhuma refeição fornecida = (75 – 0) + 5 = 75 + 5 = USD 80
- Dia 5 - Três refeições fornecidas = (75 – 75) + 5 = 0 + 5 = USD 5

- Total de refeições e despesas eventuais = Refeições e despesas eventuais de Dia 1+ Dia 2 + Dia 3+ Dia 4+ Dia 5 = USD 235
- Total de redução de despesas com refeições = Redução de despesas com refeições de Dia 1+ Dia 2 + Dia 3+ Dia 4+ Dia 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Valor total a pagar = Subsídio total – Total de redução de despesas com refeições = USD 1.150 – USD 165 = USD 985

![Despesa com diárias em que a redução de despesas com refeições é baseada no número refeições por dia.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A partir do Finance versão 10.0.23, se você usar a interface de despesas reformulada, não será possível criar despesas com diárias com datas sobrepostas. Se tentar, você receberá uma mensagem de erro.
