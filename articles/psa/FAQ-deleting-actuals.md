---
title: Por que não posso excluir registros da entidade de dados reais?
description: Este artigo fornece informações sobre por que não é possível excluir registros da entidade de dados reais.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925566"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Por que não posso excluir registros da entidade Dados Reais?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O PSA (Project Service Automation) não permite excluir dados reais porque eles atuam como a fonte da verdade em transações que têm implicações financeiras para sistemas downstream, como a contabilidade. Se os dados reais pudessem ser excluídos, a integridade das transações do relatório financeiro poderia ser duvidosa. Para estabelecer uma trilha de auditoria, os clientes devem usar diários para criar transações de compensação.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
