---
title: Modelo de segurança
description: Este tópico fornece informações sobre o modelo de segurança no Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ffcfa8a9c8e31c5665acd3c3919fa90d36a3f3ca
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896717"
---
# <a name="security-model"></a>Modelo de Segurança

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

O Microsoft Dynamics 365 Project Operations contém um modelo de segurança exclusivo que permite um modelo de segurança de negócios baseado em funções que colabora com o Microsoft Office Groups. 


## <a name="security-roles"></a>Funções de segurança
Os recursos de front-end do Project Operations incluem as seguintes funções:

| Função                          | Descrição                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Gerente de prática              | Dá suporte a relatórios entre projetos.                                                                                                            | Unidade de negócios              |
| Aprovador do projeto              | Aprova as hora e despesas de um projeto.                                                                                                                              | Unidade de negócios |
| Administrador de faturamento do projeto | Cria a proposta de fatura.                                                                                                                                                 | Unidade de negócios |
| Gerente de projeto               | Cria o plano do projeto e solicita recursos.                                                                                                                              | Unidade de negócios |
| Recurso do projeto              | Membros da equipe que pode ser reservado e relatar horas.                                                                                                          | Unidade de negócios|
| Gerente de recursos              | Todas as funções de gerenciamento de recursos, como atender solicitações e reservas de recursos, separadas para oferecer suporte a uma configuração híbrida de gerente de projeto mais gerente de recursos e uma função única e centralizada de gerente de recursos. | Unidade de negócios |


O Microsoft Project para a Web inclui as seguintes funções:
| Função                          | Descrição                                                                                                          | Scope |                                                       
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Usuário do projeto | Usuário colaborativo do projeto que é capaz de criar seus próprios projetos e exibir todos os projetos compartilhados com eles.| Usuário|
| Sistema do projeto | Função usada para o contexto do aplicativo. Os clientes não devem usar essa função do sistema. | Global|

## <a name="security-enforcement"></a>Aplicação de segurança
As ações executadas no nível do projeto são realizadas no contexto do usuário conectado. Isso significa que para criar, abrir ou excluir um projeto, o usuário deverá ter acesso disponível no CDS. O acesso no CDS pode ser concedido por meio de um dos possíveis mecanismos incluídos na plataforma. Por exemplo, um usuário com um escopo maior pode acessar o projeto ou se uma ação explícita de compartilhamento do projeto que concede acesso ao usuário tiver sido executada.

É importante considerar isso ao criar projetos no Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Colaboração moderna de grupo com o Project Operations
O Project para a Web e o Project Operations oferecem suporte a grupos modernos para colaboração. Os usuários adicionados ao projeto por meio de um grupo podem editar o plano do projeto.

O Project para a Web adiciona automaticamente usuários ao grupo após a atribuição.

Nos grupos, é possível que as permissões do projeto e os artefatos de colaboração de suporte sejam trabalhados de forma colaborativa. O diagrama a seguir descreve os eventos e mudanças de estado que acontecem durante o processo de atribuição de grupo.

O Project Operations não cria um grupo por meio de ação implícita, mas apenas por meio da ação explícita de pressionar grupos.

A pesquisa de membro do grupo na caixa de diálogo **Gerenciamento de grupo** é limitada àqueles que são definidos como parte do grupo de segurança do ambiente. Para obter mais informações, consulte [Controlar o acesso do usuário a ambientes: grupos de segurança e licenças](https://docs.microsoft.com/power-platform/admin/control-user-access).

1. O projeto é criado e é de propriedade do usuário criador.
2. O proprietário do projeto é atualizado para a equipe.
3. A equipe do proprietário é mapeada para o Grupo do Office especificado ou criado.
4. O proprietário original do projeto é adicionado ao Grupo do Office.

## <a name="deployment-recommendation"></a>Recomendação de implantação
Conforme o modelo de colaboração de grupo do Office evolui, serão adicionadas funcionalidades para fornecer um controle mais detalhado ao longo do tempo. Os clientes que implantam o Project Operations hoje são incentivados a se concentrar em um modelo de segurança tradicional do Microsoft Dynamics 365.

Para obter mais informações, consulte [Segurança no Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations e segurança do Microsoft Dynamics 365 Finance
O Project Operations inclui as seguintes funções:

- Gerente de projeto
- Contador do projeto

Para obter mais informações sobre segurança no Finance, consulte [Segurança baseada em funções](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


