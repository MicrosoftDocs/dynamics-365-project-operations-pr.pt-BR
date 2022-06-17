---
title: Visão geral de faturamento intercompanhia
description: Este artigo fornece informações e exemplos sobre o faturamento intercompanhia de projetos.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913560"
---
# <a name="intercompany-invoicing-overview"></a>Visão geral de faturamento intercompanhia

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Sua organização pode ter várias divisões, subsidiárias e outras entidades legais que transferem produtos e serviços de outros projetos entre si. A entidade legal que fornece o serviço ou produto é chamada de *entidade legal que faz o empréstimo*. A entidade legal que recebe o serviço ou produto é chamada de *entidade legal que toma o empréstimo*.

A ilustração a seguir mostra um cenário típico em que duas entidades legais, a Contoso Robotics USA (a entidade legal que toma o empréstimo) e a Contoso Robotics UK (a entidade legal que faz o empréstimo) compartilham recursos para entregar um projeto para o cliente, a Adventure works. Neste cenário, a Contoso Robotics USA é contratada para entregar o trabalho à Adventure Works.

![Faturamento intercompanhia.](./media/IntercompanyScenario.png) 

O Dynamics 365 Project Operations usa o seguinte fluxo para processar transações intercompanhia:

1. Os recursos da entidade legal que faz o empréstimo registram as transações de horas ou de despesas intercompanhia reservando tempo e despesas em relação aos projetos na entidade legal que toma o empréstimo.
2. Os custos de tempo e despesas são registrados na empresa que faz o empréstimo usando a lista de preços de custo da unidade da empresa que toma o empréstimo.
3. As transações intercompanhia de venda não cobradas são registradas na empresa que faz o empréstimo usando a lista de preços de custo da unidade da empresa que toma o empréstimo.
4. A receita não cobrada é registrada na empresa que toma o empréstimo usando a lista de preços de venda do contrato do projeto. O cliente poderá ser cobrado quando a receita não cobrada for registrada. O cliente não precisa esperar até que o processamento da fatura intercompanhia seja concluído.
5. As faturas intercompanhia de clientes são criadas periodicamente na empresa que faz o empréstimo. As faturas são criadas manualmente ou usando um processo periódico automatizado. Uma única fatura pode ser criada para cada entidade legal que toma o empréstimo ou podem ser criadas faturas separadas por projeto.
6. Quando a fatura intercompanhia do cliente é lançada na entidade legal que faz o empréstimo, a fatura de fornecedor pendente correspondente é criada na entidade legal que toma o empréstimo. Os custos na fatura de fornecedor pendente serão registrados no razão auxiliar do projeto quando a fatura for lançada.

O diagrama a seguir ilustra o faturamento intercompanhia no que se refere a eventos contábeis e lançamentos esperados na contabilidade.

![Fluxo intercompanhia.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Recursos adicionais

- [Configurar faturamento intercompanhia](configure-intercompany-invoicing.md)
- [Registrar transações intercompanhia](create-intercompany-transactions.md)
- [Criar faturas intercompanhia de clientes e fornecedores](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]