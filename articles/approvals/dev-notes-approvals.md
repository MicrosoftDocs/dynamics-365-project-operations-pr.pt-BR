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
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290255"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="5a77b-103">Notas do desenvolvedor para Aprovações</span><span class="sxs-lookup"><span data-stu-id="5a77b-103">Developer notes for Approvals</span></span>

<span data-ttu-id="5a77b-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="5a77b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5a77b-105">O Dynamics 365 Project Operations inclui lógica de validação que garante a transição correta do registro através dos estágios de aprovação.</span><span class="sxs-lookup"><span data-stu-id="5a77b-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="5a77b-106">As transições de registro corretas garantem que:</span><span class="sxs-lookup"><span data-stu-id="5a77b-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="5a77b-107">Todas as linhas de suporte são criadas em tabelas relacionadas, como diários e dados reais.</span><span class="sxs-lookup"><span data-stu-id="5a77b-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="5a77b-108">O aprovador é marcado como um **Aprovador de Projeto** no projeto, antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="5a77b-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]