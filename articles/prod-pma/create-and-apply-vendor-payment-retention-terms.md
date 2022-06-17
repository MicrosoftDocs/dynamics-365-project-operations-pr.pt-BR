---
title: Criar e aplicar termos de retenção de pagamento de fornecedor
description: Este artigo fornece informações sobre como configurar e manter condições de retenção para pagamentos de fornecedores.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 2cd18375d93e503ac532cb3839c691231ea46681
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916734"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Criar e aplicar termos de retenção de pagamento de fornecedor

[!include [banner](../includes/banner.md)] 

Configurar os termos de retenção de pagamento do fornecedor para um projeto é útil quando sua organização deseja reter parte dos pagamentos feitos a um fornecedor. Por exemplo, quando você deseja reter o pagamento a um fornecedor até que os produtos entregues atendam às suas expectativas. Os termos de retenção de pagamento do fornecedor podem ser especificados quando você negocia um contrato com o fornecedor.

## <a name="create-vendor-payment-retention-terms"></a>Criar termos de retenção de pagamento de fornecedor

Você pode inserir a porcentagem do pagamento do fornecedor para retenção e a porcentagem dos valores retidos anteriormente a serem liberados. Os valores são retidos automaticamente nas faturas do fornecedor até que o contrato atinja o estado de conclusão especificado. Depois de definir os termos de retenção, você poderá aplicá-los a qualquer projeto desse fornecedor.

Use as etapas a seguir para configurar e manter os termos de retenção para pagamentos de fornecedores. 

1. Vá para **Gerenciamento e contabilidade de projeto** > **Retenção** > **Termos de retenção de pagamento de fornecedor**.
2. Selecione **Novo** para adicionar um novo termo de retenção de fornecedor. O valor de **ID da Regra** para o novo termo é inserido automaticamente. 
3. Insira uma breve descrição no campo **Descrição** e, na Guia Rápida **Termos**, selecione **Adicionar linha** para inserir valores de termo para o seguinte:

   - **Porcentagem de unidades entregues**: insira uma porcentagem de conclusão para o termo. Os valores serão retidos automaticamente nas faturas do fornecedor até que o estágio do projeto de conclusão seja igual à porcentagem especificada. Por exemplo, se você inserir 50,00, os valores serão retidos até que o projeto esteja 50% concluído.
   - **Porcentagem a reter**: insira uma porcentagem do valor da fatura do fornecedor a ser retida. Por exemplo, se você inserir 10,00, então 10% do valor em uma fatura do fornecedor serão retidos até que o projeto alcance a porcentagem de conclusão, conforme definido no campo **Porcentagem de unidades entregues**.
   - **Porcentagem para liberação**: selecione **Adicionar linha** para inserir uma porcentagem de quaisquer valores anteriormente retidos a serem liberados para o nível selecionado de conclusão do projeto.

> [!NOTE]
> Se você tiver mais de um marco para diferentes níveis de conclusão do projeto, insira uma linha de prazo de retenção de fornecedor separada para cada regra de retenção. Cada linha pode especificar uma porcentagem de retenção diferente e uma porcentagem de liberação diferente para cada nível designado de conclusão do projeto.

Depois de criar os termos de retenção de fornecedor para um fornecedor, você poderá aplicar os termos a um projeto.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Aplicar termos de retenção de fornecedor a um projeto

1. Vá para **Gerenciamento e contabilidade de projeto** > **Projetos** > **Todos os projetos** e abra um projeto na página de listagem de projetos.
2. Na FastTab **Contratos de fornecedores**, selecione **Adicionar linha**.
3. No campo **Código de conta**, selecione uma das seguintes opções: 

   - **Tabela**: os termos de retenção de fornecedor se aplicam a um único fornecedor.
   - **Grupo**: os termos de retenção de fornecedor se aplicam a todos os fornecedores em um grupo de fornecedores.
   - **Todos**: os termos de retenção de fornecedor se aplicam a todos os fornecedores.

4. No campo **Fornecedor/Grupo de fornecedores**, selecione o fornecedor ou grupo de fornecedores ao qual os termos de retenção do fornecedor se aplicam. Se você tiver selecionado **Todos** na etapa anterior, esse campo não estará disponível.
5. No campo **Termos de retenção do fornecedor**, selecione os termos de retenção que você criou no procedimento anterior.
6. Se o projeto também tiver termos de pagamento quando pago (PWP) configurados para o fornecedor, insira a porcentagem limite para o projeto no campo **Porcentagem de limite PWP**.

Os termos de retenção do fornecedor também são exibidos nas ordens de compra que você cria para o fornecedor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]