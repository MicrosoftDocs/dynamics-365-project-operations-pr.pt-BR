---
title: Inscreva-se para obter subscrições de versão preliminar do Project Operations para cenários de recursos/sem estoque
description: Este artigo fornece informações sobre como se inscrever e implantar o Project Operations para cenários baseados em recursos/sem estoque.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842001"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Inscreva-se para obter subscrições de versão preliminar do Project Operations para cenários de recursos/sem estoque

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_



Este artigo explica como inscrever-se na oferta de avaliação e implantar o ambiente Project Operations para cenários baseados em recursos/sem estoque.

## <a name="prerequisites"></a>Pré-requisitos
- O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure. Você pode criar um inquilino durante o primeiro resgate da oferta. 
- A implantação de um ambiente do Finance requer uma subscrição válida do Azure que será cobrada por ambiente. Você pode usar a subscrição existente da sua organização ou usar uma [avaliação do Azure](https://azure.microsoft.com/free/) para começar. O ambiente CDS será fornecido gratuitamente por um período limitado de 30 dias.

> [!IMPORTANT]
> Apenas uma pessoa, o administrador do locatário, em uma organização precisa executar esta tarefa. Se você não for o assinante dessa versão, espere até que sua organização se inscreva e você receba suas credenciais de usuário.
> 
> As avaliações são de uso único no locatário. Você só pode executar uma avaliação de cada vez. Recomendamos que você crie um novo locatário para o propósito de avaliação.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Avaliação de Visualização 

Antes de começar, verifique se está conectado a um navegador com a conta de trabalho do usuário no locatário em que deseja ter a versão preliminar do Project Operations.

1. Resgate o primeiro código de oferta, **Dynamics 365 Project Operations** aqui [Avaliação do Project Operations](https://aka.ms/try-po).
2. Confirme a ordem.

  Você verá que a oferta de confirmação foi resgatada com êxito.

### <a name="dynamics-365-finance-preview-trial"></a>Avaliação da versão preliminar do Dynamics 365 Finance

Vá para [Avaliação de Versão Preliminar do Dynamics 365 for Finance](https://aka.ms/trypoche) e repita as etapas da seção anterior com a oferta Inscreva-se no Ambiente Hospedado na Nuvem.  

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Você precisará de acesso administrativo ao Portal do Microsoft 365 da sua organização para concluir as etapas a seguir.

1. Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças a seus usuários.

2. Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.

3. Verifique se a licença do **Dynamics 365 Project Operations** foi selecionada e escolha **Salvar alterações**.

> [!NOTE]
> A oferta de avaliação do Finance não precisa ser atribuída a um usuário.

## <a name="start-a-new-project-in-lcs"></a>Iniciar um novo projeto no LCS

Crie um novo projeto LCS conforme descrito no artigo, [Iniciar um novo projeto no LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adicionar uma subscrição do Azure a um projeto do LCS

Para concluir esta tarefa, siga as etapas do artigo, [Adicionar uma assinatura do Azure ao projeto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implantar um ambiente de demonstração do Finance com o Project Operations para cenários de recursos/sem estoque

Siga as orientações do artigo, [Provisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implantação. Use o tipo de implantação [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para a versão preliminar. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalar dados de configuração do CDS

Instale os dados de configuração do CDS conforme descrito no artigo, [Configurar e aplicar dados de configuração no arquivo Common Data Service](resource-apply-pro-setup-config-data.md).
Conclua esta etapa somente depois que o ambiente de demonstração do Finance for implantado e os dados de demonstração estiverem prontos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
