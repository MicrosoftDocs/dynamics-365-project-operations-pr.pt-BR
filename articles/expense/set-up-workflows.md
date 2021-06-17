---
title: Configurar fluxos de trabalho para gerenciamento de despesas
description: Você pode configurar um processo de fluxo de trabalho que é usado para analisar e aprovar documentos de viagens e despesas.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001007"
---
# <a name="set-up-workflows-for-expense-management"></a>Configurar fluxos de trabalho para gerenciamento de despesas

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Você pode configurar um processo de fluxo de trabalho para analisar e aprovar documentos de viagens e despesas. É possível definir fluxos de trabalho para relatórios de despesas, requisições de viagem e solicitações de adiantamento em dinheiro.

Um fluxo de trabalho representa um processo empresarial e define como um documento flui pelo sistema. O fluxo de trabalho também indica quem deve concluir uma tarefa ou aprovar um documento. Há vários benefícios em usar o sistema de fluxo de trabalho na sua organização:

- **Processos consistentes**: você pode definir o processo de aprovação para documentos específicos, como requisições de compra e relatórios de despesas. O uso do sistema de fluxo de trabalho ajuda a garantir que os documentos sejam processados e aprovados de maneira consistente e eficiente.
- **Visibilidade de processos**: você pode rastrear o status, o histórico e as métricas de desempenho de uma instância de fluxo de trabalho específica. Isso ajuda a determinar se é necessário fazer alterações no fluxo de trabalho para melhorar a eficiência.
- **Lista de trabalho centralizada**: os usuários podem exibir uma lista de trabalho centralizada para visualizar as tarefas e aprovações do fluxo de trabalho atribuídas a eles. 

## <a name="workflow-types"></a>Tipos de fluxo de trabalho

A tabela a seguir lista os tipos de fluxo de trabalho que podem ser criados em **Gerenciamento de Despesas**.


|              <strong>Tipo</strong>              |                   <strong>Use este tipo para</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Aprovação automática de relatórios de despesas</strong> |            Criar fluxos de trabalho de aprovação para relatórios de despesas.             |
|  <strong>Lançamento automático de relatórios de despesas</strong>   |        Criar fluxos de trabalho de lançamento automático para relatórios de despesas.        |
|       <strong>Item de linha de despesas</strong>        |     Criar fluxos de trabalho de aprovação para itens de linha em relatórios de despesas.      |
| <strong>Lançamento automático de item de linha de despesas</strong> | Criar fluxos de trabalho de lançamento automático para itens de linha em relatórios de despesas. |
|       <strong>Requisição de viagem</strong>       |          Criar fluxos de trabalho de aprovação para requisições de viagem.           |
|      <strong>Solicitação de adiantamento em dinheiro</strong>      |         Criar fluxos de trabalho de aprovação para solicitações de adiantamento em dinheiro.          |
|        <strong>Recuperação do imposto IVA</strong>        | Criar fluxos de trabalho de aprovação para a recuperação do imposto sobre valor agregado (IVA).  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]