---
title: Transições de estado em uma fatura de fornecedor
description: Este tópico explica as transições de estado em uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584674"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transições de estado em uma fatura de fornecedor

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este tópico explica as transições de estado em uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations. Os seguintes estados são usados: **Rascunho**, **Em revisão**, **Confirmado**, **Em espera** e **Cancelado**.

As ilustrações a seguir mostram as transições de estado.

![Modelo de transição de estado de subcontrato.](../media/VI_State_Model.jpg)

A tabela a seguir explica o que cada estado representa no ciclo de vida de uma fatura de fornecedor no Project Operations.

| State | Description | Transições permitidas |
| --- | --- | --- |
| Rascunho | Este é o estado inicial de uma fatura de fornecedor. As linhas e os preços estão sujeitos a modificações. É possível editar e excluir uma fatura de fornecedor com este status. | Em processamento |
| Em revisão | Este estado representa o estado de processamento de uma fatura de fornecedor. Pelo menos uma linha da fatura de fornecedor tem um status de verificação **Em andamento**. | Confirmado, Em espera |
| Confirmado | Este estado representa o estágio de uma fatura de fornecedor em que o aplicativo criou dados reais de custo para cada linha da fatura de fornecedor. Todos os dados reais de custo vinculados que correspondem às linhas da fatura de fornecedor foram revertidos e substituídos pelos dados reais de custo dessas linhas da fatura de fornecedor. Não é possível editar ou excluir uma fatura de fornecedor com este status. Você pode usar o botão **Cancelar** para cancelar uma fatura de fornecedor confirmada. A ação Cancelar reverte o impacto da ação Confirmar. | Cancelado(a) |
| Em espera | <p>Este estado representa um estágio de uma fatura de fornecedor em que a fatura de fornecedor não pode ser movida devido a um problema com a fatura ou o status do fornecedor. Não é possível confirmar, cancelar, editar ou excluir uma fatura de fornecedor com este estado.</p><p>Você pode usar a ação Reabrir para mover a fatura de fornecedor para o estado **Rascunho** ou **Em revisão**. Se pelo menos uma linha na fatura de fornecedor tiver um status de verificação **Em andamento** ou **Concluído**, a fatura de fornecedor será reaberta no estado **Em revisão**. Se todas as linhas na fatura de fornecedor tiverem um status de verificação **Não iniciado**, a fatura de fornecedor será reaberta no estado **Rascunho**.</p> | Rascunho, Em revisão |
| Cancelado(a) | Este estado representa o estágio de um subcontrato em que a entrega real de materiais e/ou trabalho por recursos subcontratados não é mais necessária. Um subcontrato nesse estado não pode ser usado para estimar e definir os requisitos de recursos e materiais do projeto e também não pode ser referenciado em horas, despesas e uso de material em um projeto. Um subcontrato nesse estado não pode ser editado ou excluído. | Nenhum |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
