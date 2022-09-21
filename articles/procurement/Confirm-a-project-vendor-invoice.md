---
title: Confirmar faturas de fornecedor do projeto
description: Este artigo explica como confirmar uma fatura de fornecedor do projeto no Microsoft Dynamics 365 Project Operations e descreve o impacto financeiro dessa confirmação.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475407"
---
# <a name="confirm-project-vendor-invoices"></a>Confirmar faturas de fornecedor do projeto

_ **Aplicável a:** Project Operations para cenários baseados em recursos/sem estoque

Quando o parâmetro **A confirmação manual por PM é necessária** está habilitado, as faturas de fornecedor criadas no Microsoft Dataverse têm status **Rascunho**. As faturas de fornecedor criadas dessa maneira devem ser revisadas e confirmadas manualmente. Quando o parâmetro **A confirmação manual por PM é necessária** está desabilitado, as faturas do fornecedor criadas no Dataverse serão confirmadas automaticamente. Nenhuma outra ação é necessária. 

Depois de verificar todas as linhas de uma fatura de fornecedor no Dynamics 365 Project Operations, selecione **Confirmar** para confirmar a fatura do fornecedor.

Quando você seleciona **Confirmar** em uma fatura de fornecedor, ocorre o seguinte:

1. O status da fatura de fornecedor é atualizado para **Confirmada**.
1. A fatura de fornecedor confirmada e os registros relacionados tornam-se somente leitura e não podem ser editados ou excluídos.
1. Se algum dado real de custo fizer referência à linha da fatura de fornecedor como parte do processo de conciliação, todos os dados reais de custo associados à linha serão revertidos.
1. Novos dados reais de custo são criados usando as informações na linha da fatura de fornecedor.
1. Você não pode mais criar diários de correção, processar recuperações de entradas de hora ou cancelar a aprovação de horas originais, despesas ou dados reais de material que foram revertidos.
1. No Dynamics 365 Finance, o valor **Custo do projeto** é atualizado usando o diário de integração do projeto e a conta de integração do Procurement é *revertida* após o lançamento do diário de integração do projeto.

> [!NOTE]
> Se alguma linha de uma fatura de fornecedor tiver um status de verificação diferente de **Concluída**, a fatura do fornecedor não poderá ser confirmada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
