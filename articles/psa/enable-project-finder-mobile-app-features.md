---
title: Habilitar recursos do aplicativo Project Finder Mobile
description: Como habilitar funcionalidades de aplicativo Project Finder Mobile do Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132949"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Habilitar funcionalidades de aplicativo Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Seus recursos podem usar o aplicativo Project Finder Mobile em seu telefone com [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para encontrar novos projetos para trabalhar e atualizar seus grupos de habilidade.  
  
 O aplicativo está disponível para os telefones [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], o [!INCLUDE[tn_android](../includes/tn-android.md)] e o [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 É necessário definir algumas opções nos parâmetros que definem a unidade organizacional para permitir que os usuários vejam os requisitos de recurso e formem projetos para atualizar suas habilidades.  
  
> [!NOTE]
>  O aplicativo Project Finder Mobile funciona apenas com [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], não com instalações locais.  
  
1. Vá para **Project Service > Parâmetros**.  
  
2. Clique nos parâmetros que deseja usar para permitir os recursos do aplicativo Project Finder Mobile.  
  
3. Na área **Geral**, defina **Requisitos de recurso visíveis aos recursos** para **Sim**.  
  
4. Defina **Permitir atualização de habilidade por recurso** para **Sim**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Essa é uma configuração global. Gerentes de projeto podem definir se um projeto ficará visível na página **Equipe de projeto** do projeto.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notificações por email  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envia mensagens de email relacionadas a solicitações de recursos dos destinatários as seguintes situações:  
  
|Destinatário|Evento|  
|---------------|-----------|  
|Gerente de projeto|-   Quando se pode inserir um recurso do projeto com o aplicativo Project Finder Mobile.|  
|Recurso|-   Quando o trabalho do recurso de projeto atribuído a ele foi cumprido por outro recurso.<br />-   Solicitação para aprovação de habilidade foi aprovada ou rejeitada.<br />-   Solicitação para entrar no projeto aprovada ou rejeitada.|  
  
## <a name="privacy-notice"></a>Aviso de privacidade  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Consulte também  
 [Configurar recursos](../psa/set-up-resources.md)
