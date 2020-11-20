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
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="e7ea5-103">Habilitar funcionalidades de aplicativo Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e7ea5-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e7ea5-104">Seus recursos podem usar o aplicativo Project Finder Mobile em seu telefone com [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para encontrar novos projetos para trabalhar e atualizar seus grupos de habilidade.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="e7ea5-105">O aplicativo está disponível para os telefones [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], o [!INCLUDE[tn_android](../includes/tn-android.md)] e o [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="e7ea5-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="e7ea5-106">É necessário definir algumas opções nos parâmetros que definem a unidade organizacional para permitir que os usuários vejam os requisitos de recurso e formem projetos para atualizar suas habilidades.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e7ea5-107">O aplicativo Project Finder Mobile funciona apenas com [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], não com instalações locais.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="e7ea5-108">Vá para **Project Service > Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="e7ea5-109">Clique nos parâmetros que deseja usar para permitir os recursos do aplicativo Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="e7ea5-110">Na área **Geral**, defina **Requisitos de recurso visíveis aos recursos** para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="e7ea5-111">Defina **Permitir atualização de habilidade por recurso** para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="e7ea5-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="e7ea5-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="e7ea5-113">Essa é uma configuração global.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-113">This is a global setting.</span></span> <span data-ttu-id="e7ea5-114">Gerentes de projeto podem definir se um projeto ficará visível na página **Equipe de projeto** do projeto.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="e7ea5-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="e7ea5-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="e7ea5-116">Notificações por email</span><span class="sxs-lookup"><span data-stu-id="e7ea5-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="e7ea5-117">envia mensagens de email relacionadas a solicitações de recursos dos destinatários as seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="e7ea5-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="e7ea5-118">Destinatário</span><span class="sxs-lookup"><span data-stu-id="e7ea5-118">Recipient</span></span>|<span data-ttu-id="e7ea5-119">Evento</span><span class="sxs-lookup"><span data-stu-id="e7ea5-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="e7ea5-120">Gerente de projeto</span><span class="sxs-lookup"><span data-stu-id="e7ea5-120">Project manager</span></span>|<span data-ttu-id="e7ea5-121">-   Quando se pode inserir um recurso do projeto com o aplicativo Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="e7ea5-122">Recurso</span><span class="sxs-lookup"><span data-stu-id="e7ea5-122">Resource</span></span>|<span data-ttu-id="e7ea5-123">-   Quando o trabalho do recurso de projeto atribuído a ele foi cumprido por outro recurso.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="e7ea5-124">-   Solicitação para aprovação de habilidade foi aprovada ou rejeitada.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="e7ea5-125">-   Solicitação para entrar no projeto aprovada ou rejeitada.</span><span class="sxs-lookup"><span data-stu-id="e7ea5-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="e7ea5-126">Aviso de privacidade</span><span class="sxs-lookup"><span data-stu-id="e7ea5-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="e7ea5-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e7ea5-127">See Also</span></span>  
 [<span data-ttu-id="e7ea5-128">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="e7ea5-128">Set up resources</span></span>](../psa/set-up-resources.md)
