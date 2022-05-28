---
title: Recursos removidos ou preteridos no Dynamics 365 Project Operations
description: Este tópico descreve recursos que foram removidos ou que estão planejados para remoção do Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601556"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Recursos removidos ou preteridos no Dynamics 365 Project Operations

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não estocados, implantação Lite - fatura de acordo com pro forma e Project Operations para cenários baseados em estoque/produção__

Este tópico descreve recursos que foram removidos ou que estão planejados para remoção do Dynamics 365 Project Operations.

- Um recurso *removido* não está mais disponível no produto.
- Um recurso *preterido* não está em desenvolvimento ativo e pode ser removido em uma atualização futura.

Esta lista visa ajudá-lo a considerar essas remoções e substituições para seu próprio planejamento.

> [!NOTE]
> Informações detalhadas sobre objetos em aplicativos de finanças e operações podem ser encontradas nos [**Relatórios de referência técnica**](/dynamics/s-e/global/axtechrefrep_61). Você pode comparar as diferentes versões desses relatórios para descobrir objetos que foram alterados ou removidos em cada versão dos aplicativos de finanças e operações.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Recursos removidos ou preteridos na versão de março de 2022 do Project Operations

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parâmetro "Criar sempre transação de ajuste" de contabilidade e gerenciamento de projetos

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo para substituição/remoção** | As transações de ajuste são necessárias para fins de auditoria. Após a substituição, esse parâmetro ficará oculto. O sistema sempre criará transações de ajuste, assim como faz atualmente quando o parâmetro é definido como **Sim**. |
| **Substituído por outro recurso?** | No |
| **Áreas de produtos afetadas** | Aplicativo |
| **Opção de implantação** | Project Operations para cenários de produção/estoque |
| **Status** | Preterido: até 1º de março de 2023, ocultaremos o parâmetro e alteraremos o comportamento do sistema para que as transações de ajuste sejam sempre criadas. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parâmetro "Usar data de ajuste como nova data de projeto" de contabilidade e gerenciamento de projetos

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo para substituição/remoção** | Este parâmetro foi usado originalmente para permitir ajustes quando um período fiscal estava fechado. No entanto, ele não é mais necessário, pois, se configurado, é possível alterar a data contábil da transação para a primeira data do período em aberto. A data do projeto não deve ser alterada, pois representa a data em que a transação ocorreu. |
| **Substituído por outro recurso?** | No |
| **Áreas de produtos afetadas** | Aplicativo |
| **Opção de implantação** | Project Operations para cenários de produção/estoque |
| **Status** | Preterido: até 1º de março de 2023, ocultaremos o parâmetro e alteraremos o comportamento do sistema para que a data do projeto nunca seja alterada nos ajustes. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Fluxo de trabalho de solicitação de recursos no Project Operations para cenários baseados em estoque/produção

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo para substituição/remoção** | Preterido devido às limitações de volume de transações e baixo uso. |
| **Substituído por outro recurso?** | No |
| **Áreas de produtos afetadas** | Aplicativo |
| **Opção de implantação** | Project Operations para cenários de produção/estoque |
| **Status** | Preterido: até 1º de março de 2023, desabilitaremos a opção de solicitar recursos para o projeto usando o fluxo de trabalho. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Página de proposta de fatura do projeto sem visualizações de cabeçalho e linhas

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo para substituição/remoção** | Preterido devido a melhorias na página que foram introduzidas com a chave de recurso **Usar proposta de fatura do projeto e formulários do diário de faturas com a exibição Cabeçalho e Linhas**. |
| **Substituído por outro recurso?** | Sim |
| **Áreas de produtos afetadas** | Aplicativo |
| **Opção de implantação** | Project Operations para cenários de produção/estoque; Project Operations para cenários baseados em recursos/itens sem estoque |
| **Status** | Preterido: até 1º de março de 2023, desativaremos a página antiga (herdada) e ativaremos a chave de recurso **Usar proposta de fatura do projeto e formulários do diário de faturas com a exibição Cabeçalho e Linhas** por padrão. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Recursos removidos ou preteridos na versão de dezembro de 2021 do Project Operations

### <a name="collaboration-workspaces"></a>Espaços de trabalho de colaboração

[Criar ou vincular a um espaço de trabalho de colaboração (Projeto)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo para substituição/remoção** | Preterido devido a pouco uso. Os clientes que usam o Project Operations para cenários de recursos/não estocados podem aproveitar [Colaboração com Grupos do Office](../project-management/collaboration-groups.md). |
| **Substituído por outro recurso?** | No |
| **Áreas de produtos afetadas** | Aplicativo  |
| **Opção de implantação** | Project Operations para cenários de produção/estoque |
| **Status** | Preterido: até 1º de dezembro de 2022, planejamos não oferecer mais suporte aos espaços de trabalho de colaboração. |
