---
title: Inscrever-se para avaliações do Project Operations
description: Esse tópico fornece informações sobre como implantar uma avaliação do Dynamics 365 Project Operations.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418443"
---
# <a name="sign-up-for-project-operations-trials"></a>Inscrever-se para avaliações do Project Operations 

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - faturamento pro forma, Project Operations para cenários baseados em estoque/produção__ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tópico explica como assinar a oferta de parceiro de versão preliminar e implementar um ambiente do Dynamics 365 Project Operations.

Com a nova avaliação do Project Operations, você poderá implantar automaticamente qualquer um dos três cenários de implantação com suporte ao preencher um questionário que recomendará a melhor abordagem de implantação. Este tópico fornece informações sobre como:

- Resgatar sua oferta de avaliação.
- Iniciar o provisionamento.
- Configurar a gravação dupla.
- Saiba mais sobre Project Operations. 

A tabela a seguir descreve os detalhes da nova oferta de avaliação.

| **Item de oferta**               | **Detalhes**                                  |
|------------------------------|----------------------------------------------|
| Tipo de oferta                   | Esse tipo de oferta é voltado para o Administrador e, portanto, é necessário ser um administrador do locatário para resgatar. |
| Oferta de uso                    | Uma vez por locatário                          |
| Duração da oferta               | 30 dias de calendário                             |
| Resgates por locatário       | 0                                            |
| Número de usuários              | 25                                           |
| Ramal                    | 1 extensão, 30 dias de calendário               |
| Número de ambientes de avaliação | 3                                            |


## <a name="admin-trial-details"></a>Detalhes da avaliação de administrador
A tabela a seguir lista os detalhes da avaliação e como eles se aplicam a cada tipo de implantação.

| **Item**                      | **Lite**                                     | **Materiais sem estoque** | **Materiais com estoque** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Dados de configuração fornecidos           | Sim                                          | Sim                       | Sim (USSI)            |
| Dados transacionais            | No                                           | No                        | No                    |
| Tempo de provisionamento em minutos  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Pré-requisitos
Os pré-requisitos a seguir são necessários para a implantação de uma avaliação do Dynamics 365 Project Operations.

- Inscreva-se na [Dynamics 365 Project Operations – Avaliação de Versão Preliminar](https://www.aka.ms/try-po).
- O usuário que implementa a versão preliminar precisa ter direitos de administrador global no Locatário do Azure.

> [!IMPORTANT]
> Apenas uma pessoa em uma organização, o administrador de locatários, precisará executar essa tarefa. Se você não for o assinante dessa versão, espere até que sua organização se inscreva e você receba suas credenciais de usuário.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations – Avaliação de versão preliminar 

Antes de começar, entre em um navegador com a conta de trabalho do usuário no locatário onde deseja a versão preliminar do Project Operations.

1. Resgate o primeiro código da oferta **Dynamics 365 Project Operations – Avaliação de Versão Preliminar** colando-o na URL do navegador.

    ![Resgatar Oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme a ordem.

    ![Confirme a ordem](./media/17ConfirmOrderNew.png)

  Você verá que a oferta de confirmação foi resgatada com sucesso.

   ![Confirmação](./media/18OrderConfirmationNew.png)

  Você será redirecionado para o [centro de administração do Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Questionário e provisionamento

1.  Acesse o [centro de administração do Power Platform](https://admin.powerplatform.com/projectoperationstrial) e preencha o questionário.  
2.  Revise o tipo de implantação recomendado e selecione **Iniciar Configuração** para iniciar o provisionamento.
3.  Revise os termos e condições e depois selecione **Iniciar**.

   Após o início do provisionamento, você será redirecionado para a lista de ambientes no centro de administração do Power Platform. Enquanto o provisionamento estiver em andamento, o estado do seu ambiente será **Preparando Instância**.
 
  Após a conclusão do provisionamento, o estado do seu ambiente será **Pronto**.
 
4.  Quando o provisionamento for concluído, selecione a respectiva URL do Microsoft Dataverse e as URLs dos aplicativos do Finance and Operations para validar a implantação.

## <a name="demo-data-installation"></a>Instalação de dados de demonstração

Use os links a seguir para acessar pacotes de dados de demonstração para materiais sem estoque e cenários de implantação simples. 
- [Dados de demonstração de materiais sem estoque](resource-apply-pro-setup-config-data.md)
- [Dados de demonstração lite](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>Configuração da gravação dupla
Apenas para implantações de materiais sem estoque, configure seus mapeamentos de gravação dupla. Para mais informações, consulte [Versões de mapa de gravação dupla do Project Operations](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Atribuir licenças

Você precisará de acesso administrativo ao Portal do Microsoft 365 da sua organização para concluir as etapas a seguir.

1. Acesse o [centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus usuários.

   ![Página de aterrissagem do Centro de Administração](./media/14AdminPortal.png)

2. Na página **Usuários ativos**, selecione os usuários aos quais deseja atribuir uma licença.

   ![Atribuir Licenças](./media/15AssignLicenses.png)

3. Verifique se a licença da **Versão Preliminar do Dynamics 365 Project Operations** foi selecionada e escolha **Salvar alterações**.

## <a name="additional-resources"></a>Recursos adicionais

Os recursos a seguir fornecerão orientações úteis quando você iniciar sua jornada com o Project Operations:

- [Série de vídeos - Visão geral do Project Operations, detalhes e roteiro dos recursos](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Determinar o tipo de implantação](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>E se eu precisar de ALM ou ELM para meu ambiente de aplicativos do Finance and Operations?

- Para parceiros que precisam de recursos completos de gerenciamento do ciclo de vida do ambiente, consulte a [Solicitação de Licença de Área Restrita de Parceiro](https://experience.dynamics.com/requestlicense) para revisar a nova oferta para parceiros. 
- Para parceiros que buscam mais informações sobre Direitos de Uso Interno, consulte [Benefício de nuvem e software de Direitos de Uso Interno (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Posso estender minha avaliação além dos 30 dias?
Para estender sua avaliação, conclua as etapas a seguir.

1. No **Centro de Administração do Microsoft 365**, acesse **Cobrança** > **Seus produtos**.
2. Selecione **Dynamics 365 Project Operations (CE) - Avaliação de Versão Preliminar**.
3. Em **Data de Validade**, selecione **Estender Data**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Posso atualizar da implantação lite para a implantação de cenário com base em recursos/sem estoque?
Atualmente, não há suporte para atualizar um ambiente de uma implantação lite para uma implantação baseada em sem estoque.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Posso acessar o Lifecycle Services (LCS) para meus ambientes do Finance?  
Nº Para estas avaliações, a implantação é feita por meio do Centro de Administração do Power Platform. O acesso ao ambiente do Finance é restrito.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Posso instalar minha avaliação em um ambiente existente?
Se tiver um ambiente existente, você terá permissão para instalar a implantação lite em um ambiente do Dataverse de vendas existente do Centro de administração do Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]