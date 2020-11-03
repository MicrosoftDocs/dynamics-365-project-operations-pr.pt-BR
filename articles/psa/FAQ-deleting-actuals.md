---
title: Por que não posso excluir registros da entidade de dados reais?
description: Este tópico fornece informações sobre por que não é possível excluir registros da entidade de dados reais.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071554"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="29818-103">Por que não posso excluir registros da entidade Dados Reais?</span><span class="sxs-lookup"><span data-stu-id="29818-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="29818-104">O PSA (Project Service Automation) não permite excluir dados reais porque eles atuam como a fonte da verdade em transações que têm implicações financeiras para sistemas downstream, como a contabilidade.</span><span class="sxs-lookup"><span data-stu-id="29818-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="29818-105">Se os dados reais pudessem ser excluídos, a integridade das transações do relatório financeiro poderia ser duvidosa.</span><span class="sxs-lookup"><span data-stu-id="29818-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="29818-106">Para estabelecer uma trilha de auditoria, os clientes devem usar diários para criar transações de compensação.</span><span class="sxs-lookup"><span data-stu-id="29818-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

