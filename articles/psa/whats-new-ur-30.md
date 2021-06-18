---
title: Novidades ou alterações na Versão de Atualização 30 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 30 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010412"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="56726-103">Novidades ou alterações na Versão de Atualização 30 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="56726-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="56726-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="56726-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="56726-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="56726-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="56726-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="56726-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="56726-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="56726-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="56726-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="56726-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="56726-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 30.</span><span class="sxs-lookup"><span data-stu-id="56726-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="56726-110">Esta versão apresenta o número de build V3.10.51.61 e geralmente está disponível por meio de uma atualização automática de abril de 2021.</span><span class="sxs-lookup"><span data-stu-id="56726-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="56726-111">Versão de Atualização 30</span><span class="sxs-lookup"><span data-stu-id="56726-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="56726-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="56726-112">Bug fixes</span></span>

<span data-ttu-id="56726-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="56726-113">**Time and Expense**</span></span>

<span data-ttu-id="56726-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="56726-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="56726-115">Ocorrerá um erro quando você criar e salvar uma entrada de tempo na página **Criação Rápida** se o campo **Função** for removido.</span><span class="sxs-lookup"><span data-stu-id="56726-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="56726-116">O filtro de entrada de tempo aplica o operador de filtro errado.</span><span class="sxs-lookup"><span data-stu-id="56726-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="56726-117">As planilhas de horas copiadas não são exibidas automaticamente quando você seleciona **Copiar Semana** no controle de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="56726-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="56726-118">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="56726-118">**Resource Management**</span></span>

<span data-ttu-id="56726-119">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="56726-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="56726-120">Quando você estende uma reserva, o status de reserva atribuído à reserva definitiva fica incorreto.</span><span class="sxs-lookup"><span data-stu-id="56726-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="56726-121">A extensão de uma reserva respeita o status de reserva definido como **Confirmado** nos metadados de configuração de reserva.</span><span class="sxs-lookup"><span data-stu-id="56726-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="56726-122">Quando um status de reserva válido não é especificado, a mensagem de erro não é localizada corretamente.</span><span class="sxs-lookup"><span data-stu-id="56726-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="56726-123">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="56726-123">**Project Management**</span></span>

<span data-ttu-id="56726-124">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="56726-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="56726-125">Os projetos não podem ser criados em uma moeda e incluem tarefas relacionadas em outra moeda.</span><span class="sxs-lookup"><span data-stu-id="56726-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="56726-126">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="56726-126">**Sales**</span></span>

<span data-ttu-id="56726-127">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="56726-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="56726-128">Quando uma lista de preços é copiada, os preços não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="56726-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="56726-129">Fechar uma cotação como ganha falha quando o detalhe de custo tem um valor de origem.</span><span class="sxs-lookup"><span data-stu-id="56726-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="56726-130">Na entidade **Tarefa do Projeto**, o **Custo Estimado** foi renomeado como **Custo Planejado (Base)**.</span><span class="sxs-lookup"><span data-stu-id="56726-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="56726-131">Uma exceção de referência nula é gerada quando faturas são criadas ou excluídas.</span><span class="sxs-lookup"><span data-stu-id="56726-131">A null reference exception is generated when invoices are created or deleted.</span></span>
