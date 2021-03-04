---
title: Criar uma solução para dimensões de precificação personalizadas
description: Esse tópico fornece informações sobre como criar soluções para dimensões de precificação personalizadas.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513957"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Criar uma solução para dimensões de precificação personalizadas

 _**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_ 

>[!IMPORTANT]
>Todas as alterações de dimensão de preço personalizada devem ficar em uma solução separada. Essa importante prática recomendada oferece a flexibilidade para atualizar ou remover alterações conforme a necessidade, ajuda com a reutilização do seu trabalho e facilita a locomoção dessas alterações para outras instâncias. Depois de fazer todas as alterações necessárias, exporte essa solução como uma solução **Gerenciada** e importe-a em outras instâncias para a reutilização.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Criar uma solução para dimensões de precificação personalizadas

1.  Selecione **Configurações** > **Soluções** e selecione **Nova**.
2.  Nomeie a solução *dimensões de precificação de <your organization name>*.
3. Insira as informações necessárias restantes e selecione **Salvar**.

  ![Criação de uma solução de dimensão de precificação personalizada](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades necessárias e componentes relacionados à Solução de dimensão de preço

Adicione as seguintes entidades do Project Service à sua solução de preços para fazer alterações importantes no esquema da solução de preços. Depois de concluir este procedimento, as entidades reconhecerão as novas dimensões de precificação.

1.  Selecione **Configurações** > **Soluções** e clique duas vezes em **dimensões de precificação da <*nome de sua organização*>**.
2.  No Gerenciador de Soluções, no painel de navegação à esquerda, selecione **Adicionar Existente** > **Entidades**.
3.  Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:
 
   - **Real**
   - **Recurso Reservável**
   - **Linha de Estimativa**
   - **Tarefa do Projeto**
   - **Detalhe da Linha da Fatura**
   - **Linha do Diário**
   - **Detalhe da Linha de Contrato do Projeto**
   - **Membro da Equipe do Projeto**
   - **Detalhes da Linha de Cotação**
   - **Markup de Preço da Função**
   - **Preço da Função**
   - **Entrada de Hora**
 
   ![Adicionar entidades existentes à solução de dimensões de precificação](./media/Existing-entities-to-PD-solution.png)
 
 4. Em cada entidade, revise os componentes que estão sendo adicionados e a lista final de ativos da entidade para cada entidade. 

   >[!NOTE]
   > Inclua todos os formulários e exibições para cada uma das entidades selecionadas.

  ![Entidades adicionadas](./media/solution-component-selection.png)


5.  Nas entidades selecionadas, quando for solicitado a incluir entidades dependentes, selecione **Não, não incluir os componentes necessários.**

    ![Incluindo entidades dependentes](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]