---
title: Transições de estado em um subcontrato
description: Este artigo explica as transições de estado em um subcontrato no Microsoft Dynamics 365 Project Operations conforme o subcontrato é criado, executado e fechado.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522874"
---
# <a name="state-transitions-on-a-subcontract"></a>Transições de estado em um subcontrato 

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

Este artigo explica as transições de estado em um subcontrato no Microsoft Dynamics 365 Project Operations. Cada estado é representado como rascunho, confirmado, fechado ou cancelado. A imagem a seguir representa as transições de estado.

![Modelo de estado de subcontrato](../media/SubconStates.png)  

A tabela a seguir fornece uma descrição do que cada estado representa no ciclo de vida de um subcontrato no Project Operations.

| State | Description | Transições permitidas |
| --- | --- | --- |
| Rascunho | Isso representa o estado inicial de um subcontrato. As negociações com o fornecedor estão em andamento. As linhas e preços estão sujeitos a modificações. Um subcontrato nesse estado pode ser usado para estimar e definir os requisitos de recursos e materiais do projeto. Também pode ser referenciado em tempo, despesas e uso de material em um projeto. Um subcontrato nesse estado pode ser editado e excluído. | Confirmado |
| Confirmado | Isso representa o estágio de um subcontrato após a conclusão das negociações com o fornecedor sobre preços e itens de linha que estão sendo adquiridos. Contudo, a entrega real de materiais e/ou trabalho por recursos subcontratados ainda está em andamento. Um subcontrato nesse estado pode ser usado para estimar e definir os requisitos de recursos e materiais do projeto. Também pode ser referenciado em tempo, despesas e uso de material em um projeto. Um subcontrato nesse estado não pode ser editado ou excluído. O botão **Cancelar** permite cancelar um subcontrato confirmado. O botão **Reabrir** permite que você reabra o subcontrato para trazê-lo de volta ao status **Rascunho**. Use o botão **Fechar** para fechar um subcontrato confirmado. | Closed <br> Cancelado(a) <br> Rascunho |
| Closed | Isso representa o estágio de um subcontrato quando a entrega real de materiais e/ou trabalho por recursos subcontratados é concluída. Um subcontrato nesse estado não pode mais ser usado para estimar e dimensionar os requisitos de recursos e materiais do projeto. Além disso, ele não pode mais ser referenciado em tempo, despesa e uso de material em um projeto. Um subcontrato nesse estado não pode ser editado ou excluído. | None |
| Cancelado(a) | Isso representa o estágio de um subcontrato quando a entrega real de materiais e/ou trabalho por recursos subcontratados não é mais necessária. Um subcontrato nesse estado não pode ser usado para estimar e definir os requisitos de recursos e materiais do projeto, nem pode ser referenciado em tempo, despesas e uso de material em um projeto. Um subcontrato nesse estado não pode ser editado ou excluído. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
