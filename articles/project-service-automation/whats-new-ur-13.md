---
title: Novidades na Versão de Atualização 13 do Project Service Automation V3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado na Versão da Atualização 13 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749074"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="de052-103">Novidades na Versão de Atualização 13 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="de052-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="de052-104">Temos o orgulho de anunciar a versão mais recente do aplicativo do Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="de052-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="de052-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="de052-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="de052-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="de052-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="de052-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e vá para a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="de052-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="de052-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="de052-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="de052-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 13.</span><span class="sxs-lookup"><span data-stu-id="de052-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="de052-110">Esta versão possui um número de compilação da V3.10.3.18 e está disponível na seguinte agenda:</span><span class="sxs-lookup"><span data-stu-id="de052-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="de052-111">**Disponibilidade geral (atualização automática):** Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="de052-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="de052-112">**Atualização automática:** Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="de052-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="de052-113">Versão de Atualização 13</span><span class="sxs-lookup"><span data-stu-id="de052-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="de052-114">Correções de bugs</span><span class="sxs-lookup"><span data-stu-id="de052-114">Bug fixes</span></span>

- <span data-ttu-id="de052-115">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="de052-115">Time and Expense</span></span>

     - <span data-ttu-id="de052-116">Corrigido: A funcionalidade de pesquisa na página **Aprovação da experiência** não funciona ao pesquisar por finalidade de despesa.</span><span class="sxs-lookup"><span data-stu-id="de052-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="de052-117">Gerenciamento de Recursos</span><span class="sxs-lookup"><span data-stu-id="de052-117">Resource Management</span></span>

     - <span data-ttu-id="de052-118">Corrigido: Os números na reconciliação foram atualizados para serem justificados à direita.</span><span class="sxs-lookup"><span data-stu-id="de052-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="de052-119">Corrigido: Os Recursos Nomeados não podem ser atribuídos às tarefas por meio da guia **Agendar**.</span><span class="sxs-lookup"><span data-stu-id="de052-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="de052-120">Gerenciamento de projetos</span><span class="sxs-lookup"><span data-stu-id="de052-120">Project Management</span></span>

     - <span data-ttu-id="de052-121">Corrigido: Exceção de referência nula ao atribuir um membro da equipe quando **TransactionType** não tiver as informações de configuração para **Unidade** e **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="de052-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="de052-122">Sales</span><span class="sxs-lookup"><span data-stu-id="de052-122">Sales</span></span>

     - <span data-ttu-id="de052-123">Corrigido: Os registros do tipo de transação duplicados retornam um erro quando os registros de preço da função são criados.</span><span class="sxs-lookup"><span data-stu-id="de052-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="de052-124">Corrigido: Os botões extras para **Nova Oportunidade**, **Cotação**, **Linha de Compra** e **Adicionar Produto** estão visíveis nos comandos de Oportunidades, Cotações, Produtos da Ordem e na subgrade das Linhas baseadas no projeto.</span><span class="sxs-lookup"><span data-stu-id="de052-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


