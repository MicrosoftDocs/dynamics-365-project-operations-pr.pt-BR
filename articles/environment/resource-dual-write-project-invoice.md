---
title: Integração de faturas do projeto
description: Este artigo fornece informações sobre a integração de gravação dupla no Project Operations para faturamento de clientes.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912088"
---
# <a name="project-invoice-integration"></a>Integração de faturas do projeto

Este artigo fornece informações sobre a integração de gravação dupla no Project Operations para faturamento de clientes.

No Project Operations, o gerente do projeto gerencia a lista de pendências de cobrança do projeto e cria uma fatura pro forma para o cliente no Microsoft Dataverse. Com base nessa fatura pro forma, o administrador de contas a receber ou o contador do projeto cria uma fatura voltada para o cliente. A integração de gravação dupla garante que os detalhes da fatura proforma sejam sincronizados com os aplicativos de finanças e operações. Depois que a fatura do cliente é lançada, o sistema atualiza os dados reais do projeto relevante no Dataverse com os detalhes contábeis. O gráfico a seguir fornece uma visão geral conceitual de alto nível dessa integração.

   ![Integração de faturas do projeto.](./media/DW5Invoicing.png)

Depois que o gerente de projeto confirma a fatura proforma no Dataverse, as informações do cabeçalho da fatura proforma são sincronizadas com os aplicativos de finanças e operações usando o mapa de tabela de gravação dupla, **Proposta de fatura do projeto V2 (faturas)**. Trata-se de uma integração unidirecional do Dataverse para aplicativos de finanças e operações. Não há suporte para a criação ou exclusão de propostas de fatura do projeto diretamente nos aplicativos de finanças e operações.

A confirmação de fatura no Dataverse também dispara a lógica de negócios para criar registros relativos à cobrança na entidade **Dados Reais** . Esses registros são sincronizados com o Finance and Operations usando o mapa de tabela de gravação dupla, **Valores reais de integração do Project Operations (msdyn\_actuals).** Para obter mais informações, consulte [Estimativas e dados reais de projeto](resource-dual-write-estimates-actuals.md). 

As linhas de proposta de fatura do projeto são criadas pelo processo periódico, **Preparo de formulário de importação**. Este processo se baseia nos detalhes de dados reais de vendas cobradas na tabela **Preparo de dados reais**. Para obter mais informações, consulte [Gerenciar propostas de fatura de projeto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
