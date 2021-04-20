---
title: Novidades ou alterações na Versão de Atualização 30 do Project Service Automation V3
description: Este tópico lista os recursos e as correções novas ou alteradas disponíveis na Versão de Atualização 30 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852827"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="b313f-103">Novidades ou alterações na Versão de Atualização 30 do Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="b313f-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b313f-104">Temos o prazer de anunciar a atualização mais recente do Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b313f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b313f-105">Esta versão inclui algumas melhorias importantes na qualidade, no desempenho e na usabilidade.</span><span class="sxs-lookup"><span data-stu-id="b313f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b313f-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b313f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b313f-107">Para atualizar para esta versão, acesse a página de soluções online do Centro de Administração do Dynamics 365 para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="b313f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b313f-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b313f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b313f-109">Este tópico lista os recursos e as correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 30.</span><span class="sxs-lookup"><span data-stu-id="b313f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="b313f-110">Esta versão apresenta o número de build V3.10.51.61 e geralmente está disponível por meio de uma atualização automática de abril de 2021.</span><span class="sxs-lookup"><span data-stu-id="b313f-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="b313f-111">Versão de Atualização 30</span><span class="sxs-lookup"><span data-stu-id="b313f-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b313f-112">Correções de bug</span><span class="sxs-lookup"><span data-stu-id="b313f-112">Bug fixes</span></span>

<span data-ttu-id="b313f-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="b313f-113">**Time and Expense**</span></span>

<span data-ttu-id="b313f-114">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="b313f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b313f-115">Ocorrerá um erro quando você criar e salvar uma entrada de tempo na página **Criação Rápida** se o campo **Função** for removido.</span><span class="sxs-lookup"><span data-stu-id="b313f-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="b313f-116">O filtro de entrada de tempo aplica o operador de filtro errado.</span><span class="sxs-lookup"><span data-stu-id="b313f-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="b313f-117">As planilhas de horas copiadas não são exibidas automaticamente quando você seleciona **Copiar Semana** no controle de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="b313f-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="b313f-118">**Gerenciamento de Recursos**</span><span class="sxs-lookup"><span data-stu-id="b313f-118">**Resource Management**</span></span>

<span data-ttu-id="b313f-119">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="b313f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="b313f-120">Quando você estende uma reserva, o status de reserva atribuído à reserva definitiva fica incorreto.</span><span class="sxs-lookup"><span data-stu-id="b313f-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="b313f-121">A extensão de uma reserva respeita o status de reserva definido como **Confirmado** nos metadados de configuração de reserva.</span><span class="sxs-lookup"><span data-stu-id="b313f-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="b313f-122">Quando um status de reserva válido não é especificado, a mensagem de erro não é localizada corretamente.</span><span class="sxs-lookup"><span data-stu-id="b313f-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="b313f-123">**Gerenciamento de projetos**</span><span class="sxs-lookup"><span data-stu-id="b313f-123">**Project Management**</span></span>

<span data-ttu-id="b313f-124">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="b313f-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="b313f-125">Os projetos não podem ser criados em uma moeda e incluem tarefas relacionadas em outra moeda.</span><span class="sxs-lookup"><span data-stu-id="b313f-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="b313f-126">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="b313f-126">**Sales**</span></span>

<span data-ttu-id="b313f-127">Os seguintes problemas foram corrigidos:</span><span class="sxs-lookup"><span data-stu-id="b313f-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="b313f-128">Quando uma lista de preços é copiada, os preços não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="b313f-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="b313f-129">Fechar uma cotação como ganha falha quando o detalhe de custo tem um valor de origem.</span><span class="sxs-lookup"><span data-stu-id="b313f-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="b313f-130">Na entidade **Tarefa do Projeto**, o **Custo Estimado** foi renomeado como **Custo Planejado (Base)**.</span><span class="sxs-lookup"><span data-stu-id="b313f-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="b313f-131">Uma exceção de referência nula é gerada quando faturas são criadas ou excluídas.</span><span class="sxs-lookup"><span data-stu-id="b313f-131">A null reference exception is generated when invoices are created or deleted.</span></span>
