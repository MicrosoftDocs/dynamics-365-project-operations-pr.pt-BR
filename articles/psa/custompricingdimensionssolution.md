---
title: Criar soluções personalizadas para dimensões de preço
description: Este tópico explica como criar uma solução personalizada ao criar dimensões de preço personalizadas.
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
ms.openlocfilehash: 4dea80d8e4645675d3e89e846532ca7c0f292faa328c45938941c50dc15486fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995252"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Criar soluções personalizadas para dimensões de preço

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Todas as alterações de dimensão de preço personalizada devem ficar em uma solução separada. Essa importante prática recomendada proporciona flexibilidade no futuro para atualizar ou remover alterações conforme a necessidade, ajudará com a reutilização do seu trabalho, bem como facilitará a locomoção dessas alterações para outra instância. Depois de fazer todas as alterações necessárias, exporte essa solução como uma **Solução gerenciada** e importe-a para outras instâncias para reutilizar sua configuração de preço.

1. Selecione **Configurações** > **Soluções** e selecione **Nova**. 
2. Nomeie a solução, **dimensões de preço da \<your organization name>**, insira as informações necessárias restantes e selecione **Salvar**.

> ![Criando uma solução personalizada para dimensões de preço.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades necessárias e componentes relacionados à Solução de dimensão de preço
Você precisará adicionar as entidades a seguir do Project Service à sua solução de precificação. Conclua as etapas deste procedimento para fazer algumas alterações importantes de esquema na solução de precificação para que as entidades se tornem conscientes das novas dimensões de preço.

1. Selecione **Configurações** > **Soluções** e clique duas vezes em **\<your organization name> dimensões de preço**. 
2. No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.
3. Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:

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
- Entrada de Hora 

> ![Adicionar entidades existentes à solução de dimensões de preço.](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução.](media/Dimension-Components.png)

> [!NOTE]
> Certifique-se de incluir todos os formulários e exibições para cada uma das entidades selecionadas.

4. Quando solicitado a incluir entidades dependentes para as entidades selecionadas, selecione **Não**.

> ![Não inclua todos os componentes selecionados.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]