---
title: Visão geral dos modos de gerenciamento de recursos
description: Esse tópico fornece informações sobre a funcionalidade de Gerenciamento de recursos no Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279439"
---
# <a name="resource-management-modes-overview"></a>Visão geral dos modos de gerenciamento de recursos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


O Dynamics 365 Project Operations oferece suporte a dois modos para você executar o fluxo geral de reservas. O modo de gerenciamento é definido como um parâmetro do projeto e poderá ser modificado se as necessidades de negócios mudarem.    

## <a name="central-mode"></a>Modo Central
Para organizações que centralizam a alocação de recursos para projetos, o modo Central fornece uma maneira de garantir que os gerentes de projeto possam definir os requisitos de recursos no nível do projeto. O atendimento dos requisitos de recursos é delegado a um gerente de recursos. Os gerentes de projeto podem aceitar ou rejeitar recursos propostos pelo gerente de recursos.

![Modo Central](./media/resource-management-central.png)

Para gerenciar recursos com o modo Central, consulte:

- [Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recurso](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos indicados a partir de requisitos de recurso](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Enviar uma solicitação de recurso](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Atender uma solicitação de recursos](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Aceitar ou rejeitar um recurso de projeto proposto de uma solicitação de recurso](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modo Híbrido
Para organizações que exigem flexibilidade na alocação de recursos, o modo híbrido permite que gerentes de projeto e gerentes de recursos reservem recursos.

![Modo Híbrido](./media/resource-management-hybrid.png)

Além do processo do modo Central compatível, consulte os tópicos a seguir para gerenciar todos os outros fluxos de reserva compatíveis no modo Híbrido:

Reservar um recurso diretamente em um projeto:
- [Reservar recursos reserváveis nomeados a uma equipe de projeto e atribuir tarefas](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Reservar um recurso de um requisito de recursos:
- [Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recurso](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos indicados a partir de requisitos de recurso](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]