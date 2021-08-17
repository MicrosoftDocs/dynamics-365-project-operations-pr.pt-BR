---
title: Integração de faturas do projeto
description: Este tópico fornece informações sobre a integração de gravação dupla do Project Operations para o faturamento do cliente.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993227"
---
# <a name="project-invoice-integration"></a>Integração de faturas do projeto

Este tópico fornece informações sobre a integração de gravação dupla do Project Operations para o faturamento do cliente.

No Project Operations, o gerente do projeto gerencia a lista de pendências de cobrança do projeto e cria uma fatura pro forma para o cliente no Microsoft Dataverse. Com base nessa fatura pro forma, o administrador de contas a receber ou o contador do projeto cria uma fatura voltada para o cliente. A integração de gravação dupla garante que os detalhes da fatura pro forma sejam sincronizados com aplicativos do Finance and Operations. Depois que a fatura do cliente é lançada, o sistema atualiza os dados reais do projeto relevante no Dataverse com os detalhes contábeis. O gráfico a seguir fornece uma visão geral conceitual de alto nível dessa integração.

   ![Integração de faturas do projeto.](./media/DW5Invoicing.png)

Depois que o gerente de projeto confirma a fatura pro forma no Dataverse, as informações do cabeçalho da fatura pro forma são sincronizadas com aplicativos do Finance and Operations usando o mapa de tabela de gravação dupla, **Proposta de fatura do projeto V2 (faturas)**. Esta é uma integração unilateral do Dataverse para aplicativos do Finance and Operations. Não há suporte à criação ou exclusão de propostas de fatura do projeto diretamente em aplicativos do Finance and Operations.

A confirmação de fatura no Dataverse também dispara a lógica de negócios para criar registros relativos à cobrança na entidade **Dados Reais** . Esses registros são sincronizados com o Finance and Operations usando o mapa da tabela de gravação dupla, **Dados reais de integração do Project Operations (msdyn\_actuals).** Para obter mais informações, consulte [Estimativas e dados reais de projeto](resource-dual-write-estimates-actuals.md). 

As linhas de proposta de fatura do projeto são criadas pelo processo periódico, **Preparo de formulário de importação**. Este processo se baseia nos detalhes de dados reais de vendas cobradas na tabela **Preparo de dados reais**. Para obter mais informações, consulte [Gerenciar propostas de fatura de projeto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
