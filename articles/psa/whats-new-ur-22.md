---
title: Novidades ou alterações na Versão de Atualização 22 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 22 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 456ed68bc1d74c2c8e5d2420a3f5d1fb8e0465d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126604"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="8c21d-103">Versão de Atualização 22, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="8c21d-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="8c21d-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8c21d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8c21d-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="8c21d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8c21d-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8c21d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8c21d-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="8c21d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8c21d-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8c21d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8c21d-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 22.</span><span class="sxs-lookup"><span data-stu-id="8c21d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="8c21d-110">Esta versão apresenta o número de compilação V 3.10.33.48 e está disponível para o público em geral por meio de uma atualização automática em junho de 2020.</span><span class="sxs-lookup"><span data-stu-id="8c21d-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="8c21d-111">Versão de Atualização 22</span><span class="sxs-lookup"><span data-stu-id="8c21d-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8c21d-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="8c21d-112">Bug fixes</span></span>



<span data-ttu-id="8c21d-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="8c21d-113">**Time and Expense**</span></span>

<span data-ttu-id="8c21d-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="8c21d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8c21d-115">As **Entradas de horas** não são adicionadas automaticamente na agenda de Entradas de horas após a importação.</span><span class="sxs-lookup"><span data-stu-id="8c21d-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="8c21d-116">O seletor de data da grade **Entrada de Horas** não reconhece as configurações regionais de um usuário.</span><span class="sxs-lookup"><span data-stu-id="8c21d-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="8c21d-117">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="8c21d-117">**Resource Management**</span></span>

<span data-ttu-id="8c21d-118">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="8c21d-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="8c21d-119">No modo manual, as alterações em contornos da **Atribuição de Recurso** não são reconhecidas ao gerar os **Requisitos de Recurso**.</span><span class="sxs-lookup"><span data-stu-id="8c21d-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="8c21d-120">As **Solicitações de Recursos** não oferecem suporte aos status de solicitação.</span><span class="sxs-lookup"><span data-stu-id="8c21d-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="8c21d-121">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="8c21d-121">**Project Management**</span></span>

<span data-ttu-id="8c21d-122">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="8c21d-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="8c21d-123">Usar o clique duplo em EstimateGridControl não analisará os números no formato holandês corretamente.</span><span class="sxs-lookup"><span data-stu-id="8c21d-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="8c21d-124">Os horários atribuídos não são atualizados corretamente quando as atribuições são alteradas usando o suplemento de cliente de desktop do Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="8c21d-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="8c21d-125">As grades de Rastreamento e Estimativas do Projeto exibem o código de moeda de venda incorreto quando a moeda de contrato é diferente da moeda do cliente e a organização está configurada para exibir códigos de moeda em vez de símbolos da moeda.</span><span class="sxs-lookup"><span data-stu-id="8c21d-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="8c21d-126">A data de término de um membro da equipe adicionará um dia se o agendamento de horas de trabalho for 24 horas por dia.</span><span class="sxs-lookup"><span data-stu-id="8c21d-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="8c21d-127">No Agendamento de Projeto, adicionar uma Categoria de Transação a uma tarefa não aciona o salvamento automático.</span><span class="sxs-lookup"><span data-stu-id="8c21d-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="8c21d-128">O seguinte erro é exibido ao adicionar um membro da equipe ao Modelo do Projeto: "Requisitos de recurso não podem ser associados a modelos de projeto".</span><span class="sxs-lookup"><span data-stu-id="8c21d-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="8c21d-129">O script de regra da faixa de opções "msdyn.Approval.CanApproveOrReject" exibe um erro de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="8c21d-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="8c21d-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8c21d-130">**Sales**</span></span>

<span data-ttu-id="8c21d-131">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="8c21d-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="8c21d-132">A mensagem de erro de validação não é exibida quando uma Lista de Preços de Custo é selecionada na pesquisa de Lista de Preços no formulário/entidade "Nova Lista de Preços do Projeto de Cotação".</span><span class="sxs-lookup"><span data-stu-id="8c21d-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="8c21d-133">Fechar a cotação como ganha não direciona para o contrato criado se um Fluxo do Processo Empresarial anexado à cotação estiver no estágio final.</span><span class="sxs-lookup"><span data-stu-id="8c21d-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="8c21d-134">A reversão de **Vendas Não Cobradas** está vinculada ao custo original quando uma entrada de hora é recuperada.</span><span class="sxs-lookup"><span data-stu-id="8c21d-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="8c21d-135">Depois de selecionar o botão **Confirmar**, o status da fatura não é alterado para **Confirmado** a menos que a fatura seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="8c21d-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
