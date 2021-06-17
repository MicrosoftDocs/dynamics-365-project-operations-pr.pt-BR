---
title: Adicionar uma subscrição do Azure a um projeto do LCS
description: Este tópico fornece informações sobre como conectar sua subscrição do Azure a um projeto do LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000602"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adicionar uma subscrição do Azure a um projeto do LCS

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Ambientes hospedados em nuvem devem ser implantados usando uma subscrição existente do Azure. Este tópico explica como conectar sua subscrição existente do Azure a um projeto do LCS. 

## <a name="grant-admin-consent"></a>Conceder consentimento do administrador

1. Em seu projeto do LCS, na seção **Ambientes**, selecione **Configurações do Microsoft Azure**.

![Configurações do Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Na página **Configurações do projeto**, na guia **Conectores do Azure**, selecione **Autorizar**. Isso permite que ambientes sejam implantados neste projeto.

![Conectores do Azure](./media/2AzureConnectors.png)

3. Selecione **Autorizar** novamente para fornecer consentimento do administrador.

![Conceder Consentimento do Administrador](./media/3GrantAdminConsent.png)

4. Aceite a solicitação de permissão.

![Aceitar a Solicitação de Permissão](./media/4AcceptPermissionRequest.png)

A autorização agora está concluída. 

![Autorização bem sucedida](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Fornecer ao Dynamics Deployment Services acesso à sua subscrição do Azure

1. Acesse [cobrança do Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e selecione sua subscrição. O Dynamics Deployment Services precisa acessar essa subscrição para poder implantar ambientes.

![Detalhes da subscrição do Azure](./media/6AzureSubscription.png)

2. Selecione **Controle de Acesso (IAM)** no painel de navegação e selecione **Adicionar atribuição de função**.
3. No controle deslizante do lado direito, selecione **Função Parceiro** e, na lista fornecida, localize e selecione **Dynamics Deployment Services**. 
4. Selecione **Salvar**.

![Acesso à Subscrição](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Adicionar um conector de subscrição a um projeto do LCS

1. Em seu projeto do LCS, na página **Configurações do Microsoft Azure**, selecione **Adicionar** para adicionar um novo conector.
2. Insira sua ID da assinatura do Azure. Você pode encontrar sua ID da assinatura do Azure no [portal do Azure](https://ms.portal.azure.com/), em **Configurações** no canto inferior esquerdo da tela.
3. No campo **Configurar para usar o Azure Resource Manager**, selecione **Sim**.
4. Certifique-se de que o Domínio de Locatário do AAD de Subscrição do Azure corresponda à subscrição do Azure proprietária do domínio que você está usando e selecione **Avançar**.
5. Na tela **Configuração do Microsoft Azure**, selecione **Avançar** para confirmar. Se ocorrer um erro nessa tela, volte para a seção [Fornecer ao Dynamics Deployment Services acesso à sua subscrição do Azure](#provide) neste tópico e certifique-se de ter concluído todas as etapas.
6. Baixe o Certificado de Gerenciamento do Azure para uma pasta local em seu computador. Peça ao administrador de assinatura do Azure para carregar o certificado no Portal de Gerenciamento do Azure selecionando a assinatura e acessando **Configurações** > **Certificados de Gerenciamento**. Este certificado permite que o LCS se comunique com o Azure em seu nome. Você poderá pular essa etapa se seu usuário tiver acesso à subscrição.
7. Selecione **Avançar**.
8. Selecione a região do Azure para implantar e selecione um data center próximo ao local onde você planeja usar este sistema.
9.  Selecione **Conectar**.

Você conectou sua subscrição do Azure com êxito. Agora você pode implantar ambientes hospedados em nuvem do Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
