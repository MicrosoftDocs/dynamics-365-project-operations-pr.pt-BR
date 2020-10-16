---
title: Inscreva-se para obter subscrições de versão preliminar do Project Operations para cenários de recursos/sem estoque
description: Este tópico fornece informações sobre como subscrever e implantar o Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948742"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Inscreva-se para obter subscrições de versão preliminar do Project Operations para cenários de recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Este tópico explica como subscrever a oferta de versão preliminar/para parceiro e implantar o ambiente do Project Operations para cenários baseados em recursos/sem estoque.

## <a name="prerequisites"></a>Pré-requisitos

- Você receberá um email com um convite para participar da versão preliminar. Você pode solicitar uma versão preliminar no [site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure.
- A implantação de um ambiente do Finance requer uma subscrição válida do Azure que será cobrada por ambiente. Você pode usar a subscrição existente da sua organização ou usar uma [avaliação do Azure](https://azure.microsoft.com/en-us/free/) para começar. O ambiente CDS será fornecido gratuitamente por um período limitado de 30 dias.

## <a name="subscribe"></a>Inscrever-se

Quando sua [solicitação de versão preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) for aprovada, você receberá duas ofertas da Microsoft por email. Essas ofertas permitem que você implante a versão preliminar do Project Operations:

- Dynamics 365 Project Operations – avaliação da versão preliminar
- Avaliação da versão preliminar do Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Apenas uma pessoa, o administrador do locatário, em uma organização precisa executar esta tarefa. Se você não for o assinante dessa versão, espere até que sua organização se inscreva e você receba suas credenciais de usuário.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – avaliação da versão preliminar

1. Resgate a primeira oferta, **Avaliação do Dynamics 365 Project Operations**, com o URL fornecido no email de boas-vindas.

![Primeira Oferta](./media/1FirstOffer.png)

2. Verifique se você está conectado como o usuário que pertence à organização que assinará o serviço.
3. Prossiga com o resgate da oferta. 
4. Selecione **Sim, adicionar à minha conta**.

![Resgatar Oferta](./media/2RedeemFirstOffer.png)

![Confirmar Oferta](./media/3ConfirmFirstOffer.png)

![Oferta Resgatada](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Avaliação da versão preliminar do Dynamics 365 Finance

Repita as mesmas etapas com a segunda oferta do email de boas-vindas.

## <a name="assign-licenses"></a>Atribuir Licenças

> [!IMPORTANT]
> Você precisará de acesso administrativo ao Portal do Office 365 da sua organização para concluir as etapas a seguir.

1. Acesse [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças aos usuários.

![Portal de administração do Office](./media/5OfficeAdminPortal.png)

2. Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.

![Atribuir Licenças](./media/6AssignLicenses.png)

3. Verifique se a licença do Project Operations foi selecionada e selecione **Salvar alterações**. 

> [!NOTE]
> A oferta de avaliação do Finance não precisa ser atribuída a um usuário.

## <a name="start-a-new-project-in-lcs"></a>Iniciar um novo projeto no LCS

Criar um novo projeto do LCS conforme descrito no tópico [Iniciar novo projeto no LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adicionar uma subscrição do Azure a um projeto do LCS

Para concluir essa tarefa, siga as etapas no tópico [Adicionar uma subscrição do Azure ao projeto do LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implantar um ambiente de demonstração do Finance com o Project Operations para cenários de recursos/sem estoque

Siga as orientações no tópico [Provisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implantação. Use o tipo de implantação [ambiente de demonstração](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para a versão preliminar.

## <a name="install-cds-setup-and-configuration-data"></a>Instalar dados de configuração do CDS

Instale os dados de configuração do CDS conforme descrito no tópico [Configurar e aplicar dados de configuração no Common Data Service](resource-apply-pro-setup-config-data.md).

