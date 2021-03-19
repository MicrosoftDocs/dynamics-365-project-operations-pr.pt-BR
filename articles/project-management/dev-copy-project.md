---
title: Desenvolver modelos de projeto com Copiar Projeto
description: Este tópico fornece informações sobre como criar modelos de projeto usando a ação personalizada Copiar Projeto.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286909"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="d2472-103">Desenvolver modelos de projeto com Copiar Projeto</span><span class="sxs-lookup"><span data-stu-id="d2472-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="d2472-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="d2472-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d2472-105">O Dynamics 365 Project Operations oferece suporte à possibilidade de copiar um projeto e reverter quaisquer atribuições de volta aos recursos genéricos que representam a função.</span><span class="sxs-lookup"><span data-stu-id="d2472-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="d2472-106">Os clientes podem usar essa funcionalidade para criar modelos básicos de projeto.</span><span class="sxs-lookup"><span data-stu-id="d2472-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="d2472-107">Quando você seleciona **Copiar Projeto**, o status do projeto de destino é atualizado.</span><span class="sxs-lookup"><span data-stu-id="d2472-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="d2472-108">Usar **Razão do Status** para determinar quando a ação de cópia está concluída.</span><span class="sxs-lookup"><span data-stu-id="d2472-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="d2472-109">Selecionar **Copiar Projeto** também atualizará a data de início do projeto para a data de início atual se nenhuma data-alvo for detectada na entidade do projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="d2472-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="d2472-110">Ação personalizada Copiar Projeto</span><span class="sxs-lookup"><span data-stu-id="d2472-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="d2472-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d2472-111">Name</span></span> 

<span data-ttu-id="d2472-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="d2472-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="d2472-113">Parâmetros de entrada</span><span class="sxs-lookup"><span data-stu-id="d2472-113">Input parameters</span></span>
<span data-ttu-id="d2472-114">Há três parâmetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="d2472-114">There are three input parameters:</span></span>

| <span data-ttu-id="d2472-115">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2472-115">Parameter</span></span>          | <span data-ttu-id="d2472-116">Digitar</span><span class="sxs-lookup"><span data-stu-id="d2472-116">Type</span></span>   | <span data-ttu-id="d2472-117">Valores</span><span class="sxs-lookup"><span data-stu-id="d2472-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="d2472-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="d2472-118">ProjectCopyOption</span></span>  | <span data-ttu-id="d2472-119">Cadeia de Caracteres</span><span class="sxs-lookup"><span data-stu-id="d2472-119">String</span></span> | <span data-ttu-id="d2472-120">**{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="d2472-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="d2472-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="d2472-121">SourceProject</span></span>      | <span data-ttu-id="d2472-122">Referência da Entidade</span><span class="sxs-lookup"><span data-stu-id="d2472-122">Entity Reference</span></span> | <span data-ttu-id="d2472-123">Projeto de Origem</span><span class="sxs-lookup"><span data-stu-id="d2472-123">Source Project</span></span> |
| <span data-ttu-id="d2472-124">Destino</span><span class="sxs-lookup"><span data-stu-id="d2472-124">Target</span></span>             | <span data-ttu-id="d2472-125">Referência da Entidade</span><span class="sxs-lookup"><span data-stu-id="d2472-125">Entity Reference</span></span> | <span data-ttu-id="d2472-126">Projeto de Destino</span><span class="sxs-lookup"><span data-stu-id="d2472-126">Target Project</span></span> |


- <span data-ttu-id="d2472-127">**{"clearTeamsAndAssignments":true}**: o comportamento padrão do projeto para a Web e removerá todas as atribuições e membros da equipe.</span><span class="sxs-lookup"><span data-stu-id="d2472-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="d2472-128">**{"removeNamedResources":true}** o comportamento padrão do Project Operations e reverterá atribuições para recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="d2472-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="d2472-129">Para obter mais padrões sobre ações, consulte [Usar ações da API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="d2472-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="d2472-130">Especificar campos a serem copiados</span><span class="sxs-lookup"><span data-stu-id="d2472-130">Specify fields to copy</span></span> 
<span data-ttu-id="d2472-131">Quando a ação for chamada, **Copiar Projeto** verificará a visão do projeto **Copiar Colunas do Projeto** para determinar quais campos copiar quando o projeto for copiado.</span><span class="sxs-lookup"><span data-stu-id="d2472-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="d2472-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d2472-132">Example</span></span>
<span data-ttu-id="d2472-133">O exemplo a seguir mostra como chamar a ação personalizada **CopyProject** com o conjunto de parâmetros **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="d2472-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]