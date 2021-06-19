---
title: Trabalhar com despesas pessoais em um relatório de despesas
description: Este tópico fornece informações sobre como lidar com despesas pessoais incorridas por funcionários durante viagens de negócios.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025670"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="d0175-103">Trabalhar com despesas pessoais em um relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="d0175-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="d0175-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="d0175-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0175-105">Em uma viagem de negócios, um funcionário pode pagar despesas pessoais com seu cartão de crédito corporativo.</span><span class="sxs-lookup"><span data-stu-id="d0175-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="d0175-106">Se um processo não foi definido para lidar com despesas pessoais, o processo de aprovação do relatório de despesas pode ser interrompido quando um funcionário envia seu relatório de despesas discriminado.</span><span class="sxs-lookup"><span data-stu-id="d0175-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="d0175-107">Existem dois métodos que você pode usar para trabalhar com as despesas pessoais de um funcionário:</span><span class="sxs-lookup"><span data-stu-id="d0175-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="d0175-108">**Pago pelo funcionário**: sua organização não paga despesas pessoais que aparecem na fatura do cartão de crédito corporativo.</span><span class="sxs-lookup"><span data-stu-id="d0175-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="d0175-109">Em vez disso, o funcionário paga as despesas diretamente à empresa de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="d0175-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="d0175-110">**Pago pela empresa**: sua organização paga a conta integral do cartão de crédito corporativo e, em seguida, debita da conta do funcionário as despesas pessoais.</span><span class="sxs-lookup"><span data-stu-id="d0175-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="d0175-111">Você pode selecionar o método que sua organização usa na página **Parâmetros de gerenciamento de despesas**.</span><span class="sxs-lookup"><span data-stu-id="d0175-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="d0175-112">Ative a função de divisão de despesas quando o campo de valor pessoal tiver um valor definido</span><span class="sxs-lookup"><span data-stu-id="d0175-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="d0175-113">O recurso, **Ative a função de divisão de despesas quando o campo de valor pessoal tiver um valor definido** aplica-se apenas a relatórios de despesas que são aprovados usando um fluxo de trabalho de nível de linha.</span><span class="sxs-lookup"><span data-stu-id="d0175-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="d0175-114">Os relatórios são aprovados indo para **Processar relatórios de despesas** > **Relatórios de despesas atribuídos a mim** > **Abrir relatório de despesas**.</span><span class="sxs-lookup"><span data-stu-id="d0175-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="d0175-115">Para habilitar este recurso, vá para **Espaços de trabalho** > **Gerenciamento de recursos**, selecione **Ative a função de divisão de despesas quando o campo de valor pessoal tiver um valor definido** e, em seguida, selecione **Ativar agora**.</span><span class="sxs-lookup"><span data-stu-id="d0175-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="d0175-116">Quando o recurso estiver habilitado, as linhas de despesas que usam essa funcionalidade geram duas linhas quando o relatório é enviado.</span><span class="sxs-lookup"><span data-stu-id="d0175-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="d0175-117">Duas linhas são geradas para que o aprovador possa aprovar cada linha separadamente.</span><span class="sxs-lookup"><span data-stu-id="d0175-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
