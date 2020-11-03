---
title: Desenvolver modelos de projeto com Copiar Projeto
description: Este tópico fornece informações sobre como criar modelos de projeto usando a ação personalizada Copiar Projeto.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071368"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolver modelos de projeto com Copiar Projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

O Dynamics 365 Project Operations oferece suporte à capacidade de copiar um projeto e reverter atribuições para os recursos genéricos que representam a função. Os clientes podem usar essa funcionalidade para criar modelos básicos de projeto.

Quando você seleciona **Copiar Projeto** , o status do projeto de destino é atualizado. Usar **Razão do Status** para determinar quando a ação de cópia está concluída. Selecionar **Copiar Projeto** também atualizará a data de início do projeto para a data de início atual se nenhuma data-alvo for detectada na entidade do projeto de destino.

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


- **{"clearTeamsAndAssignments":true}** : o comportamento padrão do projeto para a Web e removerá todas as atribuições e membros da equipe.
- **{"removeNamedResources":true}** o comportamento padrão do Project Operations e reverterá atribuições para recursos genéricos.

Para obter mais padrões sobre ações, consulte [Usar ações da API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Especificar campos a serem copiados 
Quando a ação for chamada, **Copiar Projeto** verificará a visão do projeto **Copiar Colunas do Projeto** para determinar quais campos copiar quando o projeto for copiado.
