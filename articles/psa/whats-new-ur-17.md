---
title: Novidades ou alterações na Versão de Atualização 17 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 17 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143683"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="51181-103">Versão de Atualização 17, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="51181-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="51181-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="51181-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="51181-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="51181-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="51181-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="51181-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="51181-107">Para atualizar para esta versão, acesse o Centro de Administração do Dynamics 365 online e a página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="51181-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="51181-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="51181-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="51181-109">Este tópico lista os recursos e as correções novas ou alteradas para o PSA V3, Versão de Atualização 17.</span><span class="sxs-lookup"><span data-stu-id="51181-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="51181-110">Esta versão tem um número de compilação V3.10.6.34 e está geralmente disponível por meio de uma atualização automática desde março de 2020.</span><span class="sxs-lookup"><span data-stu-id="51181-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="51181-111">Versão de Atualização 17</span><span class="sxs-lookup"><span data-stu-id="51181-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="51181-112">Correções de bugs</span><span class="sxs-lookup"><span data-stu-id="51181-112">Bug fixes</span></span>

<span data-ttu-id="51181-113">**Geral**</span><span class="sxs-lookup"><span data-stu-id="51181-113">**General**</span></span>

- <span data-ttu-id="51181-114">Corrigido: Atualizar Project Service Automation para aplicar as licenças do Membro da Equipe (o Hub do Recurso do Projeto incluirá metadados do plano do Serviço do Membro da Equipe 3.x)</span><span class="sxs-lookup"><span data-stu-id="51181-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="51181-115">**Hora e Despesa**</span><span class="sxs-lookup"><span data-stu-id="51181-115">**Time and Expense**</span></span>

- <span data-ttu-id="51181-116">Fixo: Não é possível alterar uma estimativa de despesa de um valor diferente de zero para zero (0).</span><span class="sxs-lookup"><span data-stu-id="51181-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="51181-117">A alteração é ignorada.</span><span class="sxs-lookup"><span data-stu-id="51181-117">The change is ignored.</span></span>

<span data-ttu-id="51181-118">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="51181-118">**Project Management**</span></span>

- <span data-ttu-id="51181-119">Corrigido: Uma verificação de valores nulos foi adicionada ao nome da posição de um membro da equipe.</span><span class="sxs-lookup"><span data-stu-id="51181-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="51181-120">Corrigido: O campo **msdyn_userresourceid** na entidade **msdyn_resourceassignment** foi descontinuado.</span><span class="sxs-lookup"><span data-stu-id="51181-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="51181-121">Corrigido: A atualização do 2.X para 3.X agora trata contornos de esforço vazios em atribuições de tarefas.</span><span class="sxs-lookup"><span data-stu-id="51181-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="51181-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="51181-122">**Sales**</span></span>

- <span data-ttu-id="51181-123">Corrigido: **Invoice.PreValidateInvoiceUpdate** agora trata o cenário de reatribuir os proprietários dos registros corretamente.</span><span class="sxs-lookup"><span data-stu-id="51181-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="51181-124">Corrigido: Quando a classe de transação for **Hora**, **UnitGroup** agora é editável para todas as entidades, incluindo **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** e **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="51181-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="51181-125">No entanto, **Unidade** não é editável apenas para **JournalLine** e **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="51181-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


