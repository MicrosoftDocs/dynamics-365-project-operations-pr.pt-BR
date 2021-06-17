---
title: Notas do desenvolvedor para Aprovações
description: Este tópico fornece informações adicionais do desenvolvedor sobre como trabalhar com aprovações.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996777"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="a5f15-103">Notas do desenvolvedor para Aprovações</span><span class="sxs-lookup"><span data-stu-id="a5f15-103">Developer notes for Approvals</span></span>

<span data-ttu-id="a5f15-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="a5f15-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a5f15-105">O Dynamics 365 Project Operations inclui lógica de validação que garante a transição correta do registro através dos estágios de aprovação.</span><span class="sxs-lookup"><span data-stu-id="a5f15-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="a5f15-106">As transições de registro corretas garantem que:</span><span class="sxs-lookup"><span data-stu-id="a5f15-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="a5f15-107">Todas as linhas de suporte são criadas em tabelas relacionadas, como diários e dados reais.</span><span class="sxs-lookup"><span data-stu-id="a5f15-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="a5f15-108">O aprovador é marcado como um **Aprovador de Projeto** no projeto, antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="a5f15-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]