---
title: Criar uma solução para dimensões de preço personalizadas
description: Este artigo fornece informações sobre como criar soluções para dimensões de preço personalizadas.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cd7fedaa7bece16e99131bcc0faff3ce547580e8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915124"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Criar uma solução para dimensões de preço personalizadas

 _**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_ 

>[!IMPORTANT]
>Todas as alterações de dimensão de preço personalizada devem ficar em uma solução separada. Essa importante prática recomendada oferece a flexibilidade para atualizar ou remover alterações conforme a necessidade, ajuda com a reutilização do seu trabalho e facilita a locomoção dessas alterações para outras instâncias. Depois de fazer todas as alterações necessárias, exporte essa solução como uma solução **Gerenciada** e importe-a em outras instâncias para a reutilização.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Criar uma solução para dimensões de preço personalizadas

1.  Selecione **Configurações** > **Soluções** e selecione **Nova**.
2.  Nomeie a solução *dimensões de preço de \<your organization name\>*.
3. Insira as informações necessárias restantes e selecione **Salvar**.

  ![Criação de uma solução de dimensão de preço personalizada.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades necessárias e componentes relacionados à Solução de dimensão de preço

Adicione as seguintes entidades do Project Service à sua solução de preços para fazer alterações importantes no esquema da solução de preços. Depois de concluir este procedimento, as entidades reconhecerão as novas dimensões de preço.

1.  Selecione **Configurações** > **Soluções** e clique duas vezes em **dimensões de preço da <*nome de sua organização*>**.
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
 
   ![Adicionar entidades existentes à solução de dimensões de preço.](./media/Existing-entities-to-PD-solution.png)
 
 4. Em cada entidade, revise os componentes que estão sendo adicionados e a lista final de ativos da entidade para cada entidade. 

   >[!NOTE]
   > Inclua todos os formulários e exibições para cada uma das entidades selecionadas.

  ![Entidades adicionadas.](./media/solution-component-selection.png)


5.  Nas entidades selecionadas, quando for solicitado a incluir entidades dependentes, selecione **Não, não incluir os componentes necessários.**

    ![Incluindo entidades dependentes.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]