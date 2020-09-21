---
title: Criar campos e entidades personalizados
description: Este tópico explica como criar conjuntos de opções e entidades em sua própria solução na plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749140"
---
# <a name="create-custom-fields-and-entities"></a>Criar campos e entidades personalizados 

Conclua as etapas a seguir sempre que quiser criar uma entidade ou um conjunto de opções personalizado na plataforma Power Apps.  
Os procedimentos neste tópico devem ser concluídos usando a interface da Web do PSA (Project Service Automation).

> [!IMPORTANT]
> É recomendável fazer todas as alterações de dimensão de preço personalizadas em outra solução. Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância. Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a em outras instâncias para reutilizar sua configuração de preço.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Criar uma solução personalizada para dimensões de preço
1. No PSA, clique em **Configurações** > **Soluções** e em **Novo** para criar uma solução. 
2. Nomeie a solução, **dimensões de preço da \<nome da sua organização>**, insira as informações necessárias restantes e clique em **Salvar**.

> ![Criando uma solução personalizada para dimensões de preço](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Criar campos e conjuntos de opções personalizados na solução de dimensão de preço

Uma dimensão de preço pode ser um conjunto de opções ou uma entidade. Ambos deve ser criados em sua solução de preço. As etapas deste procedimento explicam como criar dimensões baseadas em entidade e dimensões baseadas em conjunto de opções.

### <a name="entity-based-dimensions"></a>Dimensões baseadas em entidade

1. No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<nome da sua organização>**.
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades**.
3. Clique em **Novo** para criar uma nova entidade denominada **Cargo Padrão**. Insira as informações necessárias restantes e clique em **Salvar**.

> ![Definição da entidade de cargo padrão](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensões baseadas em conjunto de opções 
Você pode criar duas dimensões baseadas em conjunto de opções. Use **Local de Trabalho do Recurso** para rastrear o preço do trabalho do local **Página Inicial** e do trabalho **No Local** e use **Horas de Trabalho do Recurso** com os valores **Regular** e **Horas Extras** para aplicar um markup quando o trabalho é concluído.


1. No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<nome da sua organização>**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Conjuntos de Opções**. 
3. Clique em **Novo** para criar um novo conjunto de opções, insira as informações necessárias restantes e clique em **Salvar**.

> ![Dimensão de preço baseada em conjunto de opções chamada Local de Trabalho do Recurso ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensão de preço baseada em conjunto de opções chamada Horas de Trabalho do Recurso ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Criar dados para dimensões baseadas em entidade

Você pode criar dados para dimensões baseadas em entidade manualmente, ou usando a importação ou as chamadas de serviço do Microsoft Excel. Use as etapas neste procedimento para criar dois cargos padrões, **Engenheiro de Sistemas** e **Engenheiro de Sistemas Sênior** na dimensão baseada em entidade, **Cargo Padrão**. Se os dados que quiser criar forem pequenos, como no exemplo a seguir, você poderá usar um formulário padrão.

1. No PSA, clique em **Localização Avançada**. Selecione a entidade **Cargo Padrão** e clique em **Resultados**. Todas as linhas na entidade **Cargo Padrão** serão mostradas.
2. Clique em **Novo**. No campo **Nome**, insira "Engenheiro de Sistemas" e clique em **Salvar**.
3. Feche o formulário. 
4. Repita as etapas de 1 a 3 para criar outro cargo padrão para "Engenheiro de Sistemas Sênior".

> ![Dados de Exemplo para a entidade Cargo Padrão ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades necessárias e componentes relacionados do PSA à Solução de Dimensão de Preço
Você precisará adicionar as entidades a seguir do Project Service à sua solução de precificação. Use as etapas neste procedimento para fazer algumas alterações importantes de esquema na solução de precificação para que as entidades se tornem conscientes das novas dimensões de preço.

1. No PSA, clique em **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<nome da sua organização>**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.
3. Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:

- Real
- Recurso Reservável
- Linha de Estimativa
- Detalhes da Linha da Fatura
- Linha do Diário
- Detalhes da Linha de Contrato do Projeto
- Membro da Equipe do Projeto
- Detalhes da Linha de Cotação
- Markup de Preço da Função
- Preço da Função 
- Entrada de Horas 

> ![Adicionar entidades existentes à solução de dimensões de preço](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução](media/Dimension-Components.png)

> [!NOTE]
> Certifique-se de incluir todos os formulários e exibições para cada uma das entidades selecionadas.

4. Quando solicitado a incluir entidades dependentes para as entidades selecionadas acima, clique em **Não**.

> ![Não inclua todos os componentes selecionados](media/Do-not-include-required.png)


