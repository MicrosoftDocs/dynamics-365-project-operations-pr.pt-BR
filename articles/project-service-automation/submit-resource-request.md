---
title: Enviar uma solicitação de recurso
description: Esse tópico fornece informações sobre o envio de uma solicitação para um recurso do projeto.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749120"
---
# <a name="submit-a-resource-request"></a>Enviar uma solicitação de recurso

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Você pode enviar um requisito de recurso gerado como uma solicitação de recurso. Em seguida, a solicitação é enviada para um gerenciador de recursos para aprovação.

1. No Project Service Automation (PSA), na página **Projetos**, clique na guia **Equipe** para visualizar uma lista de recursos reserváveis. 
2. Selecione o recurso genérico com um requisito de recurso da lista e clique em **Enviar solicitação**.

![Enviar solicitação de recurso](media/RM-how-to-18.png)

O status da solicitação do membro da equipe genérico será alterado para **Enviado**.

Após a solicitação ser aprovada pelo gerenciador de recursos, o recurso genérico será substituído por um recurso nomeado se o gerenciador de recurso aprovar a solicitação com a reserva de um recurso indicado. Caso contrário, o recurso genérico permanecerá na equipe e o status de solicitação será alterado para **Precisa de revisão**, se o gerenciador de recurso tiver proposto um recurso nomeado.
