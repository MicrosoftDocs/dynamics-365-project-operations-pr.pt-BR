---
title: Segurança e aprovações
description: Este artigo contém informações sobre a configuração da segurança para trabalhar com aprovações no Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841909"
---
# <a name="security-and-approvals"></a>Segurança e aprovações

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Microsoft Dynamics 365 Project Operations usa duas funções de segurança para permitir a aprovação de entradas de horários, despesas e materiais:

- Aprovador do Projeto
- Administrador do Aprovador do Projeto

## <a name="project-approver"></a>Aprovador do Projeto

Você precisa ter o direito de acesso **Aprovador do Projeto** para aprovar entradas de horários, despesas e materiais do projeto. Também é necessário ter acesso às entidades relacionadas, como **Projeto**. Esse acesso pode ser atribuído por alguém com a função **Gerente de projeto**. Além disso, é preciso fazer parte da equipe do projeto e estar marcado como um aprovador.

Para aprovar entradas que não são de projeto, você deve ser o gerente do remetente.

## <a name="project-approver-admin"></a>Administrador do Aprovador do Projeto

> [!NOTE]
> O recurso dos [Conjuntos de aprovação](approval-sets.md) precisa ser habilitado para você poder usar a funcionalidade do Administrador do Aprovador do Projeto.

O direito de acesso do **Administrador do Aprovador do Projeto** permite que os usuários ignorem políticas e aprovem entradas em todos os projetos. A atribuição dessa função ignora a lógica de validação que exige a associação à equipe e a marcação como aprovador. Você deve ter acesso às tabelas relacionadas relevantes, como **Projeto**, por meio de direitos de acesso atribuídos a você.

O contexto de usuário do SISTEMA ignora as validações da mesma forma que o direito de acesso de Administrador do Aprovador do Projeto.
