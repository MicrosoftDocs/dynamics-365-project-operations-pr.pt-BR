---
title: Novidades ou alterações na Versão de Atualização 16 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 16 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5d4851ed27028117d25efb0610c25a5aac9c8b70
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006767"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="d7941-103">Versão de Atualização 16, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="d7941-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d7941-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d7941-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d7941-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="d7941-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="d7941-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d7941-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d7941-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="d7941-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="d7941-108">Para obter mais informações, consulte [Instalar, Atualizar uma Solução Preferencial](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="d7941-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="d7941-109">Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 16.</span><span class="sxs-lookup"><span data-stu-id="d7941-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="d7941-110">Esta versão tem um número de compilação de V3.10.6.34 e está geralmente disponível por meio de uma atualização automática em janeiro de 2020.</span><span class="sxs-lookup"><span data-stu-id="d7941-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="d7941-111">Versão de Atualização 16</span><span class="sxs-lookup"><span data-stu-id="d7941-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d7941-112">Correções de bugs</span><span class="sxs-lookup"><span data-stu-id="d7941-112">Bug fixes</span></span>

-   <span data-ttu-id="d7941-113">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="d7941-113">Time and Expense</span></span>

    -   <span data-ttu-id="d7941-114">Corrigido: Os usuários que tentarem enviar entradas de hora e despesas excluídas para aprovações receberão mensagens de erro relevantes.</span><span class="sxs-lookup"><span data-stu-id="d7941-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="d7941-115">Gerenciamento de projetos</span><span class="sxs-lookup"><span data-stu-id="d7941-115">Project Management</span></span>

    -   <span data-ttu-id="d7941-116">Corrigido: As unidades de recursos definidas para membros da equipe em modelos são respeitadas e os modelos são aplicados a um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="d7941-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="d7941-117">Corrigido: Melhoria no tratamento da reatribuição de propriedade do registro.</span><span class="sxs-lookup"><span data-stu-id="d7941-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="d7941-118">Corrigido: Os projetos que estão no processo de serem copiados não poderão ser copiados até que todas as operações de cópia sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="d7941-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="d7941-119">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="d7941-119">Resource Management</span></span>

    -   <span data-ttu-id="d7941-120">Fixo: Estender reservas agora aceita curtas durações corretamente e não mais cria zero horas para reservas prolongadas.</span><span class="sxs-lookup"><span data-stu-id="d7941-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="d7941-121">Corrigido: A exibição da reconciliação agora é renderizada quando o fuso horário do projeto for +5:30 GMT e o horário do usuário for diferente.</span><span class="sxs-lookup"><span data-stu-id="d7941-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="d7941-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d7941-122">Sales</span></span>

    -   <span data-ttu-id="d7941-123">Corrigido: Quando um projeto mapeado para uma linha de contrato for removida e um novo projeto for mapeado, os registros do novo projeto não estavam sendo reavaliados com base nas regras de faturamento e preço definidas na linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="d7941-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="d7941-124">Isso foi corrigido nessa versão.</span><span class="sxs-lookup"><span data-stu-id="d7941-124">This has been fixed in this release.</span></span> <span data-ttu-id="d7941-125">Os preços e os registros atuais do projeto mapeado recentemente serão revertidos e recriados corretamente com base nas regras de faturamento e cobrança da linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="d7941-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="d7941-126">Os registros atuais de um projeto não mapeado também serão reavaliados e recriados como consequência.</span><span class="sxs-lookup"><span data-stu-id="d7941-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="d7941-127">Corrigido: Uma validação adicional foi incluída a um campo **Valor** da linha de estimativa para garantir que os valores nulos não sejam persistentes.</span><span class="sxs-lookup"><span data-stu-id="d7941-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="d7941-128">Corrigido: Quando dados reais tiverem sido atualizados em um projeto, um botão de atualização foi adicionado ao formulário principal do projeto para permitir que os usuários sincronizem novamente os dados reais.</span><span class="sxs-lookup"><span data-stu-id="d7941-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="d7941-129">Corrigido: Quando os usuários atualizarem do 2.X para 3.X, os projetos com valor NULL para o nome do projeto serão permitidos.</span><span class="sxs-lookup"><span data-stu-id="d7941-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]