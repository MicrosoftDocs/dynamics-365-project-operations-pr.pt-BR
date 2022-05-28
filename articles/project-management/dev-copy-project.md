---
title: Desenvolver modelos de projeto com Copiar Projeto
description: Este tópico fornece informações sobre como criar modelos de projeto usando a ação personalizada Copiar Projeto.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590884"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolver modelos de projeto com Copiar Projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations oferece suporte à possibilidade de copiar um projeto e reverter quaisquer atribuições de volta aos recursos genéricos que representam a função. Os clientes podem usar essa funcionalidade para criar modelos básicos de projeto.

Quando você seleciona **Copiar Projeto**, o status do projeto de destino é atualizado. Usar **Razão do Status** para determinar quando a ação de cópia está concluída. Selecionar **Copiar Projeto** também atualizará a data de início do projeto para a data de início atual se nenhuma data-alvo for detectada na entidade do projeto de destino.

## <a name="copy-project-custom-action"></a>Ação personalizada Copiar Projeto

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Parâmetros de entrada

Há três parâmetros de entrada:

- **ReplaceNamedResources** ou **ClearTeamsAndAssignments** – Defina somente uma das opções. Não defina ambas.

    - **\{"ReplaceNamedResources":true\}** – O comportamento padrão do Project Operations. Todos os recursos nomeados são substituídos por recursos genéricos.
    - **\{"ClearTeamsAndAssignments":true\}** – O comportamento padrão do Project for the Web. Todas as atribuições e os membros de equipe são removidos.

- **SourceProject** – A referência de entidade do projeto de origem para cópia. Esse parâmetro não pode ser nulo.
- **Target** – A referência de entidade do projeto de destino para cópia. Esse parâmetro não pode ser nulo.

A tabela a seguir traz um resumo dos três parâmetros.

| Parâmetro                | Type             | Valor                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **True** ou **False** |
| ClearTeamsAndAssignments | Boolean          | **True** ou **False** |
| SourceProject            | Referência da Entidade | O projeto de origem    |
| Target                   | Referência da Entidade | O projeto de destino    |

Para obter mais padrões sobre ações, consulte [Usar ações da API Web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validações

As validações a seguir são feitas.

1. Null verifica e recupera os projetos de origem e de destino para confirmar a existência dos dois na organização.
2. O sistema valida se o projeto de destino é válido para cópia verificando as seguintes condições:

    - Não há atividade anterior no projeto (inclusive a seleção da guia **Tarefas**) e o projeto é recém-criado.
    - Não há cópia anterior, nenhuma importação foi solicitada no projeto e o projeto não tem o status **Falha**.

3. A operação não é chamada usando HTTP.

## <a name="specify-fields-to-copy"></a>Especificar campos a serem copiados

Quando a ação for chamada, **Copiar Projeto** verificará a visão do projeto **Copiar Colunas do Projeto** para determinar quais campos copiar quando o projeto for copiado.

### <a name="example"></a>Exemplo

O exemplo a seguir mostra como chamar a ação personalizada **CopyProjectV3** com o conjunto de parâmetros **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
