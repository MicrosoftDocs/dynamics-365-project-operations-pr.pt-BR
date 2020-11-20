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
ms.openlocfilehash: e1a645b157c56066e56b22ea8cf0324fbc1ddd2c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120304"
---
# <a name="reporting-home-page"></a><span data-ttu-id="6a5bf-103">Home page de relatórios</span><span class="sxs-lookup"><span data-stu-id="6a5bf-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6a5bf-104">O Microsoft Dynamics 365 Project Service Automation permite que organizações baseadas em projetos gerenciem com eficiência as operações de seus negócios.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="6a5bf-105">Em qualquer projeto, os membros da equipe devem gerenciar a oportunidade, cotar e planejar o trabalho, abastecer os projetos, gerenciar o trabalho de acordo com o plano, cobrar pelo trabalho e, por fim, realizar o trabalho para concluir o projeto.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="6a5bf-106">A capacidade de relatar operações é fundamental para determinar a integridade da organização e executar as ações corretivas necessárias.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="6a5bf-107">O PSA usa os métodos e as tecnologias de relatório do Microsoft Dynamics 365 na sua criação de relatórios.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="6a5bf-108">Para obter mais informações sobre as opções de geração de relatórios, consulte o [Guia de redação de relatórios para Dynamics 365 Customer Engagement (on-premises), versão 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="6a5bf-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="6a5bf-109">Assistente de Relatório</span><span class="sxs-lookup"><span data-stu-id="6a5bf-109">Report Wizard</span></span>

<span data-ttu-id="6a5bf-110">O Assistente de Relatório permite que não desenvolvedores criem relatórios simples.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="6a5bf-111">Como o aplicativo se baseia em uma plataforma existente, a experiência é igual à experiência documentada em [Criar ou editar um relatório usando o Assistente de Relatório](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="6a5bf-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="6a5bf-112">No entanto, você usará as entidades específicas ao Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="6a5bf-113">Relatórios personalizados do SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="6a5bf-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="6a5bf-114">Se a sua empresa exigir um relatório específico que não possa ser criado usando o Assistente de Relatório, você pode criar um relatório personalizado.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="6a5bf-115">Você deve ter o Microsoft Visual Studio instalado, juntamente com o Microsoft SQL Server Data Tools e as Extensões de Criação de Relatórios apropriados.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="6a5bf-116">Para obter mais informações sobre ferramentas e versões, consulte [Ambiente de elaboração de relatório usando o SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="6a5bf-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="6a5bf-117">Para obter informações sobre como criar um relatório personalizado, consulte [Criar um novo relatório usando o SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="6a5bf-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="6a5bf-118">Aplicativos de insights do Power BI</span><span class="sxs-lookup"><span data-stu-id="6a5bf-118">Power BI insights apps</span></span>

<span data-ttu-id="6a5bf-119">Juntos, o Microsoft Power BI e o Dynamics 365 oferecem uma maneira poderosa de trabalhar com seus dados, na forma de aplicativos de insights.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="6a5bf-120">Para obter informações sobre a disponibilidade de aplicativos de insights, consulte a [página de aplicativos de insights do Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="6a5bf-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6a5bf-121">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="6a5bf-121">Additional resources</span></span>
<span data-ttu-id="6a5bf-122">Para obter mais informações sobre relatórios no PSA, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6a5bf-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="6a5bf-123">Trabalhar com o modelo de dados do Project Service</span><span class="sxs-lookup"><span data-stu-id="6a5bf-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="6a5bf-124">Painéis</span><span class="sxs-lookup"><span data-stu-id="6a5bf-124">Dashboards</span></span>](reports-dashboards.md)
