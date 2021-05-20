---
title: Home page de relatórios
description: Este tópico fornece informações sobre relatórios no Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 32b504a862f98dac4b1d9b54289476026d988c13
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951465"
---
# <a name="reporting-home-page"></a><span data-ttu-id="6b30c-103">Home page de relatórios</span><span class="sxs-lookup"><span data-stu-id="6b30c-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6b30c-104">O Microsoft Dynamics 365 Project Service Automation permite que organizações baseadas em projetos gerenciem com eficiência as operações de seus negócios.</span><span class="sxs-lookup"><span data-stu-id="6b30c-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="6b30c-105">Em qualquer projeto, os membros da equipe devem gerenciar a oportunidade, cotar e planejar o trabalho, abastecer os projetos, gerenciar o trabalho de acordo com o plano, cobrar pelo trabalho e, por fim, realizar o trabalho para concluir o projeto.</span><span class="sxs-lookup"><span data-stu-id="6b30c-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="6b30c-106">A capacidade de relatar operações é fundamental para determinar a integridade da organização e executar as ações corretivas necessárias.</span><span class="sxs-lookup"><span data-stu-id="6b30c-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="6b30c-107">O PSA usa os métodos e as tecnologias de relatório do Microsoft Dynamics 365 na sua criação de relatórios.</span><span class="sxs-lookup"><span data-stu-id="6b30c-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="6b30c-108">Para obter mais informações sobre as opções de geração de relatórios, consulte o [Guia de redação de relatórios para Dynamics 365 Customer Engagement (on-premises), versão 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="6b30c-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="6b30c-109">Assistente de Relatório</span><span class="sxs-lookup"><span data-stu-id="6b30c-109">Report Wizard</span></span>

<span data-ttu-id="6b30c-110">O Assistente de Relatório permite que não desenvolvedores criem relatórios simples.</span><span class="sxs-lookup"><span data-stu-id="6b30c-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="6b30c-111">Como o aplicativo se baseia em uma plataforma existente, a experiência é igual à experiência documentada em [Criar ou editar um relatório usando o Assistente de Relatório](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="6b30c-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="6b30c-112">No entanto, você usará as entidades específicas ao Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6b30c-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="6b30c-113">Relatórios personalizados do SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="6b30c-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="6b30c-114">Se a sua empresa exigir um relatório específico que não possa ser criado usando o Assistente de Relatório, você pode criar um relatório personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b30c-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="6b30c-115">Você deve ter o Microsoft Visual Studio instalado, juntamente com o Microsoft SQL Server Data Tools e as Extensões de Criação de Relatórios apropriados.</span><span class="sxs-lookup"><span data-stu-id="6b30c-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="6b30c-116">Para obter mais informações sobre ferramentas e versões, consulte [Ambiente de elaboração de relatório usando o SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="6b30c-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="6b30c-117">Para obter informações sobre como criar um relatório personalizado, consulte [Criar um novo relatório usando o SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="6b30c-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="6b30c-118">Aplicativos de insights do Power BI</span><span class="sxs-lookup"><span data-stu-id="6b30c-118">Power BI insights apps</span></span>

<span data-ttu-id="6b30c-119">Juntos, o Microsoft Power BI e o Dynamics 365 oferecem uma maneira poderosa de trabalhar com seus dados, na forma de aplicativos de insights.</span><span class="sxs-lookup"><span data-stu-id="6b30c-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="6b30c-120">Para obter informações sobre a disponibilidade de aplicativos de insights, consulte a [página de aplicativos de insights do Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="6b30c-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6b30c-121">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="6b30c-121">Additional resources</span></span>
<span data-ttu-id="6b30c-122">Para obter mais informações sobre relatórios no PSA, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6b30c-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="6b30c-123">Trabalhar com o modelo de dados do Project Service</span><span class="sxs-lookup"><span data-stu-id="6b30c-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="6b30c-124">Painéis</span><span class="sxs-lookup"><span data-stu-id="6b30c-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]