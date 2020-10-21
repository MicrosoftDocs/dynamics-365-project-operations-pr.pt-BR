---
title: Inscreva-se para receber uma assinatura de versão preliminar
description: Este tópico fornece informações sobre como assinar e implantar a implantação simplificada do Project Operations - transação para faturamento pró-forma.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948739"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Inscreva-se para obter uma assinatura de visualização para implantação simplificada - negócio para faturamento pró-forma

Este tópico explica como assinar a oferta de parceiro de visualização e implantar Dynamics 365 Project Operations - oferta para faturamento pró-forma.

> [!NOTE]
> Este processo mudará nas próximas versões de Project Operations.

## <a name="prerequisites"></a>Pré-requisitos

- Você receberá um email com um convite para participar da versão preliminar. Você pode solicitar uma versão preliminar no [site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure.
- O usuário que implantar a visualização precisará de um número de telefone e um cartão de crédito válido. Durante a inscrição, o cartão não será cobrado por seis meses. Após seis meses, você precisa cancelar a assinatura. 
- Reveja todos os termos e condições.

## <a name="subscribe"></a>Inscrever-se

Quando você recebe uma aprovação de [solicitação de versão preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), você receberá duas ofertas da Microsoft por email. Essas ofertas permitem que você implante a versão preliminar do Project Operations:

- Teste de visualização do Dynamics 365 Customer Service - código de uso único
- Dynamics 365 Project Operations - avaliação prévia

### <a name="dynamics-365-customer-service-paid-offer"></a>Oferta paga do Dynamics 365 Customer Service

1. Usando uma janela do navegador InPrivate/Incognito, resgate o primeiro código de oferta do Dynamics 365 Customer Service. Para se inscrever no SAC, você precisará de:

- Um número de telefone
- Um cartão de crédito. Durante a inscrição, o cartão não será cobrado por seis meses. Após seis meses, você precisa cancelar a assinatura.
- Reveja todos os termos e condições.

2. Apresentem suas informações de contato.

![Informações do Contato](./media/1ContactInformation.png)

3. Forneça os detalhes do novo inquilino.

![Criar identificação de usuário](./media/2CreateUserID.png)

4. Verifique sua identidade, salve seu novo ID de usuário e selecione **Configuração**.

![Salvar informações](./media/3SaveInfo.png)

5. Conclua a inscrição do cartão de crédito e analise todos os termos e condições. 

![Concluir cartão de crédito](./media/4CompleteCreditCard.png)

![Pagar com cartão de crédito](./media/5CreditCardCheckout.png)

![Salvar pedido](./media/6SaveOrder.png)

![Confirmação do cartão de crédito](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Cancelar a oferta empresarial do Dynamics 365 Customer Service

A Oferta empresarial do Dynamics 365 Customer Service é fornecida gratuitamente por seis meses. A oferta será renovada pela taxa integral no final do período de seis meses. Para cancelar antes da data de renovação, siga as instruções a seguir. 

> [!NOTE]
> Depois de concluir essas etapas, você não poderá mais usar o ambiente de visualização pública do Project Operations.

1. Vá ao [Portal de administração](https://admin.microsoft.com/), e abaixo de **Faturamento**, selecione **Seus produtos**.

![Portal do administrador, sua página de produtos](./media/8AdminPortal.png)

2. Selecione a **Oferta empresarial do Dynamics 365 Customer Service**.

![Cancelar assinatura](./media/9CancelSubscription.png)

3. Selecione **Configurações** > **Ações** > **Cancelar assinatura**.
4. No formulário **Cancelamento de assinatura**, insira as informações nos campos obrigatórios.
5. Selecione **Cancelar** > **Assinatura.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – avaliação da versão preliminar

1. Resgate a segunda oferta, Avaliação do Dynamics 365 Project Operations, com o URL fornecido no email de boas-vindas.

![Resgatar Oferta 2](./media/10RedeemOffer2.png)

2. Verifique se você está conectado como o usuário que pertence à mesma organização que foi assinada usando o primeiro código de oferta e, em seguida, prossiga com o resgate da oferta. 
3. Selecione **Sim, adicionar à minha conta**.

![Adicionar como conta](./media/11AddToAccount.png)

![Tela de teste agora](./media/12TryNow.png)

![Detalhes da ordem](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Você precisará de acesso administrativo ao Portal do Office 365 da sua organização para concluir as etapas a seguir.

1. Acesse [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças aos usuários.

![Página de aterrissagem do Centro de Administração](./media/14AdminPortal.png)

2. Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.

![Atribuir Licenças](./media/15AssignLicenses.png)

3. Verifique se o **SAC Enterprise** e licença do **Project Operations** foram selecionados e selecione **Salvar alterações**.

## <a name="create-a-new-cds-environment"></a>Criar um novo ambiente CDS

Provisione um novo ambiente de implantação do Project Operations CDS seguindo as instruções no tópico, [Modelo de implantação de CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar uma configuração CDS e configurar dados de demonstração

Instale a configuração do CDS e defina os dados de demonstração seguindo as instruções no tópico, [Aplicar instalação de demonstração e dados de configuração](lite-apply-demo-setup-config-data.md).
