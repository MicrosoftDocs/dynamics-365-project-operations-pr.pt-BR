---
title: Configurar fluxos de trabalho para gerenciamento de despesas
description: Você pode configurar um processo de fluxo de trabalho para analisar e aprovar documentos de viagens e despesas.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960503"
---
# <a name="set-up-expense-management-workflows"></a>Configurar fluxos de trabalho para gerenciamento de despesas

Você pode configurar um processo de fluxo de trabalho que é usado para analisar e aprovar documentos de viagens e despesas. Os documentos para os quais fluxos de trabalho podem ser definidos incluem relatórios de despesas, requisições de viagem e solicitações de adiantamento em dinheiro.

Um fluxo de trabalho representa um processo empresarial. Ele define como um documento flui pelo sistema e indica quem deve concluir uma tarefa ou aprovar um documento. Há vários benefícios em usar o sistema de fluxo de trabalho na sua organização:

-   **Processos consistentes** — você pode definir o processo de aprovação para documentos específicos, como requisições de compra e relatórios de despesas. O uso do sistema de fluxo de trabalho ajuda a garantir que documentos sejam processados e aprovados de maneira consistente e eficiente.

-   Visibilidade de processos — você pode rastrear o status, o histórico e as métricas de desempenho de uma instância de fluxo de trabalho específica. Isso ajuda a determinar se é necessário fazer alterações no fluxo de trabalho para melhorar a eficiência.

-   Lista de trabalho centralizada — os usuários podem exibir uma lista de trabalho centralizada para exibir as tarefas e aprovações do fluxo de trabalho atribuídas a eles. 

**Os tipos de fluxos de trabalho que você pode criar**

A tabela a seguir lista os tipos de fluxos de trabalho que podem ser criados em **Despesa**.


|              <strong>Tipo</strong>              |                   <strong>Use este tipo para</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Relatório de despesas</strong>         |            Criar fluxos de trabalho de aprovação para relatórios de despesas.             |
|  <strong>Lançamento automático de relatórios de despesas</strong>   |        Criar fluxos de trabalho de lançamento automático para relatórios de despesas.        |
|       <strong>Item de linha de despesas</strong>        |     Criar fluxos de trabalho de aprovação para itens de linha em relatórios de despesas.      |
| <strong>Lançamento automático de item de linha de despesas</strong> | Criar fluxos de trabalho de lançamento automático para itens de linha em relatórios de despesas. |
|       <strong>Requisição de viagem</strong>       |          Criar fluxos de trabalho de aprovação para requisições de viagem.           |
|      <strong>Solicitação de adiantamento em dinheiro</strong>      |         Criar fluxos de trabalho de aprovação para solicitações de adiantamento em dinheiro.          |
|        <strong>Recuperação do imposto IVA</strong>        | Criar fluxos de trabalho de aprovação para a recuperação do imposto sobre valor agregado (IVA).  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]