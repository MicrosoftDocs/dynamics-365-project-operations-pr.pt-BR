---
title: Novidades ou alterações na Versão de Atualização 21 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 21 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071379"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="ae314-103">Versão de Atualização 21, do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="ae314-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="ae314-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ae314-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ae314-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="ae314-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ae314-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ae314-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ae314-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="ae314-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ae314-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ae314-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ae314-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 21.</span><span class="sxs-lookup"><span data-stu-id="ae314-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="ae314-110">Esta versão apresenta o número de compilação V 3.10.32.50 e está disponível para o público em geral por meio de uma atualização automática em junho de 2020.</span><span class="sxs-lookup"><span data-stu-id="ae314-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="ae314-111">Versão de Atualização 21</span><span class="sxs-lookup"><span data-stu-id="ae314-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ae314-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="ae314-112">Bug fixes</span></span>

<span data-ttu-id="ae314-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="ae314-113">**Time and Expense**</span></span>

<span data-ttu-id="ae314-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="ae314-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ae314-115">Ao hospedar o **Controle de Grade de Entrada de Tempo** nos Painéis, a grade não usa a largura total do contêiner da grade do painel.</span><span class="sxs-lookup"><span data-stu-id="ae314-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="ae314-116">Para fusos horários específicos, o controle de grade da **Entrada de Tempo** não exibe registros.</span><span class="sxs-lookup"><span data-stu-id="ae314-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="ae314-117">As entradas de horas após 21 h aparecem no dia errado.</span><span class="sxs-lookup"><span data-stu-id="ae314-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="ae314-118">Os usuários não conseguem enviar despesas se a categoria **Recibo de despesa obrigatório** não tiver um valor definido.</span><span class="sxs-lookup"><span data-stu-id="ae314-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="ae314-119">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="ae314-119">**Resource Management**</span></span>

<span data-ttu-id="ae314-120">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="ae314-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="ae314-121">As reservas inativas são exibidas em **Reconciliação**.</span><span class="sxs-lookup"><span data-stu-id="ae314-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="ae314-122">O preenchimento de recurso genérico não tinha validação para garantir a existência de um status de reserva válido.</span><span class="sxs-lookup"><span data-stu-id="ae314-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="ae314-123">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="ae314-123">**Project Management**</span></span>

<span data-ttu-id="ae314-124">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="ae314-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="ae314-125">As grades do formulário **Projeto** ( **Atribuição de Recurso** , **Tarefa** , exibição de **Reconciliação** , **Estimativas de Despesas** ) continuam editáveis mesmo se o projeto não estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="ae314-125">The **Project** form grids ( **Resource Assignment** , **Task** , **Reconciliation** view, **Expense Estimates** ) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="ae314-126">Os clientes duplicados não podem ser mesclados com os clientes vinculados a contratos de projetos confirmados.</span><span class="sxs-lookup"><span data-stu-id="ae314-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="ae314-127">Quando um recurso sem um calendário válido é adicionado, o sistema não retorna uma mensagem de erro amigável.</span><span class="sxs-lookup"><span data-stu-id="ae314-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="ae314-128">O botão **Adicionar Tarefa** na grade de tarefas é habilitado quando o projeto está vinculado ao **Suplemento do Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="ae314-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="ae314-129">O esforço aumenta de forma incontrolável quando uma tarefa com uma categoria é atribuída a um recurso com uma função para a qual há um preço de custo definido.</span><span class="sxs-lookup"><span data-stu-id="ae314-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="ae314-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ae314-130">**Sales**</span></span>

<span data-ttu-id="ae314-131">Os seguintes aprimoramentos foram realizados:</span><span class="sxs-lookup"><span data-stu-id="ae314-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="ae314-132">**Frequência da fatura** e **Início da Cobrança** foram movidos para a guia **Agenda de Faturas**.</span><span class="sxs-lookup"><span data-stu-id="ae314-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="ae314-133">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="ae314-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="ae314-134">O **Preço de Venda Total** é 0 (zero) para **Categoria** , embora **Função** tenha um preço de venda total diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ae314-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="ae314-135">Os clientes não podem alterar o valor do campo **Status da Fatura** para **Pronto para faturamento** quando outro processo personalizado estiver atualizando um campo adicional.</span><span class="sxs-lookup"><span data-stu-id="ae314-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="ae314-136">O botão **Atualizar Linhas da Fatura** pode criar várias linhas duplicadas se for selecionado repetidas vezes.</span><span class="sxs-lookup"><span data-stu-id="ae314-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="ae314-137">O botão **Atualizar Preços** não funciona na subgrade **Preços da Função** no formulário **Exibição Rápida**.</span><span class="sxs-lookup"><span data-stu-id="ae314-137">The **Update Prices** button doesn't work on the **Role Prices** sub-grid in the **Quick View** form.</span></span>
- <span data-ttu-id="ae314-138">A lógica **Resolução da Lista de Preços de Venda** trata incorretamente os fusos horários, resultando na seleção incorreta de listas de preços.</span><span class="sxs-lookup"><span data-stu-id="ae314-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="ae314-139">O **Custo Total Real** de um projeto pode apresentar uma diferença fracionária após a aprovação de uma única entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="ae314-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="ae314-140">A lógica **Resolução de Preço** não fornece uma mensagem de erro amigável se **Preço de Função Recuperado** não tiver valores nos campos **Unidade Principal** e **Preço na Unidade Principal**.</span><span class="sxs-lookup"><span data-stu-id="ae314-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
