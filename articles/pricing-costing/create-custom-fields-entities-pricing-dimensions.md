---
title: Criar campos e entidades personalizados como dimensões de preços
description: Este tópico fornece informações sobre como criar conjuntos de opções ou entidades personalizadas.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 40a6a4173cb0e4d7ea5bcf24c8954fe9d7e079d1e9ecf4aac252b5133f12d3ff
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003622"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Criar campos e entidades personalizados como dimensões de preços

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Conclua as etapas a seguir quando quiser criar uma entidade ou um conjunto de opções personalizado para usar como dimensão de precificação. Para obter mais informações, consulte [Visão geral de dimensões de precificação](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> É recomendável fazer todas as alterações de dimensão de preço personalizadas em outra solução. Esta importante prática recomendada fornece flexibilidade no futuro para atualizar ou remover as alterações conforme necessário. Isso também ajudará na reutilização do trabalho e facilitará a portabilidade dessas alterações para outra instância. Depois de fazer todas as alterações necessárias, exporte essa solução como **Solução gerenciada** e importe-a para outras instâncias para reutilizar a configuração de preços.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Criar campos e conjuntos de opções personalizados na solução de dimensão de preço

Uma dimensão de preço pode ser um conjunto de opções ou uma entidade. Ambos deve ser criados em sua solução de preço. As etapas deste procedimento explicam como criar dimensões baseadas em entidade e dimensões baseadas em conjunto de opções.

### <a name="entity-based-dimensions"></a>Dimensões baseadas em entidade
Para criar dimensões baseadas em entidade, siga estas etapas:

1. Vá para **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**.
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades**.
3. Selecione **Novo** para criar uma nova entidade denominada **Cargo Padrão**. 
4. Insira as informações necessárias restantes e selecione **Salvar**.

> ![Definição da entidade de cargo padrão.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensões baseadas em conjunto de opções 
Você pode criar duas dimensões baseadas em conjunto de opções. 

- Use **Local de Trabalho do Recurso** para rastrear o preço do local de trabalho **Casa** e trabalho **No local**. 
- Use **Horas de trabalho do recurso** com valores **Regular** e **Hora extra** para aplicar uma marcação quando o trabalho for concluído.

O gráfico a seguir fornece uma exibição da dimensão de **Local do Trabalho do Recurso**. 

> ![Dimensão de preço baseada em conjunto de opções chamada Local de Trabalho do Recurso.](media/Option-set-PD-called-Resource-Work-Location.png)

O gráfico a seguir fornece uma exibição da dimensão de **Horas de Trabalho do Recurso**. 

> ![Dimensão de preço baseada em conjunto de opções chamada Horas de Trabalho do Recurso.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Vá para **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Conjuntos de Opções**. 
3. Selecione **Novo** para criar um novo conjunto de opções, insira as informações necessárias restantes e selecione **Salvar**.

## <a name="create-data-for-entity-based-dimensions"></a>Criar dados para dimensões baseadas em entidade

Você pode criar dados para dimensões baseadas em entidade manualmente, ou usando a importação ou as chamadas de serviço do Microsoft Excel. Use as etapas neste procedimento para criar dois cargos padrões, **Engenheiro de Sistemas** e **Engenheiro de Sistemas Sênior** na dimensão baseada em entidade, **Cargo Padrão**. Se os dados que quiser criar forem pequenos, como no exemplo a seguir, você poderá usar um formulário padrão.

1. Selecione **Localização Avançada**.
2. Selecione a entidade **Cargo Padrão** e selecione **Resultados**. Todas as linhas na entidade **Cargo Padrão** serão mostradas.
3. Selecione **Novo** e, no campo **Nome**, insira "Engenheiro de Sistemas" e selecione **Salvar**.
4. Feche a página. 
5. Repita as etapas de 1 a 3 para criar outro cargo padrão para "Engenheiro de Sistemas Sênior".

> ![Dados de exemplo para a entidade Cargo Padrão.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]