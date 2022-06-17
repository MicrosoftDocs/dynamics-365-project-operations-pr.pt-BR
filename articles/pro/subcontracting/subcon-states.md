---
title: Transições de estado em um subcontrato
description: Este artigo explica as transições de estado em um subcontrato no Microsoft Dynamics 365 Project Operations conforme o subcontrato é criado, executado e fechado.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919724"
---
# <a name="state-transitions-on-a-subcontract"></a>Transições de estado em um subcontrato 

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

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
