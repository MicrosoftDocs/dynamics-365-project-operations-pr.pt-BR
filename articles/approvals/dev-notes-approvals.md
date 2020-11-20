---
title: Notas do desenvolvedor para Aprovações
description: Este tópico fornece informações adicionais do desenvolvedor sobre como trabalhar com aprovações.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483934"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="54364-103">Notas do desenvolvedor para Aprovações</span><span class="sxs-lookup"><span data-stu-id="54364-103">Developer notes for Approvals</span></span>

<span data-ttu-id="54364-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="54364-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="54364-105">O Dynamics 365 Project Operations inclui lógica de validação que garante a transição correta do registro através dos estágios de aprovação.</span><span class="sxs-lookup"><span data-stu-id="54364-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="54364-106">As transições de registro corretas garantem que:</span><span class="sxs-lookup"><span data-stu-id="54364-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="54364-107">Todas as linhas de suporte são criadas em tabelas relacionadas, como diários e dados reais.</span><span class="sxs-lookup"><span data-stu-id="54364-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="54364-108">O aprovador é marcado como um **Aprovador de Projeto** no projeto, antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="54364-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
