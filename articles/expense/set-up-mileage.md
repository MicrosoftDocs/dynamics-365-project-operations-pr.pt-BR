---
title: Configurar quilometragem usando níveis de taxa de quilometragem
description: Este tópico fornece informações sobre taxas de quilometragem e níveis de taxas de quilometragem.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 030c6abca169b712312ad70ed2ac8262f3d0777bcf93dcccfd956f2f9e0ea77c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993047"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Configurar quilometragem usando níveis de taxa de quilometragem

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Quando uma despesa é relatada e a categoria de despesa selecionada é **Quilometragem**, o valor dessa linha de despesas é calculado de acordo com o valor *taxa por quilometragem*. Esse valor é determinado usando níveis de quilometragem definidos ou, se não houver níveis de taxa de quilometragem configurados, seguindo uma taxa padrão de quilometragem. 

As camadas de taxa de quilometragem podem ser configuradas acessando **Gerenciamento de Despesas** > **Configurar** > **Geral** > **Categorias de despesas** > **Quilometragem** > **Configuração de categoria**.

Depois de fazer upgrade para 10.0.18, se sua organização usar a categoria de despesas de quilometragem, habilite o recurso de quilometragem após revisar as alterações de design abaixo. 

O novo design de níveis de taxa de quilometragem impacta como o valor do campo **Quantidade** é processado. Antes do lançamento de 10.0.18, o valor no campo **Quantidade** foi considerado o limite inferior. Quando a acumulação cruzou esse valor, a taxa correspondente foi usada.  A partir da versão 10.0.18, o valor no campo **Quantidade** é considerado o limite superior. A taxa correspondente é usada quando o acúmulo de milhas é menor que o valor do campo **Quantidade**.  O novo modelo para níveis de quilometragem ajuda com consistência entre níveis de quilometragem e melhor usabilidade.   

Todos os relatórios de despesas aprovados serão recalculados durante a postagem de acordo com o novo design.

## <a name="example"></a>Exemplo
 
### <a name="before-version-10018"></a>Antes da versão 10.0.18
Com dois níveis de taxa de quilometragem, o campo **Quantidade** em cada camada representa o limite inferior de quilometragem. Atualmente, a camada um tem um valor de zero (0) e uma taxa de 0,45, e a camada dois tem um valor de 1000 e uma taxa de 0,25. Se as milhas ou quilômetros acumulados cruzarem o valor no campo, a taxa relacionada será usada. Se não houver linha com quantidade zero, o sistema usará a taxa de quilometragem definida no Gerenciamento de despesas. 
 
Se um funcionário enviar um relatório de despesas com 1.500 milhas, as duas linhas de quilometragem no relatório de despesas publicado seriam: 1000 (taxa de 0,45) + 500 (taxa de 0,25) = 575,00.

### <a name="after-version-10018"></a>Após a versão 10.0.18
Em 10.0.18, o campo **Quantidade** em cada camada representa o limite superior da camada. Atualmente, a camada um tem um valor de zero (999) e uma taxa de 0,45, e a camada dois tem um valor de 999.999.999,00 e uma taxa de 0,25. Se as milhas ou quilômetros acumulados cruzarem o valor no campo **Quantidade**, a taxa relacionada será usada. Se todos os limites superiores forem excedidos, o sistema usará a taxa de quilometragem definida no Gerenciamento de despesas. 
 
Para calcular corretamente o mesmo cenário, a configuração do nível deve ser alterada. O campo **Quantidade** na camada um tem um valor de 999,00 e um valor de 999.999.999,00 na camada dois. Se um funcionário exceder a quantidade total de milhas ou quilômetros na camada um, o sistema usará a taxa de quilometragem definida no Gerenciamento de despesas. 
  
Se um funcionário enviar um relatório de despesas com 1.500 milhas, as duas linhas de quilometragem no relatório de despesas publicado seriam: 1000 (taxa de 0,45) + 500 (taxa de 0,25) = 575.

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Habilite o cálculo do valor da Quilometragem para vários níveis de quilometragem com o mesmo recurso de taxa

O recurso **Cálculo do valor da Quilometragem para vários níveis de quilometragem com o mesmo recurso de taxa** melhora o cálculo da taxa de quilometragem. Conclua as etapas a seguir para ativar esse recurso.

1. Vá para **Configurações** > **Gerenciamento de Recursos**. 
2. Na lista, localize e selecione **Cálculo do valor da quilometragem para vários níveis de quilometragem com a mesma taxa** e, em seguida, selecione **Habilitar agora**.

Depois de ativar o recurso, redefina os níveis de quilometragem para refletir corretamente o valor do campo **Quantidade**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
