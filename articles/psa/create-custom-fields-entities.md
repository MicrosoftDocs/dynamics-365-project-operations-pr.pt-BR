---
title: Criar campos e entidades personalizados
description: Este tópico explica como criar conjuntos de opções e entidades em sua própria solução na plataforma Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f501bcc106a296f35bba996b6ab3a8b758cefb1926033faf04ee23c42bc94d39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992417"
---
# <a name="create-custom-fields-and-entities"></a>Criar campos e entidades personalizados 

[!include [banner](../includes/psa-now-project-operations.md)]

Conclua as etapas a seguir sempre que quiser criar uma entidade ou um conjunto de opções personalizado na plataforma Power Apps.  
Os procedimentos neste tópico devem ser concluídos usando a interface da Web do PSA (Project Service Automation).

> [!IMPORTANT]
> É recomendável fazer todas as alterações de dimensão de preço personalizadas em outra solução. Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância. Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a em outras instâncias para reutilizar sua configuração de preço.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Criar campos e conjuntos de opções personalizados na solução de dimensão de preço

Uma dimensão de preço pode ser um conjunto de opções ou uma entidade. Ambos deve ser criados em sua solução de preço. As etapas deste procedimento explicam como criar dimensões baseadas em entidade e dimensões baseadas em conjunto de opções.

### <a name="entity-based-dimensions"></a>Dimensões baseadas em entidade

1. No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **Dimensões de preços do(a) \<your organization name>**.
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades**.
3. Clique em **Novo** para criar uma nova entidade denominada **Cargo Padrão**. Insira as informações necessárias restantes e clique em **Salvar**.

> ![Definição da entidade de cargo padrão.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensões baseadas em conjunto de opções 
Você pode criar duas dimensões baseadas em conjunto de opções. Use **Local de Trabalho do Recurso** para rastrear o preço do trabalho do local **Página Inicial** e do trabalho **No Local** e use **Horas de Trabalho do Recurso** com os valores **Regular** e **Horas Extras** para aplicar um markup quando o trabalho é concluído.


1. No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **Dimensões de preços do(a) \<your organization name>**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Conjuntos de Opções**. 
3. Clique em **Novo** para criar um novo conjunto de opções, insira as informações necessárias restantes e clique em **Salvar**.

> ![Dimensão de preço baseada em conjunto de opções chamada Local de Trabalho do Recurso.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensão de preço baseada em conjunto de opções chamada Horas de Trabalho do Recurso.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Criar dados para dimensões baseadas em entidade

Você pode criar dados para dimensões baseadas em entidade manualmente, ou usando a importação ou as chamadas de serviço do Microsoft Excel. Use as etapas neste procedimento para criar dois cargos padrões, **Engenheiro de Sistemas** e **Engenheiro de Sistemas Sênior** na dimensão baseada em entidade, **Cargo Padrão**. Se os dados que quiser criar forem pequenos, como no exemplo a seguir, você poderá usar um formulário padrão.

1. No PSA, clique em **Localização Avançada**. Selecione a entidade **Cargo Padrão** e clique em **Resultados**. Todas as linhas na entidade **Cargo Padrão** serão mostradas.
2. Clique em **Novo**. No campo **Nome**, insira "Engenheiro de Sistemas" e clique em **Salvar**.
3. Feche o formulário. 
4. Repita as etapas de 1 a 3 para criar outro cargo padrão para "Engenheiro de Sistemas Sênior".

> ![Dados de exemplo para a entidade Cargo Padrão.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]