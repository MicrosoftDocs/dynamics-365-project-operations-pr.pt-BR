---
title: Novidades ou alterações no Project Service Automation versão 3.x, onda 1 2020
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado no Project Service Automation versão 3 onda 1 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280159"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="dec23-103">Novidades ou alterações no Project Service Automation versão 3.x onda 1 2020</span><span class="sxs-lookup"><span data-stu-id="dec23-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dec23-104">O tópico destaca as principais considerações de atualização ao passar para a versão mais recente do Project Service Automation (PSA) versão 3.x onda 1 2020.</span><span class="sxs-lookup"><span data-stu-id="dec23-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="dec23-105">Entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="dec23-105">Time entry</span></span>
<span data-ttu-id="dec23-106">A experiência de entrada de hora foi estendida para fornecer recursos para estender a entrada de hora em mais cenários de clientes.</span><span class="sxs-lookup"><span data-stu-id="dec23-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="dec23-107">Isso inclui a capacidade de adicionar tipos de entrada, que agora acionam um comportamento específico com base no nome do esquema de campo **Configurações de Entrada de Hora**, exibido como **Fonte de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="dec23-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="dec23-108">Uma nova solução, chamada Tempo, Despesa, Status e Aprovações (TESA) foi adicionada para oferecer suporte a essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="dec23-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="dec23-109">Consideração sobre atualização</span><span class="sxs-lookup"><span data-stu-id="dec23-109">Upgrade consideration</span></span>
<span data-ttu-id="dec23-110">Para oferecer suporte a esta funcionalidade, as funções no PSA foram atualizadas para incluir novos privilégios.</span><span class="sxs-lookup"><span data-stu-id="dec23-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="dec23-111">Esses privilégios concedem acesso de leitura à nova entidade **Configurações de Entrada de Hora**.</span><span class="sxs-lookup"><span data-stu-id="dec23-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="dec23-112">Os usuários que precisam da capacidade de registrar o tempo devem receber a função de usuário **Usuário de Entrada de Hora** além das funções existentes.</span><span class="sxs-lookup"><span data-stu-id="dec23-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="dec23-113">Esta função inclui a nova funcionalidade e garante que a entrada de hora continuará funcionando.</span><span class="sxs-lookup"><span data-stu-id="dec23-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="dec23-114">Além disso, se você tiver algum módulo de aplicativo personalizado que inclua todos os formulários para a entidade de entrada de horas, será necessário remover o **Formulário de criação rápida de entrada de tempo TESA** do módulo.</span><span class="sxs-lookup"><span data-stu-id="dec23-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="dec23-115">Alterações da entrada de hora atualmente estendida</span><span class="sxs-lookup"><span data-stu-id="dec23-115">Currently extended time entry changes</span></span>
<span data-ttu-id="dec23-116">Para minimizar o impacto aos usuários atuais da entrada de hora, esta função altera somente o principal requisito necessário para continuar utilizando a entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="dec23-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="dec23-117">Se você tiver criado exibições personalizadas ou experiências de entrada de hora separadas, será necessário configurar os campos da **Configuração de Entrada de Hora** com os valores corretos do PSA.</span><span class="sxs-lookup"><span data-stu-id="dec23-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]