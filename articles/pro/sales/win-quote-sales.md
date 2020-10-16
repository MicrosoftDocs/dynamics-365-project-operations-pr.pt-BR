---
title: Fechar cotações
description: Este tópico fornece informações sobre como fechar uma cotação no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896177"
---
# <a name="close-quotes"></a><span data-ttu-id="c94cf-103">Fechar cotações</span><span class="sxs-lookup"><span data-stu-id="c94cf-103">Close quotes</span></span> 

<span data-ttu-id="c94cf-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="c94cf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c94cf-105">Uma cotação de projeto pode ser fechada como Ganha ou Perdida.</span><span class="sxs-lookup"><span data-stu-id="c94cf-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="c94cf-106">As operações Ativar e Revisar nas cotações não têm suporte no Microsoft Dynamics 365 Project Operations, portanto, uma cotação de rascunho pode ser fechada.</span><span class="sxs-lookup"><span data-stu-id="c94cf-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="c94cf-107">Fechar uma cotação como Ganha</span><span class="sxs-lookup"><span data-stu-id="c94cf-107">Close a quote as Won</span></span>

<span data-ttu-id="c94cf-108">Fechar uma cotação de projeto como Ganha fechará a cotação com o status definido como Fechada e a razão do status definida como Ganha.</span><span class="sxs-lookup"><span data-stu-id="c94cf-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="c94cf-109">Fechar a cotação torna a cotação do projeto somente leitura e cria um contrato do projeto de rascunho que contém as informações da cotação.</span><span class="sxs-lookup"><span data-stu-id="c94cf-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="c94cf-110">Como uma cotação fechada não pode ser reaberta, será exibida uma caixa de diálogo de confirmação Há uma caixa de diálogo de confirmação antes que as alterações sejam feitas, pois uma cotação fechada não pode ser reaberta e as alterações são irreversíveis.</span><span class="sxs-lookup"><span data-stu-id="c94cf-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="c94cf-111">Se a cotação for anexada a uma oportunidade, todas as outras cotações de projeto na oportunidade serão automaticamente fechadas como Perdidas.</span><span class="sxs-lookup"><span data-stu-id="c94cf-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="c94cf-112">Impacto financeiro de fechar uma cotação como Ganha</span><span class="sxs-lookup"><span data-stu-id="c94cf-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="c94cf-113">Se houver dados reais de horas registradas em um projeto enquanto ele ainda estiver anexado a uma cotação de rascunho, somente o custo do tempo ou da despesa será registrado.</span><span class="sxs-lookup"><span data-stu-id="c94cf-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="c94cf-114">Depois que uma cotação for fechada como Ganha, o aplicativo vai refatorar os custos revertendo os custos reais mais antigos e recriando os novos custos reais.</span><span class="sxs-lookup"><span data-stu-id="c94cf-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="c94cf-115">O aplicativo processará esses custos reais com base no Método de cobrança da linha de contrato associada do projeto.</span><span class="sxs-lookup"><span data-stu-id="c94cf-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="c94cf-116">Se os valores reais de custo fizerem referência a uma linha de contrato de tempo e material, o sistema criará automaticamente os valores reais de vendas não faturados correspondentes para quando a cotação for fechada e o contrato de projeto for criado.</span><span class="sxs-lookup"><span data-stu-id="c94cf-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="c94cf-117">Se os custos reais fizerem referência a uma linha de contrato de preço fixo, o aplicativo vai parar de reprocessar os custos reais com base nas regras de faturamento dividido para os clientes do contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="c94cf-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="c94cf-118">Fechando uma cotação como perdida:</span><span class="sxs-lookup"><span data-stu-id="c94cf-118">Closing a quote as lost:</span></span>

<span data-ttu-id="c94cf-119">Fechar uma cotação de projeto como perdida definirá o status como Fechada e razão do status como Perdida.</span><span class="sxs-lookup"><span data-stu-id="c94cf-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="c94cf-120">Fechar a cotação torna a cotação do projeto somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c94cf-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="c94cf-121">Como uma cotação fechada não pode ser reaberta e antes de fechar uma cotação, uma caixa de diálogo de confirmação confirmará suas alterações.</span><span class="sxs-lookup"><span data-stu-id="c94cf-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c94cf-122">Se a cotação de projeto fechada como Perdida tiver um projeto referenciado em qualquer uma de suas linhas, esse projeto também será marcado como Fechado e todas as reservas de recursos desse dia em diante serão canceladas.</span><span class="sxs-lookup"><span data-stu-id="c94cf-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="c94cf-123">No Project Operations, fechar uma cotação como Ganha ou Perdida não afetará o status da Oportunidade, que permanecerá aberta até que seja fechada manualmente.</span><span class="sxs-lookup"><span data-stu-id="c94cf-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
