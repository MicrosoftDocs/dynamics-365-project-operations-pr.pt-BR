---
title: Despesas entre empresas
description: Um trabalhador que é empregado por uma entidade legal em uma organização pode executar trabalho para outra entidade legal na mesma organização. Nessa situação, você pode usar o recurso de despesas entre empresas para atribuir as despesas do trabalhador à entidade legal para a qual o trabalho foi executado.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071579"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="40414-104">Despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="40414-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40414-105">Um trabalhador que é empregado por uma entidade legal em uma organização pode executar trabalho para outra entidade legal na mesma organização.</span><span class="sxs-lookup"><span data-stu-id="40414-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="40414-106">Nessa situação, você pode usar o recurso de despesas entre empresas para atribuir as despesas do trabalhador à entidade legal para a qual o trabalho foi executado.</span><span class="sxs-lookup"><span data-stu-id="40414-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="40414-107">A entidade legal que emprega o trabalhador é chamada de entidade legal que concede empréstimo.</span><span class="sxs-lookup"><span data-stu-id="40414-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="40414-108">A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal que contrai empréstimo.</span><span class="sxs-lookup"><span data-stu-id="40414-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="40414-109">Para que um trabalhador possa criar e enviar despesas para o trabalho que é executado para uma entidade legal diferente, na entidade legal que concede empréstimo, na página **Parâmetros de gerenciamento de despesas** , selecione a opção **Permitir linhas de despesas entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="40414-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="40414-110">Lançamento de imposto para despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="40414-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40414-111">Se desejar usar grupos de impostos associados à entidade legal que concede empréstimo (origem) em vez da entidade legal que contrai empréstimo (destino) no relatório de despesas, você precisará definir isso na configuração do imposto sobre vendas da contabilidade.</span><span class="sxs-lookup"><span data-stu-id="40414-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="40414-112">Quando o parâmetro de contabilidade **Entidade legal para lançamento de imposto entre empresas** estiver configurado como **Fonte** e **Aplicar regras de tributação de impostos sobre vendas** estiver definido como **Não** , será utilizada a combinação fiscal para a entidade legal que concede empréstimo.</span><span class="sxs-lookup"><span data-stu-id="40414-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="40414-113">Quando o mesmo parâmetro for definido como **Destino** , será utilizada a combinação fiscal para entidade legal que contrai empréstimo.</span><span class="sxs-lookup"><span data-stu-id="40414-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="40414-114">Para entidades legais nos Estados Unidos, quando o parâmetro é definido como **Fonte** , o campo **Imposto sobre vendas a receber** também deve ser configurado na nova página **Grupos de lançamentos contábeis**.</span><span class="sxs-lookup"><span data-stu-id="40414-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="40414-115">O mecanismo de contabilidade usará as informações desse campo para a entrada contábil relacionada a impostos.</span><span class="sxs-lookup"><span data-stu-id="40414-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="40414-116">O comportamento é consistente para linhas de despesas lançadas com ou sem um projeto.</span><span class="sxs-lookup"><span data-stu-id="40414-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  