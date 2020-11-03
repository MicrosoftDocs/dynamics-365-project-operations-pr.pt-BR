---
title: Criar soluções personalizadas para dimensões de preço
description: Este tópico explica como criar uma solução personalizada ao criar dimensões de preço personalizadas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071437"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Criar soluções personalizadas para dimensões de preço

> [!IMPORTANT]
> Todas as alterações de dimensão de preço personalizada devem ficar em uma solução separada. Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância. Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a para outras instâncias para reutilizar sua configuração de preço.

1. Selecione **Configurações** > **Soluções** e selecione **Nova**. 
2. Nomeie a solução, **dimensões de preço da \<your organization name>** , insira as informações necessárias restantes e selecione **Salvar**.

> ![Criando uma solução personalizada para dimensões de preço](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades necessárias e componentes relacionados à Solução de dimensão de preço
Você precisará adicionar as entidades a seguir do Project Service à sua solução de precificação. Conclua as etapas deste procedimento para fazer algumas alterações importantes de esquema na solução de precificação para que as entidades se tornem conscientes das novas dimensões de preço.

1. Selecione **Configurações** > **Soluções** e clique duas vezes em **\<your organization name> dimensões de preço**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.
3. Na caixa de diálogo **Componentes da Solução** , selecione as seguintes entidades:

- Real
- Recurso Reservável
- Linha de Estimativa
- Tarefa do Projeto
- Detalhe da Linha da Fatura
- Linha do Diário
- Detalhe da Linha de Contrato do Projeto
- Membro da Equipe do Projeto
- Detalhes da Linha de Cotação
- Markup de Preço da Função
- Preço da Função 
- Entrada de Horas 

> ![Adicionar entidades existentes à solução de dimensões de preço](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução](media/Dimension-Components.png)

> [!NOTE]
> Certifique-se de incluir todos os formulários e exibições para cada uma das entidades selecionadas.

4. Quando solicitado a incluir entidades dependentes para as entidades selecionadas, selecione **Não**.

> ![Não inclua todos os componentes selecionados](media/Do-not-include-required.png)


