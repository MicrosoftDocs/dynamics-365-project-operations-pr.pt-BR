---
title: Inscrever-se em uma assinatura de versão preliminar - lite
description: Este tópico fornece informações sobre como assinar e implantar a implantação simplificada do Project Operations - transação para faturamento pro forma.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997407"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Inscrever-se em uma assinatura de versão preliminar - lite 

Este tópico explica como assinar a oferta do parceiro de visualização e executar a implantação lite do Dynamics 365 Project Operations – oferta do faturamento pro forma.

> [!NOTE]
> Este processo mudará nas próximas versões de Project Operations.

## <a name="prerequisites"></a>Pré-requisitos

- Você receberá um email convidando para participar da versão preliminar. Você pode solicitar uma versão preliminar no [site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure.
- Reveja todos os termos e condições.

## <a name="subscribe"></a>Inscrever-se

Ao receber uma aprovação de [solicitação de versão preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), você receberá duas ofertas da Microsoft por email. Essas ofertas permitem que você implante a versão preliminar do Project Operations:

- Avaliação da versão preliminar do Dynamics 365 Project Operations (CRM)
- Office 365 Project Operations – Avaliação de versão preliminar

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

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Você precisará de acesso administrativo ao Portal do Microsoft 365 da sua organização para concluir as etapas a seguir.


1. Acesse [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças aos usuários.

![Página de aterrissagem do Centro de Administração](./media/14AdminPortal.png)

2. Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.

![Atribuir Licenças](./media/15AssignLicenses.png)

3. Verifique se as licenças da **Versão Preliminar do Dynamics 365 Project Operations (CRM)** e do **Office 365 Project Operations – Versão Preliminar** estão selecionadas. 
4. Selecione **Salvar alterações**.

## <a name="create-a-new-cds-environment"></a>Criar um novo ambiente CDS

1. Provisione um novo ambiente de implantação do Project Operations CDS seguindo as instruções no tópico, [Modelo de implantação de CDS](lite-deployment.md). Ao selecionar o tipo de ambiente, utilize **Avaliação (baseado em assinatura)**.
![Novo ambiente](./media/19CreateEnvironment.png)

2. Selecione a configuração **Habilitar aplicações do Dynamics 365** e deixe em branco **Implantar automaticamente essas aplicações**.  
3. Selecione **Salvar** para criar o ambiente.

![Adicionar banco de dados](./media/20CreateEnvironment1.png)

4. Depois de criar o ambiente, instale a solução **Microsoft Dynamics 365 Project Operations**. 

![Instalar Solução](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar uma configuração CDS e configurar dados de demonstração

Instale a configuração do CDS e defina os dados de demonstração seguindo as instruções no tópico, [Aplicar instalação de demonstração e dados de configuração](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]