---
title: Estimativa de custo de atribuições de recursos subcontratados
description: Este tópico explica como o Microsoft Dynamics 365 Project Operations calcula a estimativa de custo de atribuições de recursos subcontratados.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 5a94840a3735639532683153105fea85bea99c9d
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902807"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimativa de custo de atribuições de recursos subcontratados

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

As atribuições de tarefas dos membros da equipe do projeto subcontratados são calculadas usando a lista de preços de **Compra** anexada ao subcontrato no registro do membro da equipe relacionado. É diferente de como as atribuições de recursos de funcionários são custeadas onde as atribuições de tarefas de recursos de funcionários são custeadas usando a lista de preços de **Custo** anexada à unidade de contratação do projeto. 

Para membros da equipe de projeto genéricos que são subcontratados, as atribuições são custeadas usando uma configuração de preço baseada em função na lista de preços de compra anexada ao subcontrato. Os preços de compra também podem ser configurados especificamente para cada recurso. Esses preços específicos de recursos terão prioridade ao custear atribuições de tarefas de membros nomeados da equipe do projeto que são trabalhadores contratados. 

A prioridade de usar o preço de compra específico da função em comparação ao específico do recurso é determinada pela configuração da prioridade da dimensão de preço em **Parâmetros > Dimensões de preços baseadas em valor**.

Essa funcionalidade de derivar preços dinamicamente com base na configuração de dimensão para preços de compra de subcontratados é semelhante à forma como as taxas de custo e fatura são derivadas para funcionários em tempo integral. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Criação de atribuições de tarefas para obter estimativas de custo de recursos de subcontratados

As atribuições de tarefas para subcontratados podem ser criadas de duas maneiras: 
- Usando a guia **Tarefas**.
- Usando a guia **Equipe**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Criação de atribuições de recursos usando a guia Tarefas
Usando a lista **Recursos** na guia **Tarefas** para uma tarefa específica, você pode criar uma atribuição de tarefa para um recurso nomeado ou um recurso genérico. Se você selecionar um recurso nomeado na lista suspensa **Recursos Atribuídos** na tarefa e esse recurso for um trabalhador contratado, o recurso nomeado será atribuído à tarefa e um registro de membro da equipe do projeto correspondente será criado com o tipo de trabalhador definido para o **Trabalhador do Contrato** e a **Validade** definidos como **Inválidos**. Na próxima etapa, você precisará abrir o registro de membro da equipe do projeto e selecionar um subcontrato e uma linha de subcontrato. Isso atualizará a atribuição de tarefas para ter uma referência ao subcontrato e à linha de subcontrato e também atualizará o status do membro da equipe para **Válido**.

Se você optar por criar um membro da equipe genérico na lista suspensa **Recursos Atribuídos** na tarefa, a caixa de diálogo **Criação de membro da equipe genérico** permitirá que você selecione um subcontrato e uma linha de subcontrato. Quando o recurso genérico é atribuído à tarefa e o registro de membro da equipe do projeto correspondente é criado, você notará que o registro do membro da equipe do projeto é criado com o tipo de trabalhador definido como **Trabalhador do Contrato** e **Validade** definido para **Válido**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Criação de membros da equipe do projeto usando a guia Equipe
Usando a guia Equipe no projeto, você pode criar um membro da equipe genérico ou nomeado. Ao criar o membro da equipe, é possível selecionar o subcontrato e a linha de subcontrato. Após a criação do membro da equipe, você precisará atribuí-lo a uma tarefa usando a lista suspensa **Recursos Atribuídos** na tarefa. 

## <a name="updating-estimates"></a>Atualização de estimativas
Depois de atribuir as tarefas aos membros da equipe do projeto, você precisará acessar a guia **Estimativas** no projeto e selecionar **Atualizar preços** para garantir que as taxas de custo das atribuições de recursos do subcontratado sejam atualizadas com base na lista de preços de compra anexada ao subcontrato. Observe que as estimativas não são geradas para tarefas não atribuídas no Microsoft Dynamics 365 Project Operations. Como resultado, você precisará criar atribuições de tarefas para precificar e custear várias tarefas em seu projeto. 

> [OBSERVAÇÃO] Os membros da equipe do projeto com **Tipo de trabalhador** como **Trabalhador do Contrato**, mas sem uma referência de subcontrato, são sinalizados como **Inválidos** na grade **Membros da equipe de projeto**. Se houver algum membro da equipe do projeto com esse status, abra o registro do membro da equipe do projeto e atualize manualmente os campos de subcontrato e linha de subcontrato para que a estimativa de custo financeiro reflita com precisão o custo do subcontratado na guia **Estimativas**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
