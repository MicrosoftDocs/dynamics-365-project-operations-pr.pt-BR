---
title: Fechar uma cotação – lite
description: Este tópico fornece informações sobre como fechar uma cotação no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764850"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="daab4-103">Fechar uma cotação – lite</span><span class="sxs-lookup"><span data-stu-id="daab4-103">Close a quote - lite</span></span>

<span data-ttu-id="daab4-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="daab4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="daab4-105">Uma cotação de projeto pode ser fechada como Ganha ou Perdida.</span><span class="sxs-lookup"><span data-stu-id="daab4-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="daab4-106">Um rascunho de cotação pode ser fechado porque as operações Ativar e Revisar nas cotações não são compatíveis com o Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="daab4-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="daab4-107">Fechar uma cotação como Ganha</span><span class="sxs-lookup"><span data-stu-id="daab4-107">Close a quote as Won</span></span>

<span data-ttu-id="daab4-108">Quando você fecha uma cotação de projeto como Vencida, o status é definido como Fechado e a razão do status é Vencida.</span><span class="sxs-lookup"><span data-stu-id="daab4-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="daab4-109">Fechar a cotação torna a cotação do projeto somente leitura e cria um contrato do projeto de rascunho que contém as informações da cotação.</span><span class="sxs-lookup"><span data-stu-id="daab4-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="daab4-110">Como uma cotação fechada não pode ser reaberta, uma caixa de diálogo de confirmação confirmará suas alterações.</span><span class="sxs-lookup"><span data-stu-id="daab4-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="daab4-111">Se a cotação for anexada a uma oportunidade, todas as outras cotações de projeto na oportunidade serão automaticamente fechadas como Perdidas.</span><span class="sxs-lookup"><span data-stu-id="daab4-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="daab4-112">Impacto financeiro de fechar uma cotação como Ganha</span><span class="sxs-lookup"><span data-stu-id="daab4-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="daab4-113">Se houver algum valor real para o tempo em um projeto enquanto ele ainda está vinculado a uma cotação preliminar, apenas o custo do tempo ou despesa é registrado.</span><span class="sxs-lookup"><span data-stu-id="daab4-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="daab4-114">Depois que uma cotação for fechada como Ganha, o aplicativo vai refatorar os custos revertendo os custos reais mais antigos e recriando os novos custos reais.</span><span class="sxs-lookup"><span data-stu-id="daab4-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="daab4-115">O aplicativo processará esses custos reais com base no Método de cobrança da linha de contrato associada do projeto.</span><span class="sxs-lookup"><span data-stu-id="daab4-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="daab4-116">Se os custos reais fizerem referência a uma linha de contrato de tempo e material, os valores reais de vendas não faturados correspondentes serão criados para quando a cotação for fechada e o contrato de projeto criado.</span><span class="sxs-lookup"><span data-stu-id="daab4-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="daab4-117">Se os custos reais fizerem referência a uma linha de contrato de preço fixo, o aplicativo irá parar de reprocessar os custos reais que são baseados nas regras de faturamento dividido para os clientes do contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="daab4-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="daab4-118">Fechando uma cotação como perdida:</span><span class="sxs-lookup"><span data-stu-id="daab4-118">Closing a quote as lost:</span></span>

<span data-ttu-id="daab4-119">Quando você fecha uma cotação de projeto como Perdida, o status é definido como Fechado e a razão do status é Perdida.</span><span class="sxs-lookup"><span data-stu-id="daab4-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="daab4-120">Fechar a cotação torna a cotação do projeto somente leitura.</span><span class="sxs-lookup"><span data-stu-id="daab4-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="daab4-121">Como uma cotação fechada não pode ser reaberta e antes de fechar uma cotação, uma caixa de diálogo de confirmação confirmará suas alterações.</span><span class="sxs-lookup"><span data-stu-id="daab4-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="daab4-122">Se a cotação de projeto fechada como Perdida fizer referência a um projeto em qualquer uma de suas linhas, esse projeto também será marcado como Fechado.</span><span class="sxs-lookup"><span data-stu-id="daab4-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="daab4-123">Todas as reservas de recursos desse dia em diante serão canceladas.</span><span class="sxs-lookup"><span data-stu-id="daab4-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="daab4-124">No Project Operations, fechar uma cotação como Ganha ou Perdida não afetará o status da Oportunidade, que permanecerá aberta até que seja fechada manualmente.</span><span class="sxs-lookup"><span data-stu-id="daab4-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
