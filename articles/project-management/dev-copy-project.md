---
title: Desenvolver modelos de projeto com Copiar Projeto
description: Este tópico fornece informações sobre como criar modelos de projeto usando a ação personalizada Copiar Projeto.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642394"
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
