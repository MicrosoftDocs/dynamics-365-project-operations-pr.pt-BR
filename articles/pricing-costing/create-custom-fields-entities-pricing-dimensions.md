---
title: Criar campos e entidades personalizados como dimensões de preços
description: Este tópico fornece informações sobre como criar conjuntos de opções ou entidades personalizadas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071466"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Criar campos e entidades personalizados como dimensões de preços

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

Conclua as etapas a seguir sempre que quiser criar uma entidade ou um conjunto de opções personalizado.

> [!IMPORTANT]
> É recomendável fazer todas as alterações de dimensão de preço personalizadas em outra solução. Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância. Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a em outras instâncias para reutilizar sua configuração de preço.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Criar uma solução personalizada para dimensões de preço
1. Vá para **Configurações** > **Soluções** e selecione **Novo** para criar uma nova solução. 
2. Nomeie a solução, **dimensões de preço da \<your organization name>** , insira as informações necessárias restantes e selecione **Salvar**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Criar campos e conjuntos de opções personalizados na solução de dimensão de preço

Uma dimensão de preço pode ser um conjunto de opções ou uma entidade. Ambos deve ser criados em sua solução de preço. As etapas deste procedimento explicam como criar dimensões baseadas em entidade e dimensões baseadas em conjunto de opções.

### <a name="entity-based-dimensions"></a>Dimensões baseadas em entidade

1. Vá para **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**.
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Entidades**.
3. Selecione **Novo** para criar uma nova entidade denominada **Cargo Padrão**. 
4. Insira as informações necessárias restantes e selecione **Salvar**.


### <a name="option-set-based-dimensions"></a>Dimensões baseadas em conjunto de opções 
Você pode criar duas dimensões baseadas em conjunto de opções. Use **Local de Trabalho do Recurso** para rastrear o preço do trabalho do local **Página Inicial** e do trabalho **No Local** e use **Horas de Trabalho do Recurso** com os valores **Regular** e **Horas Extras** para aplicar um markup quando o trabalho é concluído.


1. Vá para **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Conjuntos de Opções**. 
3. Selecione **Novo** para criar um novo conjunto de opções, insira as informações necessárias restantes e selecione **Salvar**.

## <a name="create-data-for-entity-based-dimensions"></a>Criar dados para dimensões baseadas em entidade

Você pode criar dados para dimensões baseadas em entidade manualmente, ou usando a importação ou as chamadas de serviço do Microsoft Excel. Use as etapas neste procedimento para criar dois cargos padrões, **Engenheiro de Sistemas** e **Engenheiro de Sistemas Sênior** na dimensão baseada em entidade, **Cargo Padrão**. Se os dados que quiser criar forem pequenos, como no exemplo a seguir, você poderá usar um formulário padrão.

1. Selecione **Pesquisa Avançada** , a entidade **Cargo Padrão** e, depois, **Resultados**. Todas as linhas na entidade **Cargo Padrão** serão mostradas.
2. Selecione **Novo** e, no campo **Nome** , insira "Engenheiro de Sistemas" e selecione **Salvar**.
3. Fechar o formulário. 
4. Repita as etapas de 1 a 3 para criar outro cargo padrão para "Engenheiro de Sistemas Sênior".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades necessárias e componentes relacionados à Solução de Dimensão de Preço
Você precisará adicionar as entidades a seguir à solução de preço. Use as etapas neste procedimento para fazer algumas alterações importantes de esquema na solução de precificação para que as entidades se tornem conscientes das novas dimensões de preço.

1. Selecione **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da \<your organization name>**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.
3. Na caixa de diálogo **Componentes da Solução** , selecione as seguintes entidades:

  - Real
  - Recurso Reservável
  - Linha de Estimativa
  - Detalhes da Linha da Fatura
  - Linha do Diário
  - Detalhes da Linha de Contrato do Projeto
  - Membro da Equipe do Projeto
  - Detalhe da Linha de Cotação
  - Markup de Preço da Função
  - Preço da Função 
  - Entrada de Hora 


> [!NOTE]
> Certifique-se de incluir todos os formulários e exibições para cada uma das entidades selecionadas.

4. Quando solicitado a incluir entidades dependentes para as entidades selecionadas acima, selecione **Não**.

