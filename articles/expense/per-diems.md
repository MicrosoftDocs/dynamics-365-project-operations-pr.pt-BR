---
title: Diárias
description: Este tópico fornece informações sobre as regras de diária usadas no gerenciamento de despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907860"
---
# <a name="per-diems"></a>Diárias

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_


Uma diária é um subsídio pago a um funcionário que viaja a trabalho. No gerenciamento de despesas, você pode criar regras de diária para várias situações de viagem. As taxas de diária podem ser baseadas na época do ano, no local da viagem ou em ambos. Ao criar uma regra de diária, você pode especificar que uma porcentagem da taxa da diária será retida se um funcionário receber refeições ou serviços gratuitos. Você também pode definir um número mínimo e máximo de horas que a taxa da diária pode aplicar à viagem de um funcionário.

## <a name="configuration"></a>Configuração 

1. Para adicionar locais de diária, vá para **Configurar** > **Cálculos e códigos** > **Locais de diária**.
2. Para cada um dos locais adicionados acima, selecione uma taxa de diária e uma moeda que seja válida entre uma data de início e término específica para hotel, refeições e outras despesas. As taxas e moedas diárias são configuradas em **Configurar** > **Cálculos e códigos** > **Diárias**.
3. No página **Locais de diária**, configure os níveis da taxa de diária. Os níveis da taxa de diária permitem definir a divisão percentual de uma diária para hotel, refeições e outras despesas. 
4. Para especificar a redução percentual de refeição para o café da manhã, almoço ou jantar, atualize os campos na página **Parâmetros de gerenciamento de despesas** na guia **Diárias**. 
    
## <a name="submit-expenses-using-per-diem"></a>Enviar despesas usando diária
Para enviar despesas usando diárias, use a categoria de despesas **Diárias** ao criar um relatório de despesas. Digite o **Data inicial de diária**, **Data final de diária** e o **Local da diária**. O valor será calculado com base nas taxas de diária para o local selecionado e a redução de refeição será calculada com base nos níveis de taxas de diárias.
