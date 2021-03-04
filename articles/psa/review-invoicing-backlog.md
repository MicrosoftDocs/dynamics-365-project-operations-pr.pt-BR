---
title: Verificar a lista de pendências de faturamento em projetos e contratos de projetos
description: Esse tópico oferece informações sobre como revisar listas de pendências de horas, despesas e produtos, além de marcá-las como prontas para faturamento.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150474"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Verificar a lista de pendências de faturamento em projetos e contratos de projetos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Quando uma transação estiver pronta para ter uma fatura criada e processada, a transação deve ser marcada como **Pronta para faturamento**. Esse tópico descreve os tipos de transações que podem ser criadas.

## <a name="review-the-time-and-material-billing-backlog"></a>Verificar a lista de pendências de cobrança de hora e material

Quando uma entrada de hora e despesa for enviada e aprovada para um projeto, o PSA criará um projeto real. Se a combinação do projeto e a classe de transação forem mapeadas para uma linha de contrato de um projeto de tempo e materiais, dois valores reais serão criados quando a entrada for aprovada:

- Custo real 
- Valores reais de vendas não cobrados

Os valores de vendas não cobrados representam a lista de pendências de cobranças e o status da cobrança deve ser definido como **Pronto para faturar**. Quando uma fatura de projeto é criada, os valores reais de vendas não cobrados marcados como **Pronto para faturar** são copiados como detalhes das linhas de faturamento.

Para verificar a lista de pendências de cobranças de hora e materiais, vá para **Vendas** \> **Cobrança** \> **Lista de pendências de cobrança de hora e materiais**. Selecione todos os valores reais de vendas não cobrados que estão prontos para serem faturados e, em seguida, selecione **Pronto para faturar**. O status de cobrança desses valores reais é alterado para **Pronto para faturar**.

![Lista de pendências de cobrança de hora e materiais](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Revisar a lista de pendências de cobrança do produto

No PSA, quando um contrato de projeto tem linhas de contrato baseadas no produto, essas linhas são consideradas para faturamento sempre que uma fatura for criada para o contrato do projeto. Todos os produtos com linhas de contrato marcadas como **Pronto para faturar** são copiados para a fatura do projeto como linhas de faturamento do projeto.

Para analisar a lista de pendências de cobrança dos produtos, vá para **Vendas** \> **Cobrança** \> **Lista de pendências de cobrança do produto**. Selecione todas as linhas de contrato baseadas no produto que estão prontas para serem faturadas e, em seguida, selecione **Pronto para faturar**. O status de cobrança dessas linhas é alterado para **Pronto para faturar**.

![Lista de pendências de cobrança do produto](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Revisar as etapas de cobrança em contratos de preço fixo

Todas as linhas de contrato do projeto com um método de cobrança de preço fixo devem definir as etapas do contrato. Essas etapas do contrato podem ser faturadas somente se estiverem marcadas como **Pronto para faturar**. 

Para revisar as etapas de cobrança, vá para **Vendas** \> **Cobrança** \> **Etapas com preço fixo**. Selecione as etapas prontas para faturamento e, em seguida, selecione **Pronto para faturar**. O status de cobrança dessas etapas foi alterado para **Pronto para faturar**.

![Etapas de preço fixo](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]