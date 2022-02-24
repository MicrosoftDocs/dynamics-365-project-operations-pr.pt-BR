---
title: Enviar solicitação de recurso
description: Esse tópico fornece informações sobre o envio de uma solicitação para um recurso do projeto.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149709"
---
# <a name="submitting-a-resource-request"></a>Enviar solicitação de recurso

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Você pode enviar um requisito de recurso gerado como uma solicitação de recurso. Em seguida, a solicitação é enviada para um gerenciador de recursos para aprovação.

1. No Project Service Automation (PSA), na página **Projetos**, clique na guia **Equipe** para visualizar uma lista de recursos reserváveis. 
2. Selecione o recurso genérico com um requisito de recurso da lista e clique em **Enviar solicitação**.

![Enviar solicitação de recurso](media/RM-how-to-18.png)

O status da solicitação do membro da equipe genérico será alterado para **Enviado**.

Após a solicitação ser aprovada pelo gerenciador de recursos, o recurso genérico será substituído por um recurso nomeado se o gerenciador de recurso aprovar a solicitação com a reserva de um recurso indicado. Caso contrário, o recurso genérico permanecerá na equipe e o status de solicitação será alterado para **Precisa de revisão**, se o gerenciador de recurso tiver proposto um recurso nomeado.
