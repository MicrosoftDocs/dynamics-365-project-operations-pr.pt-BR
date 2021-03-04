---
title: Por que não posso excluir registros da entidade de dados reais?
description: Este tópico fornece informações sobre por que não é possível excluir registros da entidade de dados reais.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148944"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="9dee5-103">Por que não posso excluir registros da entidade Dados Reais?</span><span class="sxs-lookup"><span data-stu-id="9dee5-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9dee5-104">O PSA (Project Service Automation) não permite excluir dados reais porque eles atuam como a fonte da verdade em transações que têm implicações financeiras para sistemas downstream, como a contabilidade.</span><span class="sxs-lookup"><span data-stu-id="9dee5-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="9dee5-105">Se os dados reais pudessem ser excluídos, a integridade das transações do relatório financeiro poderia ser duvidosa.</span><span class="sxs-lookup"><span data-stu-id="9dee5-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="9dee5-106">Para estabelecer uma trilha de auditoria, os clientes devem usar diários para criar transações de compensação.</span><span class="sxs-lookup"><span data-stu-id="9dee5-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

