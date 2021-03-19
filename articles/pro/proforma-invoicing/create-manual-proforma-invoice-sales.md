---
title: Criar uma fatura pro forma manual - lite
description: Este tópico fornece informações sobre como criar uma fatura pro forma manual no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274174"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="a036f-103">Criar uma fatura pro forma manual - lite</span><span class="sxs-lookup"><span data-stu-id="a036f-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="a036f-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="a036f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a036f-105">No Dynamics 365 Project Operations, é possível criar faturas pró-forma manualmente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="a036f-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="a036f-106">Você pode criar manualmente uma fatura pro forma da página de listagem **Contratos de Projeto** ou da página de detalhes **Contrato de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a036f-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="a036f-107">Página de listagem Contratos de Projeto</span><span class="sxs-lookup"><span data-stu-id="a036f-107">Project Contracts list page</span></span>

<span data-ttu-id="a036f-108">Na página de listagem **Contratos de Projeto**, selecione um ou mais contratos de projeto e crie faturas para todos os registros selecionados.</span><span class="sxs-lookup"><span data-stu-id="a036f-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="a036f-109">O sistema verifica qual dos contratos de projeto selecionados tem uma lista de pendências **Pronto para Faturar** anterior à data de hoje.</span><span class="sxs-lookup"><span data-stu-id="a036f-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="a036f-110">Desses contratos, o sistema cria rascunhos de faturas pro forma.</span><span class="sxs-lookup"><span data-stu-id="a036f-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="a036f-111">Se um contrato de projeto tiver vários clientes, poderá haver uma fatura criada por cliente e várias faturas por contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="a036f-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="a036f-112">Todas as faturas de projeto criadas estão disponíveis na página **Fatura**, na seção **Cobrança** da área **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="a036f-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="a036f-113">Página de detalhes Contrato de Projeto</span><span class="sxs-lookup"><span data-stu-id="a036f-113">Project Contract details page</span></span>

<span data-ttu-id="a036f-114">Também é possível criar uma fatura pro forma na página de detalhes **Contrato de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a036f-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="a036f-115">O sistema verifica o contrato de projeto que tem uma lista de pendências em **Pronto para Faturar** anterior à data de hoje.</span><span class="sxs-lookup"><span data-stu-id="a036f-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="a036f-116">A partir desses contratos, o sistema cria rascunhos de faturas pro forma com base no número de clientes em cada linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="a036f-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="a036f-117">Quando há uma única fatura pro forma criada, a página **Fatura** é aberta.</span><span class="sxs-lookup"><span data-stu-id="a036f-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="a036f-118">Se várias faturas forem criadas para esse contrato de projeto, a página de lista de **Faturas** será aberta para mostrar todas as faturas criadas.</span><span class="sxs-lookup"><span data-stu-id="a036f-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]