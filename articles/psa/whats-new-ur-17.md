---
title: Novidades ou alterações na Versão de Atualização 17 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 17 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071384"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="9b8ea-103">Versão de Atualização 17, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="9b8ea-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="9b8ea-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9b8ea-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="9b8ea-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9b8ea-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="9b8ea-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9b8ea-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9b8ea-109">Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 17.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="9b8ea-110">Esta versão tem um número de compilação V3.10.6.34 e está geralmente disponível por meio de uma atualização automática desde março de 2020.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="9b8ea-111">Versão de Atualização 17</span><span class="sxs-lookup"><span data-stu-id="9b8ea-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9b8ea-112">Correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9b8ea-112">Bug fixes</span></span>

<span data-ttu-id="9b8ea-113">**Geral**</span><span class="sxs-lookup"><span data-stu-id="9b8ea-113">**General**</span></span>

- <span data-ttu-id="9b8ea-114">Corrigido: Atualizar Project Service Automation para aplicar as licenças do Membro da Equipe (o Hub do Recurso do Projeto incluirá metadados do plano do Serviço do Membro da Equipe 3.x)</span><span class="sxs-lookup"><span data-stu-id="9b8ea-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="9b8ea-115">**Hora e Despesa**</span><span class="sxs-lookup"><span data-stu-id="9b8ea-115">**Time and Expense**</span></span>

- <span data-ttu-id="9b8ea-116">Fixo: Não é possível alterar uma estimativa de despesa de um valor diferente de zero para zero (0).</span><span class="sxs-lookup"><span data-stu-id="9b8ea-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="9b8ea-117">A alteração é ignorada.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-117">The change is ignored.</span></span>

<span data-ttu-id="9b8ea-118">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="9b8ea-118">**Project Management**</span></span>

- <span data-ttu-id="9b8ea-119">Corrigido: Uma verificação de valores nulos foi adicionada ao nome da posição de um membro da equipe.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="9b8ea-120">Corrigido: O campo **msdyn_userresourceid** na entidade **msdyn_resourceassignment** foi descontinuado.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="9b8ea-121">Corrigido: A atualização do 2.X para 3.X agora trata contornos de esforço vazios em atribuições de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="9b8ea-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9b8ea-122">**Sales**</span></span>

- <span data-ttu-id="9b8ea-123">Corrigido: **Invoice.PreValidateInvoiceUpdate** agora trata o cenário de reatribuir os proprietários dos registros corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="9b8ea-124">Corrigido: Quando a classe de transação for **Hora** , **UnitGroup** agora é editável para todas as entidades, incluindo **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** e **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="9b8ea-125">No entanto, **Unidade** não é editável apenas para **JournalLine** e **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="9b8ea-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


