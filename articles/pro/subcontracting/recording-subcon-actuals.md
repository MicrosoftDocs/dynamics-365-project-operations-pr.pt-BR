---
title: Registro de tempo, despesas e uso de material para componentes subcontratados
description: Este artigo explica como tempo, despesas e uso de material registrado em projetos de componentes subcontratados são rastreados pelo Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927636"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registro de tempo, despesas e uso de material em projetos para componentes subcontratados

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Este artigo explica como tempo, despesas e uso de material registrado em projetos de componentes subcontratados são rastreados pelo Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Custos do tempo do subcontratado em projetos
No Project Operations, os trabalhadores contratados podem registrar o tempo em projetos de maneira semelhante aos funcionários. Ao inserir o tempo em projetos e/ou tarefas do projeto, um trabalhador contratado pode selecionar um subcontrato e uma linha de subcontrato específicos.

Quando o tempo enviado por trabalhadores contratados é aprovado, o custo do projeto é registrado usando a taxa de custo unitário configurada para esse recurso de trabalhador contratado na seção **Preços da função** da lista de preços de compra no subcontrato.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Custos de despesas subcontratadas em projetos
Ao inserir despesas incorridas em projetos, você pode selecionar um subcontrato e uma linha de subcontrato na entrada de despesas. 

Quando essa entrada de despesa é enviada e aprovada, o custo da despesa é registrado no projeto com base no custo unitário configurado para essa categoria de transação na seção **Preços de categoria** da lista de preços de compra no subcontrato.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Custos de materiais subcontratados em projetos
Ao inserir o uso de material em projetos, você pode selecionar um subcontrato e uma linha de subcontrato no log de uso de material. Quando o registro de uso do material é enviado e aprovado, o custo do material é registrado no projeto com base no custo unitário configurado para esse produto na seção **Itens da lista de preços** da lista de preços do subcontrato.

O uso de material também pode ser registrado para produtos fora do catálogo em projetos. Esse tipo de uso de material também pode ser vinculado a um subcontrato e linha de subcontrato. Ao registrar o uso de material para produtos fora do catálogo, você precisa inserir o custo por unidade do produto fora do catálogo. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
