---
title: Visão geral de despesa
description: Este tópico inclui informações sobre a funcionalidade Despesa no Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6c5ef2a45e8141bda38baf3eaf0a403d6db95e48
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122807"
---
# <a name="expense-home-page"></a><span data-ttu-id="6b20c-103">Home page de despesas</span><span class="sxs-lookup"><span data-stu-id="6b20c-103">Expense home page</span></span>

<span data-ttu-id="6b20c-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="6b20c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6b20c-105">O Dynamics 365 Project Operations oferece suporte à capacidade de processar despesas.</span><span class="sxs-lookup"><span data-stu-id="6b20c-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="6b20c-106">O processamento de despesas com ou sem projetos usando um fluxo de trabalho personalizável de políticas, categorias de transação e aprovações.</span><span class="sxs-lookup"><span data-stu-id="6b20c-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="6b20c-107">Em Project Operations, há dois modelos de implantação compatíveis com Despesa:</span><span class="sxs-lookup"><span data-stu-id="6b20c-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="6b20c-108">**Completa**: a implantação completa está disponível para **cenários baseados em recursos/sem estoque do Project Operations** ou **cenários baseados em ordem de produção do Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="6b20c-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="6b20c-109">**Básico**: a implantação básica está disponível para **cenários baseados em recursos/sem estoque do Project Operations** e **Implantação lite - gerenciar faturamento pro forma**.</span><span class="sxs-lookup"><span data-stu-id="6b20c-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="6b20c-110">Completo</span><span class="sxs-lookup"><span data-stu-id="6b20c-110">Full</span></span> 
<span data-ttu-id="6b20c-111">A implantação completa de Despesa fornece uma aplicação de política completa que inclui a capacidade de criar políticas, como:</span><span class="sxs-lookup"><span data-stu-id="6b20c-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="6b20c-112">Limites de categoria de despesa</span><span class="sxs-lookup"><span data-stu-id="6b20c-112">Expense category limits</span></span>
  - <span data-ttu-id="6b20c-113">Viagem</span><span class="sxs-lookup"><span data-stu-id="6b20c-113">Travel</span></span>
  - <span data-ttu-id="6b20c-114">Diária</span><span class="sxs-lookup"><span data-stu-id="6b20c-114">Per diem</span></span>
  - <span data-ttu-id="6b20c-115">Importações de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="6b20c-115">Credit card imports</span></span>
  - <span data-ttu-id="6b20c-116">Reconhecimento ótico de caracteres do recibo</span><span class="sxs-lookup"><span data-stu-id="6b20c-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="6b20c-117">Básico</span><span class="sxs-lookup"><span data-stu-id="6b20c-117">Basic</span></span> 
<span data-ttu-id="6b20c-118">O cenário de implantação básica de Despesa permite apenas registrar as despesas básicas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="6b20c-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="6b20c-119">Para obter mais informações, consulte [Entrada de despesa (lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="6b20c-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="6b20c-120">Determinar a implantação de Despesa</span><span class="sxs-lookup"><span data-stu-id="6b20c-120">Determine your Expense deployment</span></span>
<span data-ttu-id="6b20c-121">Para determinar se você está executando a implantação de gerenciamento de Despesa básica, verifique se a URL do endereço termina com **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="6b20c-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
