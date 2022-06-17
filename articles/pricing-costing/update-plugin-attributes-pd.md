---
title: Atualizar atributos de plug-in com novas dimensões de preço
description: Este artigo fornece informações sobre como atualizar atributos de plug-in para dimensões de preço.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920000"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Atualizar atributos de plug-in com novas dimensões de preço

Este artigo fornece informações sobre como atualizar atributos de plug-in para dimensões de preço.

> [!NOTE]
> Este artigo é aplicável apenas aos recursos de cotação e contrato no Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Pré-requisitos
Antes de concluir as etapas deste artigo, você deve ter concluído os procedimentos nos seguintes artigos:

  - [Criar campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md) 
  - [Adicionar campos personalizados a entidades transacionais e de configuração de preço ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurar campos personalizados como dimensões de preço](set-up-custom-fields-pricing-dimensions.md). 
  
Se você não concluiu esses procedimentos, conclua-os e retorne a este artigo.

## <a name="register-a-plug-in"></a>Registrar um plug-in
Quando um detalhe de linha de cotação é criado na página **Linha de Cotação** para uma linha de cotação de projeto, o sistema cria duas linhas de estimativa. Uma linha é para o custo da estimativa e a outra linha é para as vendas. O mesmo se aplica às linhas de contrato do projeto.

Quando você altera para a quantidade ou um campo no custo, essa alteração também é feita nas vendas. Isso é possível porque os plug-ins PreOperation em Quotelinedetail e as entidades de detalhes de linha de contrato conectam atributos específicos do custo às vendas da transação. Se você precisar que as mudanças feitas nos valores de dimensão de preço nas vendas também sejam feitas no custo, os plug-ins a seguir deverão ser registrados novamente após fazer alterações em uma dimensão de preço.

Estes são os plug-ins para atualizar e registrar novamente:

- PreOperationContractLineDetailUpdate - **Atualizar msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Atualiza msdyn_quotelinetransaction**

Conclua as etapas a seguir para atualizar e registrar novamente os plug-ins.

1. Abra **PluginRegistrationTool** e se conecte ao ambiente Project Operations Dataverse.
2. Selecione **Pesquisa** e digite as primeiras letras do plug-in a ser atualizado.
3. Após encontrar o plug-in for, selecione-o e marque **Selecionar no Formulário Principal**.
4. Selecione a etapa **Atualizar msdyn_orderlinetransaction**, clique com o botão direito do mouse e selecione **Atualizar**.
5. Na página de diálogo **Atualizar**, selecione as reticências (**...**) nos atributos de filtragem.
6. A janela de atributos de filtragem é aberta e fornece uma lista de todos os atributos na entidade e as dimensões de preço. Marque as caixas de seleção para os atributos de dimensão de preço.
7. Selecione **OK** para fechar a página e selecione **Atualizar Etapa**.
8. Repita as etapas de 2 a 7 para o segundo plug-in, **PreOperationQuoteLineDetail**. Para este plug-in, você precisa atualizar a etapa **Atualização de msdyn_quotelinetransaction**.
9. Feche **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]