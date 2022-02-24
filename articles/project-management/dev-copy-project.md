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
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2021
ms.locfileid: "5044995"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolver modelos de projeto com Copiar Projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

O Dynamics 365 Project Operations oferece suporte à possibilidade de copiar um projeto e reverter quaisquer atribuições de volta aos recursos genéricos que representam a função. Os clientes podem usar essa funcionalidade para criar modelos básicos de projeto.

Quando você seleciona **Copiar Projeto**, o status do projeto de destino é atualizado. Usar **Razão do Status** para determinar quando a ação de cópia está concluída. Selecionar **Copiar Projeto** também atualizará a data de início do projeto para a data de início atual se nenhuma data-alvo for detectada na entidade do projeto de destino.

## <a name="copy-project-custom-action"></a>Ação personalizada Copiar Projeto 

### <a name="name"></a>Nome 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parâmetros de entrada
Há três parâmetros de entrada:

| Parâmetro          | Digitar   | Valores                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Cadeia de Caracteres | **{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referência da Entidade | Projeto de Origem |
| Destino             | Referência da Entidade | Projeto de Destino |


- **{"clearTeamsAndAssignments":true}**: o comportamento padrão do projeto para a Web e removerá todas as atribuições e membros da equipe.
- **{"removeNamedResources":true}** o comportamento padrão do Project Operations e reverterá atribuições para recursos genéricos.

Para obter mais padrões sobre ações, consulte [Usar ações da API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Especificar campos a serem copiados 
Quando a ação for chamada, **Copiar Projeto** verificará a visão do projeto **Copiar Colunas do Projeto** para determinar quais campos copiar quando o projeto for copiado.


### <a name="example"></a>Exemplo
O exemplo a seguir mostra como chamar a ação personalizada **CopyProject** com o conjunto de parâmetros **removeNamedResources**.
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
