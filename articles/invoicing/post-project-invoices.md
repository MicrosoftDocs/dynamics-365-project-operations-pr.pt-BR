---
title: Visão geral do processamento de faturamento
description: Este tópico fornece uma visão geral processual de como faturar no Project Operations para cenários baseados em recursos/não estocados.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369002"
---
# <a name="invoicing-process-overview"></a>Visão geral do processamento de faturamento

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

O Project Operations para cenários baseados em recursos/não estocados oferece recursos abrangentes personalizados para atender às necessidades do gerente de projetos e do administrador de contas a receber/contador do projeto. Para o processo de faturamento, o gerente de projeto gerencia a carteira de cobrança do projeto e o administrador de contas a receber/contador do projeto cria um documento de fatura compatível e preciso voltado para o cliente.

![Diagrama do fluxo de faturamento](./media/invoicing-flow.png)

A linha de contrato do projeto define o método de cobrança para as transações de projeto associadas. Quando o gerente de projeto aprova transações de tempo e despesas, o sistema registra as transações na entidade **Dados reais do projeto** e envia as informações para o módulo do **Gerenciamento e contabilidade de projetos** no Dynamics 365 Finance. O contador do projeto então revisa e publica os registros usando o [Diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md). Esse diário inclui detalhes contábeis importantes para dados reais do projeto, como cobrança, grupo de impostos sobre vendas, grupo de impostos sobre vendas de item de cobrança e dimensões financeiras.

O gerente de projeto pode revisar as transações de vendas não faturadas usando o método de faturamento de tempo e material no [Lista de pendências de cobrança de tempo e material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) e cobrança de preço fixo em [Marcos de preço fixo](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Essas exibições permitem que você filtre e selecione as transações que precisam ser incluídas no próximo ciclo de cobrança e, em seguida, marque-as como **Pronto para faturar**.

Você pode [criar manualmente uma fatura pro forma](../proforma-invoicing/create-manual-proforma-invoice.md) ou usar um [processo periódico](../proforma-invoicing/configure-automated-invoice-creation.md). O gerente de projeto pode [ajustar um rascunho de fatura pro forma](../proforma-invoicing/manage-proforma-invoice.md) conforme necessário e, em seguida, confirmá-lo.

A fatura pro forma confirmada é enviada para o módulo **Gerenciamento e contabilidade de projetos** no Finance. O contador do projeto formata e atualiza a proposta de fatura do projeto e então posta e imprime o documento. As faturas de projeto lançadas são registradas na Contabilidade, bem como nos razões auxiliares do Cliente e do Projeto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]