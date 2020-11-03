---
title: Confirmar um contrato de projeto
description: Este tópico fornece informações sobre como confirmar um contrato no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071548"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="e31b7-103">Confirmar um contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="e31b7-103">Confirm a project contract</span></span>

<span data-ttu-id="e31b7-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="e31b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e31b7-105">Um contrato de projeto no Dynamics 365 Project Operations pode estar ativo com um motivo **Confirmado** ou fechado com um motivo **Perdido**.</span><span class="sxs-lookup"><span data-stu-id="e31b7-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed** , or closed with a reason of **Lost**.</span></span> <span data-ttu-id="e31b7-106">Quando você confirma um contrato de projeto, o status é atualizado de **Rascunho** para **Ativo** e a razão do status é **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="e31b7-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="e31b7-107">Um contrato ativo ou fechado não pode ser editado ou reaberto.</span><span class="sxs-lookup"><span data-stu-id="e31b7-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="e31b7-108">Impacto financeiro da confirmação de um contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="e31b7-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="e31b7-109">Após a confirmação de um contrato de projeto, o aplicativo recalculará os custos estornando os custos reais mais antigos e recriando os novos custos reais.</span><span class="sxs-lookup"><span data-stu-id="e31b7-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="e31b7-110">Os novos custos reais são então processados com base no método de cobrança da linha de contrato de projeto associada.</span><span class="sxs-lookup"><span data-stu-id="e31b7-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="e31b7-111">Se os valores reais de custo fizerem referência a uma linha de contrato por Tempo e Material, o aplicativo recriará automaticamente os valores reais de vendas não cobradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="e31b7-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="e31b7-112">Se os custos reais fizerem referência a uma linha de contrato de Preço Fixo, o aplicativo interromperá o reprocessamento dos custos reais.</span><span class="sxs-lookup"><span data-stu-id="e31b7-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="e31b7-113">Limites que não devem ser excedidos, configuração de encargos e preços e custos sobre os reais são avaliados e atualizados como parte do processo de confirmações.</span><span class="sxs-lookup"><span data-stu-id="e31b7-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="e31b7-114">Fechar um contrato de projeto como perdido</span><span class="sxs-lookup"><span data-stu-id="e31b7-114">Close a project contract as lost</span></span>

<span data-ttu-id="e31b7-115">Quando você fecha um contrato de projeto como perdido, o status do contrato é atualizado para **Fechado** e a razão do status é **Perdido**.</span><span class="sxs-lookup"><span data-stu-id="e31b7-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="e31b7-116">O contrato do projeto torna-se somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e31b7-116">The project contract becomes read-only.</span></span> <span data-ttu-id="e31b7-117">Um diálogo de confirmação é fornecido antes que as alterações sejam concluídas porque você não pode reabrir um contrato de projeto fechado.</span><span class="sxs-lookup"><span data-stu-id="e31b7-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="e31b7-118">Se o contrato de projeto fechado como perdido fizer referência a um projeto em suas linhas, esse projeto também será marcado como fechado.</span><span class="sxs-lookup"><span data-stu-id="e31b7-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="e31b7-119">Todas as reservas de recursos desse dia em diante serão canceladas.</span><span class="sxs-lookup"><span data-stu-id="e31b7-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="e31b7-120">Quaisquer vendas não cobradas reais no contrato de projeto que ainda não estejam em uma fatura serão estornadas.</span><span class="sxs-lookup"><span data-stu-id="e31b7-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="e31b7-121">No Dynamics 365 Project Operations, fechar um contrato de projeto como perdido não afetará o status da oportunidade associada.</span><span class="sxs-lookup"><span data-stu-id="e31b7-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="e31b7-122">A oportunidade permanecerá aberta e deverá ser fechada manualmente.</span><span class="sxs-lookup"><span data-stu-id="e31b7-122">The opportunity will remain open and must be manually closed.</span></span>
