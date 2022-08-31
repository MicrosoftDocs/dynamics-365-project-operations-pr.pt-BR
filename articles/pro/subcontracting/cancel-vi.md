---
title: Cancelar uma fatura de fornecedor do projeto
description: Este artigo explica como cancelar uma fatura de fornecedor do projeto no Microsoft Dynamics 365 Project Operations e o impacto financeiro desse cancelamento.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261076"
---
# <a name="cancel-a-project-vendor-invoice"></a>Cancelar uma fatura de fornecedor do projeto

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Depois que uma fatura de fornecedor é confirmada, não é possível editá-la ou excluí-la. Se houver um erro em uma fatura de fornecedor confirmada, você poderá usar a ação Cancelar para reverter o impacto da fatura de fornecedor e criar uma nova.

Quando você seleciona **Cancelar** em uma fatura de fornecedor, ocorre o seguinte:

1. O estado da fatura de fornecedor é atualizado para **Cancelada**.
2. A fatura de fornecedor cancelada e os registros relacionados tornam-se somente leitura e não podem ser editados ou excluídos.
3. Todos os dados reais de custo que foram criados com base nas linhas da fatura de fornecedor como parte da confirmação dela são revertidos.
4. Se algum dado real de custo foi vinculado às linhas da fatura de fornecedor como parte do processo de conciliação, ele foi revertido pela confirmação da fatura de fornecedor original. Durante o cancelamento da fatura de fornecedor, esses dados reais de custo são recriados. As origens indicam as entradas de hora, despesa ou uso de material.
5. Depois que a fatura de fornecedor for cancelada, você poderá novamente criar diários de correção, processar recuperações de entradas de hora e cancelar a aprovação dos dados reais originais de horas, despesas ou material.

> [!NOTE]
> Somente as faturas de fornecedor do projeto confirmadas podem ser canceladas. Não é possível cancelar faturas de fornecedor em outros estados.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
