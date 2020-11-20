---
title: Criar uma fatura pro forma manual - lite
description: Este tópico fornece informações sobre como criar uma fatura pro forma manual no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176372"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="5cd48-103">Criar uma fatura pro forma manual - lite</span><span class="sxs-lookup"><span data-stu-id="5cd48-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="5cd48-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="5cd48-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5cd48-105">No Dynamics 365 Project Operations, as faturas pro forma podem ser criadas manualmente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="5cd48-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="5cd48-106">Você pode criar manualmente uma fatura pro forma da página de listagem **Contratos de Projeto** ou da página de detalhes **Contrato de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="5cd48-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="5cd48-107">Página de listagem Contratos de Projeto</span><span class="sxs-lookup"><span data-stu-id="5cd48-107">Project Contracts list page</span></span>

<span data-ttu-id="5cd48-108">Na página de listagem **Contratos de Projeto**, selecione um ou mais contratos de projeto e crie faturas para todos os registros selecionados.</span><span class="sxs-lookup"><span data-stu-id="5cd48-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="5cd48-109">O sistema verifica qual dos contratos de projeto selecionados tem uma lista de pendências **Pronto para Faturar** anterior à data de hoje.</span><span class="sxs-lookup"><span data-stu-id="5cd48-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="5cd48-110">Desses contratos, o sistema cria rascunhos de faturas pro forma.</span><span class="sxs-lookup"><span data-stu-id="5cd48-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="5cd48-111">Se um contrato de projeto tiver vários clientes, poderá haver uma fatura criada por cliente e várias faturas por contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="5cd48-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="5cd48-112">Todas as faturas de projeto criadas estão disponíveis na página **Fatura**, na seção **Cobrança** da área **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="5cd48-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="5cd48-113">Página de detalhes Contrato de Projeto</span><span class="sxs-lookup"><span data-stu-id="5cd48-113">Project Contract details page</span></span>

<span data-ttu-id="5cd48-114">Uma fatura pro forma também pode ser criada da página **Contrato de Projeto**, que cria a fatura para aquele contrato de projeto específico.</span><span class="sxs-lookup"><span data-stu-id="5cd48-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="5cd48-115">O sistema verifica que o contrato de projeto tem uma lista de pendências **Pronto para Faturar** anterior à data de hoje.</span><span class="sxs-lookup"><span data-stu-id="5cd48-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="5cd48-116">A partir desses contratos, o sistema cria rascunhos de faturas pro forma com base no número de clientes em cada linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="5cd48-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="5cd48-117">Quando há uma única fatura pro forma criada, a página **Fatura** é aberta.</span><span class="sxs-lookup"><span data-stu-id="5cd48-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="5cd48-118">Se houver várias faturas criadas para esse contrato de projeto, então a página de listagem **Faturas** é aberta para mostrar todas as faturas criadas.</span><span class="sxs-lookup"><span data-stu-id="5cd48-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
