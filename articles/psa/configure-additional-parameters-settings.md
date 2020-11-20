---
title: Configurar definições de parâmetro adicionais
description: Como definir configurações de parâmetros adicionais no Project Service
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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129349"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="11136-103">Definir configurações de parâmetros adicionais (Project Service)</span><span class="sxs-lookup"><span data-stu-id="11136-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="11136-104">Depois que você configurar os itens nos tópicos anteriores, você precisará definir parâmetros de projeto adicionais para usar em seus projetos.</span><span class="sxs-lookup"><span data-stu-id="11136-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="11136-105">Ao instalar o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], você criou uma definição de parâmetros para criar todos os registros necessários para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] funcionar.</span><span class="sxs-lookup"><span data-stu-id="11136-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="11136-106">Agora é hora de voltar e configurar outros campos dessas configurações.</span><span class="sxs-lookup"><span data-stu-id="11136-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="11136-107">Você precisará ter configurado às seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="11136-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="11136-108">Unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="11136-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="11136-109">Frequência da fatura</span><span class="sxs-lookup"><span data-stu-id="11136-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="11136-110">Modelos de Horas de Trabalho</span><span class="sxs-lookup"><span data-stu-id="11136-110">Work hours template</span></span>  
  
-   <span data-ttu-id="11136-111">Lista de preços</span><span class="sxs-lookup"><span data-stu-id="11136-111">Price list</span></span>  
 
<span data-ttu-id="11136-112">Nessa etapa, você também indicará o tipo de alocação de recursos que quer:</span><span class="sxs-lookup"><span data-stu-id="11136-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="11136-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="11136-113">**Central**.</span></span> <span data-ttu-id="11136-114">Somente gerentes de recursos podem atribuir recursos para projetos.</span><span class="sxs-lookup"><span data-stu-id="11136-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="11136-115">**Híbrido**.</span><span class="sxs-lookup"><span data-stu-id="11136-115">**Hybrid**.</span></span> <span data-ttu-id="11136-116">Os gerentes de recursos, gerentes de projetos e gerentes de contas podem alocar recursos a projetos.</span><span class="sxs-lookup"><span data-stu-id="11136-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="11136-117">Para definir parâmetros de projeto:</span><span class="sxs-lookup"><span data-stu-id="11136-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="11136-118">Vá para **Project Service > Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="11136-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="11136-119">Clique na configuração de parâmetros que deseja configurar (a que você criou ao instalar o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) ou clique em **Novo** para criar um novo.</span><span class="sxs-lookup"><span data-stu-id="11136-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="11136-120">Na área **Geral**, defina todas as opções dos parâmetros do projeto.</span><span class="sxs-lookup"><span data-stu-id="11136-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="11136-121">Na área **Lista de preços**, clique em **+** para adicionar uma lista de preços, selecione uma lista de preços na lista suspensa **Lista de Preços do Parâmetro do Projeto** e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="11136-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="11136-122">Clique no botão **Salvar** no canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="11136-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="11136-123">O registro do parâmetro do projeto deve ser mantido para que o Project Service funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="11136-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="11136-124">Esse registro não deve ser excluído.</span><span class="sxs-lookup"><span data-stu-id="11136-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="11136-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="11136-125">See Also</span></span>  
 [<span data-ttu-id="11136-126">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="11136-126">Set up resources</span></span>](../psa/set-up-resources.md)