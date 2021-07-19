---
title: Novidades ou alterações na Versão de Atualização 33 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 33 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334500"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="1345b-103">Novidades ou alterações na Versão de Atualização 33 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="1345b-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1345b-104">Temos o prazer de anunciar a atualização mais recente do aplicativo Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1345b-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="1345b-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="1345b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1345b-106">É compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1345b-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1345b-107">Para atualizar para esta versão, visite o Centro de Administração para a página de soluções online do Dynamics 365 e instale a atualização.</span><span class="sxs-lookup"><span data-stu-id="1345b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="1345b-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1345b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1345b-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 33.</span><span class="sxs-lookup"><span data-stu-id="1345b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="1345b-110">Esta versão tem um número de compilação de V3.10.54.98 e geralmente fica disponível por meio de uma atualização automática em julho de 2021.</span><span class="sxs-lookup"><span data-stu-id="1345b-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="1345b-111">Versão de Atualização 33</span><span class="sxs-lookup"><span data-stu-id="1345b-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1345b-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="1345b-112">Bug fixes</span></span>

<span data-ttu-id="1345b-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="1345b-113">**Time and Expense**</span></span>

<span data-ttu-id="1345b-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="1345b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1345b-115">Dois campos bloqueados, **msdyn_description** e **msdyn_externaldescription** são editáveis após o envio.</span><span class="sxs-lookup"><span data-stu-id="1345b-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="1345b-116">Uma mensagem de erro será exibida se uma despesa não relacionada a um projeto for criada.</span><span class="sxs-lookup"><span data-stu-id="1345b-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="1345b-117">Quando uma entrada de tempo é criada, a função do recurso assume como padrão uma função inativa.</span><span class="sxs-lookup"><span data-stu-id="1345b-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="1345b-118">As linhas do diário associadas a uma despesa recuperada e excluída não são excluídas.</span><span class="sxs-lookup"><span data-stu-id="1345b-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="1345b-119">No **Formulário de Criação Rápida de entrada de horas**, atualize a exibição **Lista de Tarefas do Projeto** para alterar a data exibida por padrão para a data de início da tarefa.</span><span class="sxs-lookup"><span data-stu-id="1345b-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="1345b-120">Quando você cria uma entrada de tempo a partir da guia **Relacionado** do recurso reservável, a entrada de hora é criada incorretamente para o usuário conectado em vez do recurso reservável pai.</span><span class="sxs-lookup"><span data-stu-id="1345b-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="1345b-121">Novos campos são adicionados à caixa de diálogo **Aprovação em massa de MDD**.</span><span class="sxs-lookup"><span data-stu-id="1345b-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="1345b-122">**Planejamento do projeto**</span><span class="sxs-lookup"><span data-stu-id="1345b-122">**Project planning**</span></span>

<span data-ttu-id="1345b-123">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="1345b-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="1345b-124">Desempenho lento na criação de projetos quando os modelos de horas de trabalho do projeto são aplicados a calendários complexos.</span><span class="sxs-lookup"><span data-stu-id="1345b-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="1345b-125">Quando a data de início é maior que a data de término, um erro é exibido no modelo de projeto de cópia devido às diferenças no componente de tempo de cada campo.</span><span class="sxs-lookup"><span data-stu-id="1345b-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="1345b-126">**Gerenciamento de recursos**</span><span class="sxs-lookup"><span data-stu-id="1345b-126">**Resource management**</span></span>

<span data-ttu-id="1345b-127">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="1345b-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="1345b-128">Um parâmetro incorreto é usado na consulta de utilização de recursos e o XML leva a resultados de filtro incorretos na grade **Utilização de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="1345b-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="1345b-129">A confirmação **Estender Reservas** exibe a data de término incorreta para as reservas.</span><span class="sxs-lookup"><span data-stu-id="1345b-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="1345b-130">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="1345b-130">**Sales**</span></span>

<span data-ttu-id="1345b-131">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="1345b-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="1345b-132">Uma mensagem de erro ocorre se um preço de categoria for criado com valores ausentes.</span><span class="sxs-lookup"><span data-stu-id="1345b-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="1345b-133">Uma mensagem de erro ocorre se um marco de linha de contrato for criado sem uma linha de ordem.</span><span class="sxs-lookup"><span data-stu-id="1345b-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
