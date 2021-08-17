---
title: Trabalhar com despesas pessoais em um relatório de despesas
description: Este tópico fornece informações sobre como lidar com despesas pessoais incorridas por funcionários durante viagens de negócios.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 5e1162133eec5a85675bf686855d420c50de0eaf045d81c4b417b6fe66ee19fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993137"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Trabalhar com despesas pessoais em um relatório de despesas

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Em uma viagem de negócios, um funcionário pode pagar despesas pessoais com seu cartão de crédito corporativo. Se um processo não foi definido para lidar com despesas pessoais, o processo de aprovação do relatório de despesas pode ser interrompido quando um funcionário envia seu relatório de despesas discriminado.

Existem dois métodos que você pode usar para trabalhar com as despesas pessoais de um funcionário:

  - **Pago pelo funcionário**: sua organização não paga despesas pessoais que aparecem na fatura do cartão de crédito corporativo. Em vez disso, o funcionário paga as despesas diretamente à empresa de cartão de crédito. 
  - **Pago pela empresa**: sua organização paga a conta integral do cartão de crédito corporativo e, em seguida, debita da conta do funcionário as despesas pessoais.

Você pode selecionar o método que sua organização usa na página **Parâmetros de gerenciamento de despesas**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Ative a função de divisão de despesas quando o campo de valor pessoal tiver um valor definido

O recurso, **Ative a função de divisão de despesas quando o campo de valor pessoal tiver um valor definido** aplica-se apenas a relatórios de despesas que são aprovados usando um fluxo de trabalho de nível de linha. Os relatórios são aprovados indo para **Processar relatórios de despesas** > **Relatórios de despesas atribuídos a mim** > **Abrir relatório de despesas**. 

Para habilitar este recurso, vá para **Espaços de trabalho** > **Gerenciamento de recursos**, selecione **Ative a função de divisão de despesas quando o campo de valor pessoal tiver um valor definido** e, em seguida, selecione **Ativar agora**. 

Quando o recurso estiver habilitado, as linhas de despesas que usam essa funcionalidade geram duas linhas quando o relatório é enviado. Duas linhas são geradas para que o aprovador possa aprovar cada linha separadamente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
