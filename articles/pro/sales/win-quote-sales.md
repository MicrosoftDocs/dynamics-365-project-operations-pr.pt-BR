---
title: Fechar uma cotação – lite
description: Este tópico fornece informações sobre como fechar uma cotação no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175697"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="8dfac-103">Fechar uma cotação – lite</span><span class="sxs-lookup"><span data-stu-id="8dfac-103">Close a quote - lite</span></span>

<span data-ttu-id="8dfac-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="8dfac-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8dfac-105">Uma cotação de projeto pode ser fechada como Ganha ou Perdida.</span><span class="sxs-lookup"><span data-stu-id="8dfac-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="8dfac-106">As operações Ativar e Revisar nas cotações não têm suporte no Microsoft Dynamics 365 Project Operations, portanto, uma cotação de rascunho pode ser fechada.</span><span class="sxs-lookup"><span data-stu-id="8dfac-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="8dfac-107">Fechar uma cotação como Ganha</span><span class="sxs-lookup"><span data-stu-id="8dfac-107">Close a quote as Won</span></span>

<span data-ttu-id="8dfac-108">Fechar uma cotação de projeto como Ganha fechará a cotação com o status definido como Fechada e a razão do status definida como Ganha.</span><span class="sxs-lookup"><span data-stu-id="8dfac-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="8dfac-109">Fechar a cotação torna a cotação do projeto somente leitura e cria um contrato do projeto de rascunho que contém as informações da cotação.</span><span class="sxs-lookup"><span data-stu-id="8dfac-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="8dfac-110">Como uma cotação fechada não pode ser reaberta, será exibida uma caixa de diálogo de confirmação Há uma caixa de diálogo de confirmação antes que as alterações sejam feitas, pois uma cotação fechada não pode ser reaberta e as alterações são irreversíveis.</span><span class="sxs-lookup"><span data-stu-id="8dfac-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="8dfac-111">Se a cotação for anexada a uma oportunidade, todas as outras cotações de projeto na oportunidade serão automaticamente fechadas como Perdidas.</span><span class="sxs-lookup"><span data-stu-id="8dfac-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="8dfac-112">Impacto financeiro de fechar uma cotação como Ganha</span><span class="sxs-lookup"><span data-stu-id="8dfac-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="8dfac-113">Se houver dados reais de horas registradas em um projeto enquanto ele ainda estiver anexado a uma cotação de rascunho, somente o custo do tempo ou da despesa será registrado.</span><span class="sxs-lookup"><span data-stu-id="8dfac-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="8dfac-114">Depois que uma cotação for fechada como Ganha, o aplicativo vai refatorar os custos revertendo os custos reais mais antigos e recriando os novos custos reais.</span><span class="sxs-lookup"><span data-stu-id="8dfac-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="8dfac-115">O aplicativo processará esses custos reais com base no Método de cobrança da linha de contrato associada do projeto.</span><span class="sxs-lookup"><span data-stu-id="8dfac-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="8dfac-116">Se os valores reais de custo fizerem referência a uma linha de contrato de tempo e material, o sistema criará automaticamente os valores reais de vendas não faturados correspondentes para quando a cotação for fechada e o contrato de projeto for criado.</span><span class="sxs-lookup"><span data-stu-id="8dfac-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="8dfac-117">Se os custos reais fizerem referência a uma linha de contrato de preço fixo, o aplicativo vai parar de reprocessar os custos reais com base nas regras de faturamento dividido para os clientes do contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="8dfac-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="8dfac-118">Fechando uma cotação como perdida:</span><span class="sxs-lookup"><span data-stu-id="8dfac-118">Closing a quote as lost:</span></span>

<span data-ttu-id="8dfac-119">Fechar uma cotação de projeto como perdida definirá o status como Fechada e razão do status como Perdida.</span><span class="sxs-lookup"><span data-stu-id="8dfac-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="8dfac-120">Fechar a cotação torna a cotação do projeto somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8dfac-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="8dfac-121">Como uma cotação fechada não pode ser reaberta e antes de fechar uma cotação, uma caixa de diálogo de confirmação confirmará suas alterações.</span><span class="sxs-lookup"><span data-stu-id="8dfac-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="8dfac-122">Se a cotação de projeto fechada como Perdida tiver um projeto referenciado em qualquer uma de suas linhas, esse projeto também será marcado como Fechado e todas as reservas de recursos desse dia em diante serão canceladas.</span><span class="sxs-lookup"><span data-stu-id="8dfac-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="8dfac-123">No Project Operations, fechar uma cotação como Ganha ou Perdida não afetará o status da Oportunidade, que permanecerá aberta até que seja fechada manualmente.</span><span class="sxs-lookup"><span data-stu-id="8dfac-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
