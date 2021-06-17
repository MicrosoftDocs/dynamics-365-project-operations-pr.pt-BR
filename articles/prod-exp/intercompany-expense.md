---
title: Despesas intercompanhia
description: Este tópico fornece informações sobre como usar despesas entre empresas para atribuir as despesas de um funcionário à entidade legal para a qual o trabalho foi executado.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005057"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="944da-103">Despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="944da-103">Intercompany expenses</span></span>

<span data-ttu-id="944da-104">Um trabalhador que é empregado por uma entidade legal em uma organização pode executar trabalho para outra entidade legal na mesma organização.</span><span class="sxs-lookup"><span data-stu-id="944da-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="944da-105">Você pode usar despesas entre empresas para atribuir as despesas de um funcionário à entidade legal para a qual o trabalho foi executado.</span><span class="sxs-lookup"><span data-stu-id="944da-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="944da-106">A entidade legal que emprega o trabalhador é chamada de entidade legal que concede empréstimo.</span><span class="sxs-lookup"><span data-stu-id="944da-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="944da-107">A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal que contrai empréstimo.</span><span class="sxs-lookup"><span data-stu-id="944da-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="944da-108">Para que um funcionário possa criar e enviar despesas entre empresas, você deve habilitar as linhas de despesas entre empresas.</span><span class="sxs-lookup"><span data-stu-id="944da-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="944da-109">Na entidade legal de empréstimo, na página **Parâmetros de gerenciamento de despesas**, selecione **Permitir linhas de despesas entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="944da-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="944da-110">Lançamento de imposto para despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="944da-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="944da-111">Para usar grupos de impostos associados à entidade legal de empréstimo (origem) em vez da entidade legal de empréstimo (destino) em seu relatório de despesas, você deve habilitar a funcionalidade na configuração do imposto sobre vendas de contabilidade.</span><span class="sxs-lookup"><span data-stu-id="944da-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="944da-112">Quando o parâmetro **Entidade legal para lançamento de imposto entre empresas** está definido para **Origem** e **Aplicar regras de tributação de impostos sobre vendas** está definido como **Não**, é utilizada a combinação fiscal para a entidade legal de empréstimo.</span><span class="sxs-lookup"><span data-stu-id="944da-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="944da-113">Quando o mesmo parâmetro for definido como **Destino**, será utilizada a combinação fiscal para entidade legal que contrai empréstimo.</span><span class="sxs-lookup"><span data-stu-id="944da-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="944da-114">Para entidades legais nos Estados Unidos, quando o parâmetro é definido como **Fonte**, o campo **Imposto sobre vendas a receber** também deve ser configurado na nova página **Grupos de lançamentos contábeis**.</span><span class="sxs-lookup"><span data-stu-id="944da-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="944da-115">O mecanismo de contabilidade usará as informações desse campo para a entrada contábil relacionada a impostos.</span><span class="sxs-lookup"><span data-stu-id="944da-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="944da-116">O comportamento é consistente para linhas de despesas lançadas com ou sem um projeto.</span><span class="sxs-lookup"><span data-stu-id="944da-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]