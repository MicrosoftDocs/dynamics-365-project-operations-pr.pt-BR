---
title: Gerenciamento de subcontratos no Project Operations
description: Este tópico fornece uma visão geral do processo de gerenciamento de subcontratos de ponta a ponta no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994217"
---
# <a name="subcontract-management-in-project-operations"></a>Gerenciamento de subcontratos no Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

A subcontratação no Microsoft Dynamics 365 Project Operations suporta o fluxo do processo empresarial a seguir.

![Fluxo do processo de subcontratação](../media/SubcontractingProcessFlow.png)

Aqui está uma descrição passo a passo do processo de subcontratação.

1. O gerente de projeto cria um subcontrato com um fornecedor. Por padrão, as listas de preços anexadas ao registro do fornecedor são usadas para o subcontrato. A conta do fornecedor tem um tipo de relacionamento de **Fornecedor** ou **Provedor**.
2. O gerente de projeto pode discriminar todas as compras como itens de linha no subcontrato. As linhas do subcontrato podem ser por tempo, despesas ou produtos. A classe de transação selecionada em cada linha de subcontrato determina para que serve a linha.
3. O gerente de conta do fornecedor e o gerente de projeto podem iterar no subcontrato. O preço pode ser ajustado nas listas de preços de compra que são anexadas ao subcontrato.
4. Nesse ponto ou posteriormente no processo, se a linha do subcontrato for para tempo, o gerente de conta do fornecedor associa os contatos a cada linha do subcontrato. Essa associação fornece informações ao gerente de projeto que está trabalhando no subcontrato. Quando um contato é associado a uma linha do subcontrato, o sistema cria automaticamente um recurso reservável direto do contato, se um recurso reservável ainda não existir.
5. O método de faturamento em cada linha do subcontrato pode ser **Preço fixo** ou **Tempo e Material**. Para linhas do subcontrato de preço fixo, você pode configurar uma programação de faturamento com base em marco.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
