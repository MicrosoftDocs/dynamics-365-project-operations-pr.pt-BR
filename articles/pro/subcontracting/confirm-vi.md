---
title: Confirmar uma fatura de fornecedor do projeto
description: Este tópico explica como confirmar uma fatura de fornecedor do projeto no Microsoft Dynamics 365 Project Operations e o impacto financeiro dessa confirmação.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595714"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmar uma fatura de fornecedor do projeto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Depois de verificar todas as linhas de uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations, você pode usar a ação Confirmar para confirmar a fatura.

Quando você seleciona **Confirmar** em uma fatura de fornecedor, ocorre o seguinte:

1. O estado da fatura de fornecedor é atualizado para **Confirmada**.
2. A fatura de fornecedor confirmada e os registros relacionados tornam-se somente leitura e não podem ser editados ou excluídos.
3. Se algum dado real de custo fizer referência à linha da fatura de fornecedor como parte do processo de conciliação, todos os dados reais de custo associados à linha serão revertidos.
4. Novos dados reais de custo são criados usando as informações na linha da fatura de fornecedor.
5. Depois que a fatura de fornecedor for confirmada, você não poderá mais criar diários de correção, processar recuperações de entradas de hora ou cancelar a aprovação dos dados reais originais de horas, despesas ou material que foram revertidos.

> [!NOTE]
> Se alguma linha de uma fatura de fornecedor tiver um status de verificação diferente de **Concluída**, a fatura do fornecedor não poderá ser confirmada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
