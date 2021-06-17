---
title: Comprar materiais sem estoque usando uma fatura de fornecedor pendente
description: Este tópico explica como registrar faturas de fornecedores pendentes.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993764"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="943d7-103">Comprar materiais sem estoque usando uma fatura de fornecedor pendente</span><span class="sxs-lookup"><span data-stu-id="943d7-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="943d7-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="943d7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="943d7-105">Como uma empresa adquire materiais não estocados para um projeto, os custos podem ser logo registrados no projeto.</span><span class="sxs-lookup"><span data-stu-id="943d7-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="943d7-106">Por exemplo, a Contoso Robotics US está realizando um projeto de renovação de equipamentos e precisa de licenças de software.</span><span class="sxs-lookup"><span data-stu-id="943d7-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="943d7-107">Essas licenças são adquiridas de um fornecedor terceirizado.</span><span class="sxs-lookup"><span data-stu-id="943d7-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="943d7-108">Usando o Dynamics 365 Finance, o administrador de contas a pagar registra um documento de fatura do fornecedor pendente e atribui os custos da licença diretamente ao projeto de renovação do equipamento.</span><span class="sxs-lookup"><span data-stu-id="943d7-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="943d7-109">Antes de usar a funcionalidade descrita neste tópico, revise e aplique as configurações necessárias.</span><span class="sxs-lookup"><span data-stu-id="943d7-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="943d7-110">Para obter mais informações, consulte [Habilitar materiais não estocados e faturas de fornecedores pendentes](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="943d7-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="943d7-111">Publicar uma fatura de fornecedor pendente relacionada ao projeto</span><span class="sxs-lookup"><span data-stu-id="943d7-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="943d7-112">As faturas de fornecedor pendentes podem ser registradas na página **Faturas de fornecedor pendentes** (**Contas a pagar** > **Faturas** > **Faturas de fornecedor pendentes**).</span><span class="sxs-lookup"><span data-stu-id="943d7-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="943d7-113">Conclua as seguintes etapas para postar uma fatura de fornecedor pendente relacionada ao projeto:</span><span class="sxs-lookup"><span data-stu-id="943d7-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="943d7-114">Acesse **Contas a pagar** > **Faturas** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="943d7-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="943d7-115">No campo **Conta da fatura**, selecione um fornecedor e, no campo **Número**, insira a identificação da fatura do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="943d7-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="943d7-116">Adicione uma linha à fatura do fornecedor e, no campo **Número de item**, selecione o item não estocado adquirido do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="943d7-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="943d7-117">As linhas da fatura do fornecedor baseadas em uma categoria de compras não podem ser registradas no projeto.</span><span class="sxs-lookup"><span data-stu-id="943d7-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="943d7-118">Adicione a quantidade comprada.</span><span class="sxs-lookup"><span data-stu-id="943d7-118">Add the quantity purchased.</span></span> <span data-ttu-id="943d7-119">O sistema preencherá o preço unitário com base na configuração de preço do item não estocado.</span><span class="sxs-lookup"><span data-stu-id="943d7-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="943d7-120">Verifique o valor total e outros detalhes necessários na linha.</span><span class="sxs-lookup"><span data-stu-id="943d7-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="943d7-121">Nos detalhes da linha, na guia **Projeto**, selecione a ID do projeto em que este item será gravado.</span><span class="sxs-lookup"><span data-stu-id="943d7-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="943d7-122">Opcionalmente, selecione o número da atividade e atualize a categoria do projeto e a propriedade da linha.</span><span class="sxs-lookup"><span data-stu-id="943d7-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="943d7-123">Poste a fatura de fornecedor pendente.</span><span class="sxs-lookup"><span data-stu-id="943d7-123">Post pending vendor invoice.</span></span> <span data-ttu-id="943d7-124">Quando a fatura for postada, o sistema registrará:</span><span class="sxs-lookup"><span data-stu-id="943d7-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="943d7-125">O valor do saldo do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="943d7-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="943d7-126">O valor do imposto.</span><span class="sxs-lookup"><span data-stu-id="943d7-126">The sales tax amount.</span></span>
    - <span data-ttu-id="943d7-127">O custo do projeto é registrado na conta de integração de aquisições.</span><span class="sxs-lookup"><span data-stu-id="943d7-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="943d7-128">A transação real do projeto no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="943d7-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="943d7-129">Esta transação é posteriormente processada usando o [diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="943d7-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="943d7-130">A postagem deste diário move o valor da conta de integração de aquisições para a conta de custo do projeto.</span><span class="sxs-lookup"><span data-stu-id="943d7-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
