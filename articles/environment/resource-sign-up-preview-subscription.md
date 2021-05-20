---
title: Inscreva-se para obter subscrições de versão preliminar do Project Operations para cenários de recursos/sem estoque
description: Este tópico fornece informações sobre como subscrever e implantar o Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 917ead8ff6d9d3ef8374f8ccde608b6cebd50c8c
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948450"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Inscreva-se para obter subscrições de versão preliminar do Project Operations para cenários de recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tópico explica como subscrever a oferta de versão preliminar/para parceiro e implantar o ambiente do Project Operations para cenários baseados em recursos/sem estoque.

## <a name="prerequisites"></a>Pré-requisitos

- Você receberá um email com um convite para participar da versão preliminar. Você pode solicitar uma versão preliminar no [site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure.
- A implantação de um ambiente do Finance requer uma subscrição válida do Azure que será cobrada por ambiente. Você pode usar a subscrição existente da sua organização ou usar uma [avaliação do Azure](https://azure.microsoft.com/en-us/free/) para começar. O ambiente CDS será fornecido gratuitamente por um período limitado de 30 dias.

## <a name="subscribe"></a>Inscrever-se

Quando sua [solicitação de versão preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) for aprovada, você receberá três ofertas da Microsoft por email. Essas ofertas permitem que você implante a versão preliminar do Project Operations:

- Avaliação da versão preliminar do Dynamics 365 Project Operations (CRM)
- Office 365 Project Operations – Avaliação de versão preliminar
- Dynamics 365 Finance – Avaliação de versão preliminar

> [!IMPORTANT]
> Apenas uma pessoa, o administrador do locatário, em uma organização precisa executar esta tarefa. Se você não for o assinante dessa versão, espere até que sua organização se inscreva e você receba suas credenciais de usuário.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Avaliação da versão preliminar do Dynamics 365 Project Operations (CRM) 

Antes de começar, verifique se está conectado a um navegador com a conta de trabalho do usuário no locatário em que deseja ter a versão preliminar do Project Operations.

1. Resgate o primeiro código da oferta, **Dynamics 365 Project Operations (CRM) – Avaliação da versão preliminar** colando-o na URL do navegador.

![Resgatar Oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme a ordem.

![Confirme a ordem](./media/17ConfirmOrderNew.png)

Você verá que a oferta de confirmação foi resgatada com êxito.

![Confirmação](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – Avaliação de versão preliminar

Repita as mesmas etapas do primeiro código de oferta. Certifique-se de incluir o segundo código de oferta usando a mesma conta de usuário que foi usada com o primeiro código de oferta.

### <a name="dynamics-365-finance-preview-trial"></a>Avaliação da versão preliminar do Dynamics 365 Finance

Repita as mesmas etapas com a última oferta do email de boas-vindas.

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Você precisará de acesso administrativo ao Portal do Microsoft 365 da sua organização para concluir as etapas a seguir.

1. Acesse [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças aos usuários.

![Página de aterrissagem do Centro de Administração](./media/14AdminPortal.png)

2. Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.

![Atribuir Licenças](./media/15AssignLicenses.png)

3. Verifique se a **Versão preliminar do Dynamics 365 Project Operations (CRM)** e a licença da **Versão preliminar do Project Operations do Office 365** foi selecionada e selecione **Salvar alterações**.

> [!NOTE]
> A oferta de avaliação do Finance não precisa ser atribuída a um usuário.

## <a name="start-a-new-project-in-lcs"></a>Iniciar um novo projeto no LCS

Criar um novo projeto do LCS conforme descrito no tópico [Iniciar novo projeto no LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adicionar uma subscrição do Azure a um projeto do LCS

Para concluir essa tarefa, siga as etapas no tópico [Adicionar uma subscrição do Azure ao projeto do LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implantar um ambiente de demonstração do Finance com o Project Operations para cenários de recursos/sem estoque

Siga as orientações no tópico [Provisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implantação. Use o tipo de implantação [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para a versão preliminar. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalar dados de configuração do CDS

Instale os dados de configuração do CDS conforme descrito no tópico [Configurar e aplicar dados de configuração no Common Data Service](resource-apply-pro-setup-config-data.md).
Conclua essa etapa somente depois que o ambiente de demonstração do Finance for implantado e os dados de demonstração no FO estiverem prontos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]