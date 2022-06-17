---
title: Visão geral dos modos de gerenciamento de recursos
description: Este artigo fornece informações sobre a funcionalidade de gerenciamento de recursos no Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928418"
---
# <a name="resource-management-modes-overview"></a>Visão geral dos modos de gerenciamento de recursos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


O Dynamics 365 Project Operations oferece suporte a dois modos para você executar o fluxo geral de reservas. O modo de gerenciamento é definido como um parâmetro do projeto e poderá ser modificado se as necessidades de negócios mudarem.    

## <a name="central-mode"></a>Modo Central
Para organizações que centralizam a alocação de recursos para projetos, o modo Central fornece uma maneira de garantir que os gerentes de projeto possam definir os requisitos de recursos no nível do projeto. O atendimento dos requisitos de recursos é delegado a um gerente de recursos. Os gerentes de projeto podem aceitar ou rejeitar recursos propostos pelo gerente de recursos.

![Modo Central.](./media/resource-management-central.png)

Para gerenciar recursos com o modo Central, consulte:

- [Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recurso](/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos indicados a partir de requisitos de recurso](/dynamics365/project-service/book-named-resource)
- [Enviar uma solicitação de recurso](/dynamics365/project-service/submit-resource-request)
- [Atender uma solicitação de recursos](/dynamics365/project-service/resource-management-fulfill-requests)
- [Aceitar ou rejeitar um recurso de projeto proposto de uma solicitação de recurso](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modo Híbrido
Para organizações que exigem flexibilidade na alocação de recursos, o modo híbrido permite que gerentes de projeto e gerentes de recursos reservem recursos.

![Modo Híbrido.](./media/resource-management-hybrid.png)

Além do processo de modo central compatível, consulte os seguintes artigos para gerenciar todos os outros fluxos de reserva compatíveis no modo híbrido:

Reservar um recurso diretamente em um projeto:
- [Reservar recursos reserváveis nomeados a uma equipe de projeto e atribuir tarefas](/dynamics365/project-service/assign-named-bookable-resource)

Reservar um recurso de um requisito de recursos:
- [Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recurso](/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos indicados a partir de requisitos de recurso](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]